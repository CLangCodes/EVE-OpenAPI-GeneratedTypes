# EveESI.Models.Model.CorporationsCorporationIdCustomsOfficesGetInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AllianceTaxRate** | **double** | Only present if alliance access is allowed | [optional] 
**AllowAccessWithStandings** | **bool** | standing_level and any standing related tax rate only present when this is true | 
**AllowAllianceAccess** | **bool** |  | 
**BadStandingTaxRate** | **double** |  | [optional] 
**CorporationTaxRate** | **double** |  | [optional] 
**ExcellentStandingTaxRate** | **double** | Tax rate for entities with excellent level of standing, only present if this level is allowed, same for all other standing related tax rates | [optional] 
**GoodStandingTaxRate** | **double** |  | [optional] 
**NeutralStandingTaxRate** | **double** |  | [optional] 
**OfficeId** | **long** | unique ID of this customs office | 
**ReinforceExitEnd** | **long** |  | 
**ReinforceExitStart** | **long** | Together with reinforce_exit_end, marks a 2-hour period where this customs office could exit reinforcement mode during the day after initial attack | 
**StandingLevel** | **string** | Access is allowed only for entities with this level of standing or better | [optional] 
**SystemId** | **long** | ID of the solar system this customs office is located in | 
**TerribleStandingTaxRate** | **double** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

