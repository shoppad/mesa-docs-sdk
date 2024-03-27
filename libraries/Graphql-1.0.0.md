# Libraries &gt; Graphql.js 



### vendor/Graphql.js


#### new Graphql() 

Graphql Library






##### Returns


- `Void`



#### Graphql.send(query, variables) 

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



#### Graphql.addOrUpdateMetafields(id, metafields) 

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



#### Graphql.addMetafields(id, metafields, entity) 

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



#### Graphql.buildShopifyId(entity, id) 

Builds Shopfiy Graphql id.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| entity | `string`  | Shopfiy graphql entity. | &nbsp; |
| id | `string`  | Shopify entity id. | &nbsp; |




##### Returns


- `string`  Shopfiy graphql id



#### {Object} Metafields() 

Metafields





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Returns


- `Void`




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
