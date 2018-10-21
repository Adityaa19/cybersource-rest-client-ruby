# CyberSource::CaptureApi

All URIs are relative to *https://api.cybersource.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**capture_payment**](CaptureApi.md#capture_payment) | **POST** /v2/payments/{id}/captures | Capture a Payment
[**get_capture**](CaptureApi.md#get_capture) | **GET** /v2/captures/{id} | Retrieve a Capture


# **capture_payment**
> InlineResponse2012 capture_payment(capture_payment_request, id)

Capture a Payment

Include the payment ID in the POST request to capture the payment amount.

### Example
```ruby
# load the gem
require 'cyberSource_client'

api_instance = CyberSource::CaptureApi.new

capture_payment_request = CyberSource::CapturePaymentRequest.new # CapturePaymentRequest | 

id = "id_example" # String | The payment ID returned from a previous payment request. This ID links the capture to the payment. 


begin
  #Capture a Payment
  result = api_instance.capture_payment(capture_payment_request, id)
  p result
rescue CyberSource::ApiError => e
  puts "Exception when calling CaptureApi->capture_payment: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **capture_payment_request** | [**CapturePaymentRequest**](CapturePaymentRequest.md)|  | 
 **id** | **String**| The payment ID returned from a previous payment request. This ID links the capture to the payment.  | 

### Return type

[**InlineResponse2012**](InlineResponse2012.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **get_capture**
> InlineResponse2004 get_capture(id)

Retrieve a Capture

Include the capture ID in the GET request to retrieve the capture details. 

### Example
```ruby
# load the gem
require 'cyberSource_client'

api_instance = CyberSource::CaptureApi.new

id = "id_example" # String | The capture ID returned from a previous capture request. 


begin
  #Retrieve a Capture
  result = api_instance.get_capture(id)
  p result
rescue CyberSource::ApiError => e
  puts "Exception when calling CaptureApi->get_capture: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| The capture ID returned from a previous capture request.  | 

### Return type

[**InlineResponse2004**](InlineResponse2004.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



