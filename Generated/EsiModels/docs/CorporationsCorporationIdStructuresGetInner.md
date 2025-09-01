# EveESI.Models.Model.CorporationsCorporationIdStructuresGetInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CorporationId** | **long** | ID of the corporation that owns the structure | 
**FuelExpires** | **DateTime** | Date on which the structure will run out of fuel | [optional] 
**Name** | **string** | The structure name | [optional] 
**NextReinforceApply** | **DateTime** | The date and time when the structure&#39;s newly requested reinforcement times (e.g. next_reinforce_hour and next_reinforce_day) will take effect | [optional] 
**NextReinforceHour** | **long** | The requested change to reinforce_hour that will take effect at the time shown by next_reinforce_apply | [optional] 
**ProfileId** | **long** | The id of the ACL profile for this citadel | 
**ReinforceHour** | **long** | The hour of day that determines the four hour window when the structure will randomly exit its reinforcement periods and become vulnerable to attack against its armor and/or hull. The structure will become vulnerable at a random time that is +/- 2 hours centered on the value of this property | [optional] 
**Services** | [**List&lt;CorporationsCorporationIdStructuresGetInnerServicesInner&gt;**](CorporationsCorporationIdStructuresGetInnerServicesInner.md) | Contains a list of service upgrades, and their state | [optional] 
**State** | **string** |  | 
**StateTimerEnd** | **DateTime** | Date at which the structure will move to it&#39;s next state | [optional] 
**StateTimerStart** | **DateTime** | Date at which the structure entered it&#39;s current state | [optional] 
**StructureId** | **long** | The Item ID of the structure | 
**SystemId** | **long** | The solar system the structure is in | 
**TypeId** | **long** | The type id of the structure | 
**UnanchorsAt** | **DateTime** | Date at which the structure will unanchor | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

