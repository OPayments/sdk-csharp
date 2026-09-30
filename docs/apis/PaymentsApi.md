# OPayments.SDK.Api.PaymentsApi

All URIs are relative to *https://api.opayments.io/api/v1*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetPayment**](PaymentsApi.md#getpayment) | **GET** /payments/{paymentId} | Получить платёж |
| [**ListPayments**](PaymentsApi.md#listpayments) | **GET** /payments | Найти платежи |

<a id="getpayment"></a>
# **GetPayment**
> PaymentDetails GetPayment (Guid paymentId)

Получить платёж


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **paymentId** | **Guid** |  |  |

### Return type

[**PaymentDetails**](PaymentDetails.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Платёж. |  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **404** | Ресурс не найден. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listpayments"></a>
# **ListPayments**
> PaymentList ListPayments (string orderId = null, List<string> status = null, string paymentMethod = null, int amountFrom = null, int amountTo = null, DateTime createdFrom = null, DateTime createdTo = null, DateTime completedFrom = null, DateTime completedTo = null, string failureCode = null, string search = null, string sort = null, string sortDirection = null, string cursor = null, int limit = null)

Найти платежи

Возвращает список платежей проекта.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **orderId** | **string** | Идентификатор заказа в системе мерчанта. | [optional]  |
| **status** | [**List&lt;string&gt;**](string.md) |  | [optional]  |
| **paymentMethod** | **string** |  | [optional]  |
| **amountFrom** | **int** | Не больше amountTo, если он передан. | [optional]  |
| **amountTo** | **int** | Не меньше amountFrom, если он передан. | [optional]  |
| **createdFrom** | **DateTime** | Не позже createdTo, если он передан. | [optional]  |
| **createdTo** | **DateTime** | Не раньше createdFrom, если он передан. | [optional]  |
| **completedFrom** | **DateTime** | Не позже completedTo, если он передан. | [optional]  |
| **completedTo** | **DateTime** | Не раньше completedFrom, если он передан. | [optional]  |
| **failureCode** | **string** | Нормализованный код причины платежа. | [optional]  |
| **search** | **string** | Поиск по paymentId, orderId и описанию платежа. | [optional]  |
| **sort** | **string** |  | [optional] [default to createdAt] |
| **sortDirection** | **string** |  | [optional] [default to desc] |
| **cursor** | **string** | Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. При одинаковом sort key API использует стабильный вторичный ID. | [optional]  |
| **limit** | **int** | Количество записей в ответе. | [optional] [default to 20] |

### Return type

[**PaymentList**](PaymentList.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Страница платежей. |  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **403** | Операция недоступна для проекта. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

