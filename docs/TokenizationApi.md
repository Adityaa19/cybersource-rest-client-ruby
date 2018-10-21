# CyberSource::TokenizationApi

All URIs are relative to *https://api.cybersource.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tokenize**](TokenizationApi.md#tokenize) | **POST** /payments/flex/v1/tokens/ | Tokenize card


# **tokenize**
> InlineResponse2001 tokenize(opts)

Tokenize card

Returns a token representing the supplied card details. The token replaces card data and can be used as the Subscription ID in the CyberSource Simple Order API or SCMP API. This is an unauthenticated call that you should initiate from your customer’s device or browser.

### Example
```ruby
# load the gem
require 'cyberSource_client'

api_instance = CyberSource::TokenizationApi.new

opts = { 
  tokenize_request: CyberSource::TokenizeRequest.new # TokenizeRequest | 
}

begin
  #Tokenize card
  result = api_instance.tokenize(opts)
  p result
rescue CyberSource::ApiError => e
  puts "Exception when calling TokenizationApi->tokenize: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tokenize_request** | [**TokenizeRequest**](TokenizeRequest.md)|  | [optional] 

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



