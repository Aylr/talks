## Tactical Applied
# AI & ML
### Successes, Lessons Learned & Getting Started


---

# Who Am I

#### Taylor Miller PharmD

GAP first

successes

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

### What is AI/Machine Learning?
### The healthcare gap
### Successes & Benefits
### Lessons Learned
### Getting Started

---

## Where is AI/ML Used?

- Marketing: Amazon
- Smartphones
- Consumer Goods (Siri, Alexa, Google Home)
- Entertainment: Netflix
- Travel: Airbnb
<br/>
<br/>
<br/>

## Everywhere
## ...except healthcare

---

# What about _in_ healthcare?

## Dr Topol

---

#### ML/AI in Healthcare

> We should stop training radiologists right now, in 5 years deep learning will have better performance.

#### Geoff Hinton

<img src="https://images.thestar.com/content/dam/thestar/news/world/2015/04/17/how-a-toronto-professors-research-revolutionized-artificial-intelligence/geoffrey-hinton-3.jpg.size-custom-crop.1086x0.jpg" style="width: 300px" />

Note:
- fathers of deep learning
- While there may not be much ML/AI in healthcare now, there will be
- It will come faster than you realize.

1. A Bay area startup gets FDA approval.
2. Their pricing will be orders of magnitude lower than humans.
3. Payers will change reimbursement.
4. Done.


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

## A Brief History

<div class="fragment history"><h4>1842 Ada Lovelace</h4><img src='assets/Ada_Lovelace.jpg' style='biopic'/></div>
<div class="fragment history"><h4>1950 Alan Turing</h4><img src='assets/alan_turing.jpg' style='biopic'/></div>
<div class="fragment history"><h4>1956 Marvin Minsky</h4><img src='assets/Marvin_Minksy.jpg' style='biopic'/></div>
<div class="fragment history"><h4>1965-1980s Expert Systems</h4><img src='assets/foo.jpg' style='biopic'/></div>
<div class="fragment history"><h4>1986 Rina Dechter</h4><img src='assets/Rina_Dechter.jpg' style='biopic'/></div>
<div class="fragment history"><h4>2006 Andrew Ng</h4><img src='assets/Andrew_Ng.jpg' style='biopic'/></div>

<div class="fragment ref">https://waitbutwhy.com/2015/01/artificial-intelligence-revolution-1.html</div>

Note:
- **Insert short one liners about each here**

---

# ML In 5 Minutes

---

# Signal vs Noise

**show two graphs illustrating this concept**

---

# 2 Main Types

### Unsupervised

### Supervised

Note:

- No ground truth
- Known ground truth

---

# Ground Truth?

| age | height | gender | BMI | A1c | Retinopathy |
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

# Traning

## 80% of data is used to train.

## 20% used to evaluate & validate.

Note:

- This is where you'll hear algorithm names like
    + random forest
    + linear regression
    + lasso
    + neural nets
    + deep learning

---

# But, Why ML?

Note:
- we've talked about
    + hype
    + what
- not the **why**

---

# LACE Score

- 30 day readmission or death
- Easy to calculate

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
- Tell the story of readmissions

---

# LACE Gotchas

#### 4812 patients in Ontario

<div class='ref'>doi:  10.1503/cmaj.091117</div>

Note:
- What are the changes that your patients == Ontario patients?

---

# ML vs LACE

<div class='fragment'><h2>LACE: 0.68*</h2></div>
<div class='fragment'><h2>Best literature: 0.78†</h2></div>
<div class='fragment'><h2>Client ML Model: 0.84</h2></div>

<div class='ref'>*doi: 10.1503/cmaj.091117<br/>†doi: 10.1142/9789813207813_0027.</div>

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

---

# Clinical

#### CLABSI Risk
#### Sepsis Risk
#### Heart Failure Readmission
#### COPD Readmission

Note:
- CLABSI & sepsis risks actionable and displayed in workflows
- 

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

---

# Lessons Learned

---

## Incorporating ML

1. Choose a problem
2. Organize a rich dataset
3. Develop & validate a model
4. Surface the insight

---

# Key Players

### Domain Expert
### Analyst
### Data Scientist

---

# Technical Integration

## This is hard

**maybe not needed?**

---

## Hard Lessons Learned

1. Predictions + actionable insight
2. Surface in workflows
3. Insights need context
4. Fail fast
5. Continually monitor

Note:
1. Paired
2. key to adoption
3. context for informed decision
4. work with domain expert
5. lots of moving parts

---

## healthcare.ai

### Feature Engineering

### Model Development

### Model Deployment

### Extras

---

# Resources

- healthcare.ai community
    + Education
    + Open Source Tools
    + Slack channel
- healthcatalyst.com
- taylor.miller@healthcatalyst.com

---

# healthcare.ai

## Open Source

## Simplify and Expedite Adoption

<div class="fragment">
    <img src="https://healthcare.ai/wp-content/uploads/2017/11/levi-thatcher-600x0-c-default.png" style="width: 100px"/>
    <img src="https://healthcare.ai/wp-content/uploads/2017/02/michael-mastanduno-600x0-c-default.jpg" style="width: 100px"/>
    <img src="https://healthcare.ai/wp-content/uploads/2017/02/Taylor-Larsen-600x0-c-default.png" style="width: 100px"/>
    <img src="https://healthcare.ai/wp-content/uploads/2017/07/Mike-Levy-600x0-c-default.jpg" style="width: 100px"/>
    <img src="https://healthcare.ai/wp-content/uploads/2017/02/taylor-miller-600x0-c-default.jpg" style="width: 100px"/>
</div>

---

<span class="menu-title" style="display: none">Step 2. Git-Commit</span>

### <span class="gold">STEP 2. GIT-COMMIT</span>
<br>

```shell
$ git add PITCHME.md
$ git commit -m "New slideshow content."
$ git push

Done!
```

<span class="code-presenting-annotation fragment current-only" data-code-focus="1">Add your PITCHME.md slideshow content file.</span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="2">Commit PITCHME.md to your local repo.</span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="3">Push PITCHME.md to your public repo and you're done!</span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="5">Supports GitHub, GitLab, Bitbucket, GitBucket, Gitea, and Gogs.</span>

---
