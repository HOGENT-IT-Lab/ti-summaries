# e-marketing

## Websites

### Structure
HTML (content & structure)-CSS (presentation)-JS (behaviour)

Optimized for different screen sizes (devices). Holy Trinity:
- desktop
- tablet
- smartphone

### Bootstrap
Most used free open source front-end-framework

| Advantages               | Disadvantages                    |
|:-------------------------|:---------------------------------|
| responsive               | unused code                      |
| cross browser compatible | all bootstrap pages look similar |
| short dev time           |                                  |
| flexible                 |                                  |
| free                     |                                  |

### Internal structure
- Sitemap html & xml
- Robots.txt
- Homepage links to categories or articles or ...
- these contain sub categories or ...
- ...

Create good internal linking structure! -> Google crawler can discover most of site and include it in search results

Sitemap: Provide linking structure of website

Robots.txt: indicate visting web crawlers which portions of the website they are allowed to visit.
```
User-agent: *
Disallow: /folder/
Disallow: /file.hmtl/
Disallow: /image.png
```

**DARK PATTERNS**: intentional bad linking to discourage user from doing something (e.g. unsubscribing)

### Design

3 Pillars of good design
- Accesibility
- Purpose
- Consistency

#### Accesibility
Do's and Don'ts

Physical or motor disabilities:
- *Do* make large clickable actions - *Don't* demand precision clicking
- *Do* give fields in a form space - *Don't* bunch them together
- *Do* design for keyboard or speech only use - *Don't* make dynamic content that requires a lot of mouse movement
- *Do* design with mobile and touchscreen in mind - *Don't* have short time out windows
- *Do* provide shortcuts  - *Don't* tire users with lots of typing and scrolling

Low vision:
- *Do* use goed colour contrasts and a readable font size - *Don't* use low colour contrasts and a small font size
- *Do* publish all information on web pages - *Don't* bury information in downloads
- *Do* use a combination of colour, shapes and text - *Don't* only use colour to convey meaning
- *Do* follow a linear, logical layout - *Don't* speard content all over a page
- *Do* put buttons and notifications in context - *Don't* separte actions from their context

Autistic:
- *Do* use simple colours - *Don't* use bright contrasting colours
- *Do* write plain English - *Don't* use figures of speech and idioms
- *Do* use simple sentences and bullets - *Don't* create a wall of text
- *Do* make buttons descriptive - *Don't* make buttons vague and unpredictable
- *Do* build simple and consistent layouts - *Don't* build complex and cluttered layouts

Google Search Console can detect Mobile Usability issues

#### Purpose
What is the user looking for/What are you trying to achieve?

#### Consistency
Consistent across all digital channels and devices
- visual style
- writing style
- tone of voice
- message
- ...

### Mobile First
More mobile users than desktop users! But desktop users spend more time on website.

Mobile search is Google's new priority

Indexing: crawl mobile or desktop version first -> crawl other version (if mobile version present boost mobile rank) -> determine mobile and desktop rankings

- Use same meta robots tags on mobile and desktop
- Don't lazy-load
- Use same content

Google AMP = Accelerated Mobile Pages

## SEO

Appearing at top of search results (SERP: serch engine results page) is very important. The biggest search engine is Google.

spiders/crawlers/bots

### 3 Pillars of SEO
- Technique
- Content
- Authority

Google prefers:
- HTTPS
- responsive
- relevant keywords in meta description
- short url

Domain authority vs Page authority
- lots of links from other pages to yours?

### SERP Features
- Adwords (Top or Bottom)
- In-Depth Article
- Local Teaser Pack
- Shopping Results
- Knowledge Card
- Top Stories
- Site Links
- Featured Snippet
- Knowledge Panel
- Related Questions
- Tweet
- Image Pack
- Local Pack
- Reviews
- Video

## Search Engine Advertising

- Google Display Network
    - Smart Display campaigns
    - Standard Display campaign
    
- Google Search Network
    - Appear in Google search sites or seatch partners
    - Types of ads:
        - Text
        - Dynamic search
        - call-only
    - Ad extensions:
        - Sitelinks
        - Local extensions
        - Call extensions
        - Callout extensions
        - App extensions
        - Review extensions
        - Social extensions
        - Seller ratings
- Google Keyword Planner: Find new keywords, Analyze search volume -> create a keyword plan
    - Broad match
    - Phrase match: ""
    - Exact match: []
- Google Ads
    - Account with campaigns with groups with ads with keywords
    - Ad rank = CPC Bid x Quality Score
    - Quality Score:
        - Relevance
        - Landing page
        - Expected CTR
    - Common metrics:
        - CPM (cost per thousand impressions)
        - CPC (cost per click)
        - CPA (cost per acquisition)
- Google Shopping
- YouTube
    - Skippable in-stram
    - Non-skippable in-stream
    - Video discovery
    - Bumper
    - Outstream
    - Masthead
- Google Merchant Center

## Google Analytics

Acquistion types:
- Organic traffic
- CPC/PPC
- Referral
- Email
- Social
- None (direct traffic)

Explorations:
- Free from
- Funnel
- Path
- Segment overlap
- User
- Cohort
- User lifetime

Attribution types:
- First click
- Linear
- Position-based
- Time decay
- Data Driven
- Last click

## Social media

### Meta Ads
- Reach and frequency buying 
- Auction buying

Targeting options:
- Demographics
- interests
- behaviours
- connections
- remarketing
- look-alike audiences


## AI

- AI vs Machine Learining vs Deep learning

Deep Neural Network

Overfitting & underfitting

General adversarial network

Recommendation systems
- Candidate generation: content based or collaborative filtering
- Scoring
- Reranking
