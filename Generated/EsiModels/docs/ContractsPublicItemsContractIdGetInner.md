# EveESI.Models.Model.ContractsPublicItemsContractIdGetInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IsBlueprintCopy** | **bool** |  | [optional] 
**IsIncluded** | **bool** | true if the contract issuer has submitted this item with the contract, false if the isser is asking for this item in the contract | 
**ItemId** | **long** | Unique ID for the item being sold. Not present if item is being requested by contract rather than sold with contract | [optional] 
**MaterialEfficiency** | **long** | Material Efficiency Level of the blueprint | [optional] 
**Quantity** | **long** | Number of items in the stack | 
**RecordId** | **long** | Unique ID for the item, used by the contract system | 
**Runs** | **long** | Number of runs remaining if the blueprint is a copy, -1 if it is an original | [optional] 
**TimeEfficiency** | **long** | Time Efficiency Level of the blueprint | [optional] 
**TypeId** | **long** | Type ID for item | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

