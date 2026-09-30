# OPayments.SDK.Api.BalanceApi

All URIs are relative to *https://api.opayments.io/api/v1*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetBalance**](BalanceApi.md#getbalance) | **GET** /balance | Получить баланс |

<a id="getbalance"></a>
# **GetBalance**
> Balance GetBalance ()

Получить баланс

Возвращает текущий баланс проекта.


### Parameters
This endpoint does not need any parameter.
### Return type

[**Balance**](Balance.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Баланс проекта. |  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
| **503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

