# Libraries &gt; HttpBasicAuth.js 



### vendor/HttpBasicAuth.js


#### new HttpBasicAuth() 

Send a SMS message and more with the HttpBasicAuth Rest API.





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Examples

```javascript
const HttpBasicAuth = require('vendor/HttpBasicAuth.js');
let httpRequest = new HttpBasicAuth('username', 'password');
HttpBasicAuth.get('/customers');
```


##### Returns


- `HttpBasicAuth`  



#### HttpBasicAuth.get(path[, options]) 

Make a GET request to an external Rest API




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  | Request path | &nbsp; |
| options | `Options`  | Additional configuration for Oauth calls | *Optional* |




##### Returns


- `object`  



#### HttpBasicAuth.post(path, data[, options]) 

Make a POST request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  | Request path | &nbsp; |
| data | `object`  | Request payload | &nbsp; |
| options | `Options`  | Additional configuration for Oauth calls | *Optional* |




##### Returns


- `object`  



#### HttpBasicAuth.put(path, data[, options]) 

Make a PUT request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  | Request path | &nbsp; |
| data | `object`  | Request payload | &nbsp; |
| options | `Options`  | Additional configuration for Oauth calls | *Optional* |




##### Returns


- `object`  



#### HttpBasicAuth.patch(path, data[, options]) 

Make a PATCH request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  | Request path | &nbsp; |
| data | `object`  | Request payload | &nbsp; |
| options | `Options`  | Additional configuration for Oauth calls | *Optional* |




##### Returns


- `object`  



#### HttpBasicAuth.delete(path[, options]) 

Make a DELETE request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  | Request path | &nbsp; |
| options | `Options`  | Additional configuration for Oauth calls | *Optional* |




##### Returns


- `object`  



#### HttpBasicAuth.send(method, endpoint[, options]) 

Send an HTTP Basic authenticated request.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| method | `object`  | The request type: GET, POST, PUT, PATCH, etc | &nbsp; |
| endpoint | `string`  | The HttpBasicAuth API endpoint. Ex: rate, | &nbsp; |
| data.from | `string`  | The phone number that the SMS will be sent from. Must be registered in HttpBasicAuth. | &nbsp; |
| data.body | `string`  | The SMS message text. | &nbsp; |
| options | `boolean`  |  | *Optional* |
| options.debug | `boolean`  | Set to true to debug the HttpBasicAuth API request. | *Optional* |




##### Returns


- `boolean`  




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
