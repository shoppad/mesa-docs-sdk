# Libraries &gt; Slack.js 



### vendor/Slack.js


#### new Slack() 

Send a message to a Slack Channel

To create a Slack webhook URL:

1. [Create a Slack app](https://api.slack.com/apps/new) (if you don't already have one).
2. Enable Incoming Webhooks from the settings page.
3. After the settings page refreshes, click Add New Webhook to Workspace.
4. Pick a channel that the app will post to, then click Authorize.
5. Use your [Incoming Webhook URL](https://api.slack.com/incoming-webhooks#posting_with_webhooks) as the `webhookUrl` parameter.





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Examples

```javascript
const Slack = require('vendor/Slack.js');
const slack = new Slack(Secret.get('slack-webhook-url'));
slack.send('Just a test!');
```
```javascript
slack.send('A more advanced test', {
   domain: 'mysite',
   channel: '#alerts',
   icon_emoji: ':+1:',
});
```


##### Returns


- `Void`



#### Slack.send(text[, options]) 

Post a message on Slack




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| text | `string`  | The message text. | &nbsp; |
| options | `object`  |  | *Optional* |
| options.domain | `string`  | Overwrite the Slack domain configured in the webhook settings. | *Optional* |
| options.channel | `string`  | Overwrite the Slack channel configured in the webhook. Example: `#alerts`. | *Optional* |
| options.username | `string`  | Overwrite the Slack channel configured in the webhook settings. | *Optional* |
| options.icon_emoji | `string`  | Set a custom emoji to use as the message icon. Example: `:party:`. | *Optional* |




##### Returns


- `Void`



#### Slack.constructor(webhookUrl) 

Construct Slack authentication




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| webhookUrl | `string`  | The Slack webhook URL from __. | &nbsp; |




##### Returns


- `Void`




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
