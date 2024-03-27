# Libraries &gt; Dropbox.js 



### vendor/Dropbox.js


#### new Dropbox(tokenKey) 

Methods to interact with the Dropbox API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| tokenKey | `string`  | The key of the secret containing a Dropbox oAuth token. Defaults to `dropbox.oauth`. | &nbsp; |



##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| tokenKey | `string`  | The key of the secret containing a Dropbox oAuth token. Defaults to `dropbox.oauth`. | &nbsp; |



##### Examples

```javascript
const Dropbox = require('vendor/Dropbox.js');
const dropbox = new Dropbox();
const getResponse = dropbox.request.post('https://api.dropboxapi.com/2/files/save_url', {
  path: '/file.jpg',
  url: 'https://example.com/file.jpg',
});
```


##### Returns


- `class`  




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
