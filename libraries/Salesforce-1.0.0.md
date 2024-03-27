# Libraries &gt; Salesforce.js 



### vendor/Salesforce.js


#### new Salesforce() 

Class containing methods to interact with the Salesforce Admin API.






##### Returns


- `Salesforce`  



#### Salesforce.constructor(grantType, tokenKey) 

Construct an OAuth connection




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| grantType | `String`  | The method used to receive an access token. | &nbsp; |
| tokenKey | `string`  | [description] | &nbsp; |




##### Returns


- `Void`



#### Salesforce.get(path[, options]) 

Make a GET request to Salesforce.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| options | `object`  |  | *Optional* |
| options.json | `bool`  | Automatically add JSON Content-Type headers and decode the response. Default: `true` | *Optional* |
| options.query | `object`  | Parameters to append to the querystring. | *Optional* |
| options.headers | `object`  | Headers to send to the request. | *Optional* |
| options.debug | `bool`  | Log request information and response headers. | *Optional* |
| options.include_headers | `bool`  | Include headers in the requests response, defaults to false. | *Optional* |




##### Returns


- `string` `object`  The response returned by the request. `object` if `options.json` is `true`, `string` if `options.json` is `false`.



#### Salesforce.post(path, data[, options]) 

Make a POST request to Salesforce.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `object`  |  | *Optional* |
| options.json | `bool`  | Automatically add JSON Content-Type headers and decode the response. Default: `true` | *Optional* |
| options.query | `object`  | Parameters to append to the querystring. | *Optional* |
| options.headers | `object`  | Headers to send to the request. | *Optional* |
| options.debug | `bool`  | Log request information and response headers. | *Optional* |
| options.include_headers | `bool`  | Include headers in the requests response, defaults to false. | *Optional* |




##### Returns


- `string` `object`  The response returned by the request. `object` if `options.json` is `true`, `string` if `options.json` is `false`.



#### Salesforce.put(path, data[, options]) 

Make a PUT request to Salesforce.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `object`  |  | *Optional* |
| options.json | `bool`  | Automatically add JSON Content-Type headers and decode the response. Default: `true` | *Optional* |
| options.query | `object`  | Parameters to append to the querystring. | *Optional* |
| options.headers | `object`  | Headers to send to the request. | *Optional* |
| options.debug | `bool`  | Log request information and response headers. | *Optional* |
| options.include_headers | `bool`  | Include headers in the requests response, defaults to false. | *Optional* |




##### Returns


- `string` `object`  The response returned by the request. `object` if `options.json` is `true`, `string` if `options.json` is `false`.



#### Salesforce.patch(path, data[, options]) 

Make a PATCH request to Salesforce.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `object`  |  | *Optional* |
| options.json | `bool`  | Automatically add JSON Content-Type headers and decode the response. Default: `true` | *Optional* |
| options.query | `object`  | Parameters to append to the querystring. | *Optional* |
| options.headers | `object`  | Headers to send to the request. | *Optional* |
| options.debug | `bool`  | Log request information and response headers. | *Optional* |
| options.include_headers | `bool`  | Include headers in the requests response, defaults to false. | *Optional* |




##### Returns


- `string` `object`  The response returned by the request. `object` if `options.json` is `true`, `string` if `options.json` is `false`.



#### Salesforce.delete(path, data[, options]) 

Make a DELETE request to Salesforce.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `object`  |  | *Optional* |
| options.json | `bool`  | Automatically add JSON Content-Type headers and decode the response. Default: `true` | *Optional* |
| options.query | `object`  | Parameters to append to the querystring. | *Optional* |
| options.headers | `object`  | Headers to send to the request. | *Optional* |
| options.debug | `bool`  | Log request information and response headers. | *Optional* |
| options.include_headers | `bool`  | Include headers in the requests response, defaults to false. | *Optional* |




##### Returns


- `string` `object`  The response returned by the request. `object` if `options.json` is `true`, `string` if `options.json` is `false`.



#### Salesforce.getSingleExistingRecord(selectFields, entityName, searchField, searchValue[, path]) 

Convenience method to get single record from Salesforce, using Salesforce Object Query Language




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| selectFields | `string`  | Comma-separated string with fields to select | &nbsp; |
| entityName | `string`  | Entity name | &nbsp; |
| searchField | `string`  | Field to search on | &nbsp; |
| searchValue | `string`  | Value to search for | &nbsp; |
| path | `string`  | Optional salesforce base path. If not provided, instance URL provided by access token will be used | *Optional* |




##### Returns


- `object` `bool`  Either returns single record (if only one exists), or false otherwise



#### Salesforce.createOrUpdateSalesforceEntity(payload, entityName[, path]) 

Convenience method to create or update Salesforce entity




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| payload | `object`  | Should include 'existing_record_url', with URL of existing record included if payload is for existing record | &nbsp; |
| entityName | `string`  | Entity name | &nbsp; |
| path | `string`  | Optional salesforce base path. If not provided, instance URL provided by access token will be used | *Optional* |




##### Returns


- `object`  response



#### Salesforce.responseHasErrors(response, entity) 

Convenience method to check response from salesforce update / create call




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| response | `object`  |  | &nbsp; |
| entity | `string`  |  | &nbsp; |




##### Returns


- `bool`  




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
