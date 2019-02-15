# Cameras

## Get all cameras

```shell
curl "http://https://dev.surveillus.com/camera"
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

`GET /camera`

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a camera

```shell
curl "http://dev.surveillus.com/mist/mist/camera/2"
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

`GET /camera/:Id`

## Add a Camera

```shell
curl -X POST "http://dev.surveillus.com/camera"
  -H "Authorization: Bearer $jwtToken"
  -d "name= "
  -d ""
  -d ""
```

> The above command returns:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint adds a camera

### HTTP Request

`POST /camera`

### Parameters

Name | Type | Description
--------- | ------- | -----------
Vendor | string | If set to false, the result will include kittens that have already been adopted.
Model | string | If set to false, the result will include kittens that have already been adopted.
IP Address | string | If set to false, the result will include kittens that have already been adopted.

## Update a camera

```shell
curl -X PUT "http://dev.surveillus.com/camera"
  -H "Authorization: Bearer $jwtToken"
  -d "name= "
  -d ""
  -d ""
```

> The above command returns:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint updates a specific camera

### HTTP Request

`PUT camera/:id`

### Parameters

Name | Type | Description
--------- | ------- | -----------
something | false | some description
something | true | some description

## Delete a camera

```shell
curl "http://dev.surveillus.com/mist/camera/1"
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

`DELETE camera/:id`
