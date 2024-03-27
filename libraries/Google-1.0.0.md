# Libraries &gt; Google.js 



### vendor/Google.js


#### new Google(tokenKey) 

Methods to interact with the GoogleSheets API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| tokenKey | `string`  | The key of the secret containing a Google oAuth token. Defaults to `google.oauth`. | &nbsp; |



##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| tokenKey | `string`  | The key of the secret containing a Google oAuth token. Defaults to `google.oauth`. | &nbsp; |



##### Examples

```javascript
const Google = require('vendor/Google.js');
const google = new Google();
const response = google.request.get('https://sheets.googleapis.com/v4/spreadsheets');
Mesa.log.info('Get Response: ', response);
```


##### Returns


- `class`  




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
