#Exhibits

## Get all exhibits

```shell
curl "http://dev.surveillus.com/mist/api/exhibit/"
  -H "Authorization: Bearer $TOKEN"
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

This endpoint retrieves all exhibits.

### HTTP Request

`GET /api/exhibit/list/:start/:stop`

### Parameters

Parameter | Type | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

## Get the start of an exhibit

```shell
curl "http://dev.surveillus.com/mist/api/exhibit/start/:id"
  -H "Authorization: Bearer $TOKEN"
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

This endpoint retrieves a snapshot jpeg file of the first frame of a specific exhibit

### HTTP Request

`GET /api/exhibit/start/:id`

### Parameters

## Get the middle of an exhibit

```shell
curl "http://dev.surveillus.com/mist/api/exhibit/middle/:id"
  -H "Authorization: Bearer $TOKEN"
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

This endpoint retrieves the middle of a specific exhibit

### HTTP Request

`GET /api/exhibit/middle/:id`

### Parameters

## Get the end of an exhibit

```shell
curl "http://dev.surveillus.com/mist/api/exhibit/end/:id"
  -H "Authorization: Bearer $TOKEN"
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

This endpoint retrieves a snapshot jpeg file of the last frame of a specific exhibit

### HTTP Request

`GET /api/exhibit/stop/:id`

### Parameters

## Get the mp4 clip of an exhibit

```shell
curl "http://dev.surveillus.com/mist/api/exhibit/clip/:id"
  -H "Authorization: Bearer $TOKEN"
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

This endpoint downloads the mp4 file of a specific exhibit.

### HTTP Request

`GET /api/exhibit/clip/:id`

### Parameters
