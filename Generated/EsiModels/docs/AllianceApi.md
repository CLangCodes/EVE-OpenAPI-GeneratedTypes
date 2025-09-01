# EveESI.Models.Api.AllianceApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAlliances**](AllianceApi.md#getalliances) | **GET** /alliances | List all alliances |
| [**GetAlliancesAllianceId**](AllianceApi.md#getalliancesallianceid) | **GET** /alliances/{alliance_id} | Get alliance information |
| [**GetAlliancesAllianceIdCorporations**](AllianceApi.md#getalliancesallianceidcorporations) | **GET** /alliances/{alliance_id}/corporations | List alliance&#39;s corporations |
| [**GetAlliancesAllianceIdIcons**](AllianceApi.md#getalliancesallianceidicons) | **GET** /alliances/{alliance_id}/icons | Get alliance icon |

<a id="getalliances"></a>
# **GetAlliances**
> List&lt;long&gt; GetAlliances (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List all alliances

List all active player alliances

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetAlliancesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new AllianceApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List all alliances
                List<long> result = apiInstance.GetAlliances(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AllianceApi.GetAlliances: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAlliancesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List all alliances
    ApiResponse<List<long>> response = apiInstance.GetAlliancesWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AllianceApi.GetAlliancesWithHttpInfo: " + e.Message);
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

<a id="getalliancesallianceid"></a>
# **GetAlliancesAllianceId**
> AlliancesAllianceIdGet GetAlliancesAllianceId (long allianceId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get alliance information

Public information about an alliance

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetAlliancesAllianceIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new AllianceApi(config);
            var allianceId = 789L;  // long | The ID of the alliance
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get alliance information
                AlliancesAllianceIdGet result = apiInstance.GetAlliancesAllianceId(allianceId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AllianceApi.GetAlliancesAllianceId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAlliancesAllianceIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get alliance information
    ApiResponse<AlliancesAllianceIdGet> response = apiInstance.GetAlliancesAllianceIdWithHttpInfo(allianceId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AllianceApi.GetAlliancesAllianceIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **allianceId** | **long** | The ID of the alliance |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**AlliancesAllianceIdGet**](AlliancesAllianceIdGet.md)

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

<a id="getalliancesallianceidcorporations"></a>
# **GetAlliancesAllianceIdCorporations**
> List&lt;long&gt; GetAlliancesAllianceIdCorporations (long allianceId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List alliance's corporations

List all current member corporations of an alliance

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetAlliancesAllianceIdCorporationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new AllianceApi(config);
            var allianceId = 789L;  // long | The ID of the alliance
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List alliance's corporations
                List<long> result = apiInstance.GetAlliancesAllianceIdCorporations(allianceId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AllianceApi.GetAlliancesAllianceIdCorporations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAlliancesAllianceIdCorporationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List alliance's corporations
    ApiResponse<List<long>> response = apiInstance.GetAlliancesAllianceIdCorporationsWithHttpInfo(allianceId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AllianceApi.GetAlliancesAllianceIdCorporationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **allianceId** | **long** | The ID of the alliance |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
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

<a id="getalliancesallianceidicons"></a>
# **GetAlliancesAllianceIdIcons**
> AlliancesAllianceIdIconsGet GetAlliancesAllianceIdIcons (long allianceId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get alliance icon

Get the icon urls for a alliance  This route expires daily at 11:05

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetAlliancesAllianceIdIconsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new AllianceApi(config);
            var allianceId = 789L;  // long | The ID of the alliance
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get alliance icon
                AlliancesAllianceIdIconsGet result = apiInstance.GetAlliancesAllianceIdIcons(allianceId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AllianceApi.GetAlliancesAllianceIdIcons: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAlliancesAllianceIdIconsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get alliance icon
    ApiResponse<AlliancesAllianceIdIconsGet> response = apiInstance.GetAlliancesAllianceIdIconsWithHttpInfo(allianceId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AllianceApi.GetAlliancesAllianceIdIconsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **allianceId** | **long** | The ID of the alliance |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**AlliancesAllianceIdIconsGet**](AlliancesAllianceIdIconsGet.md)

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

