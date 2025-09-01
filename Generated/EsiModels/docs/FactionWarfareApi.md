# EveESI.Models.Api.FactionWarfareApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetCharactersCharacterIdFwStats**](FactionWarfareApi.md#getcharacterscharacteridfwstats) | **GET** /characters/{character_id}/fw/stats | Overview of a character involved in faction warfare |
| [**GetCorporationsCorporationIdFwStats**](FactionWarfareApi.md#getcorporationscorporationidfwstats) | **GET** /corporations/{corporation_id}/fw/stats | Overview of a corporation involved in faction warfare |
| [**GetFwLeaderboards**](FactionWarfareApi.md#getfwleaderboards) | **GET** /fw/leaderboards | List of the top factions in faction warfare |
| [**GetFwLeaderboardsCharacters**](FactionWarfareApi.md#getfwleaderboardscharacters) | **GET** /fw/leaderboards/characters | List of the top pilots in faction warfare |
| [**GetFwLeaderboardsCorporations**](FactionWarfareApi.md#getfwleaderboardscorporations) | **GET** /fw/leaderboards/corporations | List of the top corporations in faction warfare |
| [**GetFwStats**](FactionWarfareApi.md#getfwstats) | **GET** /fw/stats | An overview of statistics about factions involved in faction warfare |
| [**GetFwSystems**](FactionWarfareApi.md#getfwsystems) | **GET** /fw/systems | Ownership of faction warfare systems |
| [**GetFwWars**](FactionWarfareApi.md#getfwwars) | **GET** /fw/wars | Data about which NPC factions are at war |

<a id="getcharacterscharacteridfwstats"></a>
# **GetCharactersCharacterIdFwStats**
> CharactersCharacterIdFwStatsGet GetCharactersCharacterIdFwStats (long characterId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Overview of a character involved in faction warfare

Statistical overview of a character involved in faction warfare  This route expires daily at 11:05

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdFwStatsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FactionWarfareApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Overview of a character involved in faction warfare
                CharactersCharacterIdFwStatsGet result = apiInstance.GetCharactersCharacterIdFwStats(characterId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FactionWarfareApi.GetCharactersCharacterIdFwStats: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdFwStatsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Overview of a character involved in faction warfare
    ApiResponse<CharactersCharacterIdFwStatsGet> response = apiInstance.GetCharactersCharacterIdFwStatsWithHttpInfo(characterId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FactionWarfareApi.GetCharactersCharacterIdFwStatsWithHttpInfo: " + e.Message);
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

[**CharactersCharacterIdFwStatsGet**](CharactersCharacterIdFwStatsGet.md)

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

<a id="getcorporationscorporationidfwstats"></a>
# **GetCorporationsCorporationIdFwStats**
> CorporationsCorporationIdFwStatsGet GetCorporationsCorporationIdFwStats (long corporationId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Overview of a corporation involved in faction warfare

Statistics about a corporation involved in faction warfare  This route expires daily at 11:05

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationsCorporationIdFwStatsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FactionWarfareApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Overview of a corporation involved in faction warfare
                CorporationsCorporationIdFwStatsGet result = apiInstance.GetCorporationsCorporationIdFwStats(corporationId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FactionWarfareApi.GetCorporationsCorporationIdFwStats: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationsCorporationIdFwStatsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Overview of a corporation involved in faction warfare
    ApiResponse<CorporationsCorporationIdFwStatsGet> response = apiInstance.GetCorporationsCorporationIdFwStatsWithHttpInfo(corporationId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FactionWarfareApi.GetCorporationsCorporationIdFwStatsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **corporationId** | **long** | The ID of the corporation |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**CorporationsCorporationIdFwStatsGet**](CorporationsCorporationIdFwStatsGet.md)

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

<a id="getfwleaderboards"></a>
# **GetFwLeaderboards**
> FwLeaderboardsGet GetFwLeaderboards (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List of the top factions in faction warfare

Top 4 leaderboard of factions for kills and victory points separated by total, last week and yesterday  This route expires daily at 11:05

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetFwLeaderboardsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new FactionWarfareApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List of the top factions in faction warfare
                FwLeaderboardsGet result = apiInstance.GetFwLeaderboards(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FactionWarfareApi.GetFwLeaderboards: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFwLeaderboardsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List of the top factions in faction warfare
    ApiResponse<FwLeaderboardsGet> response = apiInstance.GetFwLeaderboardsWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FactionWarfareApi.GetFwLeaderboardsWithHttpInfo: " + e.Message);
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

[**FwLeaderboardsGet**](FwLeaderboardsGet.md)

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

<a id="getfwleaderboardscharacters"></a>
# **GetFwLeaderboardsCharacters**
> FwLeaderboardsCharactersGet GetFwLeaderboardsCharacters (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List of the top pilots in faction warfare

Top 100 leaderboard of pilots for kills and victory points separated by total, last week and yesterday  This route expires daily at 11:05

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetFwLeaderboardsCharactersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new FactionWarfareApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List of the top pilots in faction warfare
                FwLeaderboardsCharactersGet result = apiInstance.GetFwLeaderboardsCharacters(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FactionWarfareApi.GetFwLeaderboardsCharacters: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFwLeaderboardsCharactersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List of the top pilots in faction warfare
    ApiResponse<FwLeaderboardsCharactersGet> response = apiInstance.GetFwLeaderboardsCharactersWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FactionWarfareApi.GetFwLeaderboardsCharactersWithHttpInfo: " + e.Message);
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

[**FwLeaderboardsCharactersGet**](FwLeaderboardsCharactersGet.md)

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

<a id="getfwleaderboardscorporations"></a>
# **GetFwLeaderboardsCorporations**
> FwLeaderboardsCorporationsGet GetFwLeaderboardsCorporations (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List of the top corporations in faction warfare

Top 10 leaderboard of corporations for kills and victory points separated by total, last week and yesterday  This route expires daily at 11:05

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetFwLeaderboardsCorporationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new FactionWarfareApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List of the top corporations in faction warfare
                FwLeaderboardsCorporationsGet result = apiInstance.GetFwLeaderboardsCorporations(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FactionWarfareApi.GetFwLeaderboardsCorporations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFwLeaderboardsCorporationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List of the top corporations in faction warfare
    ApiResponse<FwLeaderboardsCorporationsGet> response = apiInstance.GetFwLeaderboardsCorporationsWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FactionWarfareApi.GetFwLeaderboardsCorporationsWithHttpInfo: " + e.Message);
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

[**FwLeaderboardsCorporationsGet**](FwLeaderboardsCorporationsGet.md)

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

<a id="getfwstats"></a>
# **GetFwStats**
> List&lt;FwStatsGetInner&gt; GetFwStats (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

An overview of statistics about factions involved in faction warfare

Statistical overviews of factions involved in faction warfare  This route expires daily at 11:05

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetFwStatsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new FactionWarfareApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // An overview of statistics about factions involved in faction warfare
                List<FwStatsGetInner> result = apiInstance.GetFwStats(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FactionWarfareApi.GetFwStats: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFwStatsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // An overview of statistics about factions involved in faction warfare
    ApiResponse<List<FwStatsGetInner>> response = apiInstance.GetFwStatsWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FactionWarfareApi.GetFwStatsWithHttpInfo: " + e.Message);
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

[**List&lt;FwStatsGetInner&gt;**](FwStatsGetInner.md)

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

<a id="getfwsystems"></a>
# **GetFwSystems**
> List&lt;FwSystemsGetInner&gt; GetFwSystems (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Ownership of faction warfare systems

An overview of the current ownership of faction warfare solar systems

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetFwSystemsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new FactionWarfareApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Ownership of faction warfare systems
                List<FwSystemsGetInner> result = apiInstance.GetFwSystems(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FactionWarfareApi.GetFwSystems: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFwSystemsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ownership of faction warfare systems
    ApiResponse<List<FwSystemsGetInner>> response = apiInstance.GetFwSystemsWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FactionWarfareApi.GetFwSystemsWithHttpInfo: " + e.Message);
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

[**List&lt;FwSystemsGetInner&gt;**](FwSystemsGetInner.md)

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

<a id="getfwwars"></a>
# **GetFwWars**
> List&lt;FwWarsGetInner&gt; GetFwWars (DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Data about which NPC factions are at war

Data about which NPC factions are at war  This route expires daily at 11:05

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetFwWarsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            var apiInstance = new FactionWarfareApi(config);
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Data about which NPC factions are at war
                List<FwWarsGetInner> result = apiInstance.GetFwWars(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FactionWarfareApi.GetFwWars: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFwWarsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Data about which NPC factions are at war
    ApiResponse<List<FwWarsGetInner>> response = apiInstance.GetFwWarsWithHttpInfo(xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FactionWarfareApi.GetFwWarsWithHttpInfo: " + e.Message);
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

[**List&lt;FwWarsGetInner&gt;**](FwWarsGetInner.md)

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

