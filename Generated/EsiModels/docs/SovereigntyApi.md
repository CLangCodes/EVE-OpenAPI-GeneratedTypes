# EveESI.Models.Api.SovereigntyApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetSovereigntyCampaigns**](SovereigntyApi.md#getsovereigntycampaigns) | **GET** /sovereignty/campaigns | List sovereignty campaigns |
| [**GetSovereigntyMap**](SovereigntyApi.md#getsovereigntymap) | **GET** /sovereignty/map | List sovereignty of systems |
| [**GetSovereigntyStructures**](SovereigntyApi.md#getsovereigntystructures) | **GET** /sovereignty/structures | List sovereignty structures |

<a id="getsovereigntycampaigns"></a>
# **GetSovereigntyCampaigns**
> List&lt;SovereigntyCampaignsGetInner&gt; GetSovereigntyCampaigns (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List sovereignty campaigns

Shows sovereignty data for campaigns.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetSovereigntyCampaignsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new SovereigntyApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List sovereignty campaigns
                List<SovereigntyCampaignsGetInner> result = apiInstance.GetSovereigntyCampaigns(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SovereigntyApi.GetSovereigntyCampaigns: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSovereigntyCampaignsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List sovereignty campaigns
    ApiResponse<List<SovereigntyCampaignsGetInner>> response = apiInstance.GetSovereigntyCampaignsWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SovereigntyApi.GetSovereigntyCampaignsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;SovereigntyCampaignsGetInner&gt;**](SovereigntyCampaignsGetInner.md)

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

<a id="getsovereigntymap"></a>
# **GetSovereigntyMap**
> List&lt;SovereigntyMapGetInner&gt; GetSovereigntyMap (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List sovereignty of systems

Shows sovereignty information for solar systems

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetSovereigntyMapExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new SovereigntyApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List sovereignty of systems
                List<SovereigntyMapGetInner> result = apiInstance.GetSovereigntyMap(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SovereigntyApi.GetSovereigntyMap: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSovereigntyMapWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List sovereignty of systems
    ApiResponse<List<SovereigntyMapGetInner>> response = apiInstance.GetSovereigntyMapWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SovereigntyApi.GetSovereigntyMapWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;SovereigntyMapGetInner&gt;**](SovereigntyMapGetInner.md)

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

<a id="getsovereigntystructures"></a>
# **GetSovereigntyStructures**
> List&lt;SovereigntyStructuresGetInner&gt; GetSovereigntyStructures (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List sovereignty structures

Shows sovereignty data for structures.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetSovereigntyStructuresExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new SovereigntyApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List sovereignty structures
                List<SovereigntyStructuresGetInner> result = apiInstance.GetSovereigntyStructures(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SovereigntyApi.GetSovereigntyStructures: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSovereigntyStructuresWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List sovereignty structures
    ApiResponse<List<SovereigntyStructuresGetInner>> response = apiInstance.GetSovereigntyStructuresWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SovereigntyApi.GetSovereigntyStructuresWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;SovereigntyStructuresGetInner&gt;**](SovereigntyStructuresGetInner.md)

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

