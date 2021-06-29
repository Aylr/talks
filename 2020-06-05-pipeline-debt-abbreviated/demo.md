# GE Live Demo

- GE project should live in your pipeline source control.
- `tree`
- Here I have some csv files that I want to work with. These might be source files on S4, etc.
- talk about GE CLI noun verb
    + `great_expectations`
- `great_expectations init`
- files datasource
    + name suite: `demo`
- Show data docs and a few expectations
- **Not terribly helpful - let's make a more real suite.**

## A real suite

- `great_expectations suite delete demo`
- Scaffold a suite
    + `great_expectations suite scaffold npi`
    + Columns to include:
```
included_columns = [
    'npi',
    # 'nppes_provider_last_org_name',
    # 'nppes_provider_first_name',
    # 'nppes_provider_mi',
    'nppes_credentials',
    'nppes_provider_gender',
    'nppes_entity_code',
    ...
     'beneficiary_average_age',
    ...
    # 'beneficiary_cc_strk_percent',
    'beneficiary_avg_risk_score'
]
```
    + **not production suites!**
    + **hueristics based on data type and cardinality**

- Edit this suite
    - JSON is source of truth - compile notebooks
    - **How do you actually author an expectation?**
        + **result object**
    - Adjust a few expectations.
        + row count: 5k - 15k
        + npi
            * unique --> False!
            * **data tests must be more flexible MOSTLY**
        + credentials
            * remove unique
            * add length 2 --> 20
        + gender
            * not null mostly 0.9
            * set F/M
            * KL divergence: f:0.45, M:0.55, threshold 0.1
            * 
        + **remove uniques on credentials, numeric columns**
    - **GLOSSARY**
        - talk about extensibility
```
states = [
    "AL", "AK", "AZ", "AR", "CA", "CO", "CT", "DE", "FL","GA", "HI", "ID", "IL", "IN", "IA", "KS", "KY", "LA", "ME", "MD", "MA", "MI", "MN", "MS",
    "MO", "MT", "NE", "NV", "NH", "NJ", "NM", "NY", "NC", "ND", "OH", "OK",
    "OR", "PA", "RI", "SC", "SD", "TN", "TX", "UT", "VT", "VA", "WA", "WV",
    "WI", "WY"
]
```

            - `batch.expect_column_values_to_be_in_set("nppes_provider_state", states, mostly=0.70)`
    - Save suite

### Deployment

- Core concepts: Expectation + Batch = Validation
    + Checkpoint is an easy way to mash these together
- requires existing suite: `great_expectations suite list`
- `great_expectations checkpoint new npi_ingest npi`
- `great_expectations checkpoint run`
- swap in bad data
- configure slack 
https://hooks.slack.com/services/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

```
- name: send_slack_notification_on_validation_result
      action:
        class_name: SlackNotificationAction
        slack_webhook: ${slack}
        notify_on: all
        renderer:
          module_name: great_expectations.render.renderer.slack_renderer
          class_name: SlackRenderer
```

- `great_expectations checkpoint run`
- maybe `great_expectations checkpoint script`

- talk about extensibility
-  


## TODO

- example S3 site


