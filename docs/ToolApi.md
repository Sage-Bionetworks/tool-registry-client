# toolregistryclient.ToolApi

All URIs are relative to *http://example.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_tool**](ToolApi.md#create_tool) | **POST** /tools | Add a tool
[**list_tools**](ToolApi.md#list_tools) | **GET** /tools | List the tools in the registry


# **create_tool**
> Tool create_tool(tool)

Add a tool

Add a tool

### Example

```python
from __future__ import print_function
import time
import toolregistryclient
from toolregistryclient.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to http://example.com/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = toolregistryclient.Configuration(
    host = "http://example.com/api/v1"
)


# Enter a context with an instance of the API client
with toolregistryclient.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = toolregistryclient.ToolApi(api_client)
    tool = toolregistryclient.Tool() # Tool | 

    try:
        # Add a tool
        api_response = api_instance.create_tool(tool)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ToolApi->create_tool: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tool** | [**Tool**](Tool.md)|  | 

### Return type

[**Tool**](Tool.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**403** | Unauthorized |  -  |
**404** | The specified resource was not found |  -  |
**409** | The request conflicts with current state of the target resource |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_tools**
> PageOfTools list_tools(limit=limit, offset=offset)

List the tools in the registry

Returns the tools in the registry

### Example

```python
from __future__ import print_function
import time
import toolregistryclient
from toolregistryclient.rest import ApiException
from pprint import pprint
# Defining the host is optional and defaults to http://example.com/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = toolregistryclient.Configuration(
    host = "http://example.com/api/v1"
)


# Enter a context with an instance of the API client
with toolregistryclient.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = toolregistryclient.ToolApi(api_client)
    limit = 10 # int | Maximum number of results returned (optional) (default to 10)
offset = 0 # int | Index of the first result that must be returned (optional) (default to 0)

    try:
        # List the tools in the registry
        api_response = api_instance.list_tools(limit=limit, offset=offset)
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling ToolApi->list_tools: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Maximum number of results returned | [optional] [default to 10]
 **offset** | **int**| Index of the first result that must be returned | [optional] [default to 0]

### Return type

[**PageOfTools**](PageOfTools.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**403** | Unauthorized |  -  |
**404** | The specified resource was not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

