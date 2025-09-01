# EveESI.Models.Api.ContactsApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteCharactersCharacterIdContacts**](ContactsApi.md#deletecharacterscharacteridcontacts) | **DELETE** /characters/{character_id}/contacts | Delete contacts |
| [**GetAlliancesAllianceIdContacts**](ContactsApi.md#getalliancesallianceidcontacts) | **GET** /alliances/{alliance_id}/contacts | Get alliance contacts |
| [**GetAlliancesAllianceIdContactsLabels**](ContactsApi.md#getalliancesallianceidcontactslabels) | **GET** /alliances/{alliance_id}/contacts/labels | Get alliance contact labels |
| [**GetCharactersCharacterIdContacts**](ContactsApi.md#getcharacterscharacteridcontacts) | **GET** /characters/{character_id}/contacts | Get contacts |
| [**GetCharactersCharacterIdContactsLabels**](ContactsApi.md#getcharacterscharacteridcontactslabels) | **GET** /characters/{character_id}/contacts/labels | Get contact labels |
| [**GetCorporationsCorporationIdContacts**](ContactsApi.md#getcorporationscorporationidcontacts) | **GET** /corporations/{corporation_id}/contacts | Get corporation contacts |
| [**GetCorporationsCorporationIdContactsLabels**](ContactsApi.md#getcorporationscorporationidcontactslabels) | **GET** /corporations/{corporation_id}/contacts/labels | Get corporation contact labels |
| [**PostCharactersCharacterIdContacts**](ContactsApi.md#postcharacterscharacteridcontacts) | **POST** /characters/{character_id}/contacts | Add contacts |
| [**PutCharactersCharacterIdContacts**](ContactsApi.md#putcharacterscharacteridcontacts) | **PUT** /characters/{character_id}/contacts | Edit contacts |

<a id="deletecharacterscharacteridcontacts"></a>
# **DeleteCharactersCharacterIdContacts**
> void DeleteCharactersCharacterIdContacts (long characterId, List<long> contactIds, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Delete contacts

Bulk delete contacts

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class DeleteCharactersCharacterIdContactsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ContactsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var contactIds = new List<long>(); // List<long> | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Delete contacts
                apiInstance.DeleteCharactersCharacterIdContacts(characterId, contactIds, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContactsApi.DeleteCharactersCharacterIdContacts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteCharactersCharacterIdContactsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete contacts
    apiInstance.DeleteCharactersCharacterIdContactsWithHttpInfo(characterId, contactIds, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContactsApi.DeleteCharactersCharacterIdContactsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **contactIds** | [**List&lt;long&gt;**](long.md) |  |  |
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
| **204** | Contacts deleted |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getalliancesallianceidcontacts"></a>
# **GetAlliancesAllianceIdContacts**
> List&lt;AlliancesAllianceIdContactsGetInner&gt; GetAlliancesAllianceIdContacts (long allianceId, DateOnly xCompatibilityDate, int? page = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get alliance contacts

Return contacts of an alliance

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetAlliancesAllianceIdContactsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ContactsApi(config);
            var allianceId = 789L;  // long | The ID of the alliance
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var page = 56;  // int? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get alliance contacts
                List<AlliancesAllianceIdContactsGetInner> result = apiInstance.GetAlliancesAllianceIdContacts(allianceId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContactsApi.GetAlliancesAllianceIdContacts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAlliancesAllianceIdContactsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get alliance contacts
    ApiResponse<List<AlliancesAllianceIdContactsGetInner>> response = apiInstance.GetAlliancesAllianceIdContactsWithHttpInfo(allianceId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContactsApi.GetAlliancesAllianceIdContactsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **allianceId** | **long** | The ID of the alliance |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **page** | **int?** |  | [optional]  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;AlliancesAllianceIdContactsGetInner&gt;**](AlliancesAllianceIdContactsGetInner.md)

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

<a id="getalliancesallianceidcontactslabels"></a>
# **GetAlliancesAllianceIdContactsLabels**
> List&lt;AlliancesAllianceIdContactsLabelsGetInner&gt; GetAlliancesAllianceIdContactsLabels (long allianceId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get alliance contact labels

Return custom labels for an alliance's contacts

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetAlliancesAllianceIdContactsLabelsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ContactsApi(config);
            var allianceId = 789L;  // long | The ID of the alliance
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get alliance contact labels
                List<AlliancesAllianceIdContactsLabelsGetInner> result = apiInstance.GetAlliancesAllianceIdContactsLabels(allianceId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContactsApi.GetAlliancesAllianceIdContactsLabels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAlliancesAllianceIdContactsLabelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get alliance contact labels
    ApiResponse<List<AlliancesAllianceIdContactsLabelsGetInner>> response = apiInstance.GetAlliancesAllianceIdContactsLabelsWithHttpInfo(allianceId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContactsApi.GetAlliancesAllianceIdContactsLabelsWithHttpInfo: " + e.Message);
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

[**List&lt;AlliancesAllianceIdContactsLabelsGetInner&gt;**](AlliancesAllianceIdContactsLabelsGetInner.md)

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

<a id="getcharacterscharacteridcontacts"></a>
# **GetCharactersCharacterIdContacts**
> List&lt;CharactersCharacterIdContactsGetInner&gt; GetCharactersCharacterIdContacts (long characterId, DateOnly xCompatibilityDate, int? page = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get contacts

Return contacts of a character

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdContactsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ContactsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var page = 56;  // int? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get contacts
                List<CharactersCharacterIdContactsGetInner> result = apiInstance.GetCharactersCharacterIdContacts(characterId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContactsApi.GetCharactersCharacterIdContacts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdContactsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get contacts
    ApiResponse<List<CharactersCharacterIdContactsGetInner>> response = apiInstance.GetCharactersCharacterIdContactsWithHttpInfo(characterId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContactsApi.GetCharactersCharacterIdContactsWithHttpInfo: " + e.Message);
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

[**List&lt;CharactersCharacterIdContactsGetInner&gt;**](CharactersCharacterIdContactsGetInner.md)

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

<a id="getcharacterscharacteridcontactslabels"></a>
# **GetCharactersCharacterIdContactsLabels**
> List&lt;AlliancesAllianceIdContactsLabelsGetInner&gt; GetCharactersCharacterIdContactsLabels (long characterId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get contact labels

Return custom labels for a character's contacts

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdContactsLabelsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ContactsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get contact labels
                List<AlliancesAllianceIdContactsLabelsGetInner> result = apiInstance.GetCharactersCharacterIdContactsLabels(characterId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContactsApi.GetCharactersCharacterIdContactsLabels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdContactsLabelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get contact labels
    ApiResponse<List<AlliancesAllianceIdContactsLabelsGetInner>> response = apiInstance.GetCharactersCharacterIdContactsLabelsWithHttpInfo(characterId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContactsApi.GetCharactersCharacterIdContactsLabelsWithHttpInfo: " + e.Message);
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

[**List&lt;AlliancesAllianceIdContactsLabelsGetInner&gt;**](AlliancesAllianceIdContactsLabelsGetInner.md)

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

<a id="getcorporationscorporationidcontacts"></a>
# **GetCorporationsCorporationIdContacts**
> List&lt;CorporationsCorporationIdContactsGetInner&gt; GetCorporationsCorporationIdContacts (long corporationId, DateOnly xCompatibilityDate, int? page = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get corporation contacts

Return contacts of a corporation

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationsCorporationIdContactsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ContactsApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var page = 56;  // int? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get corporation contacts
                List<CorporationsCorporationIdContactsGetInner> result = apiInstance.GetCorporationsCorporationIdContacts(corporationId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContactsApi.GetCorporationsCorporationIdContacts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationsCorporationIdContactsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get corporation contacts
    ApiResponse<List<CorporationsCorporationIdContactsGetInner>> response = apiInstance.GetCorporationsCorporationIdContactsWithHttpInfo(corporationId, xCompatibilityDate, page, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContactsApi.GetCorporationsCorporationIdContactsWithHttpInfo: " + e.Message);
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

[**List&lt;CorporationsCorporationIdContactsGetInner&gt;**](CorporationsCorporationIdContactsGetInner.md)

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

<a id="getcorporationscorporationidcontactslabels"></a>
# **GetCorporationsCorporationIdContactsLabels**
> List&lt;AlliancesAllianceIdContactsLabelsGetInner&gt; GetCorporationsCorporationIdContactsLabels (long corporationId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get corporation contact labels

Return custom labels for a corporation's contacts

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCorporationsCorporationIdContactsLabelsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ContactsApi(config);
            var corporationId = 789L;  // long | The ID of the corporation
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get corporation contact labels
                List<AlliancesAllianceIdContactsLabelsGetInner> result = apiInstance.GetCorporationsCorporationIdContactsLabels(corporationId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContactsApi.GetCorporationsCorporationIdContactsLabels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCorporationsCorporationIdContactsLabelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get corporation contact labels
    ApiResponse<List<AlliancesAllianceIdContactsLabelsGetInner>> response = apiInstance.GetCorporationsCorporationIdContactsLabelsWithHttpInfo(corporationId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContactsApi.GetCorporationsCorporationIdContactsLabelsWithHttpInfo: " + e.Message);
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

[**List&lt;AlliancesAllianceIdContactsLabelsGetInner&gt;**](AlliancesAllianceIdContactsLabelsGetInner.md)

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

<a id="postcharacterscharacteridcontacts"></a>
# **PostCharactersCharacterIdContacts**
> List&lt;long&gt; PostCharactersCharacterIdContacts (long characterId, double standing, DateOnly xCompatibilityDate, List<long> requestBody, List<long>? labelIds = null, bool? watched = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Add contacts

Bulk add contacts with same settings

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PostCharactersCharacterIdContactsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ContactsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var standing = 1.2D;  // double | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var requestBody = new List<long>(); // List<long> | 
            var labelIds = new List<long>?(); // List<long>? |  (optional) 
            var watched = false;  // bool? |  (optional)  (default to false)
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Add contacts
                List<long> result = apiInstance.PostCharactersCharacterIdContacts(characterId, standing, xCompatibilityDate, requestBody, labelIds, watched, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContactsApi.PostCharactersCharacterIdContacts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PostCharactersCharacterIdContactsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add contacts
    ApiResponse<List<long>> response = apiInstance.PostCharactersCharacterIdContactsWithHttpInfo(characterId, standing, xCompatibilityDate, requestBody, labelIds, watched, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContactsApi.PostCharactersCharacterIdContactsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **standing** | **double** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **requestBody** | [**List&lt;long&gt;**](long.md) |  |  |
| **labelIds** | [**List&lt;long&gt;?**](long.md) |  | [optional]  |
| **watched** | **bool?** |  | [optional] [default to false] |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

**List<long>**

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

<a id="putcharacterscharacteridcontacts"></a>
# **PutCharactersCharacterIdContacts**
> void PutCharactersCharacterIdContacts (long characterId, double standing, DateOnly xCompatibilityDate, List<long> requestBody, List<long>? labelIds = null, bool? watched = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Edit contacts

Bulk edit contacts with same settings

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PutCharactersCharacterIdContactsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ContactsApi(config);
            var characterId = 789L;  // long | The ID of the character
            var standing = 1.2D;  // double | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var requestBody = new List<long>(); // List<long> | 
            var labelIds = new List<long>?(); // List<long>? |  (optional) 
            var watched = false;  // bool? |  (optional)  (default to false)
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Edit contacts
                apiInstance.PutCharactersCharacterIdContacts(characterId, standing, xCompatibilityDate, requestBody, labelIds, watched, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ContactsApi.PutCharactersCharacterIdContacts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PutCharactersCharacterIdContactsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Edit contacts
    apiInstance.PutCharactersCharacterIdContactsWithHttpInfo(characterId, standing, xCompatibilityDate, requestBody, labelIds, watched, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ContactsApi.PutCharactersCharacterIdContactsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **standing** | **double** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **requestBody** | [**List&lt;long&gt;**](long.md) |  |  |
| **labelIds** | [**List&lt;long&gt;?**](long.md) |  | [optional]  |
| **watched** | **bool?** |  | [optional] [default to false] |
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
| **204** | Contacts updated |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

