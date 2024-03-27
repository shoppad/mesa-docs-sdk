# Libraries &gt; Twilio.js 



### vendor/Twilio.js


#### new Twilio() 

Send a SMS message and more with the Twilio Rest API.





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Examples

```javascript
const Twilio = require('vendor/Twilio.js');
const twilio = new Twilio(twilioSid, twilioToken);
twilio.send({
  to: '+1123456789',
  from: '+1123456789',
  body: 'Hello :)',
});
```


##### Returns


- `Twilio`  



#### Twilio.send(data[, options]) 

Send an SMS message.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| data | `object`  |  | &nbsp; |
| data.to | `string`  | The phone number to send the SMS to, including country code and no spaces or dashes. Example (USA): +1123456789. | &nbsp; |
| data.from | `string`  | The phone number that the SMS will be sent from. Must be registered in Twilio. | &nbsp; |
| data.body | `string`  | The SMS message text. | &nbsp; |
| options | `boolean`  |  | *Optional* |
| options.debug | `boolean`  | Set to true to debug the Twilio API request. | *Optional* |




##### Returns


- `boolean`  




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
