# Bending

## Get buildingsites

This endpoint allows you to GET all buildingsites who have set the attribute `Show in banding App`

**URL** : `/buildingsites`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters** : bFavorite (true OR false) and default filters

### Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 5,
    "lastPage": "1",
    "currentPage": "1",
    "total": 2,
    "data": [
        {
            "bFavorite": true,
            "dtEntryDate": 1301484937000,
            "lngCustomerID": 10010,
            "lngProjectID": 10010,
            "sProjectName": "LOBOS Informatik AG"
        },
        {
            "bFavorite": true,
            "dtEntryDate": 1623152002000,
            "lngCustomerID": 10010,
            "lngProjectID": 2021849,
            "sProjectName": "LOBOS Informatik AG"
        }
    ]
}
```


## Get buildingsites-items

This endpoint allows you to GET all items of a buildingsites.<br/>General Condition:  Bendingapp-Status != Delivered OR Bendingapp-DeliveryDate >= (DayDate - (BendingappParameter[DaysShowDelivered]))

**URL** : `/buildingsites/:id/items`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters** : default filters

### Success Response

**Condition** : If buildingsites are found.

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 5,
    "lastPage": "1",
    "currentPage": "1",
    "total": 1,
    "data": [
        {
            "decTotalOrderNetWeight": 60.000000000,
            "dtDeliveryDate": 1625270400000,
            "lngOrderID": 2073581,
            "sBauteil": "BAUUU",
            "sOrderType": "5",
            "sTrennPlanNr": "TestRB",
            "shtBendingAppStatus": 2
        }
    ]
}
```

## Get buildingsites-statistics

This endpoint allows you to GET a statistic over all buildingsites.

**URL** : `/buildingsites-statistics`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters** : default filters

### Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 5,
    "lastPage": "1",
    "currentPage": "1",
    "total": 3,
    "data": [
        {
            "decTotalWeight": 60.000000000,
            "lngProjectID": 10010,
            "sProjectName": "LOBOS Informatik AG"
        },
        {
            "decTotalWeight": 0,
            "lngProjectID": 2019727,
            "sProjectName": "Praktikum"
        },
        {
            "decTotalWeight": 0,
            "lngProjectID": 2021849,
            "sProjectName": "LOBOS Informatik AG"
        }
    ]
}
```

## Get buildingsites-statistics-items

This endpoint allows you to GET a statistic over a selected buildingsite.

**URL** : `/buildingsites-statistics/:id/items`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : No

**Query parameters** : default filters

### Success Response

**Code** : `200 OK`

**Content example**

```json
[
    {
        "decWeight": 60.000000000,
        "dtDatum": 1625270400000,
        "lngProjectID": 10010,
        "sArticleName": "PC Leser",
        "sProjectName": "LOBOS Informatik AG"
    },
    {
        "decWeight": 60.000000000,
        "dtDatum": null,
        "lngProjectID": 10010,
        "sArticleName": "PC Leser",
        "sProjectName": "LOBOS Informatik AG"
    }
]
```

## Update buildingsites

This endpoint allows you to update a buildingsite.

**URL** : `/buildingsites/:id`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    "bFavorite": true,
    "dtEntryDate": 1301484937000,
    "lngCustomerID": 10010,
    "lngProjectID": 2019727,
    "sProjectName": "LOBOS Informatik AG"
}
```

### Success Response

**Condition** : If the buildingsite is successfully updated.

**Code** : `200 OK`

**Content example**

```json
{
    "bFavorite": true,
    "dtEntryDate": 1301484937000,
    "lngCustomerID": 10010,
    "lngProjectID": 2019727,
    "sProjectName": "LOBOS Informatik AG"
}
```

## Release buildingsites

This endpoint allows you to release a buildingsite.

**URL** : `/buildingsites/release`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    "lngOrderID": 2073581,
    "sOrderType": "5",
    "dtDeliveryDate": 1623628800000,
    "dtNewDeliveryDate": 1625270400000,
    "bCrane:": true,
    "sRemark": "helloooooo",
    "shtBendingAppStatus": 1
}

```

### Success Response

**Condition** : If the buildingsite is successfully released.

**Code** : `200 OK`

**Content example**

```json
{
    "text": "Auftrag ausgelöst"
}
```