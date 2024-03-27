# Libraries &gt; ShopifyGraphql.js 



### vendor/ShopifyGraphql.js


#### new ShopifyGraphql() 

Graphql Library






##### Returns


- `Void`



#### ShopifyGraphql.send(query, variables) 

Grapqhl call to Shopify.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| query | `string`  | Graphql query with variables. | &nbsp; |
| variables | `object`  | Object with graphql query variables. | &nbsp; |




##### Examples

```javascript
// Query example
const query = `query {
    shop {
      name
      primaryDomain {
        url
        host
      }
    }
   }`;
const rest =  Graphql.send(query, '');
```


##### Returns


- `object`  Graphql response.



#### ShopifyGraphql.addOrUpdateMetafields(id, metafields) 

Adds a metafields to Shopify order. This function will add a metafield id
to the payload if metafield already exits.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| id | `string`  | Shopify Order ID. | &nbsp; |
| metafields | `Array.&#60;Metafields&#62;`  | Array of metafields. | &nbsp; |




##### Examples

```javascript
const shopifyOrderId = 1234;
const metafields = [{
       namespace: "example",
       key: "example_key",
       value: "example_value"
   }];
const response =  Graphql.addOrUpdateMetafields(shopifyOrderId, metafields, "order");
Mesa.log.info('Graphql response: ', response);
```


##### Returns


- `object`  Graphql response



#### ShopifyGraphql.addMetafields(id, metafields, entity) 

Adds a metafield to a Shopify entity. This function will throw an error if
metafield exists and you do not pass an id.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| id | `string`  | Entity id. | &nbsp; |
| metafields | `Array.&#60;Metafields&#62;`  | Array of metafields. | &nbsp; |
| entity | `string`  | Entity: Order | Product | &nbsp; |




##### Returns


- `Void`



#### ShopifyGraphql.groupMetafieldsByKey(data) 

Takes metafield results, returns object keyed by the metafield key




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| data | `object`  |  | &nbsp; |




##### Returns


- `object`  metafields



#### ShopifyGraphql.buildShopifyId(entity, id) 

Builds Shopfiy Graphql id.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| entity | `string`  | Shopfiy graphql entity. | &nbsp; |
| id | `string`  | Shopify entity id. | &nbsp; |




##### Returns


- `string`  Shopfiy graphql id



#### ShopifyGraphql.extractShopifyId(gid) 

Builds Shopfiy Graphql id.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| gid | `string`  | Shopfiy graphql id (ex: gid://shopify/ShippingLabelV2/637424009250) | &nbsp; |




##### Returns


- `string`  Shopfiy id without the gid notation (ex: 637424009250)



#### {Object} Metafields() 

Metafields





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Returns


- `Void`




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
