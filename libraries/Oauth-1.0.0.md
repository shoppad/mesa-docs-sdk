# Libraries &gt; Oauth.js 



### vendor/Oauth.js


#### new Oauth(grantType, tokenKey) 

Class containing methods to authenticate and make authenticated requests with a third party API




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| grantType | `string`  | Oauth grant type. One of: `refresh_token`, `password`, or `custom`. | &nbsp; |
| tokenKey | `string`  | The key of the secret containing the oAuth token information. | &nbsp; |




##### Examples

```javascript
// Refresh token flow.
const Oauth = require('vendor/Oauth.js');
const oauth = new Oauth('refresh_token', 'service.oauth');
```
```javascript
// Username password flow.
const Oauth = require('vendor/Oauth.js');
// Save username and password from external standalone secrets.
let token = JSON.decode(Mesa.secret.get('service.oauth', '{}'));
token.username = Mesa.secret.get('service-username');
token.password = Mesa.secret.get('service-password');
Mesa.secret.set('service.oauth', JSON.stringify(token));
const oauth = new Oauth('password', 'service.oauth');
```
```javascript
// Skubana flow (access_token that does not expire)
const Oauth = require('vendor/Oauth.js');
const oauth = new Oauth('custom', 'skubana.oauth');
const getResponse = oauth.get('https://dev.skubana.com/v1/orders');
Mesa.log.info('Get Response: ', getResponse);
```
```javascript
// Oauth Usage
const getResponse = oauth.get('https://example.com/products.json');
const postResponse = oauth.post('https://example.com/products.json', {});
Mesa.log.info('Get Response: ', getResponse);
Mesa.log.info('Post Response: ', postResponse);
```


##### Returns


- `Void`



#### constructor(grantType, tokenKey, hasHeaders) 






##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| grantType | `string`  |  | &nbsp; |
| tokenKey | `string`  |  | &nbsp; |
| hasHeaders | `boolean`  |  | &nbsp; |




##### Returns


- `Void`



#### init() 

Init the access token






##### Returns


- `Void`



#### request(method, path, data, options) 

Request method with the refresh token retry if fails.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| method | `string`  | Request method. | &nbsp; |
| path | `string`  | Request path. | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `Types.RequestOptions`  | Additional configuration for Oauth calls | &nbsp; |




##### Returns


- `object`  



#### get(path[, options]) 

Make a GET request to an external Rest API




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  | Request path | &nbsp; |
| options | `Types.RequestOptions`  | Additional configuration for Oauth calls | *Optional* |




##### Returns


- `object`  



#### post(path, data[, options]) 

Make a POST request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  | Request path | &nbsp; |
| data | `object`  | Request payload | &nbsp; |
| options | `Types.RequestOptions`  | Additional configuration for Oauth calls | *Optional* |




##### Returns


- `object`  



#### put(path, data[, options]) 

Make a PUT request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  | Request path | &nbsp; |
| data | `object`  | Request payload | &nbsp; |
| options | `Types.RequestOptions`  | Additional configuration for Oauth calls | *Optional* |




##### Returns


- `object`  



#### patch(path, data[, options]) 

Make a PATCH request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  | Request path | &nbsp; |
| data | `object`  | Request payload | &nbsp; |
| options | `Types.RequestOptions`  | Additional configuration for Oauth calls | *Optional* |




##### Returns


- `object`  



#### delete(path[, options]) 

Make a DELETE request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  | Request path | &nbsp; |
| options | `Types.RequestOptions`  | Additional configuration for Oauth calls | *Optional* |




##### Returns


- `object`  




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
