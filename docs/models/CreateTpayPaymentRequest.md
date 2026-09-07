# OPayments.SDK.Model.CreateTpayPaymentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**OrderId** | **string** | Идентификатор заказа в системе мерчанта. | 
**Amount** | **int** | Сумма в копейках. | 
**Currency** | **string** |  | 
**Ip** | **string** | IP-адрес плательщика: IPv4 или IPv6. | 
**CallbackUrl** | **string** | HTTPS-адрес уведомлений. | 
**SuccessUrl** | **string** | HTTPS-адрес для успешной оплаты. | 
**FailedUrl** | **string** | HTTPS-адрес для отменённой оплаты. | 
**DeviceData** | [**TpayDeviceData**](TpayDeviceData.md) |  | 
**Description** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

