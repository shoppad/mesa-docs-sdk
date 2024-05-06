# MESA Script Specification 



### 


#### module.exports(payload, context) 

A Mesa Script exports a class with a script() method that is passed the following parameters:




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| payload | `object`  | The payload data | &nbsp; |
| context | `<a href="#-object-context">context</a>`  | Contains data relative to the current task that is running. | &nbsp; |




##### Returns


- `Void`



#### {object} context() 

context parameter




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| payload | `object`  | The payload data | &nbsp; |
| shop | `<a href="#-object-shop">shop</a>`  | Complete Shopify shop object | &nbsp; |
| shop.email | `string`  | Merchant's email address | &nbsp; |
| shop.myshopify_domain | `string`  | Shop string. Example: myshop.myshopify.com | &nbsp; |
| shop.myshopify_domain | `domain`  | Shop's domain if it has been customized, otherwise the myshopify domain | &nbsp; |
| steps | `object`  | An object containing the full payload for each step run in this automation so far, keyed by each step's key. For example `steps.shopify`. | &nbsp; |
| trigger | `<a href="#-object-trigger">trigger</a>`  | The complete Trigger object contains information about the current step being run | &nbsp; |
| task | `<a href="#-object-task">task</a>`  | The complete Task object contains information about this specific task run | &nbsp; |
| automation | `<a href="#-object-automation">automation</a>`  | The complete Automation object contains information about the workflow | &nbsp; |




##### Returns


- `Void`



#### {object} task() 

task model generated from https://transform.tools/json-to-jsdoc




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| is_test | `boolean`  |  | &nbsp; |
| is_premium | `boolean`  |  | &nbsp; |
| execution_time | `number`  |  | &nbsp; |
| memory | `number`  |  | &nbsp; |
| replay_of |  |  | &nbsp; |
| replayed_by |  |  | &nbsp; |
| replay_count | `number`  |  | &nbsp; |
| automation | `object`  |  | &nbsp; |
| automation._id | `string`  |  | &nbsp; |
| automation.automation_name | `string`  |  | &nbsp; |
| trigger | `object`  |  | &nbsp; |
| trigger._id | `string`  |  | &nbsp; |
| trigger.trigger_name | `string`  |  | &nbsp; |
| trigger.trigger_type | `string`  |  | &nbsp; |
| trigger.trigger_key | `string`  |  | &nbsp; |
| trigger.task_id | `string`  |  | &nbsp; |
| parents | `Array.&#60;object&#62;`  |  | &nbsp; |
| parents._id | `string`  |  | &nbsp; |
| parents.trigger_name | `string`  |  | &nbsp; |
| parents.trigger_type | `string`  |  | &nbsp; |
| parents.trigger_key | `string`  |  | &nbsp; |
| parents.task_id | `string`  |  | &nbsp; |
| depth_parent_id | `string`  |  | &nbsp; |
| child_id |  |  | &nbsp; |
| child_fails | `number`  | The number of child failed tasks. | &nbsp; |
| child_stops | `number`  | The number of child stopped tasks. | &nbsp; |
| child_completes | `number`  | The number of child completed tasks that successfully completed all of the steps in the workflow. | &nbsp; |
| source | `string`  |  | &nbsp; |
| context | `object`  |  | &nbsp; |
| context.headers | `object`  | A key-value object of all of the headers passed to this task (if it was an input) | &nbsp; |
| context.timestamp | `string`  |  | &nbsp; |
| payload_hash | `string`  | A hash of the payload that is used to deduplicate duplicate webhooks | &nbsp; |
| billable | `boolean`  | Whether or not this was a billable task (criteria: is an input, not a test, etc) | &nbsp; |
| billable_amount | `number`  | The number of units this task cost (1 if just the input for an automation, 2 if it's the input of an automation that contains a premium step) | &nbsp; |
| unbillable_reason | `string`  | The reason this task is unbillable. `not_input`, etc | &nbsp; |
| external_id | `string`  | The ID of this object in the external system (shopify order id, etc) | &nbsp; |
| external_label | `string`  | A human-readable representation of this object in the external system (Shopify Order Name like #1001, etc) | &nbsp; |
| external_url | `string`  | The URL to the record in the external system, for example a link to the Shopify order in the admin | &nbsp; |
| enqueued | `boolean`  |  | &nbsp; |
| active | `boolean`  |  | &nbsp; |
| _id |  |  | &nbsp; |
| created_at |  |  | &nbsp; |
| updated_at |  |  | &nbsp; |




##### Returns


- `Void`



#### {object} trigger() 

trigger model generated from https://transform.tools/json-to-jsdoc




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| schema | `number`  |  | &nbsp; |
| version | `string`  |  | &nbsp; |
| trigger_type | `string`  |  | &nbsp; |
| is_premium | `boolean`  |  | &nbsp; |
| is_pro | `boolean`  |  | &nbsp; |
| uuid | `string`  |  | &nbsp; |
| automation | `string`  |  | &nbsp; |
| type | `string`  |  | &nbsp; |
| entity | `string`  |  | &nbsp; |
| action | `string`  |  | &nbsp; |
| operation_id | `string`  |  | &nbsp; |
| name | `string`  |  | &nbsp; |
| key | `string`  |  | &nbsp; |
| trigger_name | `string`  |  | &nbsp; |
| metadata | `object`  |  | &nbsp; |
| metadata.script | `string`  |  | &nbsp; |
| metadata.mapping | `Array.&#60;object&#62;`  |  | &nbsp; |
| metadata.mapping.destination | `string`  |  | &nbsp; |
| metadata.mapping.source | `string`  |  | &nbsp; |
| local_fields | `Array.&#60;object&#62;`  |  | *Optional* |
| local_fields.key | `string`  |  | &nbsp; |
| local_fields.type | `string`  |  | &nbsp; |
| local_fields.tokens | `string`  |  | &nbsp; |
| local_fields.location | `string`  |  | &nbsp; |
| weight | `number`  |  | &nbsp; |
| script |  |  | &nbsp; |
| on_error | `string`  |  | &nbsp; |
| _id | `string`  |  | &nbsp; |
| created_at | `string`  |  | &nbsp; |
| updated_at | `string`  |  | &nbsp; |
| tokens_ignore_previous |  |  | &nbsp; |
| response | `Array.&#60;object&#62;`  |  | &nbsp; |
| fields | `Array.&#60;object&#62;`  |  | &nbsp; |
| fields.key | `string`  |  | &nbsp; |
| fields.type | `string`  |  | &nbsp; |
| fields.tokens | `string`  |  | &nbsp; |
| fields.location | `string`  |  | &nbsp; |
| fields.label | `string`  |  | &nbsp; |
| fields.file | `string`  |  | &nbsp; |
| response_example | `object`  |  | &nbsp; |
| response_example.trigger_type | `string`  |  | &nbsp; |
| response_example.connector | `string`  |  | &nbsp; |
| response_example.title | `string`  |  | &nbsp; |
| response_example.description | `string`  |  | &nbsp; |
| response_example.icon | `string`  |  | &nbsp; |
| response_example.endpoint | `string`  |  | &nbsp; |
| response_example.operation_id | `string`  |  | &nbsp; |
| response_example.key | `string`  |  | &nbsp; |
| {} |  | request_example | &nbsp; |
| configuration_aside |  |  | &nbsp; |
| connector_name | `string`  |  | &nbsp; |
| icon | `string`  |  | &nbsp; |
| description | `string`  |  | &nbsp; |
| raw_metadata | `object`  | The raw metadata without any token replacements. This can be helpful if we want to to have a field where the merchant enters a token (like Dropbox) | *Optional* |




##### Returns


- `Void`



#### {object} automation() 

automation model generated from https://transform.tools/json-to-jsdoc




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| uuid | `string`  |  | &nbsp; |
| key | `string`  |  | &nbsp; |
| name | `string`  |  | &nbsp; |
| version | `string`  |  | &nbsp; |
| template | `string`  |  | &nbsp; |
| helpscout_article_id | `string`  |  | &nbsp; |
| description | `string`  |  | &nbsp; |
| video | `string`  |  | &nbsp; |
| is_premium | `boolean`  |  | &nbsp; |
| enabled | `boolean`  |  | &nbsp; |
| did_complete | `boolean`  |  | &nbsp; |
| logging | `boolean`  |  | &nbsp; |
| debug | `boolean`  |  | &nbsp; |
| seconds | `number`  |  | &nbsp; |
| notifications | `object`  |  | &nbsp; |
| notifications.enabled | `boolean`  |  | &nbsp; |
| _id | `string`  |  | &nbsp; |
| created_at | `string`  |  | &nbsp; |
| updated_at | `string`  |  | &nbsp; |
| inputs | `array.trigger`  |  | &nbsp; |
| outputs | `array.trigger`  |  | &nbsp; |
| scripts | `array.script`  |  | &nbsp; |
| source_entity | `string`  |  | &nbsp; |
| {} |  | field_provides | &nbsp; |
| key_editable | `boolean`  |  | &nbsp; |




##### Returns


- `Void`



#### {object} trigger() 

trigger model generated from https://transform.tools/json-to-jsdoc




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| schema | `number`  |  | &nbsp; |
| version | `string`  |  | &nbsp; |
| trigger_type | `string`  |  | &nbsp; |
| is_premium | `boolean`  |  | &nbsp; |
| is_pro | `boolean`  |  | &nbsp; |
| uuid | `string`  |  | &nbsp; |
| automation | `string`  |  | &nbsp; |
| type | `string`  |  | &nbsp; |
| entity | `string`  |  | &nbsp; |
| action | `string`  |  | &nbsp; |
| operation_id | `string`  |  | &nbsp; |
| name | `string`  |  | &nbsp; |
| key | `string`  |  | &nbsp; |
| trigger_name | `string`  |  | &nbsp; |
| metadata | `object`  |  | &nbsp; |
| metadata.host | `string`  |  | &nbsp; |
| metadata.allow_duplicate | `boolean`  |  | &nbsp; |
| {} |  | local_fields | &nbsp; |
| weight | `number`  |  | &nbsp; |
| script |  |  | &nbsp; |
| on_error |  |  | &nbsp; |
| _id | `string`  |  | &nbsp; |
| created_at | `string`  |  | &nbsp; |
| updated_at | `string`  |  | &nbsp; |
| tokens_ignore_previous |  |  | &nbsp; |
| {} |  | response | &nbsp; |
| fields | `Array.&#60;object&#62;`  |  | &nbsp; |
| fields.key | `string`  |  | &nbsp; |
| fields.label | `string`  |  | &nbsp; |
| fields.type | `string`  |  | &nbsp; |
| fields.disabled | `boolean`  |  | &nbsp; |
| fields.export | `boolean`  |  | &nbsp; |
| fields.copy | `boolean`  |  | &nbsp; |
| {} |  | response_example | &nbsp; |
| {} |  | request_example | &nbsp; |
| configuration_aside |  |  | &nbsp; |
| connector_name | `string`  |  | &nbsp; |
| icon | `string`  |  | &nbsp; |
| description | `string`  |  | &nbsp; |




##### Returns


- `Void`



#### {object} json() 

script model generated from https://transform.tools/json-to-jsdoc




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| automation | `string`  |  | &nbsp; |
| script_id | `string`  |  | &nbsp; |
| filename | `string`  |  | &nbsp; |
| version | `string`  |  | &nbsp; |
| _id | `string`  |  | &nbsp; |
| created_at | `string`  |  | &nbsp; |
| updated_at | `string`  |  | &nbsp; |




##### Returns


- `Void`



#### {object} shop() 

shop model generated from https://transform.tools/json-to-jsdoc




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| id | `number`  |  | &nbsp; |
| name | `string`  |  | &nbsp; |
| email | `string`  |  | &nbsp; |
| domain | `string`  |  | &nbsp; |
| province | `string`  |  | &nbsp; |
| country | `string`  |  | &nbsp; |
| address1 | `string`  |  | &nbsp; |
| zip | `string`  |  | &nbsp; |
| city | `string`  |  | &nbsp; |
| source |  |  | &nbsp; |
| phone | `string`  |  | &nbsp; |
| latitude |  |  | &nbsp; |
| longitude |  |  | &nbsp; |
| primary_locale | `string`  |  | &nbsp; |
| address2 |  |  | &nbsp; |
| created_at | `string`  |  | &nbsp; |
| updated_at | `string`  |  | &nbsp; |
| country_code | `string`  |  | &nbsp; |
| country_name | `string`  |  | &nbsp; |
| currency | `string`  |  | &nbsp; |
| customer_email | `string`  |  | &nbsp; |
| timezone | `string`  |  | &nbsp; |
| iana_timezone | `string`  |  | &nbsp; |
| shop_owner | `string`  |  | &nbsp; |
| money_format | `string`  |  | &nbsp; |
| money_with_currency_format | `string`  |  | &nbsp; |
| weight_unit | `string`  |  | &nbsp; |
| province_code | `string`  |  | &nbsp; |
| taxes_included | `boolean`  |  | &nbsp; |
| auto_configure_tax_inclusivity |  |  | &nbsp; |
| tax_shipping |  |  | &nbsp; |
| county_taxes | `boolean`  |  | &nbsp; |
| plan_display_name | `string`  |  | &nbsp; |
| plan_name | `string`  |  | &nbsp; |
| has_discounts | `boolean`  |  | &nbsp; |
| has_gift_cards | `boolean`  |  | &nbsp; |
| myshopify_domain | `string`  |  | &nbsp; |
| google_apps_domain |  |  | &nbsp; |
| google_apps_login_enabled |  |  | &nbsp; |
| money_in_emails_format | `string`  |  | &nbsp; |
| money_with_currency_in_emails_format | `string`  |  | &nbsp; |
| eligible_for_payments | `boolean`  |  | &nbsp; |
| requires_extra_payments_agreement | `boolean`  |  | &nbsp; |
| password_enabled | `boolean`  |  | &nbsp; |
| has_storefront | `boolean`  |  | &nbsp; |
| eligible_for_card_reader_giveaway | `boolean`  |  | &nbsp; |
| finances | `boolean`  |  | &nbsp; |
| primary_location_id | `number`  |  | &nbsp; |
| cookie_consent_level | `string`  |  | &nbsp; |
| visitor_tracking_consent_preference | `string`  |  | &nbsp; |
| checkout_api_supported | `boolean`  |  | &nbsp; |
| multi_location_enabled | `boolean`  |  | &nbsp; |
| setup_required | `boolean`  |  | &nbsp; |
| pre_launch_enabled | `boolean`  |  | &nbsp; |
| enabled_presentment_currencies | `Array.&#60;string&#62;`  |  | &nbsp; |




##### Returns


- `Void`




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
