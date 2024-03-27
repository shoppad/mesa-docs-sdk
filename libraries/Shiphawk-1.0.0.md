# Libraries &gt; Shiphawk.js 



### vendor/Shiphawk.js


#### new Shiphawk() 

Create ShipHawk Shipping labels.  See the [Create Shipping Labels With ShipHawk When Order Is Fulfilled template]() for an example.





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Returns


- `Shiphawk`  



#### Shiphawk.createRateRequest(data) 

Create a ShipHawk Rate Request.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| data | `object`  |  | &nbsp; |
| data.items | `array`  | Array of Rate Item Request objects. See https://apidocs.shiphawk.com/#rate-item-request-object. | &nbsp; |
| data.type.weight | `float`  | The weight of the package in pounds | &nbsp; |
| data.type.length | `float`  | The length of the package in inches | *Optional* |
| data.type.width | `float`  | The width of the package in inches | *Optional* |
| data.type.height | `float`  | The height of the package in inches | *Optional* |
| data.value | `float`  | The value of the package in dollars | *Optional* |
| data.origin_address | `object`  | Address Object representing the destination address. See https://apidocs.shiphawk.com/#address-resources. | &nbsp; |
| data.origin_address.zip | `string`  | The origin address zip code | &nbsp; |
| data.destination_address | `object`  | Address Object representing the destination address. See https://apidocs.shiphawk.com/#address-resources. | &nbsp; |
| data.destination_address.zip | `string`  | The destination address zip code | &nbsp; |




##### Returns


- `object`  



#### Shiphawk.createShipment(data) 

Create a ShipHawk shipment




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| data | `object`  |  | &nbsp; |
| data.rate_id | `string`  | The Rate ID returned by a request to `Shiphawk.createRateRequest(data)`. | &nbsp; |
| data.origin_address | `object`  | Address Object representing the origin address. See https://apidocs.shiphawk.com/#address-resources. | &nbsp; |
| data.destination_address | `object`  | Address Object representing the destination address. See https://apidocs.shiphawk.com/#address-resources. | &nbsp; |
| data.label_format | `string`  | Default: PDF values: ZPL, PDF | *Optional* |
| data.include_return_label | `boolean`  | Default: false | *Optional* |




##### Returns


- `object`  



#### Shiphawk.sanitizeAddress(shopifyAddress[, email, phoneNumber]) 

Convert a Shopify address to a [ShipHawk Address resource](https://apidocs.shiphawk.com/#address-resources).




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| shopifyAddress | `object`  |  | &nbsp; |
| email | `string`  |  | *Optional* |
| phoneNumber | `string`  |  | *Optional* |




##### Returns


- `object Object`  



#### Shiphawk.request(method, endpoint, data, options) 

Make a ShipHawk API request




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| method | `string`  |  | &nbsp; |
| endpoint | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `object`  |  | &nbsp; |




##### Returns


- `Object`  




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
