---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - curl

toc_footers:
  - <a href='http://surveillus.com/privacy-policy/'>Privacy Policy</a>
  - <a href='#'>API V 0.0.12</a>

includes:
  - exhibits
  - associations
  - cameras
  - subscriptions
  - triggers

search: true
---

# Introduction

Welcome to the Surveillus API documentation.  

The API documentation contains a general overview about the design and technology that has been implemented, followed by reference information about specific endpoints.

The purpose of our API is to make it easy to add video and image features to your web or mobile app. We want this API to be useful to you. If you run into any problems please feel free to <a href='http://surveillus.com/contact/'>contact</a> us.

## API Base

The base address for Surveillus API will be provided to you.

## Authentication

> To authenticate, use this code:

```shell
curl "https://www.example.com/mist/authenticate"
  -H "Content-Type: application/json"
  -d "apikey=ezEjgGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkZXNjcmlwdGlvbiI6IlFBIGxvY2FsIEFQSSBLZXkiLCJhcHBsaWNhdGlvbk5hbWUiOiJRQXMgTWFnaWMgS2V5IiwicHJvY1R5cGUiOiJsb2NhbCIsImF1dGhUeX2DIjoiYXBpa2V5IiwidXVpZCI6InQ1dE5lSzNsVmNzVkpuSEIiLCJpYXQiOjE1NDk0MTQwNjQsImF1ZCI6InByZS1BbHBoYSIsImlzcyI6IlN1cnZlaWxsdXMgRGV2ZWxvcG1lbnQiLCJzdJBiOiJBUEkgQWNjZXNzIn0.SUrut-yYfOZOXnLSetb82Lln2oeofSEtrK-itW3xoEjY"
```

> The above command returns:

```json
{
    "jwtToken": "eyHhbGciOiJZUzI1NiIsInR6cCI6IkpXVCJ9.eyJhdXRoVH2wZSI6InRva3UuIiwiY29tbWVudCI6IlJlbW90ZSBMb2NrIJzzWXIgT25lIiwibG9ja1N0XYRlSWQiOiJPbmUiLCJ1dWlkIjoiUjI3c1ZaOEhXaU5DdFRCMiIsInN1YiI6IkFQSSBBY2Nlc3MiLCJpc3N1ZXIiOiJTdXJ2ZWlsbHTvIERldmVsb3BtZW50IiwiYXVkaWVuY2UiOiJwcmUtQWxwaGiLCJzdWJqZWN0IjoiQVBJIEFjY2VzcyIsImV4cGlyZXNJbiI6IjI0aCIsImlhdCI6MTU0OTY2OTkzMiwiZXhwIjoxNTQ5NzU2MzMyfQ.Xv7Md43ZuC4GaWdi822WdDx78pa_QcM7_wkHjWgumuI"
}
```

Surveillus uses API keys to allow access to the API. In order to interact with the Surveillus API, you or your application must first authenticate. All requests to our API require authentication through a given API key.

JSON Web Tokens (JWT) are a standard way of representing security claims between your application and Surveillus API. To generate new tokens you need to authenticate using an API key.  Surveillus expects for the jwtToken to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer $jwtToken`

### HTTP Request

`POST /mist/authenticate`

<aside class="notice">
Use this API to authenticate and get a jwtToken to use with other API calls that need a token for security.
</aside>

## Requests

Surveillus API is based on REST principles and supports the following methods:

Method | Action | 
--------- | -----------
GET | Requests information that is returned as a JSON object
POST | Creates resources with all necessary attributes to create a new object
PUT | Changes and/or replaces resources or collections
DELETE | Removes a specified object

## Responses

The Surveillus API uses the following error responses:

Error Code | Meaning
---------- | -------
400 | Bad Request -- There was something wrong with your request.
401 | Unauthorized -- Your API key is incorrect.
403 | Forbidden -- You do not have access to the requested resource.
404 | Not Found -- The specified resource could not be found.
405 | Method Not Allowed -- You tried to access a resource with an invalid method.
429 | Too Many Requests -- You've made too many API requests in a short time
500 | Internal Server Error -- There was an issue on our end. Please try your request again.
503 | Service Unavailable -- The API is offline for maintenance. Please try again later.
