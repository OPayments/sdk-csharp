# OPayments.SDK.Api.RefundsApi

All URIs are relative to *https://api.opayments.io/api/v1*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreatePaymentRefund**](RefundsApi.md#createpaymentrefund) | **POST** /payments/{paymentId}/refunds | Создать возврат |
| [**GetRefund**](RefundsApi.md#getrefund) | **GET** /refunds/{refundId} | Получить возврат |
| [**ListPaymentRefunds**](RefundsApi.md#listpaymentrefunds) | **GET** /payments/{paymentId}/refunds | Найти возвраты платежа |
| [**ListRefunds**](RefundsApi.md#listrefunds) | **GET** /refunds | Найти возвраты проекта |

<a id="createpaymentrefund"></a>
# **CreatePaymentRefund**
> Refund CreatePaymentRefund (Guid paymentId, CreateRefundRequest createRefundRequest, string idempotencyKey = null)

Создать возврат


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **paymentId** | **Guid** |  |  |
| **createRefundRequest** | [**CreateRefundRequest**](CreateRefundRequest.md) |  |  |
| **idempotencyKey** | **string** |  | [optional]  |

### Return type

[**Refund**](Refund.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ранее созданный возврат с теми же параметрами. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **202** | Возврат принят в обработку. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **404** | Ресурс не найден. |  * X-Request-Id -  <br>  |
| **409** | Параметры ранее созданного возврата отличаются. |  * X-Request-Id -  <br>  |
| **422** | Операция невозможна в текущем статусе платежа. |  * X-Request-Id -  <br>  |
| **415** | Тело запроса должно быть JSON. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
| **500** | Внутренняя ошибка сервиса. |  * X-Request-Id -  <br>  |
| **502** | Внешний сервис вернул некорректный ответ. |  * X-Request-Id -  <br>  |
| **503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  * Retry-After -  <br>  |
| **504** | Внешний сервис не ответил вовремя. |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getrefund"></a>
# **GetRefund**
> Refund GetRefund (Guid refundId)

Получить возврат


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **refundId** | **Guid** |  |  |

### Return type

[**Refund**](Refund.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Возврат. |  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **404** | Возврат не найден. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listpaymentrefunds"></a>
# **ListPaymentRefunds**
> RefundPage ListPaymentRefunds (Guid paymentId, string status = null, RefundReason reasonCode = null, string cursor = null, int limit = null)

Найти возвраты платежа


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **paymentId** | **Guid** |  |  |
| **status** | **string** |  | [optional]  |
| **reasonCode** | **RefundReason** |  | [optional]  |
| **cursor** | **string** | Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. При одинаковом sort key API использует стабильный вторичный ID. | [optional]  |
| **limit** | **int** | Количество записей в ответе. | [optional] [default to 20] |

### Return type

[**RefundPage**](RefundPage.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Страница возвратов платежа. |  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **404** | Ресурс не найден. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listrefunds"></a>
# **ListRefunds**
> RefundPage ListRefunds (string status = null, string paymentMethod = null, Guid paymentId = null, RefundReason reasonCode = null, DateTime createdFrom = null, DateTime createdTo = null, string cursor = null, int limit = null)

Найти возвраты проекта

Возвращает возвраты по всем платежам текущего проекта. Сортировка всегда `createdAt DESC, refundId DESC`; курсор нельзя использовать с другими фильтрами.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **status** | **string** |  | [optional]  |
| **paymentMethod** | **string** |  | [optional]  |
| **paymentId** | **Guid** | Идентификатор исходного платежа. | [optional]  |
| **reasonCode** | **RefundReason** |  | [optional]  |
| **createdFrom** | **DateTime** | Не позже createdTo, если он передан. | [optional]  |
| **createdTo** | **DateTime** | Не раньше createdFrom, если он передан. | [optional]  |
| **cursor** | **string** | Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. При одинаковом sort key API использует стабильный вторичный ID. | [optional]  |
| **limit** | **int** | Количество записей в ответе. | [optional] [default to 20] |

### Return type

[**RefundPage**](RefundPage.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Страница возвратов платежа. |  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

