# Live Demo

LINKS
- http://tiny.cc/udem-ge
- doc: https://docs.google.com/document/d/1v8rRjGALiXZlBgE6nQJ0vuNz5iKEf5ZmDGULxePXoUY
- stories https://docs.google.com/forms/d/1-NfH7lP7Yez2WrnEMOnG765aPJYeoV4md457bn7k5ak/edit#responses

- GE project should live in your pipeline source control.
- talk about GE CLI noun verb
- Here I have some csv files that I want to work with. These might be source files on S4, etc.
- `great_expectations init`
- files datasource
- Show data docs and a few expectations
- Scaffold a suite
    + `great_expectations suite scaffold`
    + Columns to include:
```included_columns = [
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

- Edit this suite
    - JSON is source of truth - compile notebooks
    - Adjust a few expectations.
        + **remove uniques on credentials, numeric columns**
        - `states = ["AL", "AK", "AZ", "AR", "CA", "CO", "CT", "DE", "FL", "GA", "HI", "ID", "IL", "IN", "IA", "KS", "KY", "LA", "ME", "MD", "MA", "MI", "MN", "MS", "MO", "MT", "NE", "NV", "NH", "NJ", "NM", "NY", "NC", "ND", "OH", "OK", "OR", "PA", "RI", "SC", "SD", "TN", "TX", "UT", "VT", "VA", "WA", "WV", "WI", "WY",]`
        - `batch.expect_column_values_to_be_in_set("nppes_provider_state", states)
            - `batch.expect_column_values_to_be_in_set("nppes_provider_state", states, mostly=0.70)`

            ```python
            batch.expect_column_value_lengths_to_be_between(
                "nppes_provider_last_org_name", min_value=1, max_value=20, mostly=0.95
            )
            ```
    - Add an expectation using the glossary.
        - talk about extensibility
    - TODO
    - Save suite
- Deployment
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

- show off file structure
- talk about extensibility
-  

...


## TODO

- make .venv with latest GE
- Slack webhook to UDEM?
- S3 link in slack?
- bitly link to repo
- example S3 site
- GE slack link
- ge.io link
- GE github link


