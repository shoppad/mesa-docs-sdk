# Libraries &gt; Cloudinary.js 



### vendor/Cloudinary.js


#### new Cloudinary(cloudName, apiKey, apiSecret) 

Methods to interact with the Cloudinary API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| cloudName | `string`  | The account's Cloudinary cloud name. | &nbsp; |
| apiKey | `string`  | The API Key from the Cloudinary dashboard. | &nbsp; |
| apiSecret | `string`  | the API secret from the Cloudinary dashboard. * | &nbsp; |




##### Examples

```javascript
const Cloudinary = require('vendor/Cloudinary.js');
const cloudinary = new Cloudinary(cloudName, api, secret);
const response = cloudinary.upload('https://api.cloudinaryapi.com/2/files/save_url', {
  eager: 'w_400,h_300,c_pad',
});
```


##### Returns


- `class`  



#### Cloudinary.upload() 

Upload a file to Cloudinary, and optionally perform eager transformations.





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Examples

```javascript
const cloudinary = new Cloudinary(cloudName, api, secret);
const response = cloudinary.request('http://google.com/favicon.png', {
  eager: 'w_400,h_300,c_pad',
});
```


##### Returns


- `Void`



#### Cloudinary.search() 

Search a file in Cloudinary by public ID





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Returns


- `Void`



#### Cloudinary.request() 

Make a generic request to the Cloudinary API





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Examples

```javascript
const cloudinary = new Cloudinary(cloudName, api, secret);
const response = cloudinary.request('POST', 'upload', {file: 'http://google.com/favicon.png'});
```


##### Returns


- `Void`



#### {Object} Data() 

data parameter for Cloudinary API calls





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Returns


- `Void`



#### {Object} Options() 

options parameter for Cloudinary API calls





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Returns


- `Void`




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
