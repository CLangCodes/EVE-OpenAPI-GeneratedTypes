# EveESI.Models.Api.FittingsApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteCharactersCharacterIdFittingsFittingId**](FittingsApi.md#deletecharacterscharacteridfittingsfittingid) | **DELETE** /characters/{character_id}/fittings/{fitting_id} | Delete fitting |
| [**GetCharactersCharacterIdFittings**](FittingsApi.md#getcharacterscharacteridfittings) | **GET** /characters/{character_id}/fittings | Get fittings |
| [**PostCharactersCharacterIdFittings**](FittingsApi.md#postcharacterscharacteridfittings) | **POST** /characters/{character_id}/fittings | Create fitting |

<a id="deletecharacterscharacteridfittingsfittingid"></a>
# **DeleteCharactersCharacterIdFittingsFittingId**
> void DeleteCharactersCharacterIdFittingsFittingId (long characterId, long fittingId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Delete fitting

Delete a fitting from a character

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class DeleteCharactersCharacterIdFittingsFittingIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FittingsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var fittingId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Delete fitting
                apiInstance.DeleteCharactersCharacterIdFittingsFittingId(characterId, fittingId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FittingsApi.DeleteCharactersCharacterIdFittingsFittingId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCharactersCharacterIdFittingsFittingIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete fitting
    apiInstance.DeleteCharactersCharacterIdFittingsFittingIdWithHttpInfo(characterId, fittingId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FittingsApi.DeleteCharactersCharacterIdFittingsFittingIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **fittingId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

void (empty response body)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Fitting deleted |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcharacterscharacteridfittings"></a>
# **GetCharactersCharacterIdFittings**
> List&lt;CharactersCharacterIdFittingsGetInner&gt; GetCharactersCharacterIdFittings (long characterId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get fittings

Return fittings of a character

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdFittingsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FittingsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get fittings
                List<CharactersCharacterIdFittingsGetInner> result = apiInstance.GetCharactersCharacterIdFittings(characterId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FittingsApi.GetCharactersCharacterIdFittings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdFittingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get fittings
    ApiResponse<List<CharactersCharacterIdFittingsGetInner>> response = apiInstance.GetCharactersCharacterIdFittingsWithHttpInfo(characterId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FittingsApi.GetCharactersCharacterIdFittingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CharactersCharacterIdFittingsGetInner&gt;**](CharactersCharacterIdFittingsGetInner.md)

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

<a id="postcharacterscharacteridfittings"></a>
# **PostCharactersCharacterIdFittings**
> CharactersCharacterIdFittingsPost PostCharactersCharacterIdFittings (long characterId, DateOnly xCompatibilityDate, PostCharactersCharacterIdFittingsRequest postCharactersCharacterIdFittingsRequest, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Create fitting

Save a new fitting for a character

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PostCharactersCharacterIdFittingsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FittingsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var postCharactersCharacterIdFittingsRequest = new PostCharactersCharacterIdFittingsRequest(); // PostCharactersCharacterIdFittingsRequest | 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Create fitting
                CharactersCharacterIdFittingsPost result = apiInstance.PostCharactersCharacterIdFittings(characterId, xCompatibilityDate, postCharactersCharacterIdFittingsRequest, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FittingsApi.PostCharactersCharacterIdFittings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PostCharactersCharacterIdFittingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create fitting
    ApiResponse<CharactersCharacterIdFittingsPost> response = apiInstance.PostCharactersCharacterIdFittingsWithHttpInfo(characterId, xCompatibilityDate, postCharactersCharacterIdFittingsRequest, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FittingsApi.PostCharactersCharacterIdFittingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **postCharactersCharacterIdFittingsRequest** | [**PostCharactersCharacterIdFittingsRequest**](PostCharactersCharacterIdFittingsRequest.md) |  |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**CharactersCharacterIdFittingsPost**](CharactersCharacterIdFittingsPost.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

