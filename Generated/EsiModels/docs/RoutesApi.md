# EveESI.Models.Api.RoutesApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetRouteOriginDestination**](RoutesApi.md#getrouteorigindestination) | **GET** /route/{origin}/{destination} | Get route |

<a id="getrouteorigindestination"></a>
# **GetRouteOriginDestination**
> List&lt;long&gt; GetRouteOriginDestination (long destination, long origin, DateOnly xCompatibilityDate, List<long>? avoid = null, List<List<long>>? connections = null, string? flag = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get route

Get the systems between origin and destination

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetRouteOriginDestinationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new RoutesApi(config);
            var destination = 789L;  // long | 
            var origin = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var avoid = new List<long>?(); // List<long>? |  (optional) 
            var connections = new List<List<long>>?(); // List<List<long>>? |  (optional) 
            var flag = "shortest";  // string? |  (optional)  (default to shortest)
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get route
                List<long> result = apiInstance.GetRouteOriginDestination(destination, origin, xCompatibilityDate, avoid, connections, flag, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RoutesApi.GetRouteOriginDestination: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRouteOriginDestinationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get route
    ApiResponse<List<long>> response = apiInstance.GetRouteOriginDestinationWithHttpInfo(destination, origin, xCompatibilityDate, avoid, connections, flag, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RoutesApi.GetRouteOriginDestinationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **destination** | **long** |  |  |
| **origin** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **avoid** | [**List&lt;long&gt;?**](long.md) |  | [optional]  |
| **connections** | [**List&lt;List&lt;long&gt;&gt;?**](List&lt;long&gt;.md) |  | [optional]  |
| **flag** | **string?** |  | [optional] [default to shortest] |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

**List<long>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

