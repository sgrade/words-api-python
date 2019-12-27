# swagger_client.WordApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_word**](WordApi.md#add_word) | **POST** /word | Add a new word to the store
[**delete_word**](WordApi.md#delete_word) | **DELETE** /word/{wordId} | Deletes a word
[**get_word_by_id**](WordApi.md#get_word_by_id) | **GET** /word/{wordId} | Find word by ID
[**update_word**](WordApi.md#update_word) | **PUT** /word | Update an existing word
[**update_word_with_form**](WordApi.md#update_word_with_form) | **POST** /word/{wordId} | Updates a word in the store with form data
[**upload_file**](WordApi.md#upload_file) | **POST** /word/{wordId}/uploadImage | uploads an image

# **add_word**
> add_word(body)

Add a new word to the store

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: wordstore_auth
configuration = swagger_client.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = swagger_client.WordApi(swagger_client.ApiClient(configuration))
body = swagger_client.Word() # Word | Word object that needs to be added to the store

try:
    # Add a new word to the store
    api_instance.add_word(body)
except ApiException as e:
    print("Exception when calling WordApi->add_word: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Word**](Word.md)| Word object that needs to be added to the store | 

### Return type

void (empty response body)

### Authorization

[wordstore_auth](../README.md#wordstore_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_word**
> delete_word(word_id, api_key=api_key)

Deletes a word

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.WordApi()
word_id = 789 # int | Word id to delete
api_key = 'api_key_example' # str |  (optional)

try:
    # Deletes a word
    api_instance.delete_word(word_id, api_key=api_key)
except ApiException as e:
    print("Exception when calling WordApi->delete_word: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **word_id** | **int**| Word id to delete | 
 **api_key** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_word_by_id**
> Word get_word_by_id(word_id)

Find word by ID

Returns a single word

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.WordApi()
word_id = 789 # int | ID of word to return

try:
    # Find word by ID
    api_response = api_instance.get_word_by_id(word_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WordApi->get_word_by_id: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **word_id** | **int**| ID of word to return | 

### Return type

[**Word**](Word.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_word**
> update_word(body)

Update an existing word

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.WordApi()
body = swagger_client.Word() # Word | Word object that needs to be added to the store

try:
    # Update an existing word
    api_instance.update_word(body)
except ApiException as e:
    print("Exception when calling WordApi->update_word: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Word**](Word.md)| Word object that needs to be added to the store | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_word_with_form**
> update_word_with_form(word_id, name=name, status=status)

Updates a word in the store with form data

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.WordApi()
word_id = 789 # int | ID of word that needs to be updated
name = 'name_example' # str |  (optional)
status = 'status_example' # str |  (optional)

try:
    # Updates a word in the store with form data
    api_instance.update_word_with_form(word_id, name=name, status=status)
except ApiException as e:
    print("Exception when calling WordApi->update_word_with_form: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **word_id** | **int**| ID of word that needs to be updated | 
 **name** | **str**|  | [optional] 
 **status** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_file**
> ApiResponse upload_file(word_id, body=body)

uploads an image

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.WordApi()
word_id = 789 # int | ID of word to update
body = swagger_client.Object() # Object |  (optional)

try:
    # uploads an image
    api_response = api_instance.upload_file(word_id, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling WordApi->upload_file: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **word_id** | **int**| ID of word to update | 
 **body** | [**Object**](Object.md)|  | [optional] 

### Return type

[**ApiResponse**](ApiResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/octet-stream
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

