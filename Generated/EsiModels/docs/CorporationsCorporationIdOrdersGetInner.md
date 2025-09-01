# EveESI.Models.Model.CorporationsCorporationIdOrdersGetInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Duration** | **long** | Number of days for which order is valid (starting from the issued date). An order expires at time issued + duration | 
**Escrow** | **double** | For buy orders, the amount of ISK in escrow | [optional] 
**IsBuyOrder** | **bool** | True if the order is a bid (buy) order | [optional] 
**Issued** | **DateTime** | Date and time when this order was issued | 
**IssuedBy** | **long** | The character who issued this order | 
**LocationId** | **long** | ID of the location where order was placed | 
**MinVolume** | **long** | For buy orders, the minimum quantity that will be accepted in a matching sell order | [optional] 
**OrderId** | **long** | Unique order ID | 
**Price** | **double** | Cost per unit for this order | 
**Range** | **string** | Valid order range, numbers are ranges in jumps | 
**RegionId** | **long** | ID of the region where order was placed | 
**TypeId** | **long** | The type ID of the item transacted in this order | 
**VolumeRemain** | **long** | Quantity of items still required or offered | 
**VolumeTotal** | **long** | Quantity of items required or offered at time order was placed | 
**WalletDivision** | **long** | The corporation wallet division used for this order. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

