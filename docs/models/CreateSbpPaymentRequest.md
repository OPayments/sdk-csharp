# OPayments.SDK.Model.CreateSbpPaymentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**OrderId** | **string** | Идентификатор заказа в системе мерчанта. | 
**Amount** | **int** | Сумма в копейках. | 
**Metadata** | [**PaymentMetadata**](PaymentMetadata.md) |  | 
**CallbackUrl** | **string** | HTTPS-адрес для уведомлений о платеже. | 
**SuccessUrl** | **string** | HTTPS-адрес для успешной оплаты. | 
**FailedUrl** | **string** | HTTPS-адрес для отменённой оплаты. | 
**Description** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

