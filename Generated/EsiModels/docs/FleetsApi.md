# EveESI.Models.Api.FleetsApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteFleetsFleetIdMembersMemberId**](FleetsApi.md#deletefleetsfleetidmembersmemberid) | **DELETE** /fleets/{fleet_id}/members/{member_id} | Kick fleet member |
| [**DeleteFleetsFleetIdSquadsSquadId**](FleetsApi.md#deletefleetsfleetidsquadssquadid) | **DELETE** /fleets/{fleet_id}/squads/{squad_id} | Delete fleet squad |
| [**DeleteFleetsFleetIdWingsWingId**](FleetsApi.md#deletefleetsfleetidwingswingid) | **DELETE** /fleets/{fleet_id}/wings/{wing_id} | Delete fleet wing |
| [**GetCharactersCharacterIdFleet**](FleetsApi.md#getcharacterscharacteridfleet) | **GET** /characters/{character_id}/fleet | Get character fleet info |
| [**GetFleetsFleetId**](FleetsApi.md#getfleetsfleetid) | **GET** /fleets/{fleet_id} | Get fleet information |
| [**GetFleetsFleetIdMembers**](FleetsApi.md#getfleetsfleetidmembers) | **GET** /fleets/{fleet_id}/members | Get fleet members |
| [**GetFleetsFleetIdWings**](FleetsApi.md#getfleetsfleetidwings) | **GET** /fleets/{fleet_id}/wings | Get fleet wings |
| [**PostFleetsFleetIdMembers**](FleetsApi.md#postfleetsfleetidmembers) | **POST** /fleets/{fleet_id}/members | Create fleet invitation |
| [**PostFleetsFleetIdWings**](FleetsApi.md#postfleetsfleetidwings) | **POST** /fleets/{fleet_id}/wings | Create fleet wing |
| [**PostFleetsFleetIdWingsWingIdSquads**](FleetsApi.md#postfleetsfleetidwingswingidsquads) | **POST** /fleets/{fleet_id}/wings/{wing_id}/squads | Create fleet squad |
| [**PutFleetsFleetId**](FleetsApi.md#putfleetsfleetid) | **PUT** /fleets/{fleet_id} | Update fleet |
| [**PutFleetsFleetIdMembersMemberId**](FleetsApi.md#putfleetsfleetidmembersmemberid) | **PUT** /fleets/{fleet_id}/members/{member_id} | Move fleet member |
| [**PutFleetsFleetIdSquadsSquadId**](FleetsApi.md#putfleetsfleetidsquadssquadid) | **PUT** /fleets/{fleet_id}/squads/{squad_id} | Rename fleet squad |
| [**PutFleetsFleetIdWingsWingId**](FleetsApi.md#putfleetsfleetidwingswingid) | **PUT** /fleets/{fleet_id}/wings/{wing_id} | Rename fleet wing |

<a id="deletefleetsfleetidmembersmemberid"></a>
# **DeleteFleetsFleetIdMembersMemberId**
> void DeleteFleetsFleetIdMembersMemberId (long fleetId, long memberId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Kick fleet member

Kick a fleet member

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class DeleteFleetsFleetIdMembersMemberIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var memberId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Kick fleet member
                apiInstance.DeleteFleetsFleetIdMembersMemberId(fleetId, memberId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.DeleteFleetsFleetIdMembersMemberId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteFleetsFleetIdMembersMemberIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Kick fleet member
    apiInstance.DeleteFleetsFleetIdMembersMemberIdWithHttpInfo(fleetId, memberId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.DeleteFleetsFleetIdMembersMemberIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **memberId** | **long** |  |  |
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
| **204** | Fleet member kicked |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletefleetsfleetidsquadssquadid"></a>
# **DeleteFleetsFleetIdSquadsSquadId**
> void DeleteFleetsFleetIdSquadsSquadId (long fleetId, long squadId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Delete fleet squad

Delete a fleet squad, only empty squads can be deleted

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class DeleteFleetsFleetIdSquadsSquadIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var squadId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Delete fleet squad
                apiInstance.DeleteFleetsFleetIdSquadsSquadId(fleetId, squadId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.DeleteFleetsFleetIdSquadsSquadId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteFleetsFleetIdSquadsSquadIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete fleet squad
    apiInstance.DeleteFleetsFleetIdSquadsSquadIdWithHttpInfo(fleetId, squadId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.DeleteFleetsFleetIdSquadsSquadIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **squadId** | **long** |  |  |
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
| **204** | Squad deleted |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletefleetsfleetidwingswingid"></a>
# **DeleteFleetsFleetIdWingsWingId**
> void DeleteFleetsFleetIdWingsWingId (long fleetId, long wingId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Delete fleet wing

Delete a fleet wing, only empty wings can be deleted. The wing may contain squads, but the squads must be empty

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class DeleteFleetsFleetIdWingsWingIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var wingId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Delete fleet wing
                apiInstance.DeleteFleetsFleetIdWingsWingId(fleetId, wingId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.DeleteFleetsFleetIdWingsWingId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteFleetsFleetIdWingsWingIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete fleet wing
    apiInstance.DeleteFleetsFleetIdWingsWingIdWithHttpInfo(fleetId, wingId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.DeleteFleetsFleetIdWingsWingIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **wingId** | **long** |  |  |
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
| **204** | Wing deleted |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcharacterscharacteridfleet"></a>
# **GetCharactersCharacterIdFleet**
> CharactersCharacterIdFleetGet GetCharactersCharacterIdFleet (long characterId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get character fleet info

Return the fleet ID the character is in, if any.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdFleetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get character fleet info
                CharactersCharacterIdFleetGet result = apiInstance.GetCharactersCharacterIdFleet(characterId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.GetCharactersCharacterIdFleet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdFleetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get character fleet info
    ApiResponse<CharactersCharacterIdFleetGet> response = apiInstance.GetCharactersCharacterIdFleetWithHttpInfo(characterId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.GetCharactersCharacterIdFleetWithHttpInfo: " + e.Message);
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

[**CharactersCharacterIdFleetGet**](CharactersCharacterIdFleetGet.md)

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

<a id="getfleetsfleetid"></a>
# **GetFleetsFleetId**
> FleetsFleetIdGet GetFleetsFleetId (long fleetId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get fleet information

Return details about a fleet

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetFleetsFleetIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get fleet information
                FleetsFleetIdGet result = apiInstance.GetFleetsFleetId(fleetId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.GetFleetsFleetId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFleetsFleetIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get fleet information
    ApiResponse<FleetsFleetIdGet> response = apiInstance.GetFleetsFleetIdWithHttpInfo(fleetId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.GetFleetsFleetIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**FleetsFleetIdGet**](FleetsFleetIdGet.md)

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

<a id="getfleetsfleetidmembers"></a>
# **GetFleetsFleetIdMembers**
> List&lt;FleetsFleetIdMembersGetInner&gt; GetFleetsFleetIdMembers (long fleetId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get fleet members

Return information about fleet members

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetFleetsFleetIdMembersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get fleet members
                List<FleetsFleetIdMembersGetInner> result = apiInstance.GetFleetsFleetIdMembers(fleetId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.GetFleetsFleetIdMembers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFleetsFleetIdMembersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get fleet members
    ApiResponse<List<FleetsFleetIdMembersGetInner>> response = apiInstance.GetFleetsFleetIdMembersWithHttpInfo(fleetId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.GetFleetsFleetIdMembersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;FleetsFleetIdMembersGetInner&gt;**](FleetsFleetIdMembersGetInner.md)

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

<a id="getfleetsfleetidwings"></a>
# **GetFleetsFleetIdWings**
> List&lt;FleetsFleetIdWingsGetInner&gt; GetFleetsFleetIdWings (long fleetId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get fleet wings

Return information about wings in a fleet

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetFleetsFleetIdWingsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get fleet wings
                List<FleetsFleetIdWingsGetInner> result = apiInstance.GetFleetsFleetIdWings(fleetId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.GetFleetsFleetIdWings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetFleetsFleetIdWingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get fleet wings
    ApiResponse<List<FleetsFleetIdWingsGetInner>> response = apiInstance.GetFleetsFleetIdWingsWithHttpInfo(fleetId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.GetFleetsFleetIdWingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;FleetsFleetIdWingsGetInner&gt;**](FleetsFleetIdWingsGetInner.md)

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

<a id="postfleetsfleetidmembers"></a>
# **PostFleetsFleetIdMembers**
> void PostFleetsFleetIdMembers (long fleetId, DateOnly xCompatibilityDate, PostFleetsFleetIdMembersRequest postFleetsFleetIdMembersRequest, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Create fleet invitation

Invite a character into the fleet. If a character has a CSPA charge set it is not possible to invite them to the fleet using ESI

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PostFleetsFleetIdMembersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var postFleetsFleetIdMembersRequest = new PostFleetsFleetIdMembersRequest(); // PostFleetsFleetIdMembersRequest | 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Create fleet invitation
                apiInstance.PostFleetsFleetIdMembers(fleetId, xCompatibilityDate, postFleetsFleetIdMembersRequest, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.PostFleetsFleetIdMembers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PostFleetsFleetIdMembersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create fleet invitation
    apiInstance.PostFleetsFleetIdMembersWithHttpInfo(fleetId, xCompatibilityDate, postFleetsFleetIdMembersRequest, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.PostFleetsFleetIdMembersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **postFleetsFleetIdMembersRequest** | [**PostFleetsFleetIdMembersRequest**](PostFleetsFleetIdMembersRequest.md) |  |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

void (empty response body)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Fleet invitation sent |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="postfleetsfleetidwings"></a>
# **PostFleetsFleetIdWings**
> FleetsFleetIdWingsPost PostFleetsFleetIdWings (long fleetId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Create fleet wing

Create a new wing in a fleet

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PostFleetsFleetIdWingsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Create fleet wing
                FleetsFleetIdWingsPost result = apiInstance.PostFleetsFleetIdWings(fleetId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.PostFleetsFleetIdWings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PostFleetsFleetIdWingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create fleet wing
    ApiResponse<FleetsFleetIdWingsPost> response = apiInstance.PostFleetsFleetIdWingsWithHttpInfo(fleetId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.PostFleetsFleetIdWingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**FleetsFleetIdWingsPost**](FleetsFleetIdWingsPost.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="postfleetsfleetidwingswingidsquads"></a>
# **PostFleetsFleetIdWingsWingIdSquads**
> FleetsFleetIdWingsWingIdSquadsPost PostFleetsFleetIdWingsWingIdSquads (long fleetId, long wingId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Create fleet squad

Create a new squad in a fleet

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PostFleetsFleetIdWingsWingIdSquadsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var wingId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Create fleet squad
                FleetsFleetIdWingsWingIdSquadsPost result = apiInstance.PostFleetsFleetIdWingsWingIdSquads(fleetId, wingId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.PostFleetsFleetIdWingsWingIdSquads: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PostFleetsFleetIdWingsWingIdSquadsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create fleet squad
    ApiResponse<FleetsFleetIdWingsWingIdSquadsPost> response = apiInstance.PostFleetsFleetIdWingsWingIdSquadsWithHttpInfo(fleetId, wingId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.PostFleetsFleetIdWingsWingIdSquadsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **wingId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**FleetsFleetIdWingsWingIdSquadsPost**](FleetsFleetIdWingsWingIdSquadsPost.md)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="putfleetsfleetid"></a>
# **PutFleetsFleetId**
> void PutFleetsFleetId (long fleetId, DateOnly xCompatibilityDate, PutFleetsFleetIdRequest putFleetsFleetIdRequest, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Update fleet

Update settings about a fleet

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PutFleetsFleetIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var putFleetsFleetIdRequest = new PutFleetsFleetIdRequest(); // PutFleetsFleetIdRequest | 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Update fleet
                apiInstance.PutFleetsFleetId(fleetId, xCompatibilityDate, putFleetsFleetIdRequest, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.PutFleetsFleetId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PutFleetsFleetIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update fleet
    apiInstance.PutFleetsFleetIdWithHttpInfo(fleetId, xCompatibilityDate, putFleetsFleetIdRequest, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.PutFleetsFleetIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **putFleetsFleetIdRequest** | [**PutFleetsFleetIdRequest**](PutFleetsFleetIdRequest.md) |  |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

void (empty response body)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Fleet updated |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="putfleetsfleetidmembersmemberid"></a>
# **PutFleetsFleetIdMembersMemberId**
> void PutFleetsFleetIdMembersMemberId (long fleetId, long memberId, DateOnly xCompatibilityDate, PutFleetsFleetIdMembersMemberIdRequest putFleetsFleetIdMembersMemberIdRequest, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Move fleet member

Move a fleet member around

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PutFleetsFleetIdMembersMemberIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var memberId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var putFleetsFleetIdMembersMemberIdRequest = new PutFleetsFleetIdMembersMemberIdRequest(); // PutFleetsFleetIdMembersMemberIdRequest | 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Move fleet member
                apiInstance.PutFleetsFleetIdMembersMemberId(fleetId, memberId, xCompatibilityDate, putFleetsFleetIdMembersMemberIdRequest, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.PutFleetsFleetIdMembersMemberId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PutFleetsFleetIdMembersMemberIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Move fleet member
    apiInstance.PutFleetsFleetIdMembersMemberIdWithHttpInfo(fleetId, memberId, xCompatibilityDate, putFleetsFleetIdMembersMemberIdRequest, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.PutFleetsFleetIdMembersMemberIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **memberId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **putFleetsFleetIdMembersMemberIdRequest** | [**PutFleetsFleetIdMembersMemberIdRequest**](PutFleetsFleetIdMembersMemberIdRequest.md) |  |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

void (empty response body)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Fleet invitation sent |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="putfleetsfleetidsquadssquadid"></a>
# **PutFleetsFleetIdSquadsSquadId**
> void PutFleetsFleetIdSquadsSquadId (long fleetId, long squadId, DateOnly xCompatibilityDate, PutFleetsFleetIdSquadsSquadIdRequest putFleetsFleetIdSquadsSquadIdRequest, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Rename fleet squad

Rename a fleet squad

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PutFleetsFleetIdSquadsSquadIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var squadId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var putFleetsFleetIdSquadsSquadIdRequest = new PutFleetsFleetIdSquadsSquadIdRequest(); // PutFleetsFleetIdSquadsSquadIdRequest | 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Rename fleet squad
                apiInstance.PutFleetsFleetIdSquadsSquadId(fleetId, squadId, xCompatibilityDate, putFleetsFleetIdSquadsSquadIdRequest, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.PutFleetsFleetIdSquadsSquadId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PutFleetsFleetIdSquadsSquadIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rename fleet squad
    apiInstance.PutFleetsFleetIdSquadsSquadIdWithHttpInfo(fleetId, squadId, xCompatibilityDate, putFleetsFleetIdSquadsSquadIdRequest, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.PutFleetsFleetIdSquadsSquadIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **squadId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **putFleetsFleetIdSquadsSquadIdRequest** | [**PutFleetsFleetIdSquadsSquadIdRequest**](PutFleetsFleetIdSquadsSquadIdRequest.md) |  |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

void (empty response body)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Squad renamed |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="putfleetsfleetidwingswingid"></a>
# **PutFleetsFleetIdWingsWingId**
> void PutFleetsFleetIdWingsWingId (long fleetId, long wingId, DateOnly xCompatibilityDate, PutFleetsFleetIdSquadsSquadIdRequest putFleetsFleetIdSquadsSquadIdRequest, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Rename fleet wing

Rename a fleet wing

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PutFleetsFleetIdWingsWingIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new FleetsApi(config);
            var fleetId = 789L;  // long | 
            var wingId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var putFleetsFleetIdSquadsSquadIdRequest = new PutFleetsFleetIdSquadsSquadIdRequest(); // PutFleetsFleetIdSquadsSquadIdRequest | 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Rename fleet wing
                apiInstance.PutFleetsFleetIdWingsWingId(fleetId, wingId, xCompatibilityDate, putFleetsFleetIdSquadsSquadIdRequest, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FleetsApi.PutFleetsFleetIdWingsWingId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PutFleetsFleetIdWingsWingIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rename fleet wing
    apiInstance.PutFleetsFleetIdWingsWingIdWithHttpInfo(fleetId, wingId, xCompatibilityDate, putFleetsFleetIdSquadsSquadIdRequest, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FleetsApi.PutFleetsFleetIdWingsWingIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **fleetId** | **long** |  |  |
| **wingId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **putFleetsFleetIdSquadsSquadIdRequest** | [**PutFleetsFleetIdSquadsSquadIdRequest**](PutFleetsFleetIdSquadsSquadIdRequest.md) |  |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

void (empty response body)

### Authorization

[OAuth2](../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Wing renamed |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

