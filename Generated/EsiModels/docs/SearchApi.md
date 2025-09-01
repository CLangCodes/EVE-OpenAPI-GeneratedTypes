# EveESI.Models.Api.SearchApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetCharactersCharacterIdSearch**](SearchApi.md#getcharacterscharacteridsearch) | **GET** /characters/{character_id}/search | Search on a string |

<a id="getcharacterscharacteridsearch"></a>
# **GetCharactersCharacterIdSearch**
> CharactersCharacterIdSearchGet GetCharactersCharacterIdSearch (List<string> categories, long characterId, string search, DateOnly xCompatibilityDate, bool? strict = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Search on a string

Search for entities that match a given sub-string.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdSearchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SearchApi(config);
            var categories = new List<string>(); // List<string> | 
            var characterId = 789L;  // long | The ID of the character
            var search = "search_example";  // string | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var strict = false;  // bool? |  (optional)  (default to false)
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Search on a string
                CharactersCharacterIdSearchGet result = apiInstance.GetCharactersCharacterIdSearch(categories, characterId, search, xCompatibilityDate, strict, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SearchApi.GetCharactersCharacterIdSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search on a string
    ApiResponse<CharactersCharacterIdSearchGet> response = apiInstance.GetCharactersCharacterIdSearchWithHttpInfo(categories, characterId, search, xCompatibilityDate, strict, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SearchApi.GetCharactersCharacterIdSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **categories** | [**List&lt;string&gt;**](string.md) |  |  |
| **characterId** | **long** | The ID of the character |  |
| **search** | **string** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **strict** | **bool?** |  | [optional] [default to false] |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**CharactersCharacterIdSearchGet**](CharactersCharacterIdSearchGet.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  * Cache-Control -  <br>  * Content-Language -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

