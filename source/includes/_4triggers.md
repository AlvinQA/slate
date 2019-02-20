#Triggers

A trigger represents an event that can be fired to generate time stamps and time stamp clips. A trigger has a unique identifier.  You can associate triggers with cameras to generate timestamp clips when the trigger fires.

## Get all triggers

This endpoint retrieves all triggers.

### HTTP Request

`GET /mist/trigger`

## Create a trigger

This endpoint creates a trigger.

### HTTP Request

`POST /mist/trigger`

### Parameters

Name | Type | Description
--------- | ------- | -----------
something | false | Describes something.
another thing | true | Describes another thing.

## Get a trigger

This endpoint retrieves a specific trigger.

### HTTP Request

`GET /mist/trigger/:Id`

## Edit a trigger

This endpoint updates a specific trigger.

### HTTP Request

`PUT /mist/trigger/:Id`

### Parameters

Name | Type | Description
--------- | ------- | -----------
something | false | Describes something.
another thing | true | Describes another thing.

## Delete a trigger

This endpoint deletes a specific trigger.

### HTTP Request

`DELETE /mist/trigger/:Id`
