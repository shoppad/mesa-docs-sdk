# Libraries &gt; Cognito.js 



### vendor/Cognito.js


#### new Cognito() 

Send a SMS message and more with the Cognito Rest API.





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Examples

```javascript
const Cognito = require('vendor/Cognito.js');
Cognito.send({
  to: '+1123456789',
  from: '+1123456789',
  message: 'Hello :)',
});
```


##### Returns


- `Cognito`  



#### Cognito.identitySearch(phone[, firstName, lastName]) 

Initialize a new Cognito identity search. This first calls POST `/profiles` and then POST `/identity_searches`.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| phone | `string`  |  | &nbsp; |
| firstName | `string`  |  | *Optional* |
| lastName | `string`  |  | *Optional* |




##### Returns


- `object`  data returned from Cognito identity API call



#### Cognito.checkIdentitySearchJob(id) 

Look up an existing Cognito identity lookup job. This calls `/identity_searches/jobs/${id}`.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| id | `string`  | The job API | &nbsp; |




##### Returns


- `object`  Data returned from Cognito identity job lookup API call



#### send(method, endpoint, data, options) 






##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| method |  |  | &nbsp; |
| endpoint |  |  | &nbsp; |
| data |  |  | &nbsp; |
| options |  |  | &nbsp; |




##### Returns


- `boolean`  




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
