# Libraries &gt; Shopify.js 



### vendor/Shopify.js


#### Shopify() 

Interact with the Shopify Admin API.






##### Returns


- `Void`



#### Shopify.get(path[, options, connectionInfo]) 

Make a GET request to a Shopify site.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| options | `<a href="#vendor-shopify.js-object-options">Options</a>`  | Additional configuration for Shopify calls | *Optional* |
| connectionInfo | `<a href="#vendor-shopify.js-object-connectioninfo">ConnectionInfo</a>`  | If you would like to connect to a separate Shopify website that Mesa is not installed on, create a Custom App and include a `connectionInfo` object. | *Optional* |




##### Returns


- `object`  



#### Shopify.post(path, data[, options, connectionInfo]) 

Make a POST request to a Shopify site.

By default Shopify calls will auto-wrap any outgoing JSON data, eg. Shopify.post('/admin/products.json', data) will result in
{ "product": { data } }
use options.skipJsonWrap=true to override this behavior




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `<a href="#vendor-shopify.js-object-options">Options</a>`  | Additional configuration for Shopify calls | *Optional* |
| connectionInfo | `<a href="#vendor-shopify.js-object-connectioninfo">ConnectionInfo</a>`  | If you would like to connect to a separate Shopify website that Mesa is not installed on, create a Custom App and include a `connectionInfo` object. | *Optional* |




##### Returns


- `object`  



#### Shopify.put(path, data[, options, connectionInfo]) 

Make a PUT request to a Shopify site.

By default Shopify calls will auto-wrap any outgoing JSON data, eg. Shopify.put('/admin/products.json', data) will result in
{ "product": { data } }
use options.skipJsonWrap=true to override this behavior




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `<a href="#vendor-shopify.js-object-options">Options</a>`  | Additional configuration for Shopify calls | *Optional* |
| connectionInfo | `<a href="#vendor-shopify.js-object-connectioninfo">ConnectionInfo</a>`  | If you would like to connect to a separate Shopify website that Mesa is not installed on, create a Custom App and include a `connectionInfo` object. | *Optional* |




##### Returns


- `object`  



#### Shopify.patch(path, data[, options, connectionInfo]) 

Make a PATCH request to a Shopify site.

By default Shopify calls will auto-wrap any outgoing JSON data, eg. Shopify.patch('/admin/products.json', data) will result in
{ "product": { data } }
use options.skipJsonWrap=true to override this behavior




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `<a href="#vendor-shopify.js-object-options">Options</a>`  | Additional configuration for Shopify calls | *Optional* |
| connectionInfo | `<a href="#vendor-shopify.js-object-connectioninfo">ConnectionInfo</a>`  | If you would like to connect to a separate Shopify website that Mesa is not installed on, create a Custom App and include a `connectionInfo` object. | *Optional* |




##### Returns


- `object`  



#### Shopify.delete(path[, options, connectionInfo]) 

Make a DELETE request to a Shopify site.

By default Shopify calls will auto-wrap any outgoing JSON data, eg. Shopify.post('/admin/products.json', data) will result in
{ "product": { data } }
use options.skipJsonWrap=true to override this behavior




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| options | `<a href="#vendor-shopify.js-object-options">Options</a>`  | Additional configuration for Shopify calls | *Optional* |
| connectionInfo | `<a href="#vendor-shopify.js-object-connectioninfo">ConnectionInfo</a>`  | If you would like to connect to a separate Shopify website that Mesa is not installed on, create a Custom App and include a `connectionInfo` object. | *Optional* |




##### Returns


- `object`  



#### getAllProducts([query&#x3D;{}, limit&#x3D;250]) 

Make consecutive calls to Shopify in order to retrieve all products.
https://help.shopify.com/en/api/reference/products/product




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| query&#x3D;{} | `object`  | Parameters to append to the Shopify querystring. | *Optional* |
| limit&#x3D;250 | `number`  | Result count for Shopify query. | *Optional* |




##### Examples

```javascript
// returns array of all products
const Shopify = require('vendor/Shopify.js');
Shopify.getAllProducts();
```


##### Returns


- `array`  



#### appendToArray([data], The) 

Update a value if it already exists, or append it to the array if it does not exist.
The example routine below should be every time we are updating `tags` or `note_attributes` to ensure
that multiple Automations will work nicely with each other and not overwrite values set in other
Automations.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| data | `array`  | An array of values that you would like to append a value to | *Optional* |
| The | `string` `object`  | value to append to the array. For `tags`, this would be a `string`. For `note_attributes`, this would be an object. | &nbsp; |




##### Examples

```javascript
Mesa.log.debug('Calling shopify to get the latest order note_attributes');
const order = Shopify.get(`admin/orders/${payload.id}.json`);
let noteAttributes = order.order.note_attributes;
noteAttributes = Shopify.appendToArray(noteAttributes, {
   name: 'dob',
   value: 'Jan 1 2000',
});
```


##### Returns


- `array`  



#### getVariantInventoryData(variantId) 

Get inventory location information for a Shopify variant.
https://help.shopify.com/en/api/reference/inventory/inventorylevel




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| variantId | `number`  | Shopify variant id. | &nbsp; |




##### Examples

```javascript
// returns { inventory_item_id: {number}, [ { inventory_levels: { inventory_item_id: {number}, location_id: {number}, available: {number}, updated_at: {string} } ] }
const Shopify = require('vendor/Shopify.js');
Shopify.getVariantInventoryData(123456);
```


##### Returns


- `&lt;a href&#x3D;&quot;#vendor-shopify.js-object-inventorydata&quot;&gt;InventoryData&lt;/a&gt;`  



#### buildVariantInventoryUpdate(variantId, inventoryCount[, adjust&#x3D;true, fulfillableAlter]) 

Build InventoryLevel update information for a Shopify variant.
https://help.shopify.com/en/api/reference/inventory/inventorylevel




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| variantId | `number`  | Shopify variant id. | &nbsp; |
| inventoryCount | `number`  | Value to set as inventory. | &nbsp; |
| adjust&#x3D;true | `bool`  | Switch for available_adjustment vs available. | *Optional* |
| fulfillableAlter | `<a href="#vendor-shopify.js-fulfillablealter">fulfillableAlter</a>`  | Callback function allows fulfillment location to be altered. | *Optional* |




##### Examples

```javascript
// note string for location_id, as it is required by Shopify API post
// returns { inventory_item_id: {number}, location_id: {string}, available|available_adjustment: {number} } ] }
const Shopify = require('vendor/Shopify.js');
Shopify.buildVariantInventoryUpdate(123456, 10, true|false);
```


##### Returns


- `&lt;a href&#x3D;&quot;#vendor-shopify.js-object-inventoryupdatedata&quot;&gt;InventoryUpdateData&lt;/a&gt;`  



#### {Object} Options() 

options parameter for Shopify calls

By default Shopify calls will auto-wrap any outgoing JSON data, eg. Shopify.post('/admin/products.json', data) will result in
{ "product": { data } }
use skipJsonWrap=true to override this behavior





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Returns


- `Void`



#### {Object} ConnectionInfo() 

connectionInfo parameter for Shopify calls





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Returns


- `Void`



#### {Object} FulfillableLocation() 

Fulfillable location shape returned by fulfillableAlter
https://help.shopify.com/en/api/reference/inventory/location




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| location_id | `number`  | The ID of the location that the inventory level belongs to. | &nbsp; |




##### Returns


- `Void`



#### {Function} fulfillableAlter(inventoryLevels) 

Callback allows buildVariantInventoryUpdate fulfillment location to be altered.
https://help.shopify.com/en/api/reference/inventory/inventorylevel




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| inventoryLevels | `Array.&#60;Object&#62;`  | Inventory levels for the variant at different locations. | &nbsp; |
| inventoryLevels.inventory_item_id | `number`  | Inventory item id for variant | &nbsp; |
| inventoryLevels.location_id | `number`  | Location id | &nbsp; |
| inventoryLevels.available | `number`  | Inventory count | &nbsp; |
| inventoryLevels.updated_at | `string`  | Last updated | &nbsp; |




##### Returns


- `&lt;a href&#x3D;&quot;#vendor-shopify.js-object-fulfillablelocation&quot;&gt;FulfillableLocation&lt;/a&gt;`  fulfillableLocation



#### {Object} InventoryData() 

Return from getVariantInventoryData.





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Returns


- `Void`



#### {Object} InventoryUpdateData() 

Return from buildVariantInventoryUpdate.  Will either have available or available_adjustment depending on adjust param.
https://help.shopify.com/en/api/reference/inventory/inventorylevel





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Returns


- `Void`




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
