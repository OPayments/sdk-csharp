# OPayments.SDK.Model.Payment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PaymentId** | **Guid** |  | 
**OrderId** | **string** |  | 
**Amount** | **int** | Сумма в копейках. | 
**Currency** | **string** |  | 
**PaymentMethod** | **string** |  | 
**Status** | **string** |  | 
**CreatedAt** | **DateTime** |  | 
**UpdatedAt** | **DateTime** |  | 
**Description** | **string** |  | [optional] 
**PaymentUrl** | **string** | Адрес оплаты для платежа в статусе pending. | [optional] 
**FailureCode** | **string** |  | [optional] 
**FailureMessage** | **string** | Нормализованное сообщение, безопасное для показа мерчанту; никогда не содержит сырой ответ провайдера, credentials или данные карты. | [optional] 
**RefundSummary** | [**RefundSummary**](RefundSummary.md) |  | [optional] 
**CompletedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

