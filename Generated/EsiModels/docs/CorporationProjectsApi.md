# EveESI.Models.Api.CorporationProjectsApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetCorporationsProjectsContribution**](CorporationProjectsApi.md#getcorporationsprojectscontribution) | **GET** /corporations/{corporation_id}/projects/{project_id}/contribution/{character_id} | Get your project contribution |
| [**GetCorporationsProjectsContributors**](CorporationProjectsApi.md#getcorporationsprojectscontributors) | **GET** /corporations/{corporation_id}/projects/{project_id}/contributors | List project contributors |
| [**GetCorporationsProjectsDetail**](CorporationProjectsApi.md#getcorporationsprojectsdetail) | **GET** /corporations/{corporation_id}/projects/{project_id} | Get project details |
| [**GetCorporationsProjectsListing**](CorporationProjectsApi.md#getcorporationsprojectslisting) | **GET** /corporations/{corporation_id}/projects | List corporation projects |

<a id="getcorporationsprojectscontribution"></a>
# **GetCorporationsProjectsContribution**
> CorporationsProjectsContribution GetCorporationsProjectsContribution (long corporationId, Guid projectId, long characterId, DateOnly xCompatibilityDate, string? ifModifiedSince = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get your project contribution

Show your contribution to a corporation project.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationsProjectsContributionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CorporationProjectsApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var projectId = "projectId_example";  // Guid | The ID of the project
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var ifModifiedSince = "ifModifiedSince_example";  // string? | The date the resource was last modified. A 304 will be returned if the resource has not been modified since this date. (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get your project contribution
                CorporationsProjectsContribution result = apiInstance.GetCorporationsProjectsContribution(corporationId, projectId, characterId, xCompatibilityDate, ifModifiedSince, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CorporationProjectsApi.GetCorporationsProjectsContribution: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationsProjectsContributionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get your project contribution
    ApiResponse<CorporationsProjectsContribution> response = apiInstance.GetCorporationsProjectsContributionWithHttpInfo(corporationId, projectId, characterId, xCompatibilityDate, ifModifiedSince, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CorporationProjectsApi.GetCorporationsProjectsContributionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **corporationId** | **long** | The ID of the corporation |  |
| **projectId** | **Guid** | The ID of the project |  |
| **characterId** | **long** | The ID of the character |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **ifModifiedSince** | **string?** | The date the resource was last modified. A 304 will be returned if the resource has not been modified since this date. | [optional]  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**CorporationsProjectsContribution**](CorporationsProjectsContribution.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcorporationsprojectscontributors"></a>
# **GetCorporationsProjectsContributors**
> CorporationsProjectsContributors GetCorporationsProjectsContributors (long corporationId, Guid projectId, DateOnly xCompatibilityDate, string? after = null, string? before = null, long? limit = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List project contributors

Listing of all contributors to a corporation project.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationsProjectsContributorsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CorporationProjectsApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var projectId = "projectId_example";  // Guid | The ID of the project
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var after = "after_example";  // string? | Return records from after this cursor (mutual exclusive with 'before'). '0' to start from the beginning. (optional) 
            var before = "before_example";  // string? | Return records from before this cursor (mutual exclusive with 'after'). '0' to start from the end. (optional) 
            var limit = 10L;  // long? | The amount of records to retrieve per request. (optional)  (default to 10)
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List project contributors
                CorporationsProjectsContributors result = apiInstance.GetCorporationsProjectsContributors(corporationId, projectId, xCompatibilityDate, after, before, limit, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CorporationProjectsApi.GetCorporationsProjectsContributors: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationsProjectsContributorsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List project contributors
    ApiResponse<CorporationsProjectsContributors> response = apiInstance.GetCorporationsProjectsContributorsWithHttpInfo(corporationId, projectId, xCompatibilityDate, after, before, limit, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CorporationProjectsApi.GetCorporationsProjectsContributorsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **corporationId** | **long** | The ID of the corporation |  |
| **projectId** | **Guid** | The ID of the project |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **after** | **string?** | Return records from after this cursor (mutual exclusive with &#39;before&#39;). &#39;0&#39; to start from the beginning. | [optional]  |
| **before** | **string?** | Return records from before this cursor (mutual exclusive with &#39;after&#39;). &#39;0&#39; to start from the end. | [optional]  |
| **limit** | **long?** | The amount of records to retrieve per request. | [optional] [default to 10] |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**CorporationsProjectsContributors**](CorporationsProjectsContributors.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcorporationsprojectsdetail"></a>
# **GetCorporationsProjectsDetail**
> CorporationsProjectsDetail GetCorporationsProjectsDetail (long corporationId, Guid projectId, DateOnly xCompatibilityDate, string? ifModifiedSince = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get project details

Get the details of a corporation project.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationsProjectsDetailExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CorporationProjectsApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var projectId = "projectId_example";  // Guid | The ID of the project
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var ifModifiedSince = "ifModifiedSince_example";  // string? | The date the resource was last modified. A 304 will be returned if the resource has not been modified since this date. (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get project details
                CorporationsProjectsDetail result = apiInstance.GetCorporationsProjectsDetail(corporationId, projectId, xCompatibilityDate, ifModifiedSince, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CorporationProjectsApi.GetCorporationsProjectsDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationsProjectsDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get project details
    ApiResponse<CorporationsProjectsDetail> response = apiInstance.GetCorporationsProjectsDetailWithHttpInfo(corporationId, projectId, xCompatibilityDate, ifModifiedSince, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CorporationProjectsApi.GetCorporationsProjectsDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **corporationId** | **long** | The ID of the corporation |  |
| **projectId** | **Guid** | The ID of the project |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **ifModifiedSince** | **string?** | The date the resource was last modified. A 304 will be returned if the resource has not been modified since this date. | [optional]  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**CorporationsProjectsDetail**](CorporationsProjectsDetail.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcorporationsprojectslisting"></a>
# **GetCorporationsProjectsListing**
> CorporationsProjectsListing GetCorporationsProjectsListing (long corporationId, DateOnly xCompatibilityDate, string? after = null, string? before = null, long? limit = null, string? state = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List corporation projects

Listing of all (active) corporation projects.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationsProjectsListingExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CorporationProjectsApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var after = "after_example";  // string? | Return records from after this cursor (mutual exclusive with 'before'). '0' to start from the beginning. (optional) 
            var before = "before_example";  // string? | Return records from before this cursor (mutual exclusive with 'after'). '0' to start from the end. (optional) 
            var limit = 10L;  // long? | The amount of records to retrieve per request. (optional)  (default to 10)
            var state = "All";  // string? | Filter by state (optional)  (default to Active)
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List corporation projects
                CorporationsProjectsListing result = apiInstance.GetCorporationsProjectsListing(corporationId, xCompatibilityDate, after, before, limit, state, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CorporationProjectsApi.GetCorporationsProjectsListing: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationsProjectsListingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List corporation projects
    ApiResponse<CorporationsProjectsListing> response = apiInstance.GetCorporationsProjectsListingWithHttpInfo(corporationId, xCompatibilityDate, after, before, limit, state, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CorporationProjectsApi.GetCorporationsProjectsListingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **corporationId** | **long** | The ID of the corporation |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **after** | **string?** | Return records from after this cursor (mutual exclusive with &#39;before&#39;). &#39;0&#39; to start from the beginning. | [optional]  |
| **before** | **string?** | Return records from before this cursor (mutual exclusive with &#39;after&#39;). &#39;0&#39; to start from the end. | [optional]  |
| **limit** | **long?** | The amount of records to retrieve per request. | [optional] [default to 10] |
| **state** | **string?** | Filter by state | [optional] [default to Active] |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**CorporationsProjectsListing**](CorporationsProjectsListing.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

