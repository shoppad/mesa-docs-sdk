# Libraries &gt; Mapping.js 



### vendor/Mapping.js


#### Mapping() 

The mapping utility can be used to define a relationship between objects from different sources.
After defining the relationship, utility methods can be used to do things such as convert data from one
source to another, allowing users to then post to API endpoints without additional data manipulation.






##### Returns


- `Void`



#### Mapping.convert(Map, payload, input, ouput[, Processors]) 

Converts data from one source into another source's schema.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| Map | `<a href="#vendor-mapping.js-object-map">Map</a>`  | An object defining a relationship between objects from different sources. | &nbsp; |
| payload | `Object`  | The data from the input. | &nbsp; |
| input | `String`  | The key for the input as defined in `Map` (I.e.,`salesforce` or `shopify` in `Map`'s example). | &nbsp; |
| ouput | `String`  | The key for the output as defined in `Map` (I.e.,`salesforce` or `shopify` in `Map`'s example). | &nbsp; |
| Processors | `<a href="#vendor-mapping.js-object-processors">Processors</a>`  | Optional, an object containing functions that are used to process data while converting. | *Optional* |




##### Examples

```javascript
// First, we define a relationship between Shopify's customer object and SalesForce's
// contact object (See the Map object documention for details).
const Map = {
  email: {
    shopify: 'email',
    salesforce: 'Email'
  },
  address1: {
    shopify: 'default_address.address1',
    salesforce: 'MailingStreet'
  },
};

// Now that we have this relationship defined, we can use it to convert data both ways.
// Say for instance, we are receiving a webhook from Shopify that contains
// an updated customer object, and we want to put this new customer data into Salesforce.
// Using the mapping utility, we can convert the updated customer object from Shopify
// to match the format of Salesforce's contact object.

const Mapping = require('./vendor/Mapping.js');

// Updated customer record coming in from a Shopify webhook
const shopifyCustomer = payload;

// payload = {
//   email: 'hello@gmail.com',
//   default_address: {
//     address1: '123 Main Street'
//   }
// }


// Call convert method to take data from the shopifyCustomer and turn it into a salesforceContact
const salesforceContact = Mapping.convert(relationship, shopifyCustomer, 'salesforce', 'shopify');

// salesforceContact = {
//   Email: 'hello@gmail.com',
//   MailingStreet: '123 Main Street',
// }

// The salesforceContact can now be sent to Salesforce without additional data manipulation.
```


##### Returns


- `Object`  



#### {Object} Processors() 

Processors parameter for the `convert` method. Contains functions that modify the data being converted.





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Examples

```javascript
//
// Define processor functions
//

addName = (payload) => {
  if (!payload.name) {
    payload.name = 'John';
  }

  return payload;
}

updateEmail = (fieldKey, inputValue) => {
  if (fieldKey === 'email' && !inputValue.includes('+')) {
    return inputValue + '+mesa';
  } else {
    return inputValue;
  }
}

wrapCustomerOutput = (payload) => {
  return { customer: payload };
}

// The Processors param to pass to the convert method. 
const Processors = {
  preProcess: [ addName ],
  process: [ updateEmail ],
  postProcess: [ wrapCustomerOutput ],
};
```


##### Returns


- `Void`



#### {Object} Map() 

Map parameter for the `convert` method. Defines a relationship between objects from different sources. The relationship is defined using javascript paths.






##### Examples

```javascript
// Here we are defining a relationship bewtween Shopify's
// customer object and Salesforce's contact object.

// The Shopify object's schema:
// {
//   email: 'hello@gmail.com',
//   default_address: {
//     address1: '123 Main Street'
//   }
// }

// The Salesforce object's schema:
// {
//   Email: 'hello@gmail.com',
//   MailingStreet: '123 Main Street'
// }

// The resulting Map
const Map = {
  email: {
    shopify: 'email',
    salesforce: 'Email'
  },
  address1: {
    shopify: 'default_address.address1',
    salesforce: 'MailingStreet'
  },
};
```


##### Returns


- `Void`




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
