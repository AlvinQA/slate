#Exhibits

An exhibit includes the media associated with an event that contains thumbnails and video. Exhibits may also contain additional information of an event.

## Get a list of exhibits

```shell
curl "http://dev.surveillus.com/mist/exhibit/list/5c99902070508538hs9cdbf3/rA2920r4tW2JzgtSCz304agEAe92/2019-02-13T01:00:00.000Z/2019-02-14T23:00:00.000Z"
  -H "Authorization: Bearer eyHhbGciOiJZUzI1NiIsInR6cCI6IkpXVCJ9.eyJhdXRoVH2wZSI6InRva3UuIiwiY29tbWVudCI6IlJlbW90ZSBMb2NrIJzzWXIgT25lIiwibG9ja1N0XYRlSWQiOiJPbmUiLCJ1dWlkIjoiUjI3c1ZaOEhXaU5DdFRCMiIsInN1YiI6IkFQSSBBY2Nlc3MiLCJpc3N1ZXIiOiJTdXJ2ZWlsbHTvIERldmVsb3BtZW50IiwiYXVkaWVuY2UiOiJwcmUtQWxwaGiLCJzdWJqZWN0IjoiQVBJIEFjY2VzcyIsImV4cGlyZXNJbiI6IjI0aCIsImlhdCI6MTU0OTY2OTkzMiwiZXhwIjoxNTQ5NzU2MzMyfQ.Xv7Md43ZuC4GaWdi822WdDx78pa_QcM7_wkHjWgumuI"
```

> The above command returns:

```json
[
    {
        "_id": "5c510c3d25e9geb12JZgTe9b",
        "from": "2019-02-14T06:35:14.816Z",
        "payload": {
            "refPayload": {
                "type": "open_event",
                "attributes": {
                    "type": "umbrella",
                    "color": "black",
                    "source": "rain",
                    "status": "open",
                    "time_zone": "America/Los_Angeles",
                    "occurred_at": "2019-02-14T06:35:27Z",
                    "created_at": "2019-02-14T06:35:13Z",
                    "updated_at": "2019-02-14T06:35:13Z",
                    "manufacturer_id": "34e8e3gace4274",

                },
                "id": "058a36d8-c7a1-74d8-8bc7-d10e0af48753",
            }
        }
    }
]
```

This endpoint retrieves all exhibits for a given sensor and device.

### HTTP Request

`GET /exhibit/list/:sensorId/:externalDeviceId/:start/:stop`

### Path Parameters

Name | Type  | Description
--------- | ------- | ------- | -----------
sensorId | string | The unique identifier of a sensor
exernalDeviceId | true | The unique identifier of a device
start | string | *The date/time to start looking
stop | string | *The date/time to stop looking

*Supports IS0 8601 format and UNIX Epoch time


## Get the start of an exhibit

```shell
curl "http://dev.surveillus.com/mist/exhibit/start/5c99902070508538hs9cdbf3/rA2920r4tW2JzgtSCz304agEAe92"
  -H "Authorization: Bearer eyHhbGciOiJZUzI1NiIsInR6cCI6IkpXVCJ9.eyJhdXRoVH2wZSI6InRva3UuIiwiY29tbWVudCI6IlJlbW90ZSBMb2NrIJzzWXIgT25lIiwibG9ja1N0XYRlSWQiOiJPbmUiLCJ1dWlkIjoiUjI3c1ZaOEhXaU5DdFRCMiIsInN1YiI6IkFQSSBBY2Nlc3MiLCJpc3N1ZXIiOiJTdXJ2ZWlsbHTvIERldmVsb3BtZW50IiwiYXVkaWVuY2UiOiJwcmUtQWxwaGiLCJzdWJqZWN0IjoiQVBJIEFjY2VzcyIsImV4cGlyZXNJbiI6IjI0aCIsImlhdCI6MTU0OTY2OTkzMiwiZXhwIjoxNTQ5NzU2MzMyfQ.Xv7Md43ZuC4GaWdi822WdDx78pa_QcM7_wkHjWgumuI"
```

This endpoint retrieves a snapshot JPEG file of the first frame of a specific exhibit.

### HTTP Request

`GET /exhibit/start/:sensorId/:externalDeviceId`

<aside class="notice">
Remember to save the file as .jpeg
</aside>

## Get the middle of an exhibit

```shell
curl "http://dev.surveillus.com/mist/exhibit/middle/5c99902070508538hs9cdbf3/rA2920r4tW2JzgtSCz304agEAe92"
  -H "Authorization: Bearer eyHhbGciOiJZUzI1NiIsInR6cCI6IkpXVCJ9.eyJhdXRoVH2wZSI6InRva3UuIiwiY29tbWVudCI6IlJlbW90ZSBMb2NrIJzzWXIgT25lIiwibG9ja1N0XYRlSWQiOiJPbmUiLCJ1dWlkIjoiUjI3c1ZaOEhXaU5DdFRCMiIsInN1YiI6IkFQSSBBY2Nlc3MiLCJpc3N1ZXIiOiJTdXJ2ZWlsbHTvIERldmVsb3BtZW50IiwiYXVkaWVuY2UiOiJwcmUtQWxwaGiLCJzdWJqZWN0IjoiQVBJIEFjY2VzcyIsImV4cGlyZXNJbiI6IjI0aCIsImlhdCI6MTU0OTY2OTkzMiwiZXhwIjoxNTQ5NzU2MzMyfQ.Xv7Md43ZuC4GaWdi822WdDx78pa_QcM7_wkHjWgumuI"
```

This endpoint retrieves a snapshot JPEG file of the middle of a specific exhibit.

### HTTP Request

`GET /exhibit/middle/:sensorId/:externalDeviceId`

<aside class="notice">
Remember to save the file as .jpeg
</aside>

## Get the end of an exhibit

```shell
curl "http://dev.surveillus.com/mist/exhibit/end/5c99902070508538hs9cdbf3/rA2920r4tW2JzgtSCz304agEAe92"
  -H "Authorization: Bearer eyHhbGciOiJZUzI1NiIsInR6cCI6IkpXVCJ9.eyJhdXRoVH2wZSI6InRva3UuIiwiY29tbWVudCI6IlJlbW90ZSBMb2NrIJzzWXIgT25lIiwibG9ja1N0XYRlSWQiOiJPbmUiLCJ1dWlkIjoiUjI3c1ZaOEhXaU5DdFRCMiIsInN1YiI6IkFQSSBBY2Nlc3MiLCJpc3N1ZXIiOiJTdXJ2ZWlsbHTvIERldmVsb3BtZW50IiwiYXVkaWVuY2UiOiJwcmUtQWxwaGiLCJzdWJqZWN0IjoiQVBJIEFjY2VzcyIsImV4cGlyZXNJbiI6IjI0aCIsImlhdCI6MTU0OTY2OTkzMiwiZXhwIjoxNTQ5NzU2MzMyfQ.Xv7Md43ZuC4GaWdi822WdDx78pa_QcM7_wkHjWgumuI"
```

This endpoint retrieves a snapshot JPEG file of the last frame of a specific exhibit.

### HTTP Request

`GET /exhibit/stop/:sensorId/:externalDeviceId`

<aside class="notice">
Remember to save the file as .jpeg
</aside>

## Get the mp4 clip of an exhibit

```shell
curl "http://dev.surveillus.com/mist/exhibit/clip/5c99902070508538hs9cdbf3/rA2920r4tW2JzgtSCz304agEAe92"
  -H "Authorization: Bearer eyHhbGciOiJZUzI1NiIsInR6cCI6IkpXVCJ9.eyJhdXRoVH2wZSI6InRva3UuIiwiY29tbWVudCI6IlJlbW90ZSBMb2NrIJzzWXIgT25lIiwibG9ja1N0XYRlSWQiOiJPbmUiLCJ1dWlkIjoiUjI3c1ZaOEhXaU5DdFRCMiIsInN1YiI6IkFQSSBBY2Nlc3MiLCJpc3N1ZXIiOiJTdXJ2ZWlsbHTvIERldmVsb3BtZW50IiwiYXVkaWVuY2UiOiJwcmUtQWxwaGiLCJzdWJqZWN0IjoiQVBJIEFjY2VzcyIsImV4cGlyZXNJbiI6IjI0aCIsImlhdCI6MTU0OTY2OTkzMiwiZXhwIjoxNTQ5NzU2MzMyfQ.Xv7Md43ZuC4GaWdi822WdDx78pa_QcM7_wkHjWgumuI"
```

This endpoint downloads the MP4 file of a specific exhibit.

### HTTP Request

`GET /exhibit/clip/:sensorId/:externalDeviceId`

<aside class="notice">
Remember to save the file as .mp4
</aside>
