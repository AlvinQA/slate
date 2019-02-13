# Cameras

## Get all cameras

```shell
curl "http://https://dev.surveillus.com/api/camera"
  -H "Authorization: Bearer $TOKEN"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all cameras.

### HTTP Request

`GET /api/camera`

### Parameters

Parameter | Type | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a camera

```shell
curl "http://dev.surveillus.com/mist/api/mist/camera/2"
  -H "Authorization: Bearer $TOKEN"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific camera.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET api/camera/:Id`

### Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Add a Camera

This endpoint adds a camera

### HTTP Request

'POST api/camera'

### Parameters

Parameter | Type | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

## Update a camera

This endpoint updates a specific camera

### HTTP Request

'PUT api/camera/:id'

### Parameters

Parameter | Type | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

## Delete a camera

```shell
curl "http://dev.surveillus.com/mist/api/camera/1"
  -X DELETE
  -H "Authorization: Bearer $TOKEN"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific camera.

### HTTP Request

`DELETE api/camera/:id`

### URL Parameters

Parameter | Description
--------- | -----------
Id | The ID of the camera to delete
