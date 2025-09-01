# EveESI.Models.Api.IndustryApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetCharactersCharacterIdIndustryJobs**](IndustryApi.md#getcharacterscharacteridindustryjobs) | **GET** /characters/{character_id}/industry/jobs | List character industry jobs |
| [**GetCharactersCharacterIdMining**](IndustryApi.md#getcharacterscharacteridmining) | **GET** /characters/{character_id}/mining | Character mining ledger |
| [**GetCorporationCorporationIdMiningExtractions**](IndustryApi.md#getcorporationcorporationidminingextractions) | **GET** /corporation/{corporation_id}/mining/extractions | Moon extraction timers |
| [**GetCorporationCorporationIdMiningObservers**](IndustryApi.md#getcorporationcorporationidminingobservers) | **GET** /corporation/{corporation_id}/mining/observers | Corporation mining observers |
| [**GetCorporationCorporationIdMiningObserversObserverId**](IndustryApi.md#getcorporationcorporationidminingobserversobserverid) | **GET** /corporation/{corporation_id}/mining/observers/{observer_id} | Observed corporation mining |
| [**GetCorporationsCorporationIdIndustryJobs**](IndustryApi.md#getcorporationscorporationidindustryjobs) | **GET** /corporations/{corporation_id}/industry/jobs | List corporation industry jobs |
| [**GetIndustryFacilities**](IndustryApi.md#getindustryfacilities) | **GET** /industry/facilities | List industry facilities |
| [**GetIndustrySystems**](IndustryApi.md#getindustrysystems) | **GET** /industry/systems | List solar system cost indices |

<a id="getcharacterscharacteridindustryjobs"></a>
# **GetCharactersCharacterIdIndustryJobs**
> List&lt;CharactersCharacterIdIndustryJobsGetInner&gt; GetCharactersCharacterIdIndustryJobs (long characterId, DateOnly xCompatibilityDate, bool? includeCompleted = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List character industry jobs

List industry jobs placed by a character

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdIndustryJobsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new IndustryApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var includeCompleted = true;  // bool? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List character industry jobs
                List<CharactersCharacterIdIndustryJobsGetInner> result = apiInstance.GetCharactersCharacterIdIndustryJobs(characterId, xCompatibilityDate, includeCompleted, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IndustryApi.GetCharactersCharacterIdIndustryJobs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdIndustryJobsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List character industry jobs
    ApiResponse<List<CharactersCharacterIdIndustryJobsGetInner>> response = apiInstance.GetCharactersCharacterIdIndustryJobsWithHttpInfo(characterId, xCompatibilityDate, includeCompleted, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IndustryApi.GetCharactersCharacterIdIndustryJobsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **includeCompleted** | **bool?** |  | [optional]  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CharactersCharacterIdIndustryJobsGetInner&gt;**](CharactersCharacterIdIndustryJobsGetInner.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcharacterscharacteridmining"></a>
# **GetCharactersCharacterIdMining**
> List&lt;CharactersCharacterIdMiningGetInner&gt; GetCharactersCharacterIdMining (long characterId, DateOnly xCompatibilityDate, int? page = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Character mining ledger

Paginated record of all mining done by a character for the past 30 days

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdMiningExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new IndustryApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var page = 56;  // int? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Character mining ledger
                List<CharactersCharacterIdMiningGetInner> result = apiInstance.GetCharactersCharacterIdMining(characterId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IndustryApi.GetCharactersCharacterIdMining: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdMiningWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Character mining ledger
    ApiResponse<List<CharactersCharacterIdMiningGetInner>> response = apiInstance.GetCharactersCharacterIdMiningWithHttpInfo(characterId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IndustryApi.GetCharactersCharacterIdMiningWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **page** | **int?** |  | [optional]  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CharactersCharacterIdMiningGetInner&gt;**](CharactersCharacterIdMiningGetInner.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  * X-Pages - The total number of pages in the result set. <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcorporationcorporationidminingextractions"></a>
# **GetCorporationCorporationIdMiningExtractions**
> List&lt;CorporationCorporationIdMiningExtractionsGetInner&gt; GetCorporationCorporationIdMiningExtractions (long corporationId, DateOnly xCompatibilityDate, int? page = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Moon extraction timers

Extraction timers for all moon chunks being extracted by refineries belonging to a corporation.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationCorporationIdMiningExtractionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new IndustryApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var page = 56;  // int? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Moon extraction timers
                List<CorporationCorporationIdMiningExtractionsGetInner> result = apiInstance.GetCorporationCorporationIdMiningExtractions(corporationId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IndustryApi.GetCorporationCorporationIdMiningExtractions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationCorporationIdMiningExtractionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Moon extraction timers
    ApiResponse<List<CorporationCorporationIdMiningExtractionsGetInner>> response = apiInstance.GetCorporationCorporationIdMiningExtractionsWithHttpInfo(corporationId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IndustryApi.GetCorporationCorporationIdMiningExtractionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **corporationId** | **long** | The ID of the corporation |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **page** | **int?** |  | [optional]  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CorporationCorporationIdMiningExtractionsGetInner&gt;**](CorporationCorporationIdMiningExtractionsGetInner.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  * X-Pages - The total number of pages in the result set. <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcorporationcorporationidminingobservers"></a>
# **GetCorporationCorporationIdMiningObservers**
> List&lt;CorporationCorporationIdMiningObserversGetInner&gt; GetCorporationCorporationIdMiningObservers (long corporationId, DateOnly xCompatibilityDate, int? page = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Corporation mining observers

Paginated list of all entities capable of observing and recording mining for a corporation

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationCorporationIdMiningObserversExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new IndustryApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var page = 56;  // int? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Corporation mining observers
                List<CorporationCorporationIdMiningObserversGetInner> result = apiInstance.GetCorporationCorporationIdMiningObservers(corporationId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IndustryApi.GetCorporationCorporationIdMiningObservers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationCorporationIdMiningObserversWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Corporation mining observers
    ApiResponse<List<CorporationCorporationIdMiningObserversGetInner>> response = apiInstance.GetCorporationCorporationIdMiningObserversWithHttpInfo(corporationId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IndustryApi.GetCorporationCorporationIdMiningObserversWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **corporationId** | **long** | The ID of the corporation |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **page** | **int?** |  | [optional]  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CorporationCorporationIdMiningObserversGetInner&gt;**](CorporationCorporationIdMiningObserversGetInner.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  * X-Pages - The total number of pages in the result set. <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcorporationcorporationidminingobserversobserverid"></a>
# **GetCorporationCorporationIdMiningObserversObserverId**
> List&lt;CorporationCorporationIdMiningObserversObserverIdGetInner&gt; GetCorporationCorporationIdMiningObserversObserverId (long corporationId, long observerId, DateOnly xCompatibilityDate, int? page = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Observed corporation mining

Paginated record of all mining seen by an observer

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationCorporationIdMiningObserversObserverIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new IndustryApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var observerId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var page = 56;  // int? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Observed corporation mining
                List<CorporationCorporationIdMiningObserversObserverIdGetInner> result = apiInstance.GetCorporationCorporationIdMiningObserversObserverId(corporationId, observerId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IndustryApi.GetCorporationCorporationIdMiningObserversObserverId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationCorporationIdMiningObserversObserverIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Observed corporation mining
    ApiResponse<List<CorporationCorporationIdMiningObserversObserverIdGetInner>> response = apiInstance.GetCorporationCorporationIdMiningObserversObserverIdWithHttpInfo(corporationId, observerId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IndustryApi.GetCorporationCorporationIdMiningObserversObserverIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **corporationId** | **long** | The ID of the corporation |  |
| **observerId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **page** | **int?** |  | [optional]  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CorporationCorporationIdMiningObserversObserverIdGetInner&gt;**](CorporationCorporationIdMiningObserversObserverIdGetInner.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  * X-Pages - The total number of pages in the result set. <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcorporationscorporationidindustryjobs"></a>
# **GetCorporationsCorporationIdIndustryJobs**
> List&lt;CorporationsCorporationIdIndustryJobsGetInner&gt; GetCorporationsCorporationIdIndustryJobs (long corporationId, DateOnly xCompatibilityDate, bool? includeCompleted = null, int? page = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List corporation industry jobs

List industry jobs run by a corporation

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationsCorporationIdIndustryJobsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new IndustryApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var includeCompleted = false;  // bool? |  (optional)  (default to false)
            var page = 56;  // int? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List corporation industry jobs
                List<CorporationsCorporationIdIndustryJobsGetInner> result = apiInstance.GetCorporationsCorporationIdIndustryJobs(corporationId, xCompatibilityDate, includeCompleted, page, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IndustryApi.GetCorporationsCorporationIdIndustryJobs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationsCorporationIdIndustryJobsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List corporation industry jobs
    ApiResponse<List<CorporationsCorporationIdIndustryJobsGetInner>> response = apiInstance.GetCorporationsCorporationIdIndustryJobsWithHttpInfo(corporationId, xCompatibilityDate, includeCompleted, page, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IndustryApi.GetCorporationsCorporationIdIndustryJobsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **corporationId** | **long** | The ID of the corporation |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **includeCompleted** | **bool?** |  | [optional] [default to false] |
| **page** | **int?** |  | [optional]  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CorporationsCorporationIdIndustryJobsGetInner&gt;**](CorporationsCorporationIdIndustryJobsGetInner.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  * X-Pages - The total number of pages in the result set. <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getindustryfacilities"></a>
# **GetIndustryFacilities**
> List&lt;IndustryFacilitiesGetInner&gt; GetIndustryFacilities (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List industry facilities

Return a list of industry facilities

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetIndustryFacilitiesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new IndustryApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List industry facilities
                List<IndustryFacilitiesGetInner> result = apiInstance.GetIndustryFacilities(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IndustryApi.GetIndustryFacilities: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetIndustryFacilitiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List industry facilities
    ApiResponse<List<IndustryFacilitiesGetInner>> response = apiInstance.GetIndustryFacilitiesWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IndustryApi.GetIndustryFacilitiesWithHttpInfo: " + e.Message);
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

[**List&lt;IndustryFacilitiesGetInner&gt;**](IndustryFacilitiesGetInner.md)

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

<a id="getindustrysystems"></a>
# **GetIndustrySystems**
> List&lt;IndustrySystemsGetInner&gt; GetIndustrySystems (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List solar system cost indices

Return cost indices for solar systems

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetIndustrySystemsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new IndustryApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List solar system cost indices
                List<IndustrySystemsGetInner> result = apiInstance.GetIndustrySystems(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IndustryApi.GetIndustrySystems: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetIndustrySystemsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List solar system cost indices
    ApiResponse<List<IndustrySystemsGetInner>> response = apiInstance.GetIndustrySystemsWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IndustryApi.GetIndustrySystemsWithHttpInfo: " + e.Message);
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

[**List&lt;IndustrySystemsGetInner&gt;**](IndustrySystemsGetInner.md)

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

