## Tactical Applied
# AI & ML
### Successes, Lessons Learned & Getting Started

---

# Who Am I

#### Taylor Miller PharmD
#### Data Scientist @ Health Catalyst

github: @Aylr

---

# Who are you?

Note:
- how many work in healthcare?
- how many are analysts?
- clinicians?
- leaders?
- new to machine learning?

---

# What to expect

### Healthcare gap
### What is ML?
### Why ML?
### Successes
### Lessons Learned

---

## Where is AI/ML Used?

- Marketing & Finance: Amazon, PayPal
- Consumer Goods: Siri, Alexa, Google Home, Tesla
- Entertainment: Facebook, Netflix, YouTube, Spotify
- Travel: Airbnb, Kayak, Uber
- Industry: GE, Kuka
<br/>
<br/>
<br/>

<div class='fragment'><h2>Everywhere</h2></div>
<div class='fragment'><h2>...except healthcare<sup>*</sup></h2></div>

Note:
- GE **digital twin**

---

# What about _in_ healthcare?

Note:
- Lots of hype from Google, IBM, etc.

---

> We should stop training radiologists right now, in 5 years deep learning will have better performance.

#### Geoff Hinton

<img src="https://images.thestar.com/content/dam/thestar/news/world/2015/04/17/how-a-toronto-professors-research-revolutionized-artificial-intelligence/geoffrey-hinton-3.jpg" style="width: 300px" />

_(one of the creators of deep learning)_

Note:
- one of the creators of deep learning
- While there may not be much ML/AI in healthcare now, there will be
- It will come faster than you realize.
- process
    1. A Bay area startup gets FDA approval.
    2. Their pricing will be orders of magnitude lower than humans.
    3. Payers will change reimbursement.
    4. Done.

---

<h1 style='margin-top: -2em'>A Brief History</h1>

<h2 class="fragment current-only history">1842 Ada Lovelace<br/><img src='https://upload.wikimedia.org/wikipedia/commons/1/1a/Ada_Lovelace_portrait_circa_1840.jpg' style='width:200px' /></h2>
<h2 class="fragment current-only history">1950 Alan Turing<br/><img src='https://upload.wikimedia.org/wikipedia/commons/a/a1/Alan_Turing_Aged_16.jpg' style='width:200px' /></h2>
<h2 class="fragment current-only history">1956 Marvin Minsky<br/><img src='http://www.kurzweilai.net/images/Marvin-Minksy-PhD-B3.png' style='width:200px' /></h2>
<h2 class="fragment current-only history">1965-1980s Expert Systems</h2>
<h2 class="fragment current-only history">1986 Rina Dechter<br/><img src='https://upload.wikimedia.org/wikipedia/commons/thumb/d/d0/Rina_Dechter.jpg/1920px-Rina_Dechter.jpg' style='width:200px' /></h2>
<h2 class="fragment current-only history">2006 Andrew Ng<br/><img src='https://spark-summit.org/2016/wp-content/uploads/sites/12/2016/04/Andrew-Ng.jpg' style='width:200px' /></h2>

Note:
- Ada: the first computer programmer and recognized potential of a computing machine even though she never saw one work.
- Alan: General purpose computing. Father of CS
- Marvin: Coined the term AI. Foundational work for neural nets.
- Rina: CS PhD U of CA coined the term deep learning
- Andrew: Google researcher first commerical deep learning use

---

# Just What _is_ ML?

<h2 class="fragment">Automated</h2>
<h2 class="fragment">pattern finding</h2>
<h2 class="fragment">in highly dimensional</h2>
<h2 class="fragment"><i>usually</i> noisy data</h2>

---

# Wait, What?

<h2 class="fragment">Automated</h2>
<h2 class="fragment">pattern finding</h2>
<h2 class="fragment">in highly dimensional</h2>
<h2 class="fragment">noisy data</h2>

---

# ML In 5 Minutes

Note:
- Let's dig in a little deeper

---

# Signal vs Noise

![img](assets/signal2.png) &nbsp;&nbsp;&nbsp;&nbsp;
![img](assets/noise2.png)

---

# 2 Main Types

### Unsupervised

### Supervised

Note:

- No ground truth
- Known ground truth

---

# Ground Truth?

| Age | Height | Gender | BMI | A1c | Readmission |
| --- | ------ | ------ | --- | --- | ----------- |
| 33  |  152   |   F    |  18 | 5.6 |      N      |
| 66  |  168   |   M    |  21 | 8.9 |      Y      |
| ... |  ...   |   ...  | ... | ... |     ...     |
| 27  |  140   |   M    |  18 | 7.2 |      N      |
| 45  |  159   |   F    |  31 | 7.5 |      Y      |

Note:

- **Dimension** = **feature** = **field**
- **target** = ground truth

---

# Traning Data

## 80% train

## 20% Evaluate & validate

Note:

- This is where you'll hear algorithm names like
    + random forest
    + linear regression
    + lasso
    + neural nets
    + deep learning

---

# Wait!
## Do I need
# Big Data ?

<div class='fragment'><h2>Nope!</h2></div>

Note:
- Remember it all depends how strong the signals are in the noise.
- We've seen some models work well with only 100s of rows.
- We've seen lots of success with 10k-30k rows.

---

# But, Why ML?

Note:
- we've talked about
    + hype
    + how it works
- not the **why**

---

# LACE Score

### Risk of 30 day readmission or death

Note:
- study ran from 2004-2008 and published in 2010
- to tell this story, let's talk about readamissions
- this illustrates well how healthcare changes

---

# LACE

|     |                        |
| --- | ---------------------- |
| L   | Length of stay         |
| A   | Acute admission        |
| C   | Charleston comorbidity |
| E   | ER visits last 6 mo    |
|     |                        |

Note:
- Here's what's great about LACE
- Easy to calculate at discharge
- has had a large impact in quality of care

---

# LACE Gotchas

## 4812 patients in Ontario
## Only works at discharge

<div class='ref'>doi:  10.1503/cmaj.091117</div>

Note:
- Raise your hands if your patient demographics == Ontario patients?
- How actionable is it at discharge?

---

# ML vs LACE

#### C-Statistic

<div><h2>LACE: 0.68<sup>&ast;</sup></h2></div>
<div class='fragment'><h2>Best published ML: 0.78<sup>&ast;&ast;</sup></h2></div>
<div class='fragment'><h2>Client ML Model: 0.84</h2></div>

<div class='ref'><sup>&ast;</sup>doi: 10.1503/cmaj.091117<br/><sup>&ast;&ast;</sup>doi: 10.1142/9789813207813_0027</div>

Note:
- C-stats measure the balance between True Positive & False Positive Rates
- 0.5 (coin flip) <--> 1.0 (perfect)
- Model (~13k training set)
    - This means better predictions,
    - less false positives & less false negatives
    - > 100 variables
    - insights delivered in workflow = **actionable**

---

# Success Stories

Note:
- We don't aim for sexy headlines
- in other words we aren't trying to cure cancer
- chipping away at pragmatic problems
- healtcare is rife with low hanging fruit

---

# Clinical

#### CLABSI Risk
#### Sepsis Risk
#### Heart Failure Readmission
#### COPD Readmission

Note:
- 50% CLABSI reduction large teaching hospital
- CLABSI & sepsis risks actionable and displayed in workflows

---

# Operational & Financial

#### Propensity to Pay
#### Service Line Verification
#### High Cost Imaging

Note:
1. optimize resource allocation & decrease uncompensated care:
    - determines who needs reminders, financial assistance
2. Annual savings > $1.2 mil validating chart reviews

---

# Population Health

#### No-shows
#### Care Management
#### Opioid Abuse Risk

Note:
- Client able to optimize scheduling for no show patients
- Early opioid risk work

---

# Lessons Learned

---

## Incorporating ML

1. Choose a problem
2. Organize a rich dataset
3. Develop & validate a model
4. Surface the insight
5. Be Agile

Note:
- This seems obvious in retrospect.
- Surface insight in the right workflow.
- Agile development methodologies are a game changer

---

# Key Players

### Domain Expert
### Analyst
### Data Scientist

Note:
- Magic happens when you pair a good analyst with a domain expert

---

# Technical Integration

## This is hard

Note:
- Technical integration is hard.
- Make sure your data platform supports ML

---

## Hard Lessons Learned

1. Predictions + actionable insight
2. Surface in workflows
3. Insights need context
4. Fail fast
5. Continually monitor
6. Interpretation is hard

Note:
1. Paired
2. key to adoption
3. context for informed decision
4. work with domain expert
5. lots of moving parts

---
<svg width="70%" height="150px" viewBox="0 0 331 44" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"><g id="healthcareAI-logo" fill-rule="nonzero"><g id="Group"><path d="M18.5,42.5 L18.5,24.2 C18.5,19.9 17.7,18.1 12.3,18.1 C10.6,18.1 8.9,18.4 7.5,19 L7.5,42.4 L0,42.4 L0,0.9 L7.5,0.9 L7.5,13 C9.5,12.4 11.7,12 14.2,12 C25,12 26.1,17.1 26.1,23.4 L26.1,42.4 L18.5,42.4 L18.5,42.5 Z" id="Shape" fill="#FFFFFF"></path> <path d="M32.1,27.5 C32.1,16.6 35.5,12.1 45.6,12.1 C56.5,12.1 58.8,17.8 58.8,26.9 C58.8,27.7 58.8,28.5 58.7,29.3 C55.3,29.9 48.6,30.6 44.5,30.8 L39.6,31.1 C39.9,35.8 42.4,36.9 46.7,36.9 C50.7,36.9 54.4,36.5 57.5,36.1 L58.1,41.7 C54.9,42.2 50.8,42.8 45,42.8 C34.8,42.9 32.1,36.4 32.1,27.5 Z M44.5,25.7 C46.5,25.6 49.5,25.3 51.2,25.1 C51.3,24.8 51.3,24.2 51.3,23.9 C51.3,20 49.8,17.8 45.6,17.8 C40.1,17.8 39.4,21.2 39.4,25.9 L44.5,25.7 Z" id="Shape" fill="#FFFFFF"></path> <path d="M63.9,33.3 C63.9,28 66.2,24.7 72.2,23.8 C75.3,23.3 78.5,23.2 81.8,23 C81.8,19.5 80.2,18 76.3,18 C72.7,18 68.7,18.4 65.7,18.8 L65.1,13.2 C68.3,12.7 72.5,12.1 76.9,12.1 C83.6,12.1 89.1,14 89.1,21.8 L89.1,34.5 C89.1,36.5 89,38.3 88.8,40.2 C85.3,42.2 80.8,43 75.4,43 C67.1,42.9 63.9,39.7 63.9,33.3 Z M81.8,27.9 C79.6,28 77,28.1 74.9,28.6 C72.3,29.2 71.3,30.1 71.3,33.2 C71.3,36.4 73.1,37.2 76.4,37.2 C78.1,37.2 80.1,37.1 81.7,36.4 C81.8,35.2 81.9,33.7 81.9,32.4 L81.9,27.9 L81.8,27.9 Z" id="Shape" fill="#FFFFFF"></path> <path d="M96,0.9 L103.5,0.9 L103.5,34.3 C103.5,37 104.1,38.8 105.6,40.9 L99,44 C97.1,41.8 96,39.1 96,34.9 L96,0.9 Z" id="Shape" fill="#FFFFFF"></path> <path d="M121.3,4 L121.3,12.5 L127.3,12.5 L127.3,18.2 L121.3,18.2 L121.3,33.7 C121.3,36.2 122.3,37.2 124.9,37.2 C125.7,37.2 126.6,37.2 127.4,37.1 L128,42.4 C126.4,42.7 124.5,42.9 122.9,42.9 C116.6,42.9 113.9,40.1 113.9,34.4 L113.9,18.2 L109,18.2 L109,12.5 L113.9,12.5 L113.9,5.2 L121.3,4 Z" id="Shape" fill="#FFFFFF"></path> <path d="M151.9,42.5 L151.9,24.2 C151.9,19.9 151.1,18.1 145.7,18.1 C144,18.1 142.3,18.4 140.9,19 L140.9,42.4 L133.4,42.4 L133.4,0.9 L140.9,0.9 L140.9,13 C142.9,12.4 145.1,12 147.6,12 C158.4,12 159.5,17.1 159.5,23.4 L159.5,42.4 L151.9,42.4 L151.9,42.5 Z" id="Shape" fill="#FFFFFF"></path> <path d="M187.1,41.8 C184.5,42.5 181.3,42.9 177.3,42.9 C167.2,42.9 165.7,35.3 165.7,27.2 C165.7,17.4 168,12.1 179,12.1 C182.4,12.1 184.9,12.6 187,13.2 L186.4,18.7 C184.6,18.3 182.8,18 181,18 C174,18 173.2,20.1 173.2,27.2 C173.2,33.9 173.5,36.8 181,36.8 C182.8,36.8 184.5,36.5 186.4,36.1 L187.1,41.8 Z" id="Shape" fill="#FFFFFF"></path> <path d="M191.8,33.3 C191.8,28 194.1,24.7 200.1,23.8 C203.2,23.3 206.4,23.2 209.7,23 C209.7,19.5 208.1,18 204.2,18 C200.6,18 196.6,18.4 193.6,18.8 L193,13.2 C196.1,12.7 200.4,12.1 204.8,12.1 C211.5,12.1 217,14 217,21.8 L217,34.5 C217,36.5 216.9,38.3 216.7,40.2 C213.2,42.2 208.7,43 203.3,43 C195.1,42.9 191.8,39.7 191.8,33.3 Z M209.8,27.9 C207.6,28 205,28.1 202.9,28.6 C200.3,29.2 199.3,30.1 199.3,33.2 C199.3,36.4 201.1,37.2 204.4,37.2 C206.1,37.2 208.1,37.1 209.7,36.4 C209.8,35.2 209.9,33.7 209.9,32.4 L209.9,27.9 L209.8,27.9 Z" id="Shape" fill="#FFFFFF"></path> <path d="M224.4,42.5 L224.4,20.6 C224.4,18.6 224.5,16.8 224.7,14.9 C228.1,12.9 232.7,12.1 236.8,12.1 C237.9,12.1 238.9,12.2 239.8,12.3 L239.2,18.3 C238.6,18.2 237.8,18.2 237,18.2 C235.2,18.2 233.2,18.5 232,19.1 C231.9,20.3 231.8,21.8 231.8,23.1 L231.8,42.5 L224.4,42.5 Z" id="Shape" fill="#FFFFFF"></path> <path d="M243.5,27.5 C243.5,16.6 246.9,12.1 257,12.1 C268,12.1 270.2,17.8 270.2,26.9 C270.2,27.7 270.2,28.5 270.1,29.3 C266.7,29.9 260,30.6 255.9,30.8 L251,31.1 C251.3,35.8 253.8,36.9 258.1,36.9 C262.1,36.9 265.8,36.5 268.9,36.1 L269.5,41.7 C266.3,42.2 262.2,42.8 256.4,42.8 C246.2,42.9 243.5,36.4 243.5,27.5 Z M255.9,25.7 C257.9,25.6 260.9,25.3 262.6,25.1 C262.7,24.8 262.7,24.2 262.7,23.9 C262.7,20 261.2,17.8 257,17.8 C251.5,17.8 250.8,21.2 250.8,25.9 L255.9,25.7 Z" id="Shape" fill="#FFFFFF"></path> <path d="M275.7,38.6 C275.7,35.3 276.7,34.3 280.1,34.3 C283.5,34.3 284.5,35.3 284.5,38.6 C284.5,41.9 283.5,42.9 280.1,42.9 C276.7,42.9 275.7,41.8 275.7,38.6 Z" id="Shape" fill="#2AACE2"></path> <path d="M290.1,33.3 C290.1,28 292.4,24.7 298.4,23.8 C301.5,23.3 304.7,23.2 308,23 C308,19.5 306.4,18 302.5,18 C298.9,18 294.9,18.4 291.9,18.8 L291.3,13.2 C294.5,12.7 298.7,12.1 303.1,12.1 C309.8,12.1 315.3,14 315.3,21.8 L315.3,34.5 C315.3,36.5 315.2,38.3 315,40.2 C311.5,42.2 307,43 301.6,43 C293.4,42.9 290.1,39.7 290.1,33.3 Z M308,27.9 C305.8,28 303.2,28.1 301.1,28.6 C298.5,29.2 297.5,30.1 297.5,33.2 C297.5,36.4 299.3,37.2 302.6,37.2 C304.3,37.2 306.3,37.1 307.9,36.4 C308,35.2 308.1,33.7 308.1,32.4 L308.1,27.9 L308,27.9 Z" id="Shape" fill="#2AACE2"></path> <path d="M322,4.7 C322,1.6 323.1,0.5 326.4,0.5 C329.7,0.5 330.8,1.6 330.8,4.7 C330.8,7.8 329.8,8.9 326.4,8.9 C323,9 322,7.9 322,4.7 Z M322.7,12.5 L330.2,12.5 L330.2,42.5 L322.7,42.5 L322.7,12.5 Z" id="Shape" fill="#2AACE2"></path></g></g></g></svg>
<br/>

## 100% Open source

## Simplify & Expedite
## ML Adoption

<div class="fragment">
    <img src="https://healthcare.ai/wp-content/uploads/2017/11/levi-thatcher-600x0-c-default.png" style="width: 100px; height: 100px;"/>
    <img src="https://healthcare.ai/wp-content/uploads/2017/02/Taylor-Larsen-600x0-c-default.png" style="width: 100px; height: 100px;"/>
    <img src="https://healthcare.ai/wp-content/uploads/2017/02/michael-mastanduno-600x0-c-default.jpg" style="width: 100px; height: 100px;"/>
    <img src="https://healthcare.ai/wp-content/uploads/2017/02/taylor-miller-600x0-c-default.jpg" style="width: 100px; height: 100px;"/>
    <img src="https://healthcare.ai/wp-content/uploads/2017/07/Mike-Levy-600x0-c-default.jpg" style="width: 100px; height: 100px;"/>
</div>

Note:
- Feature Engineering
- Model Development
- Model Deployment
- Extras

---

# Resources

- healthcare.ai community
    + ML Basics, Tutorials, Lessons Learned
    + Open Source Tools
    + Slack channel
- taylor.miller@healthcatalyst.com

![hcai](assets/healthcareai_hex_logo_300.png)