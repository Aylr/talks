autoscale: true

# Crushing
# Pipeline Debt
_With_
# **Great Expectations**

Taylor Miller @ Superconductive

---

# 👋

I'm from Superconductive.com
We are data mercenaries for hire hell-bent on data quality.

---

# agenda

1. A thing we do that is absolutely crazy
2. How to crush pipeline debt
3. Live demo


---

![](leviathan.jpg)

Here's some software!
BTW it's...
# [fit] .
# [fit] .
# [fit] .

---

![](leviathan.jpg)

Here's some software!
BTW it's...

# [fit] **_Un_**documented
# [fit] .
# [fit] .

---

![](leviathan.jpg)

Here's some software!
BTW it's...

# [fit] **_Un_**documented
# [fit] **_Un_**tested
# [fit] .

---

![](leviathan.jpg)

Here's some software!
BTW it's...

# [fit] **_Un_**documented
# [fit] **_Un_**tested
# [fit] **_Un_**stable

---

![](leviathan.jpg)

Here's some ~~software~~ data!
BTW it's...

# [fit] .
# [fit] .
# [fit] .

---

![](leviathan.jpg)

Here's some ~~software~~ data!
BTW it's...

# [fit] **_Un_**documented
# [fit] .
# [fit] .

---

![](leviathan.jpg)

Here's some ~~software~~ data!
BTW it's...

# [fit] **_Un_**documented
# [fit] **_Un_**tested
# [fit] .

---

![](leviathan.jpg)

Here's some ~~software~~ data!
BTW it's...

# [fit] **_Un_**documented
# [fit] **_Un_**tested
# [fit] **_Un_**stable

---

# Pipeline Debt

![right fit](leviathan.jpg)

---

# Pipelines are like software.
# And also not.

|                       |     Software    |   Pipelines   |
|-----------------------|-----------------|---------------|
| _inputs are_          | usually known   | often unknown |
| _assumptions are_     | often crisp     | murky         |
| _failures created by_ | your code       | data creators |
| _tests verify_        | code            | data          |
| _tests run_           | at compile time | at run time   |
    
---

# But why test pipelines?

1. Risk mitigation
2. Pager mitigation
3. Increase trust & credibility
4. Codify knowledge & assumptions

---

# What types of risk can we mitigate?

1. Pipeline risks
2. Data risks

---

# [fit] Pipeline Risks:

# [fit] missing / empty files **_mangled loads_**
# [fit] corrupted data
# [fit] **_schema changes_** outages
# [fit] unexpected values

---

# [fit] Data Risks:

#[fit] **_distribution drift_**
#[fit] model assumptions
#[fit] **_evolution_** edge cases
#[fit] bias **_outliers_**

---

# Great Expectations
## Always know what to expect from your data

# TODO logo

---

[.build-lists: true]

## Expectations are assertions about data

- `expect_file_size_to_be_between`
- `expect_table_row_count_to_be_between`
- `expect_column_to_exist`
- `expect_column_values_to_not_be_null`
- `expect_column_values_to_be_unique`
- `expect_column_values_to_be_between`
- `expect_column_values_to_be_in_set`
- `expect_column_values_to_match_regex`
- `expect_column_mean_to_be_between`
- `expect_column_kl_divergence_to_be_less_than`
- ... and many many more[^1]

[^1]: https://docs.greatexpectations.io/en/latest/expectation_glossary.html

^ declarative

---

# Where's does the compute happen?
## Great Expectations uses different back-end compute engines
# TODO

---

# [fit] Tests are docs
# [fit] and
# [fit] Docs are tests

---

# Tests are docs and docs are tests

- Everything is JSON 🤖
- Compile to HTML or Notebooks 🤗
- Docs cannot get stale!

---

# How to crush pipeline debt

- data ingest
    + especially if the data isn't controlled your team
- before & after ML models
    + prevent malfeasant AI
- critical dashboard tables
    + Don't piss off an executive
- analytic warehouses
    + Be good data driven.

---

# How to use Great Expectations in a pipeline?

![right fit](wap_simple.png)

The WAP pattern![^2]

[^3]: Scaling Data Quality at Netflix https://www.slideshare.net/MichelleFUfford/scaling-data-quality-netflix-76917740

---

# How to use Great Expectations in a pipeline?

![right fit](wap_advanced.png)

The WAP pattern![^2]

[^2]: Scaling Data Quality at Netflix https://www.slideshare.net/MichelleFUfford/scaling-data-quality-netflix-76917740

---

# [fit] live demo

---

Thank you!

Join us at greatexpectations.io

---

# Misc

## Backstory

## Funding & Philosophy

We raised a round from CRV and Root Ventures late last year, so we have two full years of runway to work on Great Expectations.

At some point, we'll build a paid SaaS product on top of Great Expectations, but for now we're just making the open source project as useful as it can be.

We're firmly committed to keeping Great Expectations open: everything that is open source will always remain open source.