# Libraries &gt; OpenWeatherMap.js 



### vendor/OpenWeatherMap.js


#### new OpenWeatherMap() 

Get Weather Forecasts from OpenWeatherMap.

Full details on all API methods that are available at https://openweathermap.org/api.





##### Properties

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |



##### Examples

```javascript
const OpenWeatherMap = require('vendor/OpenWeatherMap.js');
const client = new OpenWeatherMap(Secret.get('openweathermap-key'));
const forecast = client.getForecast(latitude, longitude);
```


##### Returns


- `Void`



#### OpenWeatherMap.getForecast(latitude, longitude) 

Gets a 16-day forecast.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| latitude | `float`  |  | &nbsp; |
| longitude | `float`  |  | &nbsp; |




##### Returns


- `&lt;a href&#x3D;&quot;#vendor-openweathermap.js-object-forecastresponse&quot;&gt;ForecastResponse&lt;/a&gt;`  



#### OpenWeatherMap.request(method, params) 

Make an OpenWeatherMap API call.




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| method | `string`  | The OpenWeatherMap API method to call. Example: `forecast/daily`. | &nbsp; |
| params | `object`  | Additional parameters to send. Example `{lat: 122, lon: 100}`. | &nbsp; |




##### Returns


- `Void`



#### OpenWeatherMap.constructor(apiKey[, units]) 

Construct OpenWeatherMap authentication




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| apiKey | `string`  | Obtain an OpenWeatherMap `appid` from https://openweathermap.org/appid. | &nbsp; |
| units | `string`  | `imperial` (Farenheit) or `metric` (Celsius). Defaults to `imperial`. | *Optional* |




##### Returns


- `Void`



#### {Object} ForecastResponse() 








##### Examples

```javascript
{"cod":"200","message":0.0032,
"city":{"id":1851632,"name":"Shuzenji",
"coord":{"lon":138.933334,"lat":34.966671},
"country":"JP"
"timezone": 32400},
"cnt":10,
"list":[{
    "dt":1406080800,
    "temp":{
        "day":297.77,
        "min":293.52,
        "max":297.77,
        "night":293.52,
        "eve":297.77,
        "morn":297.77},
    "pressure":925.04,
    "humidity":76,
    "weather":[{"id":803,"main":"Clouds","description":"broken clouds","icon":"04d"}],}
]}
```


##### Returns


- `Void`




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
