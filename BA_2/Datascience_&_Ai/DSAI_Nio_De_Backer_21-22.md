# Samenvatting: Data Science & AI 2021-2022
## 1 Basisbegrippen, steekproefonderzoek
| Qualitatief | Quantitatief
|---|---|
|Nominaal|Interval|
| Ordinaal| Ratio

- Nominaal: categorieën: gender, ras, land, type
- Ordinaal: Rangschikbaar: Militaire rank, grootte (als in Klein, Middel, Groot, ...)
- Ratio: Er bestaat een absoluut nulpunt, een 'niets'. Bv. 0 graden Kelvin, 0kg, ...
- Interval: Er bestaat geen fixed nulpunt: graden Celsius, zuurtegraad, IQ test, ...

Een verband tussen variabelen betekend niet dat er altijd een causaal verband is! 

Steekproeven (Samples)
| Sampling Error | Non-Sampling Error
|---|---|
|Accidental (bad luck, niets aan te doen)|Accidental (per ongeluk verkeerde data ingeven)|
| **Systematic (slechte steekproef, bv. niet aselect gekozen)**| Systematic (verkeerde meetinstrumenten,...)

## 2 Analyse van één variabele
### Central tendency 
- gemiddelde
    ```python
    # Panda
    df['Categorie'].mean()
    # Numpy array
    population_mean = sum(population) / len(population)
    ```
- mediaan: sorteer waarden en pik middelste (of gemiddelde middenste 2 als even)
- mode: meest voorkomende waarde **(Qualtiatieve variabelen)**

### Dispersion of spreiding
- range: (absoluut) verschil grootste en kleinste waarde
- quartiles/kwantielen: verdeel waarden in 4 even grote subsets.
```python
# voorbeelden interkwartiel afstand
stats.iqr(df['time1'])
tips['tip'].quantile(.75) - tips['tip'].quantile(.25)
```
- variantie: bereken gemiddelde van het verschil van elke waarde met het gemiddelde
```python
tips['tip'].var()
```
- standaard deviatie: vierkantswortel variantie
    - altijd positief
    - 0 kleinste waarde: alle data gelijk aan elkaar
    - kleinere impact outliers
    - eenheid zelfde als oorspronkelijke variabele (variantie is ² van variabele)
    - samen met gemiddelde kan je al een beeld vormen van hoe verspreid
    - n-1 omdat gewoon beter

## 3 Kansrekening, centrale limietstelling, statistische toetsen
### Kansrekening
De kans stelt de relatieve frequentie voor van een gebeurtenis.
Dus bv dobbelsteen: 6 mogelijke kanten met elke een nr.
Kans is 1/6 om 1 te gooien.
Voorgesteld als P(X=1) = 1/6
- Kans altijd groter dan 0
- Alle kansen samen altijd gelijk aan 1
- Stel A en B onafhankelijke gebeurtenissen: Kans op A of kans op B == Kans op A + Kans op B
- Complement: Kans op niet A: 1- Kans op A
- Kans op A of kans op B == Kans op A + Kans op B - (Kans op A én Kans op B)

Kans distributiefunctie = P(X=x).

Verwachte waarde = som van (waarden * zijn resultaat kansdistrfunc)

Variantie en standaard dev bestaan hier ook voor

Continue kansvariabelen: bv oneindig veel waarden tussen 0 en 1
- Normaal verdeling meest voorkomende.
- Werk met integralen voor verwachtingswaarde en variantie
- Normaalverdeling kan beschreven worden adhv zijn verwachtingswaarde (u) & standaarddeviatie (o): Nor(u, o)
- standaardnormaalverdeling: Nor(0, 1) (aangeduid als Z)

```python
# m: gemiddelde, s: standaard deviatie
norm.pdf(x, loc=m, scale=s) # P(X = x)
norm.cdf(x, loc=m, scale=s) # P(X < x)
norm.sf(x, loc=m, scale=s) # P(X > x)
norm.isf(1-p, loc=m, scale=s) #p% vd operaties lager dan resultaat (bv. p=50% -> er komt 5 uit: 50% van de observaties zijn kleiner dan 5)
norm.cdf(y,loc=m,scale=s) - norm.cdf(x,loc=m,scale=s) # P(X < x < Y)
```

- Exponential Distribution: start op een bepaald punt en daalt verder.
- Continuous Uniform Distribution: alles even hoog

### Centrale limiet theorem
Als steekproef groot genoeg (>=30) zal kansverdeling steekproefgemiddelde een normaalverdeling benaderen ongeacht de kansverdeling van onderliggende populatie
- confidence interval/betrouwbaarheidsinterval: met een bepaald zekerheidsniveau ligt de parameter in dit interval
```python
# voorbeeld voor 99% (alpha)
m = df['Money'].mean()
n = len(df)
s = 98 / np.sqrt(n)
alpha = 1 - 0.99

z = stats.norm.isf(alpha/2)
lo = m - z * s
hi = m + z * s
print("Confidence interval: [%.4f, %.4f]" % (lo, hi))
```
- kleine steekproefgrootte, ongekende  -> student t
```python
# m: gemiddelde, s: standaard deviatie
t.pdf(x, loc=m, scale=s) # P(X = x)
t.cdf(x, loc=m, scale=s) # P(X < x)
t.sf(x, loc=m, scale=s) # P(X > x)
t.isf(1-p, loc=m, scale=s) #p% vd operaties lager dan resultaat (bv. p=50% -> er komt 5 uit: 50% van de observaties zijn kleiner dan 5)
# Betrouwbaarheidsinterval
# Step 1.
m = 5.2      # Sample mean
s = 1.5      # Population standard deviation
n = 15       # Sample size
alpha = .05  # 1 - alpha is the confidence level

# Stap 2.
t = stats.t.isf(alpha/2, df = n - 1) # df: degrees of freedom/vrijheidsgraden
print("t-score: %.5f" % t)

# Stap 3.
lo = m - t * s / np.sqrt(n)
hi = m + t * s / np.sqrt(n)
print("Confidence interval: [%.4f, %.4f]" % (lo, hi))
```
### Hypothesetoetsen
- H0: Basis hypothese 
- H1: Alternatief
- test statistiek
- aanvaardingsgebied (voor H0)
- kritiek gebied g (verwerpen H0)
- significantieniveau a (kans onrechtmatig verwerpen H0)

p-waarde: kans dat als H0 waar, we een test statistiek krijgen die op z'n minst zo extreem is als geobserveerde waarde.
- p < a => verwerp H0 want kans zo klein 
- p >= a => niet verwerpen H0

#### Z-testen
- Eisen:
    - random steekproef
    - voldoende groot (>30)
    - normale verdeling
    - stdev van populatie is gekend
- Rechterstaart: H1: gemiddelde > verwacht gemiddelde
```python
# Properties of the sample:
n = 30      # sample size
sm = 3.483  # sample mean
s = 0.55    # population standard deviation (assumed to be known)
a = 0.05    # significance level (chosen by the researcher)
m0 = 3.3    # hypothetical population mean (H0)

# p-waarde berekenen
p = stats.norm.sf(sm, loc=m0, scale=s/np.sqrt(n))
print("p-value: %.5f" % p)
if(p < a):
    print("p < a: reject H0")
else:
    print("p > a: do not reject H0")

# Alternartief met kritiek gebied
g = m0 + stats.norm.isf(a) * s / np.sqrt(n)
print("Critical value g ≃ %.3f" % g)
if (sm < g):
    print("sample mean = %.3f < g = %.3f: do not reject H0" % (sm, g))
else:
    print("sample mean = %.3f > g = %.3f: reject H0" % (sm, g))

```
- Linkerstaart: H1: gemiddelde < verwacht gemiddelde
```python
p = stats.norm.cdf(sm, loc=m0, scale=s/np.sqrt(n)) # Let op! cdf() ipv sf()!
g = m0 - stats.norm.isf(a) * s / np.sqrt(n)
print("Critical value g ≃ %.3f" % g)
if (sm > g):
    print("sample mean = %.3f > g = %.3f: do not reject H0" % (sm, g))
else:
    print("sample mean = %.3f < g = %.3f: reject H0" % (sm, g))

```
- Tweezijdig: H1: gemiddelde != verwacht gemiddelde
```python
p = stats.norm.sf(sm, loc=m0, scale=s/np.sqrt(n))
print("p-waarde: %.5f" % p)
if(p < a/2):
    print("p < a/2, dus H0 verwerpen")
else:
    print("p > a/2, dus H0 niet verwerpen")

g1 = m0 - stats.norm.isf(a/2) * s / np.sqrt(n)
g2 = m0 + stats.norm.isf(a/2) * s / np.sqrt(n)

print("Acceptance region [g1, g2] ≃ [%.3f, %.3f]" % (g1,g2))
if (g1 < sm and sm < g2):
    print("Sample mean = %.3f is inside acceptance region: do not reject H0" % sm)
else:
    print("Sample mean = %.3f is outside acceptance region: reject H0" % sm)
```

#### T-testen
Grotendeels zelfde
- Rechts
```python 
# Properties of the sample:
n = 20      # sample size
sm = 3.483  # sample mean
ss = 0.55   # sample(!) standard deviation
a = 0.05    # significance level (chosen by the researcher)
m0 = 3.3    # hypothetical population mean (H0)

p = p = stats.t.sf(sm, loc=m0, scale=s/np.sqrt(n), df=n-1)
print("p-value: %.5f" % p)
if(p < a):
    print("p < a: reject H0")
else:
    print("p > a: do not reject H0")

g = m0 + stats.t.isf(a, df=n-1) * s / np.sqrt(n)
print("Critical value g ≃ %.3f" % g)
if (sm < g):
    print("sample mean = %.3f < g = %.3f: do not reject H0" % (sm, g))
else:
    print("sample mean = %.3f > g = %.3f: reject H0" % (sm, g))
```

```python
# Voorbeeld tweezijdige test
observations = [
  3, 2, 3, 1, 10, 4, 2, 7, 3, 0,
  3, 1, 2, 3,  4, 0, 3, 8, 3, 7]
a = 0.05
m0 = 3.3

t_stat, p_val = stats.ttest_1samp(observations, m0)
print("Sample mean        : %.3f" % np.mean(observations))
print("t-score            : %.3f" % t_stat)
print("p-value (2-tailed) : %.5f" % p_val)
print("p-value (1-tailed) : %.5f" % (p_val/2))
```
## 4 Analyse twee kwalitatieve variabelen
X: Onafhankelijke variabele

Y: Afhankelijke variabele

Crosstabel: bereken marginale totalen (dus voor elke y totaal)
en verwachte waarden (als X geen invloed heeft zijn die ratios allemaal mooi hetzelfde). 
| / |X1 |X2 |margtot|expectvalX1|exepectvalX2
|---|---|---|---|---|---|
|Y1|1|1|2|(4*2)/13 = 0,61|(9*2)/13 = 1,38 |
|Y2|3|4|7|(4*7)/13 = 2,15| (7*9)/13 = 4,81|
|totaal|4|9|13|||
```python
# Met pandas
pd.crosstab(rlanders.Survey, rlanders.Gender, margins=True)
```
chi-squared/chi-kwadraad meet hoeveel de afwijking is van de verwachte waarden.

Probleem: betekenis waarde is afhankelijk van grootte tabel

-> Cramér's Vagina
| Cramér's V | betekenis |
|---|---|
|0| geen associatie|
|0.1| zwak|
|0.25| matig|
|0.5| sterk|
|0.75| zeer sterk|
|1|compleet|

```python
# Voorbeeld chi en cramér's
observed = pd.crosstab(rlanders.Survey, rlanders.Gender)
row_sums = observed.sum(axis=1)
col_sums = observed.sum()

expected = np.outer(row_sums, col_sums) / n

diffs = (expected - observed)**2 / expected

chi_squared = diffs.values.sum()
print('χ² ≈ %.3f' %chi_squared)

dof = min(observed.shape) - 1
cramers_v = np.sqrt(chi_squared / (dof * n))
print(cramers_v)
```
χ² voor onafhankelijkheid

H0: geen associatie (chi is klein)

H1: associatie (chi is groot)
```python
chi2.pdf(x, df=d)
chi2.cdf(x, df=d)
chi2.sf(x, df=d)
chi2.isf(1-p, df=d)

# Test procedure
alpha = .05
dimensions = observed.shape
dof = (dimensions[0]-1) * (dimensions[1]-1)

print("Chi-squared        : %.4f" % chi_squared)
print("Degrees of freedom : %d" % dof)

# Calculate critical value
g = stats.chi2.isf(alpha, df = dof)
print("Critical value     : %.4f" % g)

# Calculate p-value
p = stats.chi2.sf(chi_squared, df=dof)
print("p-value            : %.4f" % p)
```

Goodness-of-fit test
test of steekproef representatief is voor verdeling

H0: representatief

H1: niet representatief

```python
types =  ['mutant', 'human', 'alien', 'god', 'demon']
observed = np.array([127, 75, 98, 27, 73])
expected_p = np.array([.35, .17, .23, .08, .17])

alpha = 0.05               # Significance level
n = sum(observed)          # Sample size
k = len(observed)          # Number of categories
dof = k - 1                # Degrees of freedom
expected = expected_p * n  # Expected absolute frequencies in the sample
g = stats.chi2.isf(alpha, df=dof)  # Critical value

# Goodness-of-fit-test in Python:
chi2, p = stats.chisquare(f_obs=observed, f_exp=expected)

print("Significance level  ⍺ = %.2f" % alpha)
print("Sample size         n = %d" % n)
print("k = %d; df = %d" % (k, dof))
print("Chi-squared        χ² = %.4f" % chi2)
print("Critical value      g = %.4f" % g)
print("p-value             p = %.4f" % p)
```
Gestandardiseerde residuen

H0: steekproef representatief voor populatie

H1: steekproef niet representatief voor populatie

```python 
families['stdres'] = (families.observed - families.expected) / np.sqrt(families.expected * (1 - families.expected_p))
families
```
- ri [-2, 2] -> ok
- <-2 -> ondergerepresenteerd
- \>2 -> overgerepresenteerd

Cochran's regels voor chi²
- voor alle categorieën, verwachte frequentie groter dan 1
- max 1/5de categorieën mag verwachte frequentie < 5
## 5 Analyse 2 variabelen: kwalitatief vs kwantitatief
two-sample t-test: zijn gemiddelden verschillend?
- onafhankelijke steekproeven

    H0: gemiddelde_1 - gemiddelde_2 = 0

    H1: gemiddelde_1 - gemiddelde_2 < 0

    ```python
    stats.ttest_ind(a=control, b=treatment,
    alternative='less', equal_var=False)
    # alternative kan ook 'two_sided' of 'more' zijn afhankelijk van H1
    ```
- gepaarde steekproeven
    ```python
    stats.ttest_rel(regular, additives, alternative='less')
    ```
- effect grootte: Cohen's D ( ͡° ͜ʖ ͡°)
    gaat van 0.01 (zeer klein), (0.5 gemiddeld) tot 2 (gigantisch)
    - tipping point 0.4
    ```python
    def cohen_d(a, b):
    na = len(a)
    nb = len(b)
    pooled_sd = np.sqrt( ((na-1) * a.std(ddof=1)**2 +
                          (nb-1) * b.std(ddof=1)**2) / (na + nb - 2) )
    return (b.mean() - a.mean()) / pooled_sd
    ```
## 6 Analyse 2 kwantitatieve variabelen
Lineare regressie
- monotonic (zelfde richting)/ non-monotonic
- least squares: bepaal regressielijn
    ```python
    mx = male_chinstrap.flipper_length_mm.mean()
    my = male_chinstrap.body_mass_g.mean()
    xx = male_chinstrap.flipper_length_mm - mx
    yy = male_chinstrap.body_mass_g - my
    beta1 = sum(xx * yy) / sum(xx ** 2)
    beta0 = my - beta1 * mx

    # Regression line equation
    print(f"ŷ = {beta0:.2f} + {beta1:.2f} x")

    # Of
    from sklearn.linear_model import LinearRegression

    male_chinstrap_x = male_chinstrap.flipper_length_mm.values.reshape(-1,1)
    male_chinstrap_y = male_chinstrap.body_mass_g

    weight_model = LinearRegression().fit(male_chinstrap_x, male_chinstrap_y)

    print(f"Regression line: ŷ = {weight_model.intercept_:.2f} + {weight_model.coef_[0]:.2f} x")
    ```

Covariantie: toon of relatie increased (> 0)/decreased (< 0)/geen relatie
```python
mx = families.x.mean()
my = families.y.mean()

covar = sum((families.x - mx) * (families.y - my)) / (len(families.x) - 1)

# Of 
np.cov(families.x, families.y, ddof=1)[0][1]
```

Pearson's correlatie coeff R
- sterkte lineaire correlatie x en y
- R: [-1, 1]

Determinatie coeff
- R² (das letterlijk alles)
- voorbeeld: R²-waarde is 0.62 => The heart weight vs. body weight relationship accounts for 62% of the variation in body weight

```python
cor = np.corrcoef(male_cats.Hwt, male_cats.Bwt)[0][1]
print(f"R = {cor}")

print(f"R² = {cor**2}")
```
## 7 Tijdserie-analyse
- tijdserie: observaties variabele over tijd
- belangrijk om te voorspellen
- je hebt verschillende soorten patronen seizoenale fluctuaties < cycli < trend (lange termijn stijging of daling)

Verschillende soorten modellen
- simpele horizontale rechte
- simpele lineaire regressie rechte (stijgt of daalt)
- SMA voortschrijdend gemiddelde
    - gemiddelden van laatste *m* obeservaties
    - volgt traag
    ```python
    # 3 is m
    data['SMA3'] = data['number_of_heavily_wounded'].rolling(3).mean()
    ```
- WMA gewogen voortschreidend gemiddelde
    - recente observaties meer gewicht
- exponentiele afvlakking
    - parameter a toont hoe snel vergeten, hoe dichter bij a hoe sneller vergeten
    - slecht in trends te volgen
    ```python
    data['EMA_0.1'] = data['number_of_heavily_wounded'].ewm(alpha=.1, adjust=False).mean()
    ```
- dubbeke exponentiele afvlakking
    - voor trends
    - Holt
    ```python
    data_des = Holt(data['number_of_heavily_wounded']).fit(smoothing_level=.1, smoothing_trend=.2)
    ```
- driedubbele exponentiele afvlakking
    - voor seizoenale schommelingen
    - Holt-Winters
    ```python
    cov_hw = ExponentialSmoothing(df.new_cases, seasonal='add', trend='add', seasonal_periods=7, feq='D').fit()

    ```
- Forecasts

Errors berekenen met:
- mean absolute error
- mean squared error
als MSE onder standaard deviatie zit heb je een goed model!
```python
from sklearn.metrics import mean_absolute_error,mean_squared_error

print(f'MSE = {mean_squared_error(y_true=maart2021.new_cases[:7], y_pred=cov_fc[:7])}')
print(f'√MSE  = {np.sqrt(mean_squared_error(y_true=maart2021.new_cases[:7], y_pred=cov_fc[:7]))}')
print(f"stdev: %.3f" % {covid19_be[start_date:pd.to_datetime('2021-03-07')].new_cases.std()})
```