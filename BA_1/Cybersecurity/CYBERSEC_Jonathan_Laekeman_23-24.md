---
title: "Samenvatting van Cybersecurity"
author: "Jonathan Laekeman"
year: "2023-2024"
---



---
# Staten van Data
3 mogelijke staten:
- data in **rust**/**opslag**
- data tijdens het **verzenden** 
- data tijdens het **verwerken**
-> EXAMEN: in welke staat bevindt zich deze data...

## Data in rust
= Data opgeslagen op **opslagapparaten** (harde schijven, USB-sticks, databanken,...) dat niet wordt gebruikt door personen of processen.

Kan **lokaal** (harde schijf, USB-stick,...) of op **afstand** (Dropbox, Google drive, NAS,...)

-> Data kan zo **verloren** of **gestolen** worden
- Harde schijf kapot
- Laptop vergeten op trein 
- Smartphone gestolen 
=> **oplossing**: **back-ups** maken van je persoonlijke data

## Data tijdens het verzenden
Verschillende manieren:
- **Sneaker net**: gebruikt opslagapparaten om data tussen computers over te zetten(USB-stick, draagbare harde schijf,...) 
- **Bedraad netwerk**: gebruikt koperkabels
- **Draadloos netwerk**: gebruikt elektromagnetische golven (kan door iedereen in de buurt "gehoord" worden)

## Data tijdens het verwerken
= Data tijdens de **invoer**, **aanpassing**, **berekening** of **uitvoer**

organisaties gebruiken verschillende methodes om data te verzamelen
- manuele invoer, het uploaden van bestanden, dataverzameling van sensoren,...
### Aangepaste data
Data kan **aangepast** worden door manuele verandering, door gebruikers, programma's die de data wijzigen, defecte apparaten,...
-> voorbeelden van *data aanpassingen*: encoderen/decoderen, compressie/decompressie, encryptie/decryptie,... 
=> Data dat zodanig wordt aangepast dat het fouten bevat of onbruikbaar wordt, noemt men **corrupte data**.


---

# CIA-driehoek
=> heeft 3 principes:
- **Confidentiality** (vertrouwelijkheid)
-> Wie mag dit zien?
	- bv. chatgesprekken, bedrijfsgeheimen, medische dossier,...

- **Integrity** (integriteit)
-> Klopt dit wel? Is er met de data gepruts? Is de [data aangepast](#aangepaste-data)?
-> Komt dit van de juiste persoon?
	- bv. financiële transacties, contracten, pak friet 3x bestellen en wordt veranderd naar 300x, school rapport aangepast,...

- **Availability** (beschikbaarheid)
-> Kan ik er aan wanneer ik het nodig heb? 
	- bv. 112-noodcentrale, Chamilo tijdens online examen, e-mail servers, internet-toegang,...

## Confidentiality/Vertrouwelijkheid
Vertrouwelijkheid kan verkregen worden door **encryptie**, **authenticatie** en **toegangscontrole**.

> verdere uitleg in [Confidentiality](#confidentiality).


## Integrity/Integriteit
= Integriteit is de nauwkeurigheid, consistentie en **betrouwbaarheid** van data zolang die data bestaat
Een andere *term* voor **integriteit** is de **kwaliteit**

-> De nood aan integriteit hangt af van de aard van de data.
	bijvoorbeeld:
	- Facebook verifieert de data in een gebruikerspost niet
	- Transacties en bedragen bij een bank moeten steeds 100% correct zijn

### Verlies integriteit
Verlies van integriteit kan enorme schade brengen aan personen en organisaties, en kan databronnen **onbruikbaar** of **onbetrouwbaar** maken

=> **oplossing**:
Een **integriteitscontrole** is een manier om te bekijken of gegevens (bestanden, foto’s, transacties,...) nog steeds correct zijn (niet corrupt of beschadigd). Hiervoor wordt vaak een hash functie gebruikt.

> wordt verder uitgebreid behandeld in [Integrity](#integrity)


## Availability/Beschikbaarheid
= Informatiesystemen moeten op elk moment beschikbaar zijn.

-> Een **aanval** of een **fout** kan de beschikbaarheid tot systemen in gevaar brengen.
=> **Oplossing**: Er bestaan vele maatregelen voor beschikbaarheid
	bv. redundantie, backups, verhoogde weerstand, onderhoud, up-to-date software en OS, noodplannen om terug online te komen na een onvoorziene omstandigheid, gebruik van nieuwe technologieën, detecteer ongebruikelijke activiteit en beschikbaarheidstesten.

> wordt verder uitgebreid behandeld in [Availablitlity](#availability)




---

# Cybersecuritykubus
De cybersecuritykubus staat ook bekend als de <mark style="background: #FFF3A3A6;">McCumber Cube</mark>
-> Om bij het ontwerpen van een beveiligingsplan niets te vergeten, wordt dit vaak gevisualiseerd als een kubus met 3 zijden:
- **Beveiligingsprincipes**
	- = [de CIA-driehoek](#cia-driehoek)
- **De staten van data**
	- = [de staten van data](#staten-van-data)
- **Beveiligingsmaatregelen**

![Kubus](images/Pasted%20image%2020231002193414.png)


# CIA-driehoek vs Staten van data
-> Cybersecurity-specialisten proberen data in al zijn staten te beschermen voor elk aspect van de CIA-driehoek.

![](images/Pasted%20image%2020231002201030.png)


=> Ze doen dit aan de hand van **verschillende beveiligingsmaatregelen** op vlak van **technologie**(Technology), **beleid**(Policies and Practice) en **personeel**(People -> zorgen dat het personeel niet op een verkeerde link klikt)



---

# Ethiek en cyberwetten
## Inleiding
-> Is het **ethisch** om...
- wachtwoorden te delen
- persoonlijke data (bv post-it met gebruikersnaam & wachtwoord) gebruiken
- data van kwetsbare sites halen
-> Zijn bovenstaande zaken **legaal** of **illegaal**?

## Wetgeving in cybersecurity
-> Een basisprincipe van een samenleving of maatschappij is de **wetgeving**, maar dit is geen gemakkelijke taak om uit te voeren
- **Wetgeving** loopt **achter op technologie**
- "**Op tijd**" invoeren van "**de juiste**" regelgeving is essentieel
- Zie zaak "**[Bistel](https://nl.wikipedia.org/wiki/Zaak-Bistel)**"

=> **Nationale** en **internationale** pogingen om dit te regulariseren
- *België*: wetgeving rond "**ethisch hacken**"
- *Europa*: **NIS** en **NIS2** directives
- *VS*: **NIST framework**
- *Wereldwijd*: **ISO/IEC** cybersecurity model

### België (Afschermen Ethische Hacker)
-> nieuwe wet vanaf 15 februari 2023
=> afschermen van de ethische hacker

OPGELET!
- De wetgeving is nog steeds **restrictief**. => "hacking" is nog steeds **bij wet verboden**
- Ethische hackers mogen **geen frauduleuze bedoelingen** hebben en moeten de **fouten melden** binnen 48 uur

### Europa (NIS & NIS2)
- **NIS**
	- **EU-brede wetgeving** rond cybersecurity
	- Ingevoerd in 2016
	- Invoering ging moeizaam
- **NIS2**
	- Meer verduidelijking
	- Hoe **omgaan met** snelle technologische vernieuwingen
	- Meer **samenwerking** tussen lidstaten bij grote bedreigingen
	- Verplicht **meer organisaties en sectoren** werken rond cybersecurity
	- Verplicht moeten lidstaten de **wet handhaven**
	- Ingevoerd op 16 januari 2023 -> moet in de **nationale wetgeving van EU-lidstaten** staan tegen 17 oktober 2024

### VS (NIST)
**NIST** (National Institute of Standarts and Technologies)

=> Het is een **raamwerk** voor bedrijven en organisaties die cyberbeveiligingsprofessionals nodig hebben

### Wereldwijd (Het ISO/IEC cybersecurity model)
-> Het International Organization for Standardization (**ISO**) & International Electrotechnical  Commission (**IEC**) heeft een volledig framework opgesteld om te helpen dit in goede banen te leiden. 

=> Dit framework noemt het **ISO/IEC cybersecurity model**.
- Het ISO model is een **hulpmiddel** om complexe problemen te begrijpen en aan te pakken.

#### Standaard ISO/IEC 27000
- Het ISO/IEC 27000 is een **standaard** opgesteld in 2005 (geupdated in 2013). 
-> gepubliceerd door ISO

- ISO 27000 model is bruikbaar voor elk type organisatie -> bevat controle doelstellingen in de vorm van **checklists**
-> organisaties moeten **zelfs bepalen** welke controle doelstellingen voor hen van toepassing zijn

-> Alhoewel de standaard **niet verplicht** is, wordt het door veel landen en organisaties gebruikt als het model voor cybersecurity


# Aanvallers
## Hackers
-> **Hackers** (aanvallers) kunnen verschillende redenen hebben om in te breken op computers of netwerken voor toegang te verkrijgen:

- **Whit hat** = hackers breken in op netwerken of computersystemen om zwakke punten te ontdekken en zo de de **beveiligingen van deze systemen te verbeteren**.
- **Gray hat** = hackers tussen de twee andere types. Deze aanvallers kunnen een kwetsbaarheid vinden en **melden aan eigenaren als ze dat willen**.
- **Black hat** = hackers die onethische criminelen zijn die de computer- en netwerkbeveiliging schenden voor **persoonlijk gewin** of om kwaadaardige redenen, net hetzelfde met aanvallen op netwerken.

![types_hackers](images/Pasted%20image%2020231009212718.png)



## Scriptkiddies 
=> voorbeeld van **black hat** hackers

- meestal **tieners** of **hobbyisten**
- aanvallen meestal **grappen** en **vandalisme**
- **weinig** of **geen vaardigheid**
- gebruiken tools of instructies **van het internet**

## Vulnerability brokers
=> voorbeeld van **gray hat** hackers
=> **Kwetsbaarheidsbemiddelaars**

- proberen exploits te ontdekken 
- geven het door aan leveranciers
	- voor **geldprijzen** 
	- voor **beloningen**

## Hacktivisten
=> voorbeeld van **gray hat** hackers

- protesteren **tegen politieke en sociale ideeën**
- ze protesteren publiekelijk tegen organisaties of regeringen door:
	- artikelen en video's te plaatsen
	- gevoelige informatie te lekken 
	- DDoS-aanvallen uitvoeren

## Cybercriminelen
=> voorbeeld van **black hat** hackers

- werken zelfstandig of voor grote cybercrime-organisaties
- verantwoordelijk voor het **stelen van miljarden dollars** elk jaar

## State sponsored hackers
=> afhankelijk van het perspectief, **white hat** of **black hat** hackers

- stelen van **overheidsgeheimen**
- **inlichtingen verzamelen**
- netwerken **saboteren**
- hun **doelwitten** zijn:
	- buitenlandse regeringen
	- terroristische groepen 
	- bedrijven
- meeste **landen** doen aan staat gesponsorde hacking


# Verdedigers
## Cybersecurity Specialisten
-> De overheid, bedrijven, internationale organisaties moeten cybercriminelen proberen dwars te bomen 
-> door **gecoördineerde acties** om ze te beperken of af te weren, deze omvatten:

- **Vulnerability Databases** (kwetsbaarheidsdatabases)
= Publiek beschikbare databases van gekende kwetsbaarheden

- **Early Warning Systems**
= Systemen voor vroegtijdige waarschuwing

- **Share Cyber Intelligence**
= Delen van cyber intelligence, vaak door middel van samenwerking tussen publieke en private sector

- **ISM normen (bv ISO-27000)**
= Standaarden en normen voor de informatiebeveiligingsbeheer die een kader vormen voor het implementeren van beveiligingsmaatregelen binnen een organisatie


# Security vs Privacy
-> **Meer veiligheid** = **minder privacy**
vb: ingebroken in een huis
-> Als er op elke hoek van een straat een camera stond dan had er misschien niet ingebroken geweest, maar wel minder privacy

## Eeuwig strijdtoneel
=> Het is dus een **eeuwig strijdtoneel**
- Politie strijdt tegen criminaliteit
	- bv: terrorisme, kinderporno, mensensmokkel, fraude, drugshandel,...
- Burgers hebben recht op briefgeheim en privacy
	- hoe kunnen politiediensten criminelen vatten als er bv. encryptie wordt gebruikt?
- Overheid verzamelt data
	- bv: belastingsdienst, boetes,...
- Hoe ver mag de overheid hierin gaan?
	- wat als data voor iets anders wordt gebruikt?
	- wat als er een fout in de data zit?
	- wat als de definitie van "fout" verandert?

## Niets te verbergen
-> Iedereen heeft wel iets te verbergen, want niemand gaat op al deze vragen een antwoord willen geven:

- Waar woon je?
- Hoeveel verdien je?
- Pikante gesprekken, foto's, video's
- Seks partners, seksuele voorkeur,...
- "Niet-dagelijkse" hobbies
- Medische problemen, behandeling, verslavingen, therapie, doktersgeheim,...
- Financiële moeilijkheden, schulden, veel geërfd of lotto gewonnen,...
- ...

## GDPR
=> In België en Nederland bekend als de **AVG**
=> Europese **wet voor beschermen van privacy** 

-> ingevoerd in 2018
- **Recht**...
	- ... van inzage
	- ... op correctie
	- ... om vergeten te worden 
	- ... op overdracht van gegevens
	- ... beveiliging 

-> Gegevensbeschermingsautoriteit controleert naleven GDPR

- **Organisaties moeten**...
	- ... een correct doel hebben voor gegevensverzameling
	- ... enkel nodige gegevens opvragen 
	- ... voor slechts beperkte duur
	- ... toestemming vragen
- Privacyverklaring
- Soms kan **de wet je verplichten om gegevens te geven**
	- bv: foto voor identiteitskaart, scan luchthaven,...
- **Wat is toestemming?** GDPR legt regels op
	- duidelijk
	- niet automatisch aangevinkt (expliciete toestemming)
	- geen negatieve gevolgen 
	- intrekbaar
	- 13 jaar of ouder (of door voogd)





---

# Bedreigingen
## Interne aanvallen
-> Willen we liever niet, natuurlijk willen we ook geen externe, maar zeker geen interne
-> Daarom worden **IT'ers** meestal **ontslagen zonder opzegtermijn**, ze kunnen teveel schade aanrichten

- Ze zijn afkomstig van een **interne gebruiker** (vb: medewerker, contactpartner)
- Ze kunnen **grotere schade** aanrichten, omdat ze toegang hebben tot het gebouw, infrastructuur, apparatuur
- Ze kunnen al **kennis** hebben van het bedrijfsnetwerk, bronnen en vertrouwelijke gegevens, beveiligingsmaatregelen, beleidsregels en hogere niveaus van beheerdersrechten

## Externe aanvallen
- Maken misbruik van **kwetsbaarheden** in netwerkapparaten, kunnen **social engineering** gebruiken, zoals bedrog, om toegang te krijgen.
=> **Externe aanvallen** maken misbruik van zwakheden of kwetsbaarheden om **toegang** te krijgen tot **interne bronnen**.

## Mobiele apparaten
-> *Vroeger* waren veel **computers** verbonden met het bedrijfsnetwerk
-> *Nu* meer **mobiele apparaten** verbonden met het bedrijfsnetwerk
- Dit noemt **Bring Your Own Device** (**BYOD**)

=> Het **onvermogen** om mobiele apparaten centraal te **beheren** en bij te werken (updates), vormt een groeiende **bedreiging** voor organisaties.

## Internet-of-Things
-> **Internet of Things** (IoT) is de verzameling van technologieën die de **verbinding** van verschillende apparaten **met het internet** mogelijk maakt

- IoT-technologieën stellen mensen in staat **miljarden apparaten** met internet te verbinden (TV, lichten, sloten, camera's, droogkast, vaatwasser,...)
- Het heeft invloed op de **hoeveelheid gegevens** die **beschermd** moet worden. 
- Er moeten veel meer gegevens **beheerd en beveiligd** worden, deze verbindingen + uitgebreide opslagcapaciteit en opslagdiensten die worden aangeboden via cloud en virtualisatie, hebben geleid tot **exponentiële groei** van gegevens

## Impact van Big Data
**Big Data** = resultaat van datasets die groot en complex zijn. 
-> Het biedt zowel uitdagingen als kansen op basis van **3 dimensies**:
1) Het **volume** of de hoeveelheid gegevens
2) De **verscheidenheid** of het bereik van gegevenstypen en bronnen
3) De **snelheid** van gegevens
=> Deze 3 dimensies worden ook wel de **3 V's** genoemd, nl. **Volume**, **variety**, **Velocity**

## Bredere reikwijdte en cascade-effect
- **Federatief identiteitsbeheer** verwijst naar meerdere ondernemingen die hun *gebruikers dezelfde identificatiegegevens* laten gebruiken *om toegang te krijgen tot de netwerken van alle ondernemingen* in de groep. Het doel van federatief identiteitsbeheer is om identiteitsinformatie automatisch over kasteelgrenzen heen te delen.
-> Voorbeelden **Federatief identiteitsbeheer**: 
	- Je kan op verschillende sites inloggen met een facebook-, google, steam account. Ook al heeft die website niets met die accounts te maken.
	- Je kan je op verschillende sites inloggen met je e-id 

- Meest gebruikelijke manier om de federatieve identiteit te beschermen, is door inlogmogelijkheid te koppelen aan een **geautoriseerd apparaat**.

# Malware en kwaadaardige code
-> Er zijn **verschillende soorten malware**: 
- Cyber criminelen vallen de toestellen van de gebruikers aan door het installeren van **kwaadaardige code**
= **kwaadaardige software**

## Virussen
= Een **kwaadaardig stukje code** die vasthangt aan een uitvoerbaar bestand.

- De meeste virussen hebben een zekere vorm van **actie van de eindgebruiker** nodig.
- Virussen kunnen onmiddellijk of op een bepaald moment worden **geactiveerd** 

## Worm
= Een kwaadaardige code die zich kenmerkt doordat het **zichzelf repliceert** door gebruik te maken van een kwetsbaarheid in het netwerk.

- Worms zullen het **netwerk vertragen**
- Een *virus heeft een host programma nodig om te draaien*, een worm **kan op zichzelf draaien**.
- De worm heeft **geen interactie van de gebruiker** meer nodig, de worm doet al het werk zelf

## Trojan Horse
= Malware die verborgen zit in gewenste bestanden, zoals foto's of een game.

- Gebruikers zijn hier niet van bewust.
- **Trojan Horse ≠ virus** -> omdat een Trojan horse een **niet-uitvoerbaar bestand infecteert**(zoals een afbeelding, een pdf)
- **Trojan Horse ≠ worm** -> omdat een Trojan horse **zichzelf niet kopieert** naar andere computers, wat een worm wel doet.

## Logic Bomb
= Kwaadaardig programma die wordt **geactiveerd op een bepaald moment (=trigger)**.

-> Voorbeeld: werknemer die ontslagen is en die opzegtermijn moet uitdoen, kan een Logic Bomb inplanten die wordt uitgevoerd een week na zijn vertrek.

- Het **wacht op de trigger** om te activeren **om schade toe te brengen**.
- **Trigger** = een bepaalde datum, een ander programma dat wordt opgestart, bepaalde actie die wordt gedaan,...

## Ransomware
= Een computersysteem of data wordt **geblokkeerd of geëncrypteerd** tot het moment dat het slachtoffer een **geldsom betaalt**

- De key om de data opnieuw te decrypteren blijft dan geheim tot er betaald wordt
- Er is **geen garantie** dat je alles terugziet zelfs als je betaalt -> blijven criminelen

## Backdoors en Rootkits
= Een rootkit zal het **operating system aanpassen** en zo een Backdoor creëren.

-> Deze backdoor wordt dan gebruikt om het gecompromitteerde systeem binnen te dringen, zonder enige vorm van authenticatie.

## Keyboard Logging
= Computerprogramma die de **toetsenbordaanslagen** (keystrokes) gaat **opnemen** of loggen.

- Stukje software wordt op het toestel van het slachtoffer geïnstalleerd
- De dader programmeert de software om dan na afloop de log file of opname naar **zichzelf door te sturen** (via email)
- In de log file kan dan **gevoelige informatie** staan zoals de emailadressen, wachtwoorden, pincodes,...

# Misleiding en oplichting
## Kunst van het oplichten
### Social Engineering
- Gebruikt geen technologische hoogstandjes, maar is daarom niet minder doeltreffend. Het bestaat erin om het **vertrouwen van jouw slachtoffer te winnen** om dan nadien van het slachtoffer iets te verlangen.

-> voorbeeld: doen alsof je van de beveiligingsfirma bent en vragen om de poort te openen.

- Tegenwoordig één van de meest populaire hack-methodes
	- 80+ %
	- Zeer doeltreffend
	- **Mensen** zijn de zwakste schakel

## Phishing
= Vorm van fraude -> **phishing** is ontstaan door het samenvoegen van de woorden "**Password Harvesting Fishing**"

-> De aanvaller probeert **informatie** (logingegevens, credit card informatie,...) **te verkrijgen** van het slachtoffer

- Via sociale media of email een link doorgestuurd
- De webpagina **doet zich dan voor** als een loginscherm van een bank
- Gebruikers die het loginscherm wettig vinden, geven zo gegevens bloot aan de aanvallers

## Pretexting
= Het **slachtoffer wordt opgebeld** en gevraagd om **gevoelige informatie vrij te geven** om identificatie mogelijk te maken. 

- Er wordt bv een credit card nummer gevraagd aan het slachtoffer.

## Vishing
= Ofwel **voice phishing** 
= Is een vorm van criminele **telefoonfraude**, waarbij gebruik wordt gemaakt van **social engineering via de telefoon** om toegang te krijgen tot **persoonlijke en financiële informatie** met het oog op een financiële beloning

## SMiShing
= Ofwel **SMS Phishing**
= Zal fake SMS (**Short Message Service**) gebruiken om **valse berichten** te sturen.

- De dader zal het slachtoffer proberen te **lokken** *naar een website* of **verleiden** om te *bellen naar een bepaald telefoonnummer*
- Nietsvermoedende slachtoffers kunnen dan **vertrouwelijke informatie doorgeven**
- Het bezoeken van schadelijke websites kan dan zorgen voor ongewenste **malware op jouw toestel** dat wordt gedownload 

## Cat Phishing
= Het aanmaken van een **valse identiteit** om op die manier het **vertrouwen** van het slachtoffer te winnen

-> Soms gaat het over een liefdesrelatie op dating sites
-> voorbeeld: Stan Van Samang en andere bekende Vlamingen hadden naaktbeelden gedeeld met zo een valse identiteit en die persoon heeft dat verspreid

## Spear Phishing / Whaling
= **Spear Phishing** -> Phishing gericht op een **specifieke persoon**, **doelgroep**, organisatie of bedrijf

-> voorbeeld: alle werknemers of studenten van de IT-dienst van HOGent

= **Whaling** -> een vorm van spear phishing gericht op een **specifiek zeer belangrijke persoon**

-> voorbeeld: de CEO van een bedrijf, baas van de IT-dienst,...

## Pharming
= **Geen rechtstreekse interactie met gebruiker** nodig

- Verschil met phishing (pharming = "phishing without a lure")

![Pharming](images/Pasted%20image%2020231016220423.png)




## Typosquatting
= Misbruik maken van vaak voorkomende **typfouten**

-> voorbeeld: een website hosten die lijkt op `https://paypal.com` met een URL als `https://paipal.com` -> gebruikers voeren daar dan nietsvermoedend hun gegevens in

## Shoulder Surfing
= Het **aflezen/meelezen** van PIN-codes of wachtwoorden en dergelijke

- Hierdoor kan de dader dichtbij staan of hij kan een camera of verrekijker gebruiken

## Dumpster Diving
= Het zoeken van informatie in **afval**

## Impersonation
= Zich **voordoen** als iemand anders

## Piggybacking / Tailgating
= Het **mee glippen** met personen die wél toegang hebben tot een plaats met beperkte toegang

# E-mail en browser aanvallen
## Seo Poisoning
- Zoekmachines (Google,...) tonen de resultaten op basis van de query van de gebruiker
- **Zoekresultaten** worden **geordend** d.m.v. **Search Engine Optimization** (verzameling van technieken die er moet voor zorgen dat jouw website **hoog scoort bij de zoekmachines**) 
- Cybercriminelen durven SEO wel eens te misbruiken om hun **kwaadaardige software hoog** in Google **te laten ranken**

## Browser Hijacking
- Zorgt dat de browser instellingen worden gewijzigd. Op die manier kunnen criminelen ervoor zorgen dat **jouw browser doorlinkt** naar de website van de "klant" van deze crimineel
- Extension TODO
- Valse CHATGPT extensions

## Spam
= Spam, junk mail, ongewenste e-mails, allemaal synoniemen

- In de meeste gevallen gaan de ongewenste e-mails over **advertenties**
-> maar deze kunnen ook verwijzen naar **kwaadaardige links** met mogelijks misleidende informatie

## Hoaxes
= Een leugen, valse informatie

- Vaak onschadelijk..., maar niet altijd

-> Voorbeeld: "Elon Musk is Giving away Money"

## Spyware
- Probeert **informatie** te **vergaren** over een gebruiker en stuurt het door naar een externe partij. 
- Vaak worden hiervoor **beveiligingsinstellingen aangepast**
- Gaat soms over keystrokes **verzamelen** of data capture

=> Doel van spyware is om geld te verdienen 

## Adware
= Lastige **pop-ups**

- Deze **pop-ups** proberen op één of andere manier **winst** op te **leveren voor de auteur**
- **Advertentie-ondersteunende software**

![advertenties](images/Pasted%20image%2020231016224133.png)


-> Het woord spyware verwijst strikt genomen naar programma's die bijvoorbeeld toetsaanslagen, surfgedrag en ander privacygevoelige informatie achterhalen. Intussen wordt de term gebruikt voor veel meer.
Zo wordt adware vaak gemakshalve tot de spywarecategorie gerekend

## Scareware
- Probeert de gebruiker te overtuigen door ze **bang te maken**
- Het doet zich bv voor als een dialoogvenster van het besturingssysteem.

![scareware](images/Pasted%20image%2020231016224104.png)





---

# Netwerkaanvallen
## Botnets
- C&C, C2 (= **Command and Control**)
	- Computers, smartphones, Internet of Things (IoT),... worden **geïnfecteerd door malware**. 
	- De **malware** maakt een **connectie met de C&C** server van de **aanvaller**. 
	- De C&C server kan **opdrachten versturen** naar het **geïnfecteerd toestel** om **andere toestellen** te **infecteren** om het botnet te doen groeien, of aanvallen uit te voeren 

-> Eén botnet kan bestaan uit **honderden tot duizenden** geïnfecteerde toestellen onder invloed van een aanvaller

## (Distributed) Denial-of-Service attack (DDoS attack)
= aanval die resulteert in het **niet beschikbaar** zijn van een bepaalde netwerk service (bv. website)

-> een (D)DoS 
- **groot risico**
- mogelijks veel **geld en tijd verloren**
- **gemakkelijk** om het uit te voeren

![cartoon_CIA](images/Pasted%20image%2020231023194357.png)

=> computer expert ziet het als een poster van de muur trekken -> **gemakkelijk**

## Sniffing
-> gelijkaardig aan iemand **afluisteren**
=> Dader zal alle **netwerkverkeer** die passeert aan de **NIC** (**Network Interface Card**) bekijken -> ook het verkeer wat niet voor hem bedoeld was

-> Daders gebruiken **speciale software / hardware** om te sniffen 
**bijvoorbeeld**: *Wireshark*

## Spoofing
=> Werkelijkheid **vervalsen** / **technologie foppen** i.p.v. de mens

-> **Daders** passen kenmerken aan om te **doen alsof hij/zei iemand anders is**
**voorbeeld**: 
- bij **e-mail spoofing** de header aanpassen
	- From Van, Return-Path (afzender),... aanpassen -> doen alsof iemand anders mail verstuurd 
- **URL spoofing** of **IP spoofing**

## Man-in-the-middle attack
=> Cyber crimineel zal proberen informatie stelen dat wordt verstuurd over een netwerk **tussen twee toestellen**

-> Hij kan ook kiezen om **boodschap aan** te **passen** en op die manier **valse info** te **verspreiden** tussen de hosts. Deze hosts zijn zich **niet bewust** van de aanval

Een MitM-aanval laat de **dader** toe om de **controle over te nemen** terwijl de **andere partijen dit niet weten**

![man-in-the-middle](images/Pasted%20image%2020231023200326.png)


## Frauduleuze (Rogue) Access Point
=> Wordt in een (vaak draadloos) netwerk geplaatst en **doet zich voor als** een **vertrouwelijk** apparaat -> Dit laat de dader toe om MitM-attacks uit te voeren

-> Het **Access Point** wordt geplaatst en zorgt ervoor dat mensen hun **verkeer via dit Access Point** versturen waardoor het Access Point de **data** kan **zien** en **analyseren**

![access_point](images/Pasted%20image%2020231023200909.png)


# Applicatie-aanvallen
## Zero-day attack
= proberen gebruik te maken van een **kwetsbaarheid** in de software die **nog niet gekend** is

-> Dit is **altijd succesvol** (voor de dader) omdat er nog **geen oplossing** voor is...
-> Day zero (of zero hour) verwijst naar het **moment waarop** het **lek wordt ontdekt** 

![zero-day](images/Pasted%20image%2020231023201146.png)


### Voorbeeld
**Belgische Defensie** getroffen door **Log4Shell-aanval**
-> Een aanval op een vrijdag (dus waarschijnlijk geplande aanval) 

=> Er zat een kwetsbaarheid in de logging software "Log4j" die door heel veel andere bedrijven werd gebruikt 
-> dus het was geen weekend voor de cybersecurity specialisten


## Cross-site scripting (XSS)
=> Kwetsbaarheid in **web applicatie** 
-> Via XSS kan je **scripts injecteren** in een webpagina die beschikbaar is voor de gebruiker

-> Crimineel valt **niet rechtstreeks het slachtoffer aan**, maar wel de website. 
Uiteraard is het slachtoffer wel diegene die de website bezoekt

-> Dader slaagt erin om **files** te **bekijken op de web server** die **niet bedoeld** zijn **voor hem**


## Code injections
-> data opslaan van een website doen we in een **databank**, maar via een **SQL injection** valt met SQL databanken aan

=> Men **injecteert** dan een **query** om deze uit te voeren

![code-injection](images/Pasted%20image%2020231023214614.png)



## Buffer overflow
=> Wanneer **data over zijn limiet** gaat
**Buffers** = **geheugen** die door een applicatie wordt gebruikt

-> door de **data aan** te **passen** en te **vergroten** tot het de **buffers overschrijdt**, gebruikt de applicatie geheugen dat door een **ander proces** wordt gebruikt en krijg je een **error**.
-> deze **error** kan een **applicatie crash** of het **verlies van data** zijn

![buffer-overflow](images/Pasted%20image%2020231023215021.png)



## Remote Code Executions (RCE)
=> Dader gebruikt een **kwetsbaarheid** waarbij hij/zei **code vanop afstand** kan **uitvoeren**

-> het is dan bv. mogelijk om **over het netwerk** of **over het internet** het toestel van het **slachtoffer aan te vallen**


## Beschermen tegen deze aanvallen
- First-line defense: programmeurs moeten **stabiele code** schrijven
- Alle **user input** van buitenaf beschouwen als vijandige of kwaadaardige code
- Alle user input **valideren en controleren**
- Alle software waaronder plug-ins-up-to-date houden door **updates** regelmatig uit te voeren
- Niet alle **updates** worden automatisch uitgevoerd, dus **controleer zelf manueel** ook altijd eens of er geen updates kunnen worden uitgevoerd

- **Never ending story**: in de volgende jaren zal je nog meer leren hoe je je kan beschermen en hoe je een aanval uitvoert


# APT's
= **Advanced Persistent Threat** => een langdurige en doelgerichte cyberaanval waarbij een onbevoegd persoon onopgemerkt en langdurig toegang krijgt tot een netwerk
=> doel: **continu** **toegang** krijgen en **gegevens stelen**

-> APT-aanvallen richten zich vooral op **landen** en **organisaties**

- **Advanced**
	- schaal (incl. de middelen) zijn zeer geavanceerd van aard. 
	- één enkel individu kan dit niet alleen uitvoeren
	- vaak state-sponsored hackers of georganiseerde misdaad
- **Persistent**
	- doel: heel **lang onzichtbaar** blijven
- **Threat**
	- steelt inloggegevens en gevoelige data 
	- vaak een vorm van **spionage**

-> Aanvallende organisaties krijgen vaak een **code** beginnend met APT:
- Fancy Bear (aka. APT28)
- Cozy Bear (aka. APT29)
- ...


### Voorbeelden
#### Voorbeeld 1: Stuxnet
- **Advanced**
	- Een van de **meest complexe en doelgerichte** malware-aanvallen die tot nu toe bekend zijn.
	- Maakte gebruik van verschillende **zero-day** kwetsbaarheden om te infiltreren en zich te verspreiden.
	- Opmerkelijk vanwege zijn vermogen om industriële controlesystemen te manipuleren, met name de systemen die worden gebruikt in **kerncentrales en industriële faciliteiten**.
	- Bevatte ook digitale certificaten om zijn legitimiteit te verifiëren, wat suggereerde dat het door een zeer **geavanceerde (state sponsored?) actor** was ontwikkeld.
	- Oorsprong van Stuxnet was eerst niet bekend, later werd onthuld dat het een gezamenlijke operatie was van de Amerikaanse NSA en de Israëlische inlichtingendienst.

- **Persistent**
	- 2009-2010: jarenlang
	- Ontdekt in juni 2010 

- **Threat**
	- Het primaire doelwit was de **nucleaire** installatie in Natanz, Iran. 

- Een van de eerste bekende voorbeelden van **door state sponsored** cyberwapens. 

- Een keerpunt in de wereld van cybersecurity, omdat het aantoonde dat **fysieke** systemen via digitale middelen kunnen worden aangevallen. 

- Illustreerde het potentieel voor grootschalige en verwoestende cyberaanvallen op **industriële** infrastructuren


#### Voorbeeld 2: Belgacom
- **Advanced**
	- Op **grote schaal** uitgevoerd
	- Door de Britse **geheime dienst** (GCHQ), in samenwerking met de Amerikaanse NSA. 

- **Persistent**
	- 2010-2013: jarenlang
	- Ontdekt in 2013 en kreeg de naam "Operation Socialist.“

- **Threat**:
	- Malafide software werd gebruikt om toegang te krijgen tot het interne netwerk van het bedrijf voor het verzamelen van **gevoelige informatie**. 

• Het feit dat een overheidsinstantie van een ander land betrokken was bij de aanval deed veel stof opwaaien en riep **vragen** op **over de grenzen en ethiek** van digitale spionage





---

# Confidentiality
=> De kunst van het beschermen van geheimen

## Cyptografie
- *Cryptologie*: **wetenschap** van het maken en breken van **geheime codes**
- *Cryptografie*: **manier** om gegevens **op te slaan** en te verzenden, zodat alleen de ontvanger deze kan lezen
	- **Moderne cryptografie**: gebruik van **algoritmen** om gevoelige data te beschermen
	- **Cryptografie** is veel **ouder dan computers** (duizenden jaren)! Belangrijk middel voor uitwisselen berichten in diplomatieke kringen
- *Cryptoanalyse*: focust op het **kraken** van cryptografie 

### Encrypteren
=> Om **vertrouwelijkheid** (**confidentiality**) te garanderen kunnen we een bericht **encrypteren** met behulp van een specifiek algoritme (cijfer/cipher)

-> Hierbij wordt een **bericht** dat we kunnen **begrijpen** (*plain text*) omgezet naar een **onleesbaar bericht** (*cipher text*) via een aantal goed gedefinieerde stappen, vaak met behulp van een geheime **sleutel**
![Encrypteren](images/Pasted%20image%2020231030211135.png)

### Decrypteren
=> Het omgekeerde is ook mogelijk, decrypteren zet een onleesbaar bericht terug om naar de originele leesbare tekst.

-> Voor encrypteren en decrypteren wordt vaak een **combinatie** gebruikt van **verschillende technieken**:
- *Transpositie* (omzetting)
- *Substitutie* (vervanging)
- *One-time pad*

![Decrypteren](images/Pasted%20image%2020231030211411.png)

### Transpositie
![Transpositie](images/Pasted%20image%2020231030211614.png)
**Voorbeeld** van **transpositie** waarbij de volgorde van de karakters wijzigt (transpositie van een matrix, A$^T$)

### Substitutie
![Substitutie](images/Pasted%20image%2020231030212044.png)
![Substitutie Voorbeeld](images/Pasted%20image%2020231030212103.png)
**Voorbeeld** van **substitutie** waarbij karakters vervangen worden door andere karakters


### One-time pad
**Voorbeeld** van **one-time pad** waarbij een random sleutel (=pad) toegevoegd wordt aan de plain text
-> Nadien wordt het resultaat omgezet naar een getal van 2 cijfers

-> Bekijk [deze video](https://youtu.be/2_w9l9visH8?t=351) voor meer uitleg


### Twee types algoritmen
- Encrypteren (encrypt/decrypt)
- Digitale handtekening (sign/verify)
![keys](images/Pasted%20image%2020231030222713.png)


-> [Symetrische algoritme](#symmetrische-algoritmen) vs [asymetrische algoritmen](#asymmetrische-algoritmen) codering

![Voor- en Nadelen](images/Pasted%20image%2020231030222919.png)
-> Asymmetrische codering vaak gebruikt om een (tijdelijke) **sessiesleutel** voor symmetrische encryptie **uit** te **wisselen**!


#### Symmetrische algoritmen
- **Zelfde sleutel** voor **encrypteren** (versleutelen) en **decrypteren**
- Verzender en ontvanger **kennen de sleutel** voor communicatie begint
	- Groot nadeel: hoe wissel je deze veilig uit?
![Symmetrisch algoritme](images/Pasted%20image%2020231030214850.png)

##### Private-key versleuteling
**Symmetrisch** versleutelingsproces: vooraf **gedeelde sleutel** om gegevens te encrypteren en decrypteren (private-key versleuteling)

- *DES* Data Encryption Standard
	- eenvoudig, encrypteert 64-bits blokken met 56-bits sleutel
	- niet bruikbaar in praktijk, niet veilig!
- *3DES* Triple DES
	- 3x DES met verschillende sleutels
	- sleutelsterkte: ~~3x56 = 468 bits~~ in praktijk 112-168 bits afhankelijk van gekozen combinatie
- *IDEA* International Data Encryption Algorithm
	- 64-bits blokken met 128-bits sleutel
	- vervanging voor DES, gebruikt bij PGP (Pretty Good Privacy)
	- voorbeeld -> handtekeningen van de bevolking
- *AES* Advanced Encryption Standard
	- 128-bits blokken, sleutel van 128, 192 of 256 bits
	- goedgekeurd door NIST, gebruikt door Amerikaanse overheid


#### Asymmetrische algoritmen
- **Sleutelpaar** = **verschillende sleutel** voor encrypteren en decrypteren
- 1 sleutel is publiek (openbaar), andere is privé
	- Daarom ook vaak term: **publieke-sleutelcryptografie**
	- Iedereen kan bericht **encrypteren** met **publieke sleutel**, enkel **ontvanger** kan **decrypteren** met met **private sleutel**
	- Ook **omgekeerde is mogelijk**: encrypteren met private sleutel, decrypteren met publieke sleutel
![Assymetrisch algoritme](images/Pasted%20image%2020231030214917.png)

##### Public-key versleuteling
**Asymmetrische** versleutelingsproces: **verschillende sleutels** voor encrypteren en decrypteren (public key encryption) 
Niet mogelijk om via één sleutel de andere te achterhalen

- *RSA* Rivest Shamir Adleman
	- gebruikt product van 2 heel grote priemgetallen
	- vaak gebruikt in browsers
- *ECC* Elliptic Curve Cryptography
	- alternatief voor RSA: nulpunten van elliptische curven i.p.v. priemgetallen
	- voorbeeld: Sky ECC 'gsm'
	- VS: NSA gebruikt dit voor handtekeningen en uitwisselen sleutels
- *Diffie-Hellman* 
	- gebruikt om geheime sleutel (sessiesleutel) voor symmetrisch algoritme uit te wisselen
	- vaak gebruikt: SSL, TLS, SSH, IPSec,...
- *ElGamal*
	- Amerikaanse overheidsstandaard voor digitale handtekeningen
	- gratis! Niemand heeft patent...

###### Diffie-Hellman
-> wordt gebruikt om **met asymmetrische algoritmen** een **symmetrische sleutel** te **genereren**
![Diffie-Helman](images/Pasted%20image%2020231030223224.png)


## Cryptoanalyse
### Kraken van cryptografie
-> Bij het **kraken** van cryptografie probeer je een **onleesbaar** bericht (cipher text) om te vormen **naar** een **leesbaar** bericht (plain text) **zonder** dat je de **geheime sleutel** kent
-> In sommige gevallen zelfs zonder dat je weet welk algoritme gebruikt is voor de encryptie

- In theorie kan je elk algoritme kraken, maar de kans op succes hangt af van 2 factoren
	- De hoeveelheid **tijd** die je hebt voor het bericht irrelevant wordt
	- De hoeveelheid **bronnen** (mensen en computerbronnen zoals CPU en GPU) die ja kan gebruiken

### Technieken
Het is soms mogelijk om **algoritmen** te **kraken** door **op zoek** te gaan naar **bepaalde patronen** in de cipher text

-> Voor het kraken van moderne algoritmen worden vaak volgende technieken gebruikt
- *Dictionary attack*: uitproberen van verschillende waarden uit een **opgegeven lijst** (bv. woordenboek of dump van wachtwoorden)
- *Brute-force attack*: uitproberen van **alle mogelijke waarden** voor de geheime sleutel (heel tijdsintensief!)
- *Rainbow tables*: gebruikt vooraf **gemaakte, gesorteerde lijsten** met **cipher text** en de **overeenkomstige plain text**, wordt gebruikt voor het **kraken** van **hashing algoritmen** 

### CPU, GPU, AI of quantum computing?
#### CPU en GPU
- Bewerkingen nodig voor het kraken van een modern algoritme zijn vaak **veel efficiënter** uit te voeren **op** een **GPU dan** een **CPU** (en dus veel sneller!)

#### Artificial Intelligence (AI)
- **AI** kan mogelijks in de toekomst een grote rol spelen bij het kraken van encryptie, als **AI** modellen hiervoor **getraind kunnen worden** (bv. training met vaak gebruikte wachtwoorden)

#### Quantum Computing
- Verwacht wordt ook dat **quantum computing** veel **algoritmen voor encryptie onbruikbaar** zal **maken**, maar dit is nog niet voor morgen

### Enkele tools
- *John The Ripper*
	- kraken van zwakke wachtwoorden via een hash (bv. kraken van geëncrypteerde ZIP-file via hash waarde) 
	- maakt gebruik van **dictionary attacks** via een woordenboek en/of **brute-force attacks**
	- **geoptimaliseerd** voor kraken via **CPU**, beperkte ondersteuning voor GPU
- *Hashcat*
	- functionaliteit vergelijkbaar met John The Ripper
	- **geoptimaliseerd** voor kraken van wachtwoorden via **GPU**


## Data verduisteren
### Gegevensmaskering (masking)
=> gevoelige data **vervangen** door niet-gevoelige data

- **niet-gevoelige versie** ziet eruit en gedraagt zich **als het origineel**
	- geen wijzigingen nodig aan applicaties of dataopslagfaciliteiten
- vaak: vervangende gegevenssets distribueren voor testen en analyse
- verschillende **technieken** om gegevens te wijzigen, maar zinvol te houden:
	- **Vervanging** vervangt gegevens door authentiek ogende waarden (garanderen anonimiteit)
	- **Shuffling** leidt een vervangingsset af uit de gegevens die een gebruiker wil maskeren
		- werkt goed voor bv. financiële data in een testdatabase

### Steganografie
=> **verbergt** gegevens in een ander bestand
**voorbeeld**: grafisch, audio-, of ander tekstbestand

-> Geheime boodschap **valt niet op**
**voorbeeld**: niemand weet dat een foto daadwerkelijk een geheime boodschap bevat door het bestand elektronisch of op papier te bekijken

-> Verschillende **componenten** betrokken:
- *Ingebedde* gegevens= **geheim bericht**
- *Omslagtekst* verbergt gegevens die de **stego-tekst** produceren
	- Omslag en/of verborgen gegevens kunnen ook afbeelding of audio zijn
- *Stego-key* regelt het **verbergingsproces**
![Steganografie](images/Pasted%20image%2020231031131832.png)


### Gegevensverduistering (obfuscation)
Toepassen [geggevensmaskering](#gegevensmaskering-masking) en [steganografie](#steganografie) technieken 
- **Verduistering** maakt de boodschap verwarrend, dubbelzinnig of moeilijker te begrijpen
- Systeem kan opzettelijk berichten **door elkaar halen**
![code](images/Pasted%20image%2020231031144152.png)

#### Voorbeeld: JavaScript Obfuscator
![javascript voorbeeld](images/Pasted%20image%2020231031144228.png)


## Toegangscontrole
-> **Toegangscontrole** beperkt de toegang tot bepaalde informatie (bv. digitale bestanden of fysieke ruimten) tot bepaalde gekende personen, om zo vertrouwelijkheid (confidentiality) te garanderen

Hierbij worden vaak verschillende stappen gebruikt:
- *Authenticatie* wordt gebruikt om te bewijzen **wie je bent**
- *Autorisatie* controleert (na authenticatie) **wat je wel/niet mag doen**
- *Accounting* houdt bij (bv. in een logboek) **wat iemand gedaan heeft**

-> Dit komt uitgebreid aan bod in [De CIA toegepast](#de-cia-toegepast)



---

# Integrity
## Digitale handtekening
-> Aan bestanden (bv: PDF) kan een **digitale handtekening** toegevoegd worden voor het verzekeren van de **integriteit**

Hiermee kunnen **2 dingen** worden **gecontroleerd**:
- Het bestand is **niet gewijzigd** nadat de handtekening is gegenereerd
- Het bestand is daadwerkelijk **afkomstig v/d persoon** die de handtekening heeft gegenereerd, en niet van iemand anders

Om dit te realiseren wordt een **asymmetrisch algoritme** (public-key encryption) gebruikt (zie [H4](#confidentiality)) 

### Hoe werkt asymmetrische encryptie
-> Asymmetrische encryptie genereert een **publieke** en **private sleutel** per persoon. Deze sleutels zijn wiskundig aan elkaar gelinkt.
![Asymmetrische encryptie voorbeelden](images/Pasted%20image%2020231106195358.png)

In de rechter afbeelding: 
- Aan het bericht van Alice wordt een digitale handtekening toegevoegd, deze wordt *geëncrypteerd* met de **private sleutel** van Alice
- De **publieke sleutel** van Alice kan gebruikt worden om de handtekening te *decrypteren*. De handtekening wordt ongeldig als er iets wijzigt in het bericht, dus zo kan iedereen die dit wil **verifiëren** dat het **bericht niet gewijzigd** is
- Omdat je de private sleutel van Alice nodig hebt om de handtekening te maken, is het bericht dus **afkomstig van Alice**

Er is **GEEN vertrouwelijkheid** ([confidentiality](#confidentiality)) toevoegt
-> maar kan gerealiseerd worden door het bericht na toevoegen v/d handtekening te **encrypteren met** de **publieke sleutel** v/d **ontvanger (Bob)**.

### Voorbeeld sleutelpaar
- Je gebruikt hiervoor normaal software op eigen computer (GPG)
	- Genereer **NOOIT** jouw sleutels via een website
- **Voorbeeld publieke** en **private** sleutel
![publieke key](images/Pasted%20image%2020231106201236.png)
![private key](images/Schermafbeelding%202023-11-06%20201257.png)

### Voorbeeld handtekening (e-mail)
![voorbeeld handtekening](images/Pasted%20image%2020231106201622.png)


## Hashing algoritmes
>Hashing algoritme: één richtingsverkeer
>encrypteren en decrypteren: twee richtingsverkeer

-> **Controleren** of een bestand of bericht **niet gewijzigd** is 
	-> Een **hashing algoritme** of **hash functie** gebruiken. Hierbij wordt een bepaalde waarde (**hash**) berekend en toegevoegd aan het bestand of bericht. 

Op een later moment kan de hash functie opnieuw uitgevoerd worden, en zou de **hash waarde niet gewijzigd** mogen zijn.


- Het vormt een **reeks van bits** om naar een **reeks** van een **vast aantal bits**
- Het is een **wiskundige eenrichtingsfunctie**. Het is in de ene richting makkelijk te berekenen, maar onmogelijk in de andere richting.

### Eigenschappen
- Een hashing algoritme heeft de volgende eigenschappen:
	- De *input* kan **uit even welk aantal bits** bestaan
	- De *output* heeft **steeds hetzelfde aantal bits** (ongeacht aantal bits v/d input)
	- De *hash functie* is een **eenrichtingsfunctie** en is **onmogelijk om te keren**
	- **Twee verschillende inputwaarden** zullen **ALTIJD** een **verschillende outputwaarde** geven


### Werking hashing algoritme
![hashing algoritmes](images/Schermafbeelding%202023-11-06%20214937.png)

### MD5 en SHA
-> Populaire hashing algoritmes zijn **MD5** en **SHA**
#### MD5
- Het **Message Digest 5 Algorithm** (MD5) 
	- Ontwikkeld door Ron Rivest 
	- 128-bits output -> Is nu te weinig
#### SHA
- Het **Secure Hash Algorithm** (SHA)
	- Ontwikkeld door US National Institute of Standards and Technology (NIST)
	- **Verschillende varianten** afhankelijk v/h gewenst **aantal bits** voor de output
		- SHA-224 (224 bits)
		- SHA-256 (256 bits)
		- SHA-384 (384 bits)
		- SHA-512 (512 bits)
#### Andere hashing algoritmes
- Uiteraard bestaan er nog **vele andere** hashing algoritmes
- Test het [hier](https://www.fileformat.info/tool/hash.htm) zelf uit

### Botsing
Hashing algoritmes 
=> *In theorie* moeten ze **ALTIJD** een **andere output** hebben voor **verschillende inputs**
=> *In praktijk* **NIET ALTIJD** mogelijk, er zijn immers **veel meer mogelijke inputs dan outputs** (met vast aantal bits)
- Wanneer je voor 2 **verschillende inputs dezelfde output** waarde krijgt, spreekt men van een *botsing* of *collision*
![botsingen](images/Pasted%20image%2020231106221101.png)

-> Hashing algoritme **verliest nut** als botsingen **bewust** veroorzaakt kunnen worden


### Sterke en zwakke algoritmes
Hashing algoritmes kunnen onderverdeeld worden in **sterke** en **zwakke hashing algoritmes**

#### Zwakke algoritmes
**MD5** en **SHA-1** zijn **zwakke algoritmes** waarbij **botsingen** bewust kunnen veroorzaakt worden

-> **Zwakke algoritmes** gaan we **niet** (meer) **gebruiken** voor cybersecurity doeleinden

#### Sterke algoritmes
**SHA-2** en **SHA-3** zijn **sterke algoritmes**

-> Deze **sterke algoritmes** zullen we wel nog gebruiken voor cybersecurity doeleinden


## Toepassingen van hashing algoritmes
- **Controle** op **fouten** in data
- **Veilig bewaren** en controleren van **wachtwoorden**
- Identificeren van data aan de hand van een kleinere waarde (hash als **fingerprint**) 
- Efficiënte opslag van data in **hashtabellen** 

### Controle op fouten
-> Via een hashing algoritme kan je van een digitaal bestand de **hashwaarde berekenen** en dit toevoegen aan het bestand of publiceren op een website

- De **hashwaarde** kan op een later moment **opnieuw berekend** worden, bv. na downloaden van het bestand van een server
-> Indien de **nieuwe hashwaarde verschillend** = **bestand gewijzigd** en dus mogelijks onbruikbaar (bv. door een fout tijdens de download)

![toepassing Hashing](images/Pasted%20image%2020231110112340.png)


### Veilig bewaren van wachtwoorden
-> Gebruikersnaam en wachtwoord 
-> bewaard in **databanken**

- Databanken zijn een **efficiënte manier** om:
	- data op te slaan
	- data te analyseren
	- data op te vragen

-> **MAAR** databanken zijn een **doelwit van cybercriminelen**
=> Een **gelekte hoeveelheid gegevens** uit een databank = *Data Breach* 

- Als zo een lek **gebruikersnamen** en **wachtwoorden** bevat
	- **cybercriminelen** zullen gegevens uittesten op andere websites 
		=> grote oorzaak van hacks
	-> hetzelfde wachtwoord hergebruiken is dus sterk afgeraden!
	-> zelfde wachtwoord lichtjes aanpassen ook geen nut!
		=> gebruik een **wachtwoordmanager** en maak een uniek wachtwoord per website


#### Poging 1
- **Gebruikersnaam** & **wachtwoord** opslaan in de **databank** (als *plain text*) 
- -> bij het inloggen moeten we het volgende controleren:
	- Ingevulde gebruikersnaam == gebruikersnaam in databank?
	- Ingevulde wachtwoord == wachtwoord in databank?
- Eenvoudig
- Iemand met toegang tot de databank kan **alle wachtwoorden uitlezen** = **GEVAARLIJK**

![Poging 1](images/Pasted%20image%2020231110194126.png)

![Poging 1 Plain text](images/Pasted%20image%2020231110194206.png)

**PLAINTEXT GEVAARLIJK**:
-> Als je bij een site je **wachtwoord vergeten** bent en ze **sturen** je **wachtwoord** zomaar **door via mail** -> dan weet je dat ze het als **plain text opslaan**

#### Poging 2
- **Gebruikersnaam** & **hashwaarde v/h wachtwoord** opslaan in de **databank**
- -> bij inloggen moeten we het volgende controleren:
	- Ingevulde gebruikersnaam == gebruikersnaam in databank?
	- Hash(wachtwoord) == hashwaarde in databank?
- Iets complexer, maar hashwaarden kunnen snel berekend worden
- Iemand met toegang (al dan niet geautoriseerde) tot de databank kan de **wachtwoorden NIET uitlezen** = **VEILIG** 

![Poging 2](images/Pasted%20image%2020231110194953.png)

#### Salting
- 2 gebruikers die **hetzelfde wachtwoord** gebruiken -> voor beiden worden **dezelfde hashwaarde** opgeslagen
	-> Hierdoor weten aanvallers dat ze door 1 wachtwoord te kraken, 2 wachtwoorden kennen
	- **Salting** = extra maatregel om hashing veiliger te maken
	- Een **salt** = random reeks bits die wordt **toegevoegd** aan het wachtwoord voordat de hash berekend wordt
=> Gebruikers zullen een **verschillende hash** hebben wanneer ze **hetzelfde wachtwoord** gebruiken
![Salting](images/Pasted%20image%2020231110195847.png)

#### Samenvatting
- *Plain text* = **GEVAARLIJK**
![Plain Text](images/Pasted%20image%2020231110200118.png)
- *Hash wachtwoord* = **MATIG VEILIG**
	- Dezelfde wachtwoorden hebben dezelfde hashwaarden
	-> Cybercriminelen misbruiken dit
![hash](images/Pasted%20image%2020231110200136.png)
- *Hash wachtwoord + salt* = **EXTRA VEILIG!**
![hash en salt](images/Pasted%20image%2020231110200154.png)

![samen](images/Pasted%20image%2020231110200210.png)


## Kraken van hashing 
-> Bij het kraken probeer je voor een gekende **hashwaarde** (output) een **overeenkomstige input** te vinden

- Vanuit een hashwaarde de **oorspronkelijke input berekenen** is zo goed als **onmogelijk** (**EENRICHTINGSFUNCTIE**)
- Een mogelijkheid is om van **elke mogelijke inputwaarde** de **hashwaarde** te berekenen tot je dezelfde hash hebt (*brute-force attack*), **eventueel** met een **dictionary**

### Rainbow Tables
-> Je kan ook van verschillende inputs de hash berekenen, tot je een lijst hebt met **alle mogelijke hashwaarden** en de input

- Die **lijst** kan dan **gesorteerd** worden **op basis v/d hashwaarde**, zodat je snel input voor een hash kan vinden
	- Dergelijke lijst noemen we een *Rainbow Table* 
- Het opstellen van een *Rainbow Table* moet maar één keer gebeuren
	-> Je kan deze **downloaden** v/h internet
- Het **toevoegen** van een **salt** aan een wachtwoord maakt een *Rainbow Table* **onbruikbaar** voor het kraken!

![rainbow tables](images/Pasted%20image%2020231110201835.png)

### Vertragende hashing algoritmes
=> Om te **vermijden** dat er **veel pogingen** worden gedaan om een **hash te kraken** of een **collision** te **vinden** wordt er vaak gebruik gemaakt van *vertragende hashing algoritmes*

- Een aanvaller met meer rekenkracht moet zo toch nog steeds **lang wachten** om de hashwaarde te kraken
- Bekende voorbeelden:
	- PBKDF2
	- bcrypt
	- Argon2

## HMAC
=> Om **integriteit** en **authenticiteit** te garanderen van een bericht kunnen we *hashing* **combineren met** *symmetrische encryptie*

-  *Hash-based message authentication* (**HMAC**) 
	= **hashfunctie** die naast de input ook gebruik maakt van een **symmetrische sleutel voor** de **berekening** v/d **hashwaarde**

- Dit **lijkt goed op** [#Digitale handtekening](../images/#Digitale%20handtekening), maar bij **digitale handtekeningen** wordt **asymmetrische encryptie** gebruikt.

### Werking HMAC
![Pasted image 20231110203306.png](images/Pasted%20image%2020231110203306.png)
#### Alice (verzender)
- Berekent de **hashwaarde** v/h (versleuteld) bericht via **HMAC** met behulp v/d gedeelde geheime sleutel
- Voegt deze waarde (**HMAC digest** of **vingerafdruk**) toe aan het bericht en stuurt dit naar Bob

#### Bob (ontvanger)
- Berekent na ontvangen v/h bericht zelf de hashwaarde via HMAC met dezelfde sleutel
- Vergelijkt deze waarde met de waarde die Alice toevoegde aan het bericht
	- Indien **beide waarden overeenkomen** weet Bob dat het **bericht NIET GEWIJZIGD** is, en dat het **afkomstig is van Alice**

### Nut van HMAC
=> **HMAC** garandeert dus: 
- **bescherming** tegen een [Man-in-the-middle attack](#man-in-the-middle-attack) 
	- via gewone hashing zou een aanvaller een nieuwe hash kunnen berekenen na aanpassing van het bericht
- **Symmetrische sleutel geheim**
	- dus **enkel gekend door** de **zender** & **ontvanger** v/h bericht
- **Integriteit** (bericht is niet gewijzigd) 
- **Authenticiteit** (afkomstig van Alice)




---

# Availability
## Onvoorziene problemen
### Disaster Recovery Planning
-> Bij **rampen** is het nodig om de organisatie draaiende te houden. Als dat niet lukt kan het de organisatie beletten zijn activiteiten voort te zetten 

- Een **ramp** omvat:
	- **natuurlijke** rampen
		- Geologische rampen (bv: aardbevingen, vulkaanuitbarsting,...)
		- Meteorologische rampen (bv: bliksem, hagel, tornado,...)
		- Gezondheidsramp (bv: pandemie, quarantaines,...)
		- ...
	- **menselijke** acties die schade toebrengen
		- Gebeurtenissen op het werk (staking, ontslag, bewust trager werken,...)
		- Socio-politieke gebeurtenissen (vandalisme, blokkades protesten, sabotage, terreur,...)
		- Onderbreking in nutsvoorzieningen (stroom, communicatie,...)
		- ...

## Hoge beschikbaarheid
### Wat is het 5x9 principe?
=> **5x9** = "**The Five Nines**"
- Systemen en services kennen een uptime van 99,999%
	- Ofwel: ze zijn beschikbaar in 99,999% v/d tijd

-> Concreet: downtime bedraagt minder dan 5 minuten 15.36 seconden per jaar
![Pasted image 20231113195705.png](images/Pasted%20image%2020231113195705.png)

### Omgevingen met hoge beschikbaarheid (cruciale sectoren)
- *Financiële sector*
	- Trading, diensten beschikbaar voor klant, vertrouwen v/d klant
- *Gezondheidssector*
	- Patiëntenzorg de klok rond
- *Industrie*
	- Fabrieken, assemblage,...
- *Transportsector*
	- NMBS, luchtvaart,...
- *Openbare veiligheid*
	- Staat in voor de veiligheid v/d gemeenschap (brandweer, politie, leger,...)
- *Nutsvoorzieningen*
	- Energiecentrales, waterzuiveringsstations,...
- *Telecom sector*
	- Telefoon, internet, TV,...
- *Retail industrie*
	- Supply chains, leveren van producten,...
	- Denk aan de eindejaarsperiode

### Bedreigingen v/d beschikbaarheid
Er zijn heel wat **oorzaken** van **verlies van beschikbaarheid**
- Van het falen van systeem tot een natuurramp
	- System failure
	- Niet-doelbewuste oorzaak
	- Doelbewuste aanval
	- Natuurramp
	- ...


### Hoge beschikbaarheid kan je bekomen door
- Een zo **hoog** mogelijke **uptime** van diensten
	- Door te mikken naar veel "**nines**" uit het [5x9 principe](#wat-is-het-5x9-principe) 
- **Redundantie** om **single points of failure** te vermijden
- **Robuuste** systemen bouwen
- **Monitoren** v/d systemen
- **Backups**

#### Vermijden SPoF
=> **SPoF** = **Single Points of Failure** -> zwakste schakels die ervoor kunnen zorgen dat het ganse systeem faalt
![Pasted image 20231113200841.png](images/Pasted%20image%2020231113200841.png)


#### Redundantie 
- Een [single point of failure](#vermijden-spof) moet altijd vermeden worden. 
	- Dit kan gaan over:
		- hardware als data
		- processen
		- software
		- ...

- Oplossing: niet op **één element** vertrouwen
	- *N+1 redundantie* = algemeen principe
	-> Zorgt ervoor dat systemen **beschikbaar blijven** als er eentje faalt
	-> Componenten (N) moeten steeds **minimum één backup** component hebben (1)
	
	-> **Voorbeeld**: een auto heeft een reservewiel in de koffer voor als één v/d vier wielen faalt
	![Pasted image 20231113201824.png](images/Pasted%20image%2020231113201824.png)

**Voorbeeld**:
De organisatie kan **redundantie** inbouwen om **kritische processen over** te **nemen** op de **moment dat er eentje faalt**. Met gaat bv meerde load balancers voorzien (die eigenlijk allemaal hetzelfde doel hebben)


#### Systemen zullen falen
=> Elk **systeem** zal **ooit eens falen** -> vraag is **wanneer** en **wat dan**?
- **Robuuste systemen** hebben een **hoge tolerantie** voor **falen**

**Voorbeeld**:
routing protocols in een netwerk: 
Als een toestel faalt wordt er automatisch een ander weg gezocht tussen A en B. Robuustheid inbouwen is **meer dan enkel redundantie** voorzien

- **Oplossing**
	- Meer applicaties worden ontwikkeld met **bepaalde principes** waarin met er van uitgaat dat de applicatie vroeg of laat kan "**crashen**"
		- **Video** wordt **hervat** na **connectieverlies** bij een video call
		- Als je **webbrowser crasht**, kan je toch nog je **openstaande tabs recupereren**
	- Bij het nemen van back-ups of rond het beheer van schrijven (storage) zijn er systemen die "**self-healing**" zijn zoals ZFS (zie semester 2)


#### Monitoring
- Failures/problemen **detecteren** wanneer ze zich voordoen.
- Alerts/meldingen **weergeven** op communicatieplatformen
	- Discord
	- Microsoft Teams
	- Slack
	- ...
- **Visualisatie**
	- Vrije ruimte op harde schijven 
	- Temperaturen van fysieke machines
	- CPU/memory load
	- ...

![Pasted image 20231113210828.png](images/Pasted%20image%2020231113210828.png)
![Pasted image 20231113210859.png](images/Pasted%20image%2020231113210859.png)
![Pasted image 20231113210939.png](images/Pasted%20image%2020231113210939.png)


## Back-ups
### De 3-2-1-regel
- **Minstens 3** kopieën
- Op **minstens 2** verschillende media
- Waarvan **minstens 1** andere locatie
-> Meer mag altijd
![Pasted image 20231113213609.png](images/Pasted%20image%2020231113213609.png)

**Voorbeeld**:
![Pasted image 20231113213812.png](images/Pasted%20image%2020231113213812.png)
- 1 kopie op laptop
- 1 kopie op een NAS
- 1 kopie op de cloud

- 1 + 1 + 1 = **3** kopieën
- Laptop + NAS + cloud = **2**+ verschillende media
- Cloud = **1** off-site media

#### Varianten op de 3-2-1-regel
-> De regel is uitgevonden voor cloud storage bestond
- 1 of meer v/d kopieën was vroeger bijna sowieso steeds offline
- Als alles verbonden is, kan het ook beschadigd worden (bv. ransomware)
	- bv. laptop, NAS, cloud,...
- **Synchronisatie ≠ back-up**

##### 3-2-1-1-0-regel
- **1** v/d kopieën moet offline staan zonder enige verbinding (air gapped)
	- net als toen de cloud nog niet bestond
- Verifiëer de kopieën: ze mogen geen (**0**) fouten bevatten
	- **Test** de back-ups zelf en het herstellen van back-ups

##### 4-3-2-regel
- De regel
	- **4** kopieën
	- Minstens **3** verschillende media
	- Minstens **2** ander locaties
- Vooral voor gespecialiseerde bedrijven

### Welke media?
- Tapes
- [HDD](#HDD)
- [SSD](#SSD)
- USB
- CD/DVD/Blu-ray
- [NAS](#nas--network-attached-storage)
- [Cloud](#Cloud)

#### HDD vs SSD

![Pasted image 20231113215829.png](images/Pasted%20image%2020231113215829.png)

##### HDD
![Pasted image 20231113214848.png](images/Pasted%20image%2020231113214848.png)
- Kan **NIET** tegen **schokken** of **magnetisme**
- **Hot storage**
	- Datacenters houden statistieken bij over welk HDD's (niet) lang meegaan
		- Welk model, welk merk, grootte,...
	- Voorlopige cijfers geven een gemiddelde levensduur van 6-7 jaar
- **Cold storage**
	- Geen exacte cijfers
		- ongeveer 5 jaar maximum
- Bekijk de [S.M.A.R.T. waarden](https://crystalmark.info/en/software/crystaldiskinfo/)

##### SSD
- **Beperkt** aantal **writes**
- Kan **NIET** goed tegen **hoge temperaturen**
- **Hot storage**
	- Datacenters houden ook over SSD's statistieken bij
	- Technologie is nieuw
		- nog geen harde conclusies t.o.v. HDD's
- **Cold storage**
	- Alweer geen exacte cijfers
	- Best sowieso jaarlijks eens aansluiten tegen bit rot volgens JEDEC standaard
- Bekijk de  [S.M.A.R.T. waarden](https://crystalmark.info/en/software/crystaldiskinfo/)
	- zijn anderen dan bij de HDD's


#### NAS = Network Attached Storage
![Pasted image 20231113215927.png](images/Pasted%20image%2020231113215927.png)

#### Cloud
- Handig voor **off-site back-ups**
- **Automatisch**
	- Heft er niet aan te denken om een back-up te nemen
- Wat met **privacy/kost**?
	- Let op met "free tiers"
	- Als je niet betaald, kan jouw data het product zijn
- **Synchronisatie** is **GEEN back-up**!
	- Ransomware wordt gesynct
	- Deletes worden niet tegengehouden
	- ...
	- Nood aan "**immutability** of data"
- Cloud kan on-/off-prem geïnstalleerd worden
	- Ook gekend als on-/off-site


### Hoeveel back-ups bijhouden en hoe lang?
- Je houdt best **meerdere back-ups** over **langere tijd** bij
	- Je hebt niet altijd door wanneer er fouten of malware in je back-ups zitten
	- Je wil zo ver kunnen terugkeren in de back-ups als nodig om een correcte kopie van een beschadigd bestand terug te vinden
- **Automatiseer back-ups** zodat je deze **NIET vergeet**
- **Full** back-up
	- Telkens opnieuw de **volledige inhoud opslaan** (copy-paste)
	- **Verbruikt** veel **tijd** en **ruimte**
- **Incrementele** back-ups
	- Houdt **1 kopie** bij, samen met **alle verschillen** ("delta's") die er later gebeurd zijn
	- **Bespaard** veel **tijd** en **ruimte**
	- Maakt het mogelijk om bv. 30 wekelijkse back-ups + 20 maandelijkse + 5 jaarlijkse kopieën bij te houden

![Pasted image 20231113223637.png](images/Pasted%20image%2020231113223637.png)

### Test de back-ups!
- "Is it really a back-up if you haven't attempted to restore?"
- "**Untested back-up = no back-up**"

### Heb je wel alles geback-upt?
- Smartphones
	- SMS, foto's, contacten,...
- Tablets
- USB-sticks, CD's, DVD's videocassettes,...
- Social media
	- foto's, bestanden in chats,...
	- Facebook, WhatsApp, Discord,...
- Cloud
	- Google drive, OneDrive, Dropbox, MEGA,...
- E-mails





---

# De CIA toegepast
## Toegangscontrole 
### Wat is toegangscontrole?
-> Subjectief identificeren van een **subject** (gebruiker, machine, proces) 
-> Geven v/d nodige rechten om toegestane **acties** op het **object** (bestand, netwerk, machine,...) uit te voeren

>Belangrijk om niet te vergeten
>
>**subject** -> gebruiker, machine, proces,...
>**object** -> bestand, netwerk, machine,...

We maken gebruik van [**modellen**](#de-4-meest-gebruikte-modellen-voor-toegangscontrole) voor toegangscontrole en het **AAA-raamwerk**

![Pasted image 20231123104409.png](images/Pasted%20image%2020231123104409.png)
#### AAA-raamwerk
De 3 A's staan voor
- **Authentication**
	- Wie of wat de actie mag uitvoeren
- **Authorization**
	- Wat wel of niet mag op de diverse objecten
- **Accounting**
	- Houdt bij wat de actie precies inhield

-> Zie [hier](#het-aaa-raamwerk) voor het vervolg en uitbreiding van de 3 A's

### Fysieke bescherming
- **Omheiningen en barricades**
	- Buitenste beveiligingslaag
	- Omheining, beveiligingspoorten, slagbomen, bewakers,...
	
- **Biometrie**
	- Geautomatiseerde methode om **persoon** te **herkennen**
	- Op basis van een fysiologisch of gedragskenmerk
	- Gezichtsherkenning, vingerafdruk, irisscan, stemherkenning,...
	- Kunnen basis vormen voor zeer veilige **authenticatie**
	
- **Badges en toegangslogboeken**
	- Een **badge** geeft een persoon toegang tot een gebied of ruimte
	- Toegangsbadges maken gebruik van verschillende technologieën, zoals een magneetstrip, streepjescode of biometrie
	- Het systeem registreert de transactie zodat deze later kan worden opgehaald
	- Rapporten laten zien wie op welk tijdstip toegang vroeg

Op de basis kunnen we dan ook verder werken met:
- **Beveiligingskabels en sloten**
	- Kabelsloten
	![Pasted image 20231123105955.png](images/Pasted%20image%2020231123105955.png)
	- Belangrijke apparatuur in afgesloten ruimte
	- Veiligheidskooien rond apparatuur
	
- **Logout timers**
	- Toestel automatisch vergrendelen na periode van inactiviteit
	- Indien niet: doe `windows + l` anders is het systeem kwetsbaar voor onbevoegde gebruikers
	
- **Inlogtijden** beperken
	- Blokkeren login buiten kantooruren
	
- **GPS-tracking**
	- Mobiel toestel terugvinden bij diefstal of verlies
	- Maakt gebruik van GPS satellieten
	
- **Inventaris** en **RFID tags**
	- Radiofrequentie-identificatie (RFID) gebruikt radiogolven
	- Wordt gebruikt om object te identificeren en volgen
	- RFID-inventaris houdt tags bij van items die men wil volgen
	
- **Stroomvoorziening**
	- **Cruciaal** bij beschermen van informatiesystemen
	- **Continue levering** noodzakelijk voor server- en gegevensopslagfaciliteiten
	
- **Verwarming, ventilatie en airconditioning (HVAC)**
	- Cruciaal voor de **veiligheid** van mensen en informatiesystemen
	- Regelen de **omgeving** (temperatuur, vochtigheid, luchtstroom en luchtfiltering)
	
- **Hardware monitoring**
	- Vaak aangetroffen in grote **server farms**
	- Een **server farm** is een faciliteit die honderden of **duizenden servers** voor bedrijven huisvest
	
- **Bewakers** & **escorts** (=> begeleid worden)
	- Fysieke toegangscontroles zijn afhankelijk van **personeel** om in te grijpen en de daadwerkelijke **aanval** of indringing te **stoppen** 
	- Bewakers kunnen toegang tot gevoelige gebieden **controleren**
	
- **Videobewaking** & **elektronische bewaking**
	- Kan beveiligingspersoneel **aanvullen** of in sommige gevallen **vervangen**
	- Mogelijk om gebieden te bewaken zonder bewakers of personeel 
	- Video's kunnen gedurende lange periodes bewaard worden
	- Mogelijkheid tot bewegingsdetectie en bijhorende meldingen
	
- **RFID** & **draadloze bewaking**
	- Gebruikt om belangrijke informatiesystemen te beheren en te **lokaliseren**

### De 4 meest gebruikte modellen voor toegangscontrole

-> Bekijk [deze video](https://youtu.be/7PJdQGALG2k) voor de uitelg


#### Mandatory Access Control (MAC)
![Pasted image 20231123115144.png](images/Pasted%20image%2020231123115144.png)
- Meest gebruikte vorm voor toegangscontrole
	-> geschikt voor omgevingen waar maximale veiligheid noodzakelijk is
- Werkt met **classificatieniveaus/beveiligingsniveaus** bijgehouden door systemen
	-> enkel subjects met juiste machtigingen krijgen toegang tot een object

##### Voorbeeld
niveaus in het leger of de FBI
-> Unclassified -> Confidential -> Secret -> Top Secret
![Pasted image 20231123114003.png](images/Pasted%20image%2020231123114003.png)

#### Discretionary Access Control (DAC)
![Pasted image 20231123115234.png](images/Pasted%20image%2020231123115234.png)
- Minst beperkte vorm voor toegangscontrole
- **Eigenaar** van een object **verleent of beperkt toegang** tot het object aan een ander subject

##### Voorbeeld
Op Unix/Linux
`rwxrwxrwx` = rechten of permissies op Unix/Linux
![Pasted image 20231123114807.png](images/Pasted%20image%2020231123114807.png)


#### Role-based Access Control (RBAC)
![Pasted image 20231123120019.png](images/Pasted%20image%2020231123120019.png)
- Gebruikers krijgen machtigingen via hun rol
- RBAC kan werken met DAC of MAC door het beleid van beide af te dwingen

##### Voorbeelden
###### Voorbeeld 1
Werknemers hebben geen toegang tot **financiële gegevens** v/d collega's (zoals: lonen,...). 
Werknemers bij HR zijn verantwoordelijk voor het uitbetalen v/d lonen dus zij moeten wel toegang hebben, anders kunnen zij de lonen niet uitbetalen of aanpassen indien nodig

###### Voorbeeld 2
Op **school** wordt dit ook gebruikt, want leerkrachten hebben toegang tot lokale, maar leerlingen niet.
Ook hebben leerkrachten geen toegang tot het bureau v/d directeur of serverroom
-> Zo heeft elke gebruiker bepaalde mogelijkheden bij zijn bepaalde rol

#### Rule-based Access Control (RuBAC)
- Toegangscontrole op basis van specifieke regels
- Kan een aanvulling zijn op MAC, DAC of RBAC
- Veelal vastgelegd in Access Control List (ACLs)

##### Voorbeeld
###### Voorbeeld 1
Geen enkele werknemer mag buiten de kantooruren toegang hebben tot de financiële dossiers

###### Voorbeeld 2
Enkel toestellen op een bepaalde locatie krijgen toegang (google stuurt je altijd bericht of het nieuwe toestel op een nieuwe locatie wel van jou is)

### Het AAA-raamwerk

-> Bekijk [deze video](https://youtu.be/Mpv5g2m305s) voor uitleg

**Toegangscontrole** maakt gebruik v/h **AAA** (of **triple-A**) raamwerk
![Pasted image 20231123121459.png](images/Pasted%20image%2020231123121459.png)
- **Authentication** (authenticatie)
	- Wie mag iets doen?
- **Authorization** (autorisatie)
	- Wat mag iemand wel/niet doen?
- **Accounting** (boekhouding)
	- Wie heeft wat gedaan?

#### Voorbeelden
##### Voorbeeld 1: bankautomaat
- **Authentication** (authenticatie)
	- Enkel iemand met de juiste bankkaart en pincode heeft toegang tot de bankrekening (multi-factor authenticatie)
	
- **Authorization** (autorisatie)
	- Iemand kan niet meer geld afhalen dan hij heeft
	- Er is een maximum bedrag dat afgehaald kan worden per dag
	
- **Accounting** (boekhouding)
	- Op de rekeninguittreksels staat er welk bedrag er wanneer is gestort op of afgehaald v/d rekening

##### Voorbeeld 2: forum
- **Authentication** (authenticatie)
	- Je moet je aanmelden met een username en passwoord
	
- **Authorization** (autorisatie)
	- Een gewone gebruiker kan berichten lezen en zelf berichten aanmaken
	- Administratoren kunnen ook 
		- Topics beheren of afsluiten
		- Berichten van andere gebruikers bewerken en verwijderen 
		- Toegang hebben tot administrator topics die niet voor gewone gebruikers zichtbaar zijn
	
- **Accounting** (boekhouding)
	- Er zijn logs die bijhouden wanneer wie welke actie op het forum heeft uitgevoerd
	-> Op 25/09/2020 heeft administrator Alice het bericht met id 68132 van Bob verwijderd


#### Authentication (authenticatie)
Hier zijn de verschillende authenticatiemethoden:
- **What you know**
	- Wachtwoorden, wachtwoordzinnen of pincodes => wat de gebruiker weet
	- Wachtwoorden -> meest populaire verificatiemethode
- **What you have**
	- Smartcards en beveiligingssleutelhangers => wat de gebruiker heeft
- **Who you are**
	- Uniek fysiek kenmerk, zoals vingerafdruk, gezichtsherkenning,... => wat de gebruiker identificeert (wordt biometrie genoemd)

##### Multi-factor authenticatie (2FA)
Bij **multi-factor authenticatie** (ook gekend als **2FA**) worden ten minste twee verschillende authenticatiemethoden gebruikt.

###### Voorbeeld: Yubico - YubiKey
![Pasted image 20231123124023.png](images/Pasted%20image%2020231123124023.png)


#### Autorisatie (autorisatie)
=> Bepaalt **wat** een gebruiker **kan doen** na authenticatie

- Toegang tot welk (netwerk) **bronnen**?
- Wat kan de gebruiker doen met de bronnen?
	- Read, Copy, Create, Delete
	
- Verzameling **attributen** beschrijven de toegang
	- Attributen worden vergeleken met **authenticatiedatabase** 
	- Op basis hiervan vastleggen beperkingen (via **autorisatieregels**)
	
- Een **autorisatiebeleid** leg de **autorisatieregels** vast voor het beheren van toegang
-> **Voorbeeld**: enkel senior administratoren hebben toegang tot de serverruimte


#### Accounting (boekhouding)
=> Herleidt een **actie** naar een **onderwerp** (gebruiker of proces)

- Organisatie kan dit gebruiken voor **audits** of **facturering**
- **Verzamelende gegevens** kunnen zijn:
	- Inlogtijd gebruiker
	- Succesvol aangemeld?
	- Welke bronnen gebruikt?
- Laat toe om **acties, fouten en vergissingen** te **traceren**
- Implementatie via technologieën, beleid, procedures en opleidingen
- **Logbestanden**: gedetailleerde informatie op basis van gekozen parameters

## VPN
### Virtual Private Netwerk (VPN)
![Pasted image 20231123130207.png](images/Pasted%20image%2020231123130207.png)
Configuratie van een **Virtual Privaat Netwerk (VPN)**
- **Beveiligde communicatie** over publiek netwerk
	-> vb: 2 kantoren op verschillende geografische locatie kunnen zo via het internet op een veilige manier verbonden worden
	
- Maakt **privénetwerk** over het internet aan tussen **verschillend fysieke locaties**
	-> vb: gebruikers kunnen van thuis op een beveiligde manier aan IT diensten binnen bedrijfsnetwerk
	-> vb: mensen die Netflix gebruiken kunnen zich op een server zetten in een ander land om van dat land de series te zien

een **Virtual Privaat Netwerk (VPN)**:
- Maakt gebruik van **IPSec** (=> reeks protocollen ontwikkeld voor beveiligde services via netwerken te realiseren)
- **IPSec**: authenticatie, integriteit, toegangscontrole en vertrouwelijkheid
- Hoofdzakelijk: **encryptie** (codering) en **authenticatie** (verificatie) met **IPSec**
- Bescherm van **data in beweging**
- Veel varianten mogelijk
![Pasted image 20231123130535.png](images/Pasted%20image%2020231123130535.png)


## Certificaten
**Voorbeeld** van een certificaat
![Pasted image 20231123192650.png](images/Pasted%20image%2020231123192650.png)

### De basis
- Een **digitaal certificaat** is gelijkaardig aan een elektronisch paspoort
- Het laat gebruikers, toestellen en organisaties toe om **veilig informatie** te **delen** over het internet
- Een certificaat **authenticeert** en verifieert dat de verzender van bericht daadwerkelijk die persoon is
	- Het koppelt een persoon aan een publieke sleutel
- Certificaten worden uitgedeeld door betrouwbare organisaties
- Certificaten bieden ook **vertrouwelijkheid** aan door encryptie

### Gebruik bij websites
- HTTPS **versleutelt data** tussen webserver en client
	- Je kan zien of **encryptie** aan staat aan het *"slot" icoon*
![Pasted image 20231123191321.png](images/Pasted%20image%2020231123191321.png)

- HTTPS bewijst niet dat de website geen frauduleuze website is (bv: phishing)
	- Root CA's zijn geen politie
	- Initiatieven als **Let's Encrypt** laten iedereen toe om **SSL certificaten** te **genereren** voor domeinnamen (g00g1e.com, microsof1.com,...)
	- *"slot" icoon* in de webbrowser toont **enkel** aan of er **encryptie** is

- Elke browser heeft een **lijst** van **vertrouwde autoriteiten** (Root Certificate Authorities) 
	- Certificate Manager - *Firefox*
	![Pasted image 20231123192507.png](images/Pasted%20image%2020231123192507.png)
	
	- Certificate Manager - *Chrome*
	![Pasted image 20231123192551.png](images/Pasted%20image%2020231123192551.png)
	
- Organisaties bewijzen aan een **Root CA** dat ze het **internetdomein** bezitten 
![Pasted image 20231123192336.png](images/Pasted%20image%2020231123192336.png)

### Opstellen van een certificaat
-> Een digitaal certificaat volgt een **gestandaardiseerd formaat (X.509)** zodat software dit kan lezen en verstaat, ongeacht de verzender
![Pasted image 20231123193640.png](images/Pasted%20image%2020231123193640.png)

- Een **Public Key Infrastructure (PKI)** is de verzameling van beleid, functies en procedures om certificaten te bewaren, beheren, verspreiden, gebruiken en ongeldig te verklaren


## SSH
### Beveiligde toegang op afstand
**Externe toegang** laat toe dat gebruikers op afstand toegang hebben tot een lokaal intern netwerk

- **Telnet**
	- Verouderd
	- Data (o.a. login en wachtwoord) verzonden in plain text
	- **NIET veilig!**
	
- **SSH (Secured Shell)**
	- Opvolger Telnet
	- Encryptie van data
	
- **SCP (Secured Copy)**
	- Veilige overdracht van bestanden naar extern systeem
	- Maakt onderliggend gebruik van SSH (authenticatie + bescherming van data in beweging)
	
- **SFTP**
	- Veilige opdracht van bestanden naar extern systeem
	- FTP (overdracht van bestanden) over SSH
	- Je kan gebruik maken van grafische programma's zoals FileZilla, WinSCP, CyberDuck,...

![Pasted image 20231123195825.png](images/Pasted%20image%2020231123195825.png)
![Pasted image 20231123195910.png](images/Pasted%20image%2020231123195910.png)





---

# H8: Red team
## De 5 fasen
![Pasted image 20231129193409.png](images/Pasted%20image%2020231129193409.png)
### Opgelet!
De fasen van een aanval vaak lineair voorgesteld
-> In de praktijk echter **cyclisch proces** 
![Pasted image 20231130164205.png](images/Pasted%20image%2020231130164205.png)
**Voorbeeld**:
Als je in fase 3, 4 of 5 iets nieuws vindt kan je terug beginnen met reconnaissance om opnieuw dingen te vinden.


### Reconnaissance
#### Doel
- Zo veel mogelijk **informatie inwinnen** (foot-printing) over het doelwit, zonder dat men "ontdekt" wordt
- Zo **onopvallend** mogelijk
- Proberen het **doelwit** of organisatie te **begrijpen**
	- Wie? Wat? Hoe? Waar? ...
	- Waar zit de waardevolle data?
- **Beperken** v/h **aanvalsdomein** (beperkte IP-range, beperkt aantal toestellen,...) op basis van ingewonnen informatie
- Vaak wordt alles bijgehouden in een **informatiedatabank** 
	- Laat ook toe om prioriteiten op te stellen

#### 2 types
- Er zijn **twee types** van informatie inwinnen:
	- *Passief*
	- *Actief*
-> De grens is soms zeer dun

**Voorbeeld** (website bezoeken):
- Is eigenlijk contact maken (webpagina opvragen aan de server, in principe kunnen ze dit naar jou traceren)
- Wordt continu door honderden andere gebruikers gedaan (is dus heel moeilijk om te achterhalen dat jij ooit eens deze website hebt bezocht)
- Is dus onopvallend => Passief

##### Passief
-> Geen direct contact
- Anoniem: niemand kan achterhalen wie je bent

**Voorbeeld**:
- Surfen naar de website (op een "normale" manier)
- Publieke bronnen bekijken (bv. social media, kranten artikels, vacatures)
- Kijken hoe personeel zich inlogt op websites, in gebouwen,...

##### Actief
-> Direct contact

**Voorbeeld**:
- Bellen naar de helpdesk 
- Naamkaartjes vragen
- Solliciteren


#### Zoekmachines
- Elke zoekmachine heeft zijn eigen verzameling resultaten
	- [Google](https://google.com) 
	- [Bing](https://bing.com)
	- [Yandex](https://yandex.com)
	- [DuckDuckGo](https://duckduckgo.com)
	- [Yahoo!](https://yahoo.com)
- Elke zoekmachine heeft zijn eigen operatoren
	- [Google Search Operators: The Complete List](https://ahrefs.com/blog/google-advanced-search-operators/)
	- [Google Hacking Database](https://www.exploit-db.com/google-hacking-database)
- Sommige zoekmachines ondersteunen ook geavanceerde tools
	- Reverse image search

![Pasted image 20231129195713.png](images/Pasted%20image%2020231129195713.png)


#### Openbare databanken
Er zijn een hele boel openbare databanken die we legaal kunnen raadplegen
- [Overheid Vlaanderen](https://overheid.vlaanderen.be/praktisch/bibliotheken/databanken-en-zoeksystemen)
- [Staats blad monitor](https://www.staatsbladmonitor.be)
- [Witte gids](https://www.wittegids.be/)

![Pasted image 20231129201147.png](images/Pasted%20image%2020231129201147.png)


#### Job sites / vacatures
- Geven vaak informatie over belangrijke posities in een bedrijf
- Vacatures geven vaak inzicht in de gebruikte technologieën binnen een bedrijf
![Pasted image 20231130130534.png](images/Pasted%20image%2020231130130534.png)

#### Social media
- Vaak zetten mensen (onbewust) foto's of **gevoelige informatie** van zichzelf of hun werk **online**
- **Voorbeelden**
	- [Facebook](https://facebook.com)
	- [Linkedin](https://linkedin.com)
	- [Twitter](http://twitter.com)
	- [Instagram](https://instagram.com)
- Er zijn gespecialiseerde tools om informatie van social media te verzamelen
	- *Online*: PeekYou, Intelius, Pipl, Maltego,...
	- *Command line*: theHarvester, recon-ng, inSpy,...
![Pasted image 20231130130954.png](images/Pasted%20image%2020231130130954.png)

#### E-mailadressen vinden
Je kan ook e-mailadressen terug vinden van een vereniging of organisatie
- [hunter.io](https://hunter.io)
![Pasted image 20231130131219.png](images/Pasted%20image%2020231130131219.png)
-> Die e-mailadressen kan je dan eens testen op phishing

#### Websites
- De meeste organisaties hebben tegenwoordig een website
- Bevat vaak veel informatie
	- Personeel
	- Contactgegevens
	- Structuur bedrijf
- Websites kunnen ook op zich geanalyseerd worden
	- [Net craft](https://www.netcraft.com)
	- [Built with](https://builtwith.com)
	- [Wappalyzer](https://www.wappalyzer.com)
	- Ingebouwde developer tools, plug-ins (bv: r3con),... in de browser
- Soms is het beter om een hele website offline te downloaden
	- Laat toe om te experimenteren 
	- Vermijd dat jouw gedrag opvalt
	- HTTrack


#### Who is
- [Who is?](https://whois.domaintools.com)
![Pasted image 20231130132137.png](images/Pasted%20image%2020231130132137.png)

#### DNS
- Zet een **domeinnaam** (makkelijk voor mensen) om naar een **IP-adres** (moeilijk voor mensen, maar nodig voor computers)
- Kan veel informatie geven over een website
- Tools
	- nslookup
	- dig
	- host
	- dnsrecon
	- dnsmap
	- ...
![Pasted image 20231130132830.png](images/Pasted%20image%2020231130132830.png)

#### IoT
- IoT devices zijn vaak heel slecht beveiligd en bieden zo een toegang tot het bedrijf
- [Shodan](https://www.shodan.io/) is een zoekmachine voor IoT-apparaten verbonden met het internet
![Pasted image 20231130133011.png](images/Pasted%20image%2020231130133011.png)


### Scanning and enumeration
#### Doel
- Zoeken naar **zwakke punten** in de **systemen** v/h doelwit
	- *Asset management*: bedrijven dienen een inventaris te maken van hun systemen. Zo kunnen ze een inschatting maken naar kwetsbaarheid en stabiliteit toe
- Verzamelen welke technologieën gebruikt worden en welke versie
	- Eenmaal de gebruikte technologie en versie gekend zijn
	-> kwetsbaarheden opzoeken die misbruikt kunnen worden voor een aanval
	-> [exploit database](https://www.exploit-db.com/)
- Vaak technischer en actiever dan reconnaissance


#### Standaardtools
- **Ping**
	- Welke toestellen kan ik bereiken?
	- Idee over hoe goed de connectie is
- **Traceroute** / **tracert**
	- Welke route leggen berichten af in het netwerk?
	- 3 pings per tussenliggend toestel

![Pasted image 20231130154104.png](images/Pasted%20image%2020231130154104.png)


#### Scanning
- *Port Scanning*: detecteren van **open poorten** en services die draaien op het doelwit
- *Network Scanning*: gebruikte **IP-adressen** in het netwerk opsporen, bepalen welke **besturingssystemen** draaien op de toestellen, bepalen welke **toestellen** met elkaar **verbonden** zijn,...
- *Vulnerability Scanning*: Onderzoeken of er **gekende kwetsbaarheden** in het netwerk aanwezig zijn


##### Poort Scanner
- Scant de netwerkpoorten van een toestel af
	- *Open poort*: een programma aanvaart connecties op deze poort (**interessant**)
	- *Gesloten poort*: de poort is open, maar er draait geen programma achter (**NIET interessant**)
	- *Gefilterde poort*: we kunnen niet achterhalen of deze poort open of toe is, want er komt geen antwoord terug (misschien geblokkeerd door een firewall?)
- Verschillende mogelijkheden
	- Nmap
	- Masscan
	- MegaPing
	- ...
![Pasted image 20231130154421.png](images/Pasted%20image%2020231130154421.png)
-> Zie [hier](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers) voor een volledig overzicht van **alle poortnummers**


###### Nmap
- Bestaat sinds 1997
- Is één v/d populairste poort scanners
- Kan ook gokken naar **welk programma** en versie **achter** een **open poort draait**
- Wordt ook gebruikt als **netwerk scanner**
- Heeft ook een **grafisch user interface**: *Zenmap*
![Pasted image 20231130154805.png](images/Pasted%20image%2020231130154805.png)
![Pasted image 20231130154834.png](images/Pasted%20image%2020231130154834.png)


##### Netwerk Scanner
- **Scant** het **netwerk** af naar **toestellen** en **verbindingen**
- Moet wel **eerst toegang** hebben tot het netwerk 
- Verschillende mogelijkheden
	- LanState Pro
	- PRTG Network Monitor
	- Intermapper
	- Nagios
	- SolarWinds
![Pasted image 20231130155013.png](images/Pasted%20image%2020231130155013.png)


##### Vulnerability Scanner
- **Scant** het **netwerk** af naar **gekende kwetsbaarheden** die misbruikt kunnen worden
- Moet wel **eerst toegang** hebben tot het netwerk
- Verschillende mogelijkheden
	- OpenVAS
	- Nessus
	- MetaSploit (heel bekend)
	- ...
![Pasted image 20231130155318.png](images/Pasted%20image%2020231130155318.png)


#### Enumeration
- **Informatie** verzamelen op **applicatie-niveau**
	- Dus **NIET enkel** toestellen, IP-adressen en poorten
- **Vervolg op scanning**
- We **misbruiken** verschillende **netwerkprotocollen** zodat deze ons **meer** **informatie** geven over
	- Netwerkschrijven
	- Loginsystemen
	- FTP servers
	- SMB servers
	- ...

### Gaining access, Maintaining acces, Covering tracks
#### Gaining Access
- **Ontfutselen** van **logingegevens**
	- Meeste hack aanvallen slagen door [social engineering](#kunst-van-het-oplichten)
	- Reconnaissance is belangrijk om te bepalen wie er kwetsbaar is voor welke vorm van [social engineering](#kunst-van-het-oplichten)
- Gebruik maken van **exploits**
	- Vooral bij niet up-to-date systemen
- **Password cracking**
	- Dictionary 
	- Brute force
- ...


#### Maintaining Access
- Ook **gekend** als *persistence*
- Als het **aangevallen toestel afgesloten** wordt, **verlies** je ook **toegang**
	- Hoe zorg je ervoor dat je **erna nog op het netwerk** kan?
	- Installeren van **malware**
		- Rootkits, backdoors, reverse shells,...
	- Aanmaken **nieuwe gebruikers**
	- ...
- **Privilege escalation**
	- Ervoor zorgen dat je (onrechtmatig) **root-rechten** krijgt
- **Pivoting**
	- Van **toestel naar toestel springen** in het netwerk v/h doelwit
	- **Eenmaal binnen** in het netwerk, kan je **meer zien en doen**
	- Let op dat je niet wordt gedetecteerd (evasion)


#### Covering Tracks
- Onopgemerkt blijven
- **Verwijderen bewijsmateriaal**
	- **Voorbeeld** logging op een systeem: 
		- Logs verwijderen is een bewijs op zich
- **Verstoppen** van **gebruikte bestanden**
	- Gebruikers **kijken** vaak **NIET** in de *tmp-mappen*
- Als je een bestand manipuleert, **wijzigt** de **timestamp**
	- Zet deze terug
- ...


### Pentests & audit reports
#### Pentest
- Binnen de 5 fasen -> enkel **passieve** reconnaissance wettelijk toegelaten
- Voor elke andere interactie met een bedrijf, persoon of organisatie is **uitdrukkelijke toestemming** nodig
	- Vaak gecombineerd met een NDA (Non-Disclosure Agreement)
- Bij afspraken krijgt de white-hat hacker te horen wat binnen de **scope** valt
	- Dit zijn de tools, servers, mensen, software, hardware,... die de hacker mag proberen onderzoeken en aanvallen. Dit bepaalt dus ook wat voor soort pentest dit zal zijn (intern/extern, web application / social engineering, white/grey/black box)
- Dit onderzoek noemt men een *pentest* (= penetration test) of *security audit*

#### White / Grey / Black Box
- *White*: 
	- Security team weet zoveel mogelijk
	- Krijgen toegang tot alles (documentatie, broncode van applicaties, menselijk contact met de werknemers...)
	
- *Black*:
	- Ethische hacker gedraagt zich als een hacker van buitenaf 
	- Geen voorkennis -> moet vanaf nul beginnen
	- Kost veel energie en tijd -> valt soms vrij duur uit
	
- *Grey*: 
	- Deze vorm ligt tussen de vorige twee 
	- Enkele elementen gekend (IP-adressen of namen van systemen) 
	- Kent vaak geen details


#### Audit Report
- **Geschreven rapport** wordt opgeleverd als conclusie v/d pentest met de gevonden kwetsbaarheden en potentiële verbeterpunten
- Vaak een **momentopname** en kan nooit alle tekortkomingen omvatten
- Gericht op zowel **non-technische** business personen als het **IT-team** die met het resultaat aan de slag moet gaan
	- Bevat meestal een lijst van **vulnerabilities**, mogelijke **exploits** en **threats**


##### Vulnerability/Exploit/Threat
![Pasted image 20231130170216.png](images/Pasted%20image%2020231130170216.png)
###### Vulnerability
Een **Security Vulnerability** is een fout, kwetsbaarheid of misconfiguratie in de software waar hackers misbruik van kunnen maken

###### Exploit
Een **Exploit** is de manier waarop een hacker een security vulnerability kan misbruiken om een aanval uit te voeren. Vaak is dit een **specifiek stuk geschreven code**

###### Threat
Een **Threat** is de waarschijnlijkheid waarmee een exploit een security vulnerability zal misbruiken binnen een organisatie





---

# H9: Het beschermen van een ICT-omgeving
![Pasted image 20231209161012.png](images/Pasted%20image%2020231209161012.png)

## Een diepe verdediging
![Pasted image 20231209161539.png](images/Pasted%20image%2020231209161539.png)
- **Gelaagde beveiliging** 
	- Meest omvangrijke beveiliging
	- Als cybercriminelen de eerste laag kunnen binnendringen, is er altijd nog een tweede
	- **Meerdere lagen = meerdere barrières**
	
- **Beperken van toegangen** tot informatie
	- Vermindert kans op aanval
	- Alleen werknemers krijgen toegang tot informatie die ze **nodig hebben**
	
- **Diversiteit**
	- **Varieer in manieren van beveiliging**
	- Als de toegang tot één laag verschaft is mogen de andere lagen niet in gevaar komen
	- Gebruik dus in de lagen verschillende encryptie algoritmen
	
- **Obscuring** of **verduisteren** van informatie
	- Kan ook bescherming bieden
	- Organisatie kan bv. zijn OS (besturingssysteem) geheimhouden
	- Is een extra -> geen hoeksteen voor beveiliging
	
- **Simplicity** of **eenvoud**
	- Hogere beschikbaarheid
	- Als beveiliging complex is => grotere kans op fouten 


-> Steun **NOOIT** op slechts één enkel concept
**Voorbeeld**:
Security by obscurity op zich alleen is een **bad practice**

=> Streef dus altijd naar een gevarieerde combinatie


## Systemen en apparaten beschermen
### Host Hardening
![Pasted image 20231209162608.png](images/Pasted%20image%2020231209162608.png)
- Beveiliging van het **besturingssysteem** (OS)
	- Standaardconfiguratie aanpassen
	- Verwijderen onnodige software
	- Beveiligingspatches en updates

- Installeren **anti-malware**
	- Bescherming tegen virussen, worms, key loggers, spyware
	- Mobiele apparaten zijn ook kwetsbaar
	- **Let op met gratis software** -> Kan zelf malware bevatten

- **Beheer van** *patches*
	- Kunnen centraal beheerd worden 
	- Servicepack
		- Uitgebreide update-applicatie
		- Beschikbaar gesteld door fabrikant
		- Combineert verschillende patches en upgrades

- **Host-gebaseerde** *Firewall*
	- Regelt inkomend en uitgaand netwerkverkeer

- **Host** *Intrusion Detection Systems* (*HIDS*)
	- Controleert verdachte activiteiten


### Draadloze en mobiele apparaten
#### WEP (Wired Equivalent Privacy)
- Basisbescherming WiFi
- 10 tot 26 hexadecimale karakters (40 - 104 bits)
- **NIET meer veilig**

#### WPA / WPA2 (WiFi Protected Access)
- Grote verbetering ten opzichte van WEP
- Gebaseerd op AES
- Tegenwoordig is WPA2 de standaard

#### Wederzijdse authenticatie
Het toevoegen van **wederzijdse authenticatie**
- Voorkomt man-in-the-middle aanval (rogue access point)
- Authenticatie tussen beide entiteiten


### Bescherming van (host) data
#### Bestandstoegangscontrole
- **Machtigingen** op **bestanden en mappen**
- Ingesteld per gebruiker of groep gebruikers

#### File encryption
=> *Bestandscodering*
- **Encrypteren** van **gevoelige data**
- Kan op individuele bestanden of op hele harde schijf
	- Bv. BitLocker op Windows of LUKS op Linux

#### Systeem- en gegevensback-ups
- **Reservekopie** van **gevoelige data**
- Typisch op verwijderbare media (bv. tape drive)


### Content control
#### Content screening en blokkering
![Pasted image 20231210113046.png](images/Pasted%20image%2020231210113046.png)
- Beperkt de inhoud waartoe een gebruiker toegang heeft met een webbrowser via internet
- Kan bepaalde sites blokkeren
	- Pornografie
	- Controversiële religieuze of politieke inhoud
	- Social media (nuttig in bedrijfsomgevingen)
	- Torrents
	- ...

**Voorbeeld**:
Ouderlijk toezicht dat de ouders in staat stel om zijn/haar kind te beschermen tegen verschillende sites


### Disk cloning, deep freeze, kiosk mode
Software om besturingssysteem en configuratiebestanden te beschermen

#### Disk clone
- **Image** (bv. ISO) van volledige **harde schijf**

>Volledige uitleg
>
>De **inhoud v/d harde schijf** v/d computer wordt naar **naar** een **afbeeldingsbestand** gekopieerd (kan altijd teruggezet worden)


#### Deep freeze
- "Bevriest" de partitie v/d harde schijf
- Alle wijzigingen door gebruiker verloren bij herstarten
- Vooral nuttig voor publieke toestellen
	- **Voorbeeld**: internetcafé

>Volledige uitleg
>
>Deep freeze "bevriest" de partitie v/d harde schijf. Wanneer een gebruiker het systeem opnieuw opstart, **keert** het **systeem terug** naar de **bevroren configuratie**. Het systeem **slaat geen wijzigingen op** die de gebruiker aanbrengt, dus **geïnstalleerde applicaties** of opgeslagen **bestanden gaan verloren** wanneer het systeem opnieuw wordt opgestart.



#### Kiosk mode
- Afgesloten omgeving waar je niet zomaar uit kan 
- Heeft niets te maken met de harde schijf op partities, het is meer een software matige gevangenis
- Meer preventief t.o.v. disk clone en deep freeze
- Vooral nuttig voor publieke toestellen
	- **Voorbeeld**: Tablets in de bibliotheek

>Volledige uitleg
>
>Kiosk mode zorgt ervoor dat de **functionaliteit** van het systeem **sterk beperkt** wordt. Terwijl **disk clone** en **deep freeze** het systeem vooral **herstellen** na gebruik, verhindert **kiosk mode** ervoor dat de **gebruiker niets kan aanpassen** dat niet is gewenst. 
>
>**Voorbeeld**: in de bibliotheek kan je op computers de databank van de bibliotheek raadplegen, maar je kan geen browser openen om te surfen op het internet of het startscherm openen om andere programma’s te gebruiken. Ook het gebruik van schermen voor het tonen van informatie / slideshows/ ,,, op publieke ruimtes maken gebruik van dergelijke maatregelen: het systeem dient enkel om de informatie te tonen, niet om gebruikt te worden. De naam “kiosk mode” is van deze situatie afgeleid.
>![Pasted image 20231210114323.png](images/Pasted%20image%2020231210114323.png)


### Virtualisatie/Sandboxing
- Programma's worden uitgevoerd in een **virtuele omgeving** (ook soms sandbox genoemd)
- Programma's **hebben niet door** dat ze in een virtuele omgeving draaien
- Als **hackers** via de software zich een weg naar binnen hacken, **zitten** ze nog steeds **vast in de virtuele omgeving** en niet direct op het besturingssysteem v/h toestel
- Soms lukt het daders echter om deze sandbox te omzeilen en zo toch code uit te voeren op het besturingssysteem v/h slachtoffer


## Server Hardening
### Beveiligde toegang op afstand
**Externe toegang** laat toe dat gebruikers op afstand toegang hebben tot een lokaal intern netwerk

- **Telnet** (**NIET** veilig)
	- Verouderd
	- CLI op afstand
	- Data verzonden in plain text
		- o.a. login en wachtwoord
- **SSH**
	- Opvolger Telnet
	- Encryptie van data
	![Pasted image 20231211215638.png](images/Pasted%20image%2020231211215638.png)
- **SCP**
	- Veilige overdracht van bestanden naar extern systeem
	- Maakt onderliggend gebruik van SSH
		- authenticatie + bescherming van data in beweging
- **SFTP**
	- Gelijkaardig aan SCP
	- Maakt ook onderliggend gebruik van SSH
	- Makkelijker in gebruik met visuele programma's
- **VPN**
	- Meer dan CLI of overdracht bestanden


### Administratieve maatregelen
#### Poorten en services beveiligen
- Via open **poorten** kunnen cybercriminelen achterhalen welke **services** er draaien op een host
- Op veel systemen draaien meer services dan **nodig**
- Beheerder moet: 
	- Elke service bekijken 
	- Nagaan of deze noodzakelijk is 
	- Mogelijke **risico's** inschatten

#### Geprivilegieerde accounts
=> (root, admin, superuser,...)
- **Geprivilegieerde accounts** zijn krachtigste accounts
- Hebben vaak verhoogde of zelfs onbeperkte **toegang**
- Beheerder moet:
	- Deze accounts voldoende **beveiligen**
	- Eventueel **verwijderen** om risico's te beperken


#### Group policies
- Onderdeel van **Active Directory**
- Voor gebruik in **Windows** omgeving
- Laat toe om bepaalde **veiligheidsmaatregelen** in te stellen voor een groep gebruikers
	- **Voorbeeld**: Password policy, vergrendelingsbeleid, toegang tot bronnen,...

![Pasted image 20231211220400.png](images/Pasted%20image%2020231211220400.png)


#### Logboeken en waarschuwingen
- Een logboek registreert **gebeurtenissen** op een systeem
- Bevatten uitgebreide **informatie** voor elke gebeurtenis
- Belangrijk voor computerbeveiliging (AA**A** = accounting)

![Pasted image 20231211220601.png](images/Pasted%20image%2020231211220601.png)

-> zie **logboeken**


## Network Hardening
### Netwerkapparaten beschermen
#### Network Operations Centers (NOC)
- Op één of meerder locaties
- Bieden gedetailleerde **status van netwerk**
- Ground zero voor oplossen van netwerkproblemen, prestatiebewaking, softwaredistributie en updates, communicatiebeheer en apparaat beheer

![Pasted image 20231211221232.png](images/Pasted%20image%2020231211221232.png)

#### Netwerkapparaten: switches, routers,...
- Hart van het moderne netwerk
- Kwetsbaar voor diefstal, hacking en toegang op afstand
- Doelwit voor aanvallen op netwerkprotocollen of DOS aanvallen

![Pasted image 20231211221312.png](images/Pasted%20image%2020231211221312.png)

#### Firewalls
- Hardware- of software die het netwerk beveiligen
- Voorkomt dat ongeautoriseerd of potentieel gevaarlijk verkeer het netwerk binnenkomt
- Zorgt ervoor dat alleen de noodzakelijke poorten zichtbaar en beschikbaar zijn

![Pasted image 20231211221333.png](images/Pasted%20image%2020231211221333.png)

#### IDS
**IDS** = **Intrusion Detection System**

#### IPS
**IPS** = **Intrusion Prevention System**


### Een modern beveiligingsoperatiecentrum
#### Security Operation Centers (SOC)
- **Security Operations Centers** (SOC's) bieden een **aantal diensten** aan
	- Monitoring
	- Beheer
	- Oplossingen voor bedreigingen
	- Gehoste beveiliging
	- ...
- Als bedrijf **zelf** een **SOC opzetten** of een **gespecialiseerde firma** inschakelen
- De **belangrijkste elementen** van een **SOC** zijn:
	- Mensen 
	- Processen
	- Technologie

![Pasted image 20231211222019.png](images/Pasted%20image%2020231211222019.png)


#### Security Information and Event Management (SIEM)- systemen
- Verzamel en filter gegevens
- Detecteer en classificeer bedreigingen
- Analyseren en onderzoeken van bedreigingen
- Uitvoeren van preventieve maatregelen
- Pak toekomstige bedreigingen aan 


![Pasted image 20231211222301.png](images/Pasted%20image%2020231211222301.png)


## Asset management
- Bedrijven moeten weten welke **hardware**- en **software assets** in het bedrijf aanwezig zijn -> Deze assets moeten immers beveiligd zijn
- **Assets management**: 
	- Omvat het **beheren** van al deze **assets**
	- Volledig overzicht (= **inventaris**) van alle hardware- en software
- Het bedrijf kan zo een **inschatting** maken welke **beveiligingsgevaren** er zouden kunnen zijn
- Volgende zaken worden in beschouwing genomen
	- Elk hardware systeem
	- Elk besturingssysteem (OS)
	- Elk hardware netwerk toestel
	- Elk network device operation systeem
	- Elke software applicatie
	- Elke firmware
	- Alle language runtime environments
	- ...
- Sommige bedrijven kiezen voor een **automatische inventarisatie**
	- software die automatisch deze zaken bijhoudt

### Toepassingen
- **Beveiliging**
- **Updatebeleid**
	- Welke hardware of software verouderd is, zal dan binnenkort geüpdatet moeten worden?
- **Helpdesk**
	- Een klant of medewerker heeft een probleem, de helpdesk weet meteen over welk specifiek toestel het gaat
	![Pasted image 20231211223223.png](images/Pasted%20image%2020231211223223.png)


## Nood aan experten
### Hoe word je een cybersecurity expert?
- **Cybersecurity specialisten**
	- Moeten kunnen **reageren op dreigingen** zodra ze zich voordoen (ongeacht werktijden)
	- **Analyseren beleid, trends en intelligentie** om **cybercriminelen** te **begrijpen** (vaak dus speurwerk)

- Advies om cybersecurity specialist te worden:
	- **Studeer**
		- Leer de basis door IT cursussen te volgen, wees een **levenslange leerling** -> cybersecurity verandert voortdurend en specialisten moeten bijblijven
	- **Behaal certificeringen**
		- Certificeringen van organisaties zoals Microsoft en Cisco **bewijzen dat je** over de **kennis beschikt** die nodig is om werk te zoeken als cybersecurity-specialist
	- **Stages**
		- Het zoeken naar een stage binnen het gebied van cybersecurity kan leiden tot opportuniteiten in de toekomst
	- **Professionele organisaties**
		- Word lid van computerbeveiligingsorganisaties, woon vergaderingen en conferenties bij en sluit je aan bij forums en blogs om kennis op te doen van andere experten

#### Certificeringen
-> Behoefte aan bekwame en deskundige informatiebeveiligingsprofessionals
-> IT-industrie stelde standaarden voor zodat cyber-specialisten bewijs konden leveren van vaardigheden en kennisniveau

- **CompTIA Security +**
	- Door CompTIA gesponsord testprogramma 
	- Certificeert de competentie van IT-beheerders op het gebied van informatieborging

- **EC-Council Certified Ethical Hacker (CEH)** 
	- Certificering op gemiddeld niveau 
	- Cybersecurity-specialisten met deze referentie beschikken over de vaardigheden en kennis voor verschillende hackpraktijken

- **SANS GIAC Security Essentials (GSEC)** 
	- Goede keuze als instapmodel voor cybersecurity-specialisten 
	- Kunnen aantonen dat ze de beveiligingsterminologie en -concepten begrijpen en over de vaardigheden en expertise beschikken die nodig zijn voor 'hands-on' beveiligingsrollen
	- Het SANS GIAC-programma biedt ook aanvullende certificeringen op het gebied van beveiligingsadministratie, forensisch onderzoek en auditing
	
- **(ISC)² Certified Information Systems Security Professional (CISSP)**
    - Leverancier neutrale certificering
    - Voor cybersecurity-specialisten met technische en managementervaring
    - Formeel goedgekeurd door het Amerikaanse ministerie van Defensie (DoD)
    - Wereldwijd erkende branchecertificering op het gebied van beveiliging
    
- **ISACA Certified Information Security Manager (CISM)**
    - Voor cybersecurity-specialisten die verantwoordelijk zijn voor het beheren, ontwikkelen en toezicht houden op informatiebeveiligingssystemen op bedrijfsniveau
    - Geschikt voor degenen die de beste beveiligingspraktijken ontwikkelen
    
- **Cisco Certified Network Associate Security (CCNA Security)**
    - Valideert dat een cyberbeveiligingsspecialist de kennis en vaardigheden heeft om Cisco-netwerken te beveiligen

