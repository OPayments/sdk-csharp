# OPayments.SDK.Api.PaymentApi

All URIs are relative to *https://api.opayments.io/api/v1*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateSbpPayment**](PaymentApi.md#createsbppayment) | **POST** /payments/sbp | Создать платёж по СБП |
| [**CreateTpayPayment**](PaymentApi.md#createtpaypayment) | **POST** /payments/tpay | Создать платёж через T-Pay |

<a id="createsbppayment"></a>
# **CreateSbpPayment**
> Payment CreateSbpPayment (CreateSbpPaymentRequest createSbpPaymentRequest, string idempotencyKey = null)

Создать платёж по СБП


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createSbpPaymentRequest** | [**CreateSbpPaymentRequest**](CreateSbpPaymentRequest.md) |  |  |
| **idempotencyKey** | **string** |  | [optional]  |

### Return type

[**Payment**](Payment.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ранее созданный платёж СБП. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **201** | Платёж через СБП создан. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **403** | Операция недоступна для проекта. |  * X-Request-Id -  <br>  |
| **409** | Запрос конфликтует с текущим состоянием ресурса. |  * X-Request-Id -  <br>  |
| **415** | Тело запроса должно быть JSON. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
| **502** | Внешний сервис вернул некорректный ответ. |  * X-Request-Id -  <br>  |
| **503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  * Retry-After -  <br>  |
| **504** | Внешний сервис не ответил вовремя. |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createtpaypayment"></a>
# **CreateTpayPayment**
> Payment CreateTpayPayment (CreateTpayPaymentRequest createTpayPaymentRequest, string idempotencyKey = null)

Создать платёж через T-Pay


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **createTpayPaymentRequest** | [**CreateTpayPaymentRequest**](CreateTpayPaymentRequest.md) |  |  |
| **idempotencyKey** | **string** |  | [optional]  |

### Return type

[**Payment**](Payment.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ранее созданный платёж T-Pay. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **201** | Платёж через T-Pay создан. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **403** | Операция недоступна для проекта. |  * X-Request-Id -  <br>  |
| **409** | Запрос конфликтует с текущим состоянием ресурса. |  * X-Request-Id -  <br>  |
| **415** | Тело запроса должно быть JSON. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
| **502** | Внешний сервис вернул некорректный ответ. |  * X-Request-Id -  <br>  |
| **503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  * Retry-After -  <br>  |
| **504** | Внешний сервис не ответил вовремя. |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

