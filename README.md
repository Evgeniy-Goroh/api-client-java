IntaroCRM REST API client for Java
==================================

Java Client for [IntaroCRM REST API](http://docs.intarocrm.ru/rest-api/).
version: 1.0.1

Requirements
------------
* [json-simple](https://code.google.com/p/json-simple/)

Usage
------------

### Create API client class

``` java

RestApi crmApiClient = new RestApi(
    "https://demo.intarocrm.ru",
    "T9DMPvuNt7FQJMszHUdG8Fkt6xHsqngH"
);
```
Constructor arguments are:

1. Your IntaroCRM acount URL-address
2. Your site API Token

### Example: get order types list

``` java

String url, key;
Map <?, ?> orderTypes;

RestApi crmApiClient = new RestApi(url, key);
try {
    orderTypes = crmApiClient.orderTypesList();
} catch (ApiException e) {
    e.printStackTrace();
}

```