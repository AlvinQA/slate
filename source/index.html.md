---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - curl

includes:
  - exhibits
  - cameras
  - subscriptions
  - triggers
  - associations
  - testing
  - errors

search: true
---

# Introduction

Welcome to the Surveillus API documentation! You can use our API to access Surveillus API endpoints, which can get information on various..

The Surveillus API provides client access to...

The base address for Surveillus API is https://dev.surveillus.com/mist

## Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "https://dev.surveillus.com/api/authenticate"
  -H "Authorization: Bearer $TOKEN"
```

> Make sure to replace `meowmeowmeow` with your API key.

Surveillus uses API keys to allow access to the API. In order to interact with the Surveillus API, you or your application must first authenticate. All requests to our API require authentication either through a given username/password or an API key.

Surveillus expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer $TOKEN`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
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

