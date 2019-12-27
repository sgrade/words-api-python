# swagger_client.WordsApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**find_words_by_name**](WordsApi.md#find_words_by_name) | **GET** /words/findByName | Find Words by name
[**find_words_by_status**](WordsApi.md#find_words_by_status) | **GET** /words/findByStatus | Finds Words by status
[**get_words_to_learn**](WordsApi.md#get_words_to_learn) | **GET** /words | Get words to learn

# **find_words_by_name**
> list[Words] find_words_by_name(term)

Find Words by name

Returns all words, which have the term in their name

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.WordsApi()
term = 'term_example' # str | Term to search in the names

try:
    # Find Words by name
    api_response = api_instance.find_words_by_name(term)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WordsApi->find_words_by_name: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **term** | **str**| Term to search in the names | 

### Return type

[**list[Words]**](Words.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_words_by_status**
> list[Words] find_words_by_status(status)

Finds Words by status

Multiple status values can be provided with comma separated strings

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.WordsApi()
status = ['status_example'] # list[str] | Status values that need to be considered for filter

try:
    # Finds Words by status
    api_response = api_instance.find_words_by_status(status)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WordsApi->find_words_by_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | [**list[str]**](str.md)| Status values that need to be considered for filter | 

### Return type

[**list[Words]**](Words.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_words_to_learn**
> Words get_words_to_learn(limit=limit, status=status)

Get words to learn

Returns number of words to learn

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.WordsApi()
limit = 56 # int | number of words to return (optional)
status = ['status_example'] # list[str] | status of words to return (optional)

try:
    # Get words to learn
    api_response = api_instance.get_words_to_learn(limit=limit, status=status)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WordsApi->get_words_to_learn: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| number of words to return | [optional] 
 **status** | [**list[str]**](str.md)| status of words to return | [optional] 

### Return type

[**Words**](Words.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

