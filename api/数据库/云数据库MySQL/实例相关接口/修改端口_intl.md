## 1. API Description
This API (ModifyCdbInstanceVport) is used to modify the port number of an instance.
Domain for API request: <font style='color:red'>cdb.api.qcloud.com </font>


## 2. Input Parameters
The following request parameter list only provides API request parameters. Common request parameters need to be added when the API is called. For more information, refer to <a href='/document/product/236/6921' title='Common Request Parameters'>Common Request Parameters</a>. The Action field for this API is ModifyCdbInstanceVport.

| Parameter Name | Required  | Type | Description |
|---------|---------|---------|---------|
| cdbInstanceIds.n | Yes | String | One or more instance IDs (n represents array subscript starting with 0). Instance ID, such as: cdb-c1nl9rpv. It is identical to the instance ID displayed in the Cloud Database console page and can be obtained using API [Query List of Instances](/doc/api/253/1266). Its value equals to the uInstanceId field value in the output parameter.  |
| port | Yes | Int | Port number, value range: [1024-65535] |


## 3. Output Parameters
| Parameter Name | Type | Description |
|---------|---------|---------|
| code | Int | Common error code; 0: Succeeded; other values: Failed. For more information, please refer to <a href='https://intl.cloud.tencent.com/document/product/236/1743' title='Common Error Codes'>Common Error Codes</a> on the Error Code page. |
| message | String | Module error message description depending on API. |
| codeDesc | String | Error description |
| data | Array | Returned data |


## 4. Error Codes
The following error codes only include the business logic error codes for this API.

| Error Code | Error Message | Description |
|---------|---------|---------|
| 9003 | InvalidParameter | Incorrect parameter |
| 9006 | InternalError | Database internal error |
| 9013 | InternalError | System internal error |


## 5. Example
Input
<pre>
https://cdb.api.qcloud.com/v2/index.php?Action=ModifyCdbInstanceVport
&<<a href="/document/product/236/6921">Common request parameters</a>>
&cdbInstanceIds.0=cdb-11jposgk
&port=3307
</pre>

Output
```
{
    "code":"0",
    "message":"",
    "codeDesc":"Success",
    "data":[]
}
```


