# MESA SDK 


#### Mesa.log.info(message[, meta]) 

Log info to Mesa Logs.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| message | `string`  |  | &nbsp; |
| meta | `object`  |  | *Optional* |




##### Returns


- `Void`



#### Mesa.log.warn(message[, meta]) 

Log a warning to Mesa Logs.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| message | `string`  |  | &nbsp; |
| meta | `object`  |  | *Optional* |




##### Returns


- `Void`



#### Mesa.log.error(message[, meta]) 

Log an error to Mesa Logs.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| message | `string`  |  | &nbsp; |
| meta | `object`  |  | *Optional* |




##### Returns


- `Void`



#### Mesa.log.debug(message[, meta]) 

Log info to Mesa Logs only if the Automation is in Debug Mode.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| message | `string`  |  | &nbsp; |
| meta | `object`  |  | *Optional* |




##### Returns


- `Void`



#### Mesa.request.get(path, options) 

Make a GET request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| options | `Types.RequestOptions`  |  | &nbsp; |




##### Returns


- `Types.Response` `Types.ResponseRaw`  The response returned by the request. `object` if `options.json` is `true`, `string` if `options.json` is `false`.



#### Mesa.request.post(path, data, options) 

Make a POST request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `Types.RequestOptions`  |  | &nbsp; |




##### Returns


- `Types.Response` `Types.ResponseRaw`  The response returned by the request. `object` if `options.json` is `true`, `string` if `options.json` is `false`.



#### Mesa.request.put(path, data, options) 

Make a PUT request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `Types.RequestOptions`  |  | &nbsp; |




##### Returns


- `Types.Response` `Types.ResponseRaw`  The response returned by the request. `object` if `options.json` is `true`, `string` if `options.json` is `false`.



#### Mesa.request.patch(path, data, options) 

Make a PATCH request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `Types.RequestOptions`  |  | &nbsp; |




##### Returns


- `Types.Response` `Types.ResponseRaw`  The response returned by the request. `object` if `options.json` is `true`, `string` if `options.json` is `false`.



#### Mesa.request.delete(path, options) 

Make a DELETE request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| path | `string`  |  | &nbsp; |
| options | `Types.RequestOptions`  |  | &nbsp; |




##### Returns


- `Types.Response` `Types.ResponseRaw`  The response returned by the request. `object` if `options.json` is `true`, `string` if `options.json` is `false`.



#### Mesa.request.send(method, path, data, options) 

Make a request to an external Rest API.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| method | `string`  | One of `GET`, `POST`, `PUT`, `PATCH`, or `DELETE` | &nbsp; |
| path | `string`  |  | &nbsp; |
| data | `object`  |  | &nbsp; |
| options | `Types.RequestOptions`  |  | &nbsp; |




##### Returns


- `Types.Response` `Types.ResponseRaw`  The response returned by the request. `object` if `options.json` is `true`, `string` if `options.json` is `false`.



#### Mesa.request.base64_encode(string) 

Base-64 encode a string.
This is helpful when building an `Authorization` header for basic auth requests.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| string | `string`  | The string to encode | &nbsp; |




##### Returns


- `string`  The base-64 encoded version of the input string parameter.



#### Mesa.request.base64_decode(string[, strict]) 

Base64 decode a string.
Decodes data encoded with MIME base64




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| string | `string`  | The base-64 encoded version of the input string parameter. | &nbsp; |
| strict | `bool`  | If the strict parameter is set to TRUE then the base64_decode() function will return FALSE if the input contains character from outside the base64 alphabet. Defaults to FALSE. | *Optional* |




##### Returns


- `string`  The decoded string.



#### Mesa.request.hash(algorithm, string[, base64encode]) 

Generate a hash of a string.
This is helpful when creating signed requests.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| algorithm | `string`  | The algorithm to use. Options: `sha1`, `sha256`, `md5` | &nbsp; |
| string | `string`  | The string to create the hash from | &nbsp; |
| base64encode | `string`  | Should we base64-encode the raw value of the hash? | *Optional* |




##### Returns


- `string`  The raw binary data of the hash



#### Mesa.request.hashHmac(algorithm, string, string[, base64encode]) 

Generate a keyed hash value using the HMAC method.
This is helpful when creating signed requests.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| algorithm | `string`  | The algorithm to use. Options: `sha1`, `sha256`, `md5` | &nbsp; |
| string | `string`  | The string to create the hash from | &nbsp; |
| string | `string`  | Shared secret key used for generating the HMAC variant of the message digest | &nbsp; |
| base64encode | `string`  | Should we base64-encode the raw value of the hash? | *Optional* |




##### Returns


- `string`  The raw binary data of the hash



#### Mesa.request.sleep($seconds) 

Pauses execution




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| $seconds | `int`  |  | &nbsp; |




##### Returns


-  



#### Mesa.credential.get(key[, defaultValue]) 

Get a secret.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| key | `string`  |  | &nbsp; |
| defaultValue | `string`  | A default value to use if the secret cannot be found. If `defaultValue` is empty, the script will throw a fatal error if the secret is not found. | *Optional* |




##### Returns


- `string`  The secret value.



#### Mesa.credential.set(key, value[, options]) 

Save a secret value.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| key | `string`  | The credential key or id. | &nbsp; |
| value | `string`  | The value to save. This will be encrypted at rest, and can contained a stringified JSON array. | &nbsp; |
| options | `object`  |  | *Optional* |
| options.oauth_provider | `bool`  |  | *Optional* |
| options.oauth_scope | `object`  |  | *Optional* |
| options.trigger_type | `object`  |  | *Optional* |




##### Returns


- `Void`



#### Mesa.database.query(sql) 

Get a storage item




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| sql | `string`  | The SQL query to run | &nbsp; |




##### Returns


- `array`  The result of the query.



#### Mesa.storage.get(key[, defaultValue]) 

Get a storage item




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| key | `string`  |  | &nbsp; |
| defaultValue | `string`  | A default value to use if the storage key cannot be found. If `defaultValue` is empty, the script will throw a fatal error if the storage key is not found. | *Optional* |




##### Returns


- `string`  The storage value.



#### Mesa.storage.set(key, value) 

Get a storage item




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| key | `string`  |  | &nbsp; |
| value | `string`  |  | &nbsp; |




##### Returns


- `Void`



#### Mesa.liquid.render(template, params) 

Render a liquid template with the `params` passed.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| template | `string`  | String representing a liquid template. | &nbsp; |
| params | `object`  | A keyed object of parameters to replace. | &nbsp; |




##### Returns


- `string`  The rendered template code.



#### Mesa.input.getWebhookUrl(type, format, automationId, key) 

Generates the URL for input webhooks




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| type | `string`  | Type of webhook: `json`, `shopify` | &nbsp; |
| format | `string`  | Format of the returned data: `string` or `array`. If string, a full URL is returned. If `array`, URL will comprise two fields `suffix` and `prefix` | &nbsp; |
| automationId | `string`  | ID of the Automation | &nbsp; |
| key | `string`  | The key of the trigger | &nbsp; |




##### Returns


- `string` `array`  The rendered template code.



#### Mesa.output.next(payload, params) 

Pass a payload to the service and call the next step in this Automation.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| payload | `object`  |  | &nbsp; |
| params | `object`  | Parameters to send to the output, such as tokens to construct a Shopify API url | &nbsp; |
| params.enqueue | `bool`  | Defaults to false. Set to true if you are exploding multiple tasks that can be run in parallel. | *Optional* |




##### Returns


- `Void`



#### Mesa.output.send(outputKey, payload, enqueue) 

Call an arbitrary output from a MESA Script




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| outputKey | `string`  |  | &nbsp; |
| payload | `object`  |  | &nbsp; |
| enqueue | `bool`  | Defaults to false. Set to true if you are exploding multiple tasks that can be run in parallel. | &nbsp; |




##### Returns


- `Void`



#### Mesa.automation.send(automationKey, payload) 

Call another automation from a MESA Script




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| automationKey | `string`  | In the form `${automationKey}`, this will trigger the first input in the Automation. In the form `${automationKey}/${inputKey}`, this will trigger a specific input in the automation. | &nbsp; |
| payload | `object`  |  | &nbsp; |




##### Returns


- `Void`



#### Mesa.ftp.deleteFile(filename) 

Delete the file loaded by the Input.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| filename | `string`  | Typically passed from `context.filename`. | &nbsp; |




##### Returns


- `Void`



#### Mesa.ftp.moveFile(filename, destinationFilenameAndPath) 

Move the file loaded by the Input to a new location.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| filename | `string`  | Typically passed from `context.filename`. | &nbsp; |
| destinationFilenameAndPath | `string`  |  | &nbsp; |




##### Returns


- `Void`



#### Mesa.xml.decode(xmlString[, namespaceSep&#x3D;&#x27;_&#x27;]) 

Convert an XML file into an {object}.  This function will condense XML namespaces into {namespaceSep = '_'} separated values:
<soapenv:Body> becomes { soapenv_Body: {} }




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| xmlString | `string`  | The xml file to be decoded | &nbsp; |
| namespaceSep&#x3D;&#x27;_&#x27; | `string`  | Namespace separator for replacing <soapenv:Body> type values with soapenv_Body | *Optional* |




##### Returns


- `object`  



#### Mesa.xml.encode(xmlObject[, wrapReplace, namespaceSep&#x3D;&#x27;_&#x27;]) 

Convert an object into an XML string.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| xmlObject | `object`  | The object to be turned into xml. | &nbsp; |
| wrapReplace | `string`  | Replace the default <doc> wrapping provided with another value | *Optional* |
| namespaceSep&#x3D;&#x27;_&#x27; | `string`  | Namespace separator for replacing soapenv_Body: {} values with <soapenv:Body> | *Optional* |




##### Examples

```javascript
// returns <?xml version="1.0" encoding="UTF-8"?><doc>\n  <book>\n ...
Mesa.xml.encode({ book: { ... }});
```
```javascript
// returns <?xml version="1.0" encoding="UTF-8"?><soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">\n  <soapenv:Body>\n ...
Mesa.xml.encode({ soapenv_Body: { ... } }, '<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">');
```


##### Returns


- `string`  



#### Mesa.xml.valid(xmlString) 

Check if xml is valid




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| xmlString | `string`  |  | &nbsp; |




##### Examples

```javascript
// returns true
Mesa.xml.valid('<?xml version="1.0" encoding="UTF-8"?><doc><book><Name>My Book</Name></book></doc>');
```
```javascript
// throws error about namespace
Mesa.xml.valid('<?xml version="1.0" encoding="UTF-8"?><soapenv:Envelope><book><Name>My Book</Name></book></soapenv:Envelope>');
```


##### Returns


- `bool`  



#### Mesa.csv.decode(data[, returnObject, options]) 

Convert a CSV file into an object.  Keys will be matched from the first header row of the CSV file.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| data | `string`  |  | &nbsp; |
| returnObject | `bool`  | Defaults to `true`, which will return an object keyed by the first row in the CSV content. Set to `false` to return an array. | *Optional* |
| options | `object`  |  | *Optional* |
| options.delimiter&#x3D;&#x27;,&#x27; | `string`  | The delimiter to use when parsing the CSV file. Must be a single character. | *Optional* |




##### Returns


- `object` `array`  



#### Mesa.csv.encode(data[, headerRow]) 

Convert an object a CSV string.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| data | `object`  |  | &nbsp; |
| headerRow | `bool`  | Defaults to `true`. Set to `false` to skip the header row when returning CSV. | *Optional* |




##### Returns


- `string`  



#### Mesa.vo.push(outputKey, payload) 

Push to a Virtual Output.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| outputKey | `string`  |  | &nbsp; |
| payload | `mixed`  |  | &nbsp; |




##### Returns


- `Void`



#### Mesa.vo.clear(outputKey) 

Mark the matching Virtual Output records as cleared by the current Mesa Script.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| outputKey | `string`  |  | &nbsp; |




##### Returns


- `Void`



#### Mesa.vo.clearOne(outputKey, mesaId) 

Mark a single Virtual Output record as cleared by the current Mesa Script.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| outputKey | `string`  |  | &nbsp; |
| mesaId | `string`  | The ID of the record to clear (returned as mesa_id in the Virtual Output). | &nbsp; |




##### Returns


- `Void`



#### Mesa.date.setTimezone(timezone) 

Set the timezone to use to execute all script commands.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| timezone | `string`  | The timezone identifier, like UTC or America/Los_Angeles. [See a full list of TZ Database names](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). | &nbsp; |




##### Returns


- `string`  The timezone identifier, like UTC or Europe/Lisbon.



#### Mesa.date.format(format, timestamp) 

Returns a date as a formatted string.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| format | `string`  | The format of the outputted date string. [See full list of options](https://docs.getmesa.com/built-in/ftp/working-with-dates). | &nbsp; |
| timestamp | `int`  | Defaults to now. Optional | &nbsp; |




##### Returns


- `string`  The formatted date string.



#### Mesa.email.send(to, subject, body[, from]) 

Send an email.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| to | `string`  |  | &nbsp; |
| subject | `string`  |  | &nbsp; |
| body | `string`  |  | &nbsp; |
| from | `string`  | All emails will be sent from no-reply@getmesa.com. The from email address will be used as the From name and reply-to email address. | *Optional* |




##### Returns


- `Void`





[Full list of MESA Libraries](libraries/README.md)