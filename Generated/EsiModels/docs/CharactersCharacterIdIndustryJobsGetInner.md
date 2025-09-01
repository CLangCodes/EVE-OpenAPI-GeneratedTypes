# EveESI.Models.Model.CharactersCharacterIdIndustryJobsGetInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActivityId** | **long** | Job activity ID | 
**BlueprintId** | **long** |  | 
**BlueprintLocationId** | **long** | Location ID of the location from which the blueprint was installed. Normally a station ID, but can also be an asset (e.g. container) or corporation facility | 
**BlueprintTypeId** | **long** |  | 
**CompletedCharacterId** | **long** | ID of the character which completed this job | [optional] 
**CompletedDate** | **DateTime** | Date and time when this job was completed | [optional] 
**Cost** | **double** | The sume of job installation fee and industry facility tax | [optional] 
**Duration** | **long** | Job duration in seconds | 
**EndDate** | **DateTime** | Date and time when this job finished | 
**FacilityId** | **long** | ID of the facility where this job is running | 
**InstallerId** | **long** | ID of the character which installed this job | 
**JobId** | **long** | Unique job ID | 
**LicensedRuns** | **long** | Number of runs blueprint is licensed for | [optional] 
**OutputLocationId** | **long** | Location ID of the location to which the output of the job will be delivered. Normally a station ID, but can also be a corporation facility | 
**PauseDate** | **DateTime** | Date and time when this job was paused (i.e. time when the facility where this job was installed went offline) | [optional] 
**Probability** | **double** | Chance of success for invention | [optional] 
**ProductTypeId** | **long** | Type ID of product (manufactured, copied or invented) | [optional] 
**Runs** | **long** | Number of runs for a manufacturing job, or number of copies to make for a blueprint copy | 
**StartDate** | **DateTime** | Date and time when this job started | 
**StationId** | **long** | ID of the station where industry facility is located | 
**Status** | **string** |  | 
**SuccessfulRuns** | **long** | Number of successful runs for this job. Equal to runs unless this is an invention job | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

