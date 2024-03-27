# Libraries &gt; Googlesheets.js 



### vendor/Googlesheets.js


#### new GoogleSheets(request) 

Methods to interact with the GoogleSheets API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| request | `Oauth`  | Authenticated request. | &nbsp; |



##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| request | `Oauth`  | Authenticated request. | &nbsp; |



##### Returns


- `class`  



#### GoogleSheets.read() 

Google Sheets basic reading






##### Examples

```javascript
const Google = require('vendor/Google.js');
let secretsKeys = {
   refresh_token: "example_secret_refresh_token",
   access_token: "example_secret_access_token",
   expires_at: "example_secret_expires_at",
   client_id: "example_secret_client_id",
   client_secret: "example_secret_client_secret",
};
const google = new Google('refresh_token', secretsKeys);
const basicReading = google.sheets.basicReading('3p9f4pf-gS2jA_HpC1Yt-3MhQSOMNluRrmBlPcUC2Ugts', "Sheet1", "A1","D5");
Mesa.log.info('Basic Reading: ', basicReading);
```


##### Returns


- `Void`



#### GoogleSheets.write() 

Google Sheets writing






##### Examples

```javascript
const Google = require('vendor/Google.js');
let secretsKeys = {
   refresh_token: "example_secret_refresh_token",
   access_token: "example_secret_access_token",
   expires_at: "example_secret_expires_at",
   client_id: "example_secret_client_id",
   client_secret: "example_secret_client_secret",
};
const google = new Google('refresh_token', secretsKeys);
const values = [[ "customer_id", "customer_name"], [ "1234", "Joe doe"]];
const payload = {range: "Sheet1!A1:D5",majorDimension: "ROWS",values: values};
const basicWriting = google.sheets.basicWriting('3p9f4pf-gS2jA_HpC1Yt-3MhQSOMNluRrmBlPcUC2Ugts', "Sheet1", "A1","D5", payload);
Mesa.log.info('Basic Writing: ', basicWriting);
```


##### Returns


- `Void`



#### GoogleSheets.addOrUpdate(rowPayload, sheetPayload[, headerId&#x3D;null, columnKey&#x3D;null, id&#x3D;null]) 

Adds or updates a Google Sheets Payload.

To support updates to the payload, you need to pass the headerId, columnKey and Id.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| rowPayload | `array`  | Array with row payload. | &nbsp; |
| sheetPayload | `array`  | Google Sheets payload. | &nbsp; |
| headerId&#x3D;null | `number`  | Location of the header. | *Optional* |
| columnKey&#x3D;null | `string`  | Column name of the forgein key. | *Optional* |
| id&#x3D;null | `string`  | Payload ID, in the case of a duplicated ID we will update the payload. | *Optional* |




##### Examples

```javascript
const Google = require('vendor/Google.js');
let secretsKeys = {
   refresh_token: "example_secret_refresh_token",
   access_token: "example_secret_access_token",
   expires_at: "example_secret_expires_at",
   client_id: "example_secret_client_id",
   client_secret: "example_secret_client_secret",
};
const google = new Google('refresh_token', secretsKeys);
const rowPayload = ['12345', 'Mary Jane'];
const sheetPayload = [[ "customer_id", "customer_name"], [ "1234", "Joe doe"]];
const updatedSheetsPayload = google.sheets.addOrUpdate(rowPayload, sheetPayload, 0, 'customer_id', '12345');
Mesa.log.info('Sheets Payload', updatedSheetsPayload);
// [[ "customer_id", "customer_name"], [ "1234", "Joe doe"], [ "12345", "Mary Jane"]]
```


##### Returns


- `Void`




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
