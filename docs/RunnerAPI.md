# RunnerAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getV1RunnerModels**](RunnerAPI.md#getv1runnermodels) | **GET** /v1/runner/models | List configured runner model routes
[**postV1RunnerChat**](RunnerAPI.md#postv1runnerchat) | **POST** /v1/runner/chat | Multi-turn chat completion
[**postV1RunnerGenerate**](RunnerAPI.md#postv1runnergenerate) | **POST** /v1/runner/generate | Single-prompt generation


# **getV1RunnerModels**
```swift
    open class func getV1RunnerModels(completion: @escaping (_ data: GetV1RunnerModels200Response?, _ error: Error?) -> Void)
```

List configured runner model routes



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import LthnApi


// List configured runner model routes
RunnerAPI.getV1RunnerModels() { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GetV1RunnerModels200Response**](GetV1RunnerModels200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **postV1RunnerChat**
```swift
    open class func postV1RunnerChat(postV1RunnerChatRequest: PostV1RunnerChatRequest, completion: @escaping (_ data: PostV1RunnerChat200Response?, _ error: Error?) -> Void)
```

Multi-turn chat completion



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import LthnApi

let postV1RunnerChatRequest = post_v1_runner_chat_request(messages: [post_v1_runner_chat_request_messages_inner(content: "content_example", role: "role_example")]) // PostV1RunnerChatRequest | 

// Multi-turn chat completion
RunnerAPI.postV1RunnerChat(postV1RunnerChatRequest: postV1RunnerChatRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **postV1RunnerChatRequest** | [**PostV1RunnerChatRequest**](PostV1RunnerChatRequest.md) |  | 

### Return type

[**PostV1RunnerChat200Response**](PostV1RunnerChat200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **postV1RunnerGenerate**
```swift
    open class func postV1RunnerGenerate(postV1RunnerGenerateRequest: PostV1RunnerGenerateRequest, completion: @escaping (_ data: PostV1RunnerChat200Response?, _ error: Error?) -> Void)
```

Single-prompt generation



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import LthnApi

let postV1RunnerGenerateRequest = post_v1_runner_generate_request(prompt: "prompt_example") // PostV1RunnerGenerateRequest | 

// Single-prompt generation
RunnerAPI.postV1RunnerGenerate(postV1RunnerGenerateRequest: postV1RunnerGenerateRequest) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **postV1RunnerGenerateRequest** | [**PostV1RunnerGenerateRequest**](PostV1RunnerGenerateRequest.md) |  | 

### Return type

[**PostV1RunnerChat200Response**](PostV1RunnerChat200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

