# EveESI.Models.Api.CalendarApi

All URIs are relative to *https://esi.evetech.net*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetCharactersCharacterIdCalendar**](CalendarApi.md#getcharacterscharacteridcalendar) | **GET** /characters/{character_id}/calendar | List calendar event summaries |
| [**GetCharactersCharacterIdCalendarEventId**](CalendarApi.md#getcharacterscharacteridcalendareventid) | **GET** /characters/{character_id}/calendar/{event_id} | Get an event |
| [**GetCharactersCharacterIdCalendarEventIdAttendees**](CalendarApi.md#getcharacterscharacteridcalendareventidattendees) | **GET** /characters/{character_id}/calendar/{event_id}/attendees | Get attendees |
| [**PutCharactersCharacterIdCalendarEventId**](CalendarApi.md#putcharacterscharacteridcalendareventid) | **PUT** /characters/{character_id}/calendar/{event_id} | Respond to an event |

<a id="getcharacterscharacteridcalendar"></a>
# **GetCharactersCharacterIdCalendar**
> List&lt;CharactersCharacterIdCalendarGetInner&gt; GetCharactersCharacterIdCalendar (long characterId, DateOnly xCompatibilityDate, long? fromEvent = null, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

List calendar event summaries

Get 50 event summaries from the calendar. If no from_event ID is given, the resource will return the next 50 chronological event summaries from now. If a from_event ID is specified, it will return the next 50 chronological event summaries from after that event

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdCalendarExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CalendarApi(config);
            var characterId = 789L;  // long | The ID of the character
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var fromEvent = 789L;  // long? |  (optional) 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // List calendar event summaries
                List<CharactersCharacterIdCalendarGetInner> result = apiInstance.GetCharactersCharacterIdCalendar(characterId, xCompatibilityDate, fromEvent, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.GetCharactersCharacterIdCalendar: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdCalendarWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List calendar event summaries
    ApiResponse<List<CharactersCharacterIdCalendarGetInner>> response = apiInstance.GetCharactersCharacterIdCalendarWithHttpInfo(characterId, xCompatibilityDate, fromEvent, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.GetCharactersCharacterIdCalendarWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **fromEvent** | **long?** |  | [optional]  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CharactersCharacterIdCalendarGetInner&gt;**](CharactersCharacterIdCalendarGetInner.md)

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

<a id="getcharacterscharacteridcalendareventid"></a>
# **GetCharactersCharacterIdCalendarEventId**
> CharactersCharacterIdCalendarEventIdGet GetCharactersCharacterIdCalendarEventId (long characterId, long eventId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get an event

Get all the information for a specific event

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdCalendarEventIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CalendarApi(config);
            var characterId = 789L;  // long | The ID of the character
            var eventId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get an event
                CharactersCharacterIdCalendarEventIdGet result = apiInstance.GetCharactersCharacterIdCalendarEventId(characterId, eventId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.GetCharactersCharacterIdCalendarEventId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdCalendarEventIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an event
    ApiResponse<CharactersCharacterIdCalendarEventIdGet> response = apiInstance.GetCharactersCharacterIdCalendarEventIdWithHttpInfo(characterId, eventId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.GetCharactersCharacterIdCalendarEventIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **eventId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**CharactersCharacterIdCalendarEventIdGet**](CharactersCharacterIdCalendarEventIdGet.md)

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

<a id="getcharacterscharacteridcalendareventidattendees"></a>
# **GetCharactersCharacterIdCalendarEventIdAttendees**
> List&lt;CharactersCharacterIdCalendarEventIdAttendeesGetInner&gt; GetCharactersCharacterIdCalendarEventIdAttendees (long characterId, long eventId, DateOnly xCompatibilityDate, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Get attendees

Get all invited attendees for a given event

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class GetCharactersCharacterIdCalendarEventIdAttendeesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CalendarApi(config);
            var characterId = 789L;  // long | The ID of the character
            var eventId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Get attendees
                List<CharactersCharacterIdCalendarEventIdAttendeesGetInner> result = apiInstance.GetCharactersCharacterIdCalendarEventIdAttendees(characterId, eventId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.GetCharactersCharacterIdCalendarEventIdAttendees: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCharactersCharacterIdCalendarEventIdAttendeesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get attendees
    ApiResponse<List<CharactersCharacterIdCalendarEventIdAttendeesGetInner>> response = apiInstance.GetCharactersCharacterIdCalendarEventIdAttendeesWithHttpInfo(characterId, eventId, xCompatibilityDate, acceptLanguage, ifNoneMatch, xTenant);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.GetCharactersCharacterIdCalendarEventIdAttendeesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **eventId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **acceptLanguage** | **string?** | The language to use for the response. | [optional] [default to en] |
| **ifNoneMatch** | **string?** | The ETag of the previous request. A 304 will be returned if this matches the current ETag. | [optional]  |
| **xTenant** | **string?** | The tenant ID for the request. | [optional] [default to &quot;tranquility&quot;] |

### Return type

[**List&lt;CharactersCharacterIdCalendarEventIdAttendeesGetInner&gt;**](CharactersCharacterIdCalendarEventIdAttendeesGetInner.md)

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

<a id="putcharacterscharacteridcalendareventid"></a>
# **PutCharactersCharacterIdCalendarEventId**
> void PutCharactersCharacterIdCalendarEventId (long characterId, long eventId, DateOnly xCompatibilityDate, PutCharactersCharacterIdCalendarEventIdRequest putCharactersCharacterIdCalendarEventIdRequest, string? acceptLanguage = null, string? ifNoneMatch = null, string? xTenant = null)

Respond to an event

Set your response status to an event

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EveESI.Models.Api;
using EveESI.Models.Client;
using EveESI.Models.Model;

namespace Example
{
    public class PutCharactersCharacterIdCalendarEventIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://esi.evetech.net";
            // Configure OAuth2 access token for authorization: OAuth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CalendarApi(config);
            var characterId = 789L;  // long | The ID of the character
            var eventId = 789L;  // long | 
            var xCompatibilityDate = DateOnly.Parse("2025-08-26");  // DateOnly | The compatibility date for the request.
            var putCharactersCharacterIdCalendarEventIdRequest = new PutCharactersCharacterIdCalendarEventIdRequest(); // PutCharactersCharacterIdCalendarEventIdRequest | 
            var acceptLanguage = "en";  // string? | The language to use for the response. (optional)  (default to en)
            var ifNoneMatch = "ifNoneMatch_example";  // string? | The ETag of the previous request. A 304 will be returned if this matches the current ETag. (optional) 
            var xTenant = ;  // string? | The tenant ID for the request. (optional)  (default to "tranquility")

            try
            {
                // Respond to an event
                apiInstance.PutCharactersCharacterIdCalendarEventId(characterId, eventId, xCompatibilityDate, putCharactersCharacterIdCalendarEventIdRequest, acceptLanguage, ifNoneMatch, xTenant);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CalendarApi.PutCharactersCharacterIdCalendarEventId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PutCharactersCharacterIdCalendarEventIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Respond to an event
    apiInstance.PutCharactersCharacterIdCalendarEventIdWithHttpInfo(characterId, eventId, xCompatibilityDate, putCharactersCharacterIdCalendarEventIdRequest, acceptLanguage, ifNoneMatch, xTenant);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CalendarApi.PutCharactersCharacterIdCalendarEventIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **characterId** | **long** | The ID of the character |  |
| **eventId** | **long** |  |  |
| **xCompatibilityDate** | **DateOnly** | The compatibility date for the request. |  |
| **putCharactersCharacterIdCalendarEventIdRequest** | [**PutCharactersCharacterIdCalendarEventIdRequest**](PutCharactersCharacterIdCalendarEventIdRequest.md) |  |  |
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
| **204** | Event updated |  * Cache-Control -  <br>  * ETag -  <br>  * Last-Modified -  <br>  |
| **0** | Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

