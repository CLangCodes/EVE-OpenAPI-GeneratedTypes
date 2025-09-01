# EveESI.Models.Api.AssetsApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetCharactersCharacterIdAssets**](AssetsApi.md#getcharacterscharacteridassets) | **GET** /characters/{character_id}/assets | Get character assets |
| [**GetCorporationsCorporationIdAssets**](AssetsApi.md#getcorporationscorporationidassets) | **GET** /corporations/{corporation_id}/assets | Get corporation assets |
| [**PostCharactersCharacterIdAssetsLocations**](AssetsApi.md#postcharacterscharacteridassetslocations) | **POST** /characters/{character_id}/assets/locations | Get character asset locations |
| [**PostCharactersCharacterIdAssetsNames**](AssetsApi.md#postcharacterscharacteridassetsnames) | **POST** /characters/{character_id}/assets/names | Get character asset names |
| [**PostCorporationsCorporationIdAssetsLocations**](AssetsApi.md#postcorporationscorporationidassetslocations) | **POST** /corporations/{corporation_id}/assets/locations | Get corporation asset locations |
| [**PostCorporationsCorporationIdAssetsNames**](AssetsApi.md#postcorporationscorporationidassetsnames) | **POST** /corporations/{corporation_id}/assets/names | Get corporation asset names |

<a id="getcharacterscharacteridassets"></a>
# **GetCharactersCharacterIdAssets**
> List&lt;CharactersCharacterIdAssetsGetInner&gt; GetCharactersCharacterIdAssets (long characterId, DateOnly xCompatibilityDate, int? page = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get character assets

Return a list of the characters assets

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdAssetsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new AssetsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var page = 56;  // int? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get character assets
                List<CharactersCharacterIdAssetsGetInner> result = apiInstance.GetCharactersCharacterIdAssets(characterId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AssetsApi.GetCharactersCharacterIdAssets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdAssetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get character assets
    ApiResponse<List<CharactersCharacterIdAssetsGetInner>> response = apiInstance.GetCharactersCharacterIdAssetsWithHttpInfo(characterId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AssetsApi.GetCharactersCharacterIdAssetsWithHttpInfo: " + e.Message);
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

[**List&lt;CharactersCharacterIdAssetsGetInner&gt;**](CharactersCharacterIdAssetsGetInner.md)

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

<a id="getcorporationscorporationidassets"></a>
# **GetCorporationsCorporationIdAssets**
> List&lt;CorporationsCorporationIdAssetsGetInner&gt; GetCorporationsCorporationIdAssets (long corporationId, DateOnly xCompatibilityDate, int? page = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get corporation assets

Return a list of the corporation assets

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationsCorporationIdAssetsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new AssetsApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var page = 56;  // int? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get corporation assets
                List<CorporationsCorporationIdAssetsGetInner> result = apiInstance.GetCorporationsCorporationIdAssets(corporationId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AssetsApi.GetCorporationsCorporationIdAssets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationsCorporationIdAssetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get corporation assets
    ApiResponse<List<CorporationsCorporationIdAssetsGetInner>> response = apiInstance.GetCorporationsCorporationIdAssetsWithHttpInfo(corporationId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AssetsApi.GetCorporationsCorporationIdAssetsWithHttpInfo: " + e.Message);
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

[**List&lt;CorporationsCorporationIdAssetsGetInner&gt;**](CorporationsCorporationIdAssetsGetInner.md)

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

<a id="postcharacterscharacteridassetslocations"></a>
# **PostCharactersCharacterIdAssetsLocations**
> List&lt;CharactersCharacterIdAssetsLocationsPostInner&gt; PostCharactersCharacterIdAssetsLocations (long characterId, DateOnly xCompatibilityDate, List<long> requestBody, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get character asset locations

Return locations for a set of item ids, which you can get from character assets endpoint. Coordinates for items in hangars or stations are set to (0,0,0)

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PostCharactersCharacterIdAssetsLocationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new AssetsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var requestBody = new List<long>(); // List<long> | 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get character asset locations
                List<CharactersCharacterIdAssetsLocationsPostInner> result = apiInstance.PostCharactersCharacterIdAssetsLocations(characterId, xCompatibilityDate, requestBody, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AssetsApi.PostCharactersCharacterIdAssetsLocations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PostCharactersCharacterIdAssetsLocationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get character asset locations
    ApiResponse<List<CharactersCharacterIdAssetsLocationsPostInner>> response = apiInstance.PostCharactersCharacterIdAssetsLocationsWithHttpInfo(characterId, xCompatibilityDate, requestBody, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AssetsApi.PostCharactersCharacterIdAssetsLocationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **requestBody** | [**List&lt;long&gt;**](long.md) |  |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CharactersCharacterIdAssetsLocationsPostInner&gt;**](CharactersCharacterIdAssetsLocationsPostInner.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="postcharacterscharacteridassetsnames"></a>
# **PostCharactersCharacterIdAssetsNames**
> List&lt;CharactersCharacterIdAssetsNamesPostInner&gt; PostCharactersCharacterIdAssetsNames (long characterId, DateOnly xCompatibilityDate, List<long> requestBody, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get character asset names

Return names for a set of item ids, which you can get from character assets endpoint. Typically used for items that can customize names, like containers or ships.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PostCharactersCharacterIdAssetsNamesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new AssetsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var requestBody = new List<long>(); // List<long> | 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get character asset names
                List<CharactersCharacterIdAssetsNamesPostInner> result = apiInstance.PostCharactersCharacterIdAssetsNames(characterId, xCompatibilityDate, requestBody, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AssetsApi.PostCharactersCharacterIdAssetsNames: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PostCharactersCharacterIdAssetsNamesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get character asset names
    ApiResponse<List<CharactersCharacterIdAssetsNamesPostInner>> response = apiInstance.PostCharactersCharacterIdAssetsNamesWithHttpInfo(characterId, xCompatibilityDate, requestBody, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AssetsApi.PostCharactersCharacterIdAssetsNamesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **requestBody** | [**List&lt;long&gt;**](long.md) |  |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CharactersCharacterIdAssetsNamesPostInner&gt;**](CharactersCharacterIdAssetsNamesPostInner.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="postcorporationscorporationidassetslocations"></a>
# **PostCorporationsCorporationIdAssetsLocations**
> List&lt;CharactersCharacterIdAssetsLocationsPostInner&gt; PostCorporationsCorporationIdAssetsLocations (long corporationId, DateOnly xCompatibilityDate, List<long> requestBody, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get corporation asset locations

Return locations for a set of item ids, which you can get from corporation assets endpoint. Coordinates for items in hangars or stations are set to (0,0,0)

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PostCorporationsCorporationIdAssetsLocationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new AssetsApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var requestBody = new List<long>(); // List<long> | 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get corporation asset locations
                List<CharactersCharacterIdAssetsLocationsPostInner> result = apiInstance.PostCorporationsCorporationIdAssetsLocations(corporationId, xCompatibilityDate, requestBody, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AssetsApi.PostCorporationsCorporationIdAssetsLocations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PostCorporationsCorporationIdAssetsLocationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get corporation asset locations
    ApiResponse<List<CharactersCharacterIdAssetsLocationsPostInner>> response = apiInstance.PostCorporationsCorporationIdAssetsLocationsWithHttpInfo(corporationId, xCompatibilityDate, requestBody, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AssetsApi.PostCorporationsCorporationIdAssetsLocationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **corporationId** | **long** | The ID of the corporation |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **requestBody** | [**List&lt;long&gt;**](long.md) |  |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CharactersCharacterIdAssetsLocationsPostInner&gt;**](CharactersCharacterIdAssetsLocationsPostInner.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="postcorporationscorporationidassetsnames"></a>
# **PostCorporationsCorporationIdAssetsNames**
> List&lt;CharactersCharacterIdAssetsNamesPostInner&gt; PostCorporationsCorporationIdAssetsNames (long corporationId, DateOnly xCompatibilityDate, List<long> requestBody, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get corporation asset names

Return names for a set of item ids, which you can get from corporation assets endpoint. Only valid for items that can customize names, like containers or ships

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PostCorporationsCorporationIdAssetsNamesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new AssetsApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var requestBody = new List<long>(); // List<long> | 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get corporation asset names
                List<CharactersCharacterIdAssetsNamesPostInner> result = apiInstance.PostCorporationsCorporationIdAssetsNames(corporationId, xCompatibilityDate, requestBody, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AssetsApi.PostCorporationsCorporationIdAssetsNames: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PostCorporationsCorporationIdAssetsNamesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get corporation asset names
    ApiResponse<List<CharactersCharacterIdAssetsNamesPostInner>> response = apiInstance.PostCorporationsCorporationIdAssetsNamesWithHttpInfo(corporationId, xCompatibilityDate, requestBody, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AssetsApi.PostCorporationsCorporationIdAssetsNamesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **corporationId** | **long** | The ID of the corporation |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **requestBody** | [**List&lt;long&gt;**](long.md) |  |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CharactersCharacterIdAssetsNamesPostInner&gt;**](CharactersCharacterIdAssetsNamesPostInner.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

