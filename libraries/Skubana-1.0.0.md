# Libraries &gt; Skubana.js 



### vendor/Skubana.js


#### new Skubana(token) 

Methods to interact with the Skubana API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| token | `tokenKey`  | Secrets names. | &nbsp; |



##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| token | `tokenKey`  | Secrets names. | &nbsp; |



##### Examples

```javascript
// Skubana flow.
const Skubana = require('vendor/Skubana.js');
const skubana = new Skubana();
const getResponse = skubana.get('https://api.dev.skubana.com/v1/orders');
```


##### Returns


- `class`  



#### Skubana.getOrders([queries&#x3D;{}]) 

Skubana retrieve orders api.
{@link} https://documentation.skubana.com/spec/#operation/getOrdersUsingGET




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| queries&#x3D;{} | `Object`  | queries parameters. | *Optional* |




##### Examples

```javascript
// Skubana flow.
const Skubana = require('vendor/Skubana.js');
const skubana = new Skubana();
const getResponse = skubana.getOrders();
Mesa.log.info('Get Response: ', getResponse);
```


##### Returns


- `Void`



#### Skubana.getInventory([queries&#x3D;{}]) 

Skubana retrieve inventory api.
{@link} https://documentation.skubana.com/spec/#operation/getInventoryUsingGET




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| queries&#x3D;{} | `Object`  | queries parameters. | *Optional* |




##### Examples

```javascript
// Skubana flow.
const Skubana = require('vendor/Skubana.js');
const skubana = new Skubana();
const getResponse = skubana.getInventory();
Mesa.log.info('Get Response: ', getResponse);
```


##### Returns


- `Void`



#### Skubana.getPurchaseOrders([queries&#x3D;{}]) 

Skubana retrieve inventory api.
{@link} https://documentation.skubana.com/spec/#operation/getPurchaseOrdersUsingGET




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| queries&#x3D;{} | `Object`  | queries parameters. | *Optional* |




##### Examples

```javascript
// Skubana flow.
const Skubana = require('vendor/Skubana.js');
const skubana = new Skubana();
const getResponse = skubana.getPurchaseOrders();
Mesa.log.info('Get Response: ', getResponse);
```


##### Returns


- `Void`




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
