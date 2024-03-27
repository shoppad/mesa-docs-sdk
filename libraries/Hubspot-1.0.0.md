# Libraries &gt; Hubspot.js 



### vendor/Hubspot.js


#### new Hubspot() 

Interacts with the HubSpot API for creation of contacts and deals.
Also includes a request method which can be used to call any API method on the HubSpot API.






##### Returns


- `Hubspot`  



#### Hubspot.constructor(apiKey, token) 

Constructor - accepts API Key for HubSpot (for legacy template support), or oauth (for new templates)




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| apiKey | `string`  | [Hubspot API key]. See: https://knowledge.hubspot.com/integrations/how-do-i-get-my-hubspot-api-key | &nbsp; |
| token | `string`  |  | &nbsp; |




##### Examples

```javascript

// Initiate Hubspot, passing in HubSpot API key, which should be stored in a secret
const hubspot = new Hubspot(Mesa.secret.get('hubspot-hapi'));
```


##### Returns


- `Void`



#### Hubspot.request(method, endpoint, payload, options) 






##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| method | `string`  | (GET / POST / PUT / PATCH / DELETE) | &nbsp; |
| endpoint | `string`  | The relative path, e.g. 'contacts/v1/contact' | &nbsp; |
| payload | `object`  | Data to pass to endpoint, | &nbsp; |
| options | `object`  | Optional params See https://docs.getmesa.com/built-in/custom-code/sdk#vendor-mesa.js-mesa.request.get | &nbsp; |




##### Returns


- `Object`  response object from HubSpot API



#### Hubspot.oauthRequest(method, path, payload, options) 

Request to use for new oauth methods




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| method | `string`  | (GET / POST / PUT / PATCH / DELETE) | &nbsp; |
| path | `string`  | The full path, e.g. 'contacts/v1/contact' | &nbsp; |
| payload | `object`  | Data to pass to endpoint, | &nbsp; |
| options | `object`  | Optional params See https://docs.getmesa.com/built-in/custom-code/sdk#vendor-mesa.js-mesa.request.get | &nbsp; |




##### Returns


- `Void`



#### getContactByEmail(email) 

Get HubSpot contact by email




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| email | `string`  | address | &nbsp; |




##### Examples

```javascript

// Initiate Hubspot, passing in HubSpot API key
const hubspot = new Hubspot(Mesa.secret.get('hubspot-hapi'));

// Example call
const response = hubspot.getContactByEmail('john.doe@domain.tld');
```


##### Returns


- `object`  response object from HubSpot API



#### createContact(data) 

Create a HubSpot Contact

If contact already exists (based on the email address provided in the data), response will show the ID of the existing Contact




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| data | `object`  | Request payload | &nbsp; |
| data.properties | `array`  | Array of Contact Properties. Details on parameters you can use: https://developers.hubspot.com/docs/methods/contacts/create_contact | &nbsp; |




##### Examples

```javascript

// Example payload (must be wrapped with 'properties')
const postData = {
  properties:[
    {
      property: "email",
      value: "name@domain.tld"
    },
    {
      property: "firstname",
      value: "John"
    },
    {
      property: "lastname",
      value: "Doe"
    }
  ]
};

// Initiate Hubspot, passing in HubSpot API key
const hubspot = new Hubspot(Mesa.secret.get('hubspot-hapi'));

// Example call
const response = hubspot.createContact(postData);
```


##### Returns


- `object`  response object from HubSpot API



#### createOrUpdateContact(data) 

Create or update a HubSpot Contact

Return data includes `isNew` parameter which will be set to `true` if contact created, or `false` if updated




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| data | `object`  | Request payload | &nbsp; |
| data.properties | `array`  | Array of Contact Properties. Details on parameters you can use: https://developers.hubspot.com/docs/methods/contacts/create_or_update | &nbsp; |




##### Examples

```javascript

// Example payload - must be wrapped in 'properties'
const postData = {
  properties:[
    {
      property: "firstname",
      value: "John"
    },
    {
      property: "lastname",
      value: "Doe"
    }
  ]
};

// Initiate Hubspot, passing in HubSpot API key
const hubspot = new Hubspot(Mesa.secret.get('hubspot-hapi'));

// Example call
const response = hubspot.createOrUpdateContact(postData, 'john.doe@domain.tld');
```


##### Returns


- `object`  response object from HubSpot API



#### createDeal(data) 

Create a HubSpot Deal

A deal can be created without associatedVids (contact IDs).




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| data | `object`  |  | &nbsp; |
| data.properties | `array`  | Array of Deal Properties. Details on parameters you can use: https://developers.hubspot.com/docs/methods/deals/create_deal | &nbsp; |




##### Examples

```javascript

// Example payload - must be wrapped in 'properties', and include 'associations' if you want to link a deal to a contact
const postData = {
  associations: [
    associatedVids: [
      123456
    ]
  ],
  properties: [
    {
      name: "dealname",
      value: "John's first deal",
    },
    {
      name: "dealname",
      value: "John's first deal",
    },
    {
      name: "dealstage",
      value: "appointmentscheduled",
    },
    {
      name: "dealtype",
      value: "newbusiness",
    },
    {
      name: "10.99",
      value: "amount",
    }
  ]
};

// Initiate Hubspot, passing in HubSpot API key
const hubspot = new Hubspot(Mesa.secret.get('hubspot-hapi'));

// Example call
const response = hubspot.createDeal(postData);
```


##### Returns


- `object`  response object from HubSpot API



#### createWorkflow(data) 

Create HubSpot workflow




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| data | `object`  | containing JSON data for workflow. Details on parameters you can use: https://developers.hubspot.com/docs/methods/workflows/v3/create_workflow | &nbsp; |




##### Examples

```javascript

// Create JSON payload to pass through (see https://developers.hubspot.com/docs/methods/workflows/v3/create_workflow for structure)
const postData = "{}";

// Initiate Hubspot, passing in HubSpot API key
const hubspot = new Hubspot(Mesa.secret.get('hubspot-hapi'));

// Example call
const response = hubspot.createWorkflow(postData);
```


##### Returns


- `object`  response object from HubSpot API




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
