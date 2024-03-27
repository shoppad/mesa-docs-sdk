# Libraries &gt; Utils.js 



### vendor/Utils.js


#### Utils() 

Miscellaneous utils for MESA scripts






##### Returns


- `Void`



#### removeKeysPrefix(payload, prefix) 

Remove prefix from keys




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| payload | `Object`  |  | &nbsp; |
| prefix | `string`  |  | &nbsp; |




##### Returns


- `Object`  



#### wrapOutput(payload, key) 

Wrap output with a parent key




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| payload | `Object`  |  | &nbsp; |
| key | `string`  |  | &nbsp; |




##### Returns


- `Object`  



#### dateIsBeforeOffset(date, syncDelayMs) 

Check date vs current time with an offset applied




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| date | `Object`  |  | &nbsp; |
| syncDelayMs | `int`  |  | &nbsp; |




##### Returns


- `Object`  



#### removeNullEntries(payload) 

Remove payload entries with null values




##### Parameters

| Name | Type | Description |  |
| ---- | ---- | ----------- | -------- |
| payload |  |  | &nbsp; |




##### Returns


- `Object`  



#### getTimezones() 

// Returns a list of timezones,with label = user friendly timezone, value IANA teimzone value
    // Taken from: https://stackoverflow.com/a/52265733






##### Returns


-  [] array




*Documentation generated with [doxdox](https://github.com/neogeek/doxdox).*
