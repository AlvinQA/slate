#Triggers

A trigger represents an event that can be fired to generate time stamps and time stamp clips. A trigger has a unique identifier.  You can associate triggers with cameras to generate timestamp clips when the trigger fires.

## Get all triggers

This endpoint retrieves all triggers.

### HTTP Request

`GET /trigger`

## Create a trigger

This endpoint creates a trigger.

### HTTP Request

`POST /trigger`

### Parameters

Parameter | Type | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

## Get a trigger

This endpoint retrieves a specific trigger.

### HTTP Request

`GET /trigger/:Id

## Edit a trigger

This endpoint updates a specific trigger.

### HTTP Request

`PUT /trigger/:Id`

### Parameters

Parameter | Type | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

## Delete a trigger

This endpoint deletes a specific trigger.

### HTTP Request

`DELETE /trigger/:Id`
