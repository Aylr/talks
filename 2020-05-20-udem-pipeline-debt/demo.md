## LINKS

- http://tiny.cc/udem-ge
- doc: https://docs.google.com/document/d/1v8rRjGALiXZlBgE6nQJ0vuNz5iKEf5ZmDGULxePXoUY
- stories https://docs.google.com/forms/d/1-NfH7lP7Yez2WrnEMOnG765aPJYeoV4md457bn7k5ak/edit#responses

## Live Demo

- GE project should live in your pipeline source control.
- `tree`
- talk about GE CLI noun verb
- Here I have some csv files that I want to work with. These might be source files on S4, etc.
- `great_expectations init`
- files datasource
    + name suite: `demo`
- Show data docs and a few expectations
- **Not terribly helpful - let's make a more real suite.**
- `great_expectations suite delete demo`
- Scaffold a suite
    + `great_expectations suite scaffold`
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
        + npi
            * **data tests must be more flexible MOSTLY**
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

- `great_expectations checkpoint new`
- `great_expectations checkpoint run`
- swap in bad data
- configure slack

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


