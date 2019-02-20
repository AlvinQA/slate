# Subscriptions

A subscription is a way to receive a notification when a trigger fires.  It has a unique identifier, criteria that describes triggers and timestamps, and has actions like a web hook URL, email address(s), and text numbers(s).

## Get all subscriptions

This endpoint retrieves all subscriptions.

### HTTP Request

`GET /subscription`

## Create a subscription

```shell
curl -X POST "http://www.example.com/mist/subscription"
  -H "Authorization: Bearer $jwtToken"
  -d " "
  -d " "
  -d " "
```

This endpoint creates a subscription.

### HTTP Request

`POST /mist/subscription`

## Get a subscription

This endpoint retrieves a specific subscription.

### HTTP Request

`GET /mist/subscription/:Id`

## Edit a subscription

This endpoint updates a specific subscription.

### HTTP Request

`PUT /mist/subscription`

## Delete a subscription

This endpoint deletes a specific subscription.

### HTTP Request

`DELETE /mist/subscription/:Id`
