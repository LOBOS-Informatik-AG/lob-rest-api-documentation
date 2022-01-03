# Favorites

## Get favorite-lists

This endpoint allows you to get all the favorites-list

**URL** : `/favorites`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters** : Default filters

### Success Response

**Code** : `200 OK`

**Content example**

```json
[
    {
        "gListID": "9c29a83f-6382-4264-a8b4-2515713cc7f9",
        "sListname": "My favorites"
    },
  {}
]
```

## Get favorite-list by id

This endpoint allows you to get a favorites-list by id

**URL** : `/favorites/:id`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

### Success Response

**Condition** : If the favorite-list is found.

**Code** : `200 OK`

**Content example**

```json
{
    "gListID": "9c29a83f-6382-4264-a8b4-2515713cc7f9",
    "sListname": "Test"
}
```

**or**

**Condition** : if no favorite-list is found.

**Content example**

```json
{
    "text": "Kein(e) Favorit(en) gefunden"
}
```


## Create favorite-list

This endpoint allows you to create a favorites-list

**URL** : `/favorites/:id`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```json
{
    "sListname": "Test 1463"
}
```

### Success Response

**Condition** : If the favorite-list is successfully created.

**Code** : `200 OK`

**Content example**

```json
{
    "gListID": "b31db048-7f79-4366-90c2-e9053aa6e376",
    "sListname": "Test 1463"
}
```

## Update favorite-list

This endpoint allows you to update a favorites-list

**URL** : `/favorites/:id`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```json
{
    "gListID": "cb3aac5b-b139-4b64-9baf-dc717adbe0a0",
    "sListname": "Test 37"
}
```

### Success Response

**Condition** : If the favorite-list is successfully updated.

**Code** : `200 OK`

**Content example**

```json
{
    "gListID": "cb3aac5b-b139-4b64-9baf-dc717adbe0a0",
    "sListname": "Test 37"
}
```

## Delete favorite-list

This endpoint allows you to delete a favorite

**URL** : `/favorites/:id`

**Method** : <img src="https://img.shields.io/badge/DELETE%20-%23323330.svg?&style=flat&color=red"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
None
```

### Success Response

**Condition** : If the favorite-list is deleted successfully.

**Code** : `200 OK`

**Content example**

```
None
```

## Get favorite-items

This endpoint allows you to get all the favorites-list

**URL** : `/favorites/:id/items`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters** : Default filters

### Success Response

**Code** : `200 OK`

**Content example**

```json
[
    {
        "decQuantity": 66,
        "gListID": "5b6d093d-cf88-4070-b089-bb23b5d5d714",
        "oArticle": {
            "decQuantityPackage": null,
            "decSalesPrice1": 532.00,
            "lngSalesPriceUnit": 1,
            "sArticleCode1": "Quark",
            "sArticleCode2": "Software",
            "sArticleCode3": "Grafik - DTP",
            "sArticleID": "7600165E",
            "sEAN": "",
            "sGTIN": {
                "isNotNull": false,
                "value": ""
            },
            "sName": "QuarkXPress Passport Mac UV",
            "sQuantityUnitPackage": "",
            "sQuantityUnitSales": "Stk",
            "shtPlanningCode": 4,
            "shtStatus": 2
        },
        "shtItemID": 1
    },
  {}
]
```

## Create favorite-item

This endpoint allows you create a favorite

**URL** : `/favorites/:id/items`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    "decQuantity": 66.234,
    "gListID": "5b6d093d-cf88-4070-b089-bb23b5d5d714",
    "oArticle": {
        "decQuantityPackage": null,
        "decSalesPrice1": null,
        "lngSalesPriceUnit": null,
        "sArticleCode1": null,
        "sArticleCode2": null,
        "sArticleCode3": null,
        "sArticleID": "2000045H",
        "sEAN": null,
        "sGTIN": "",
        "sName": null,
        "sQuantityUnitPackage": null,
        "sQuantityUnitSales": null,
        "shtPlanningCode": null,
        "shtStatus": null
    },
    "shtItemID": null
}
```

### Success Response

**Condition** : If the favorite is created.

**Code** : `200 OK`

**Content example**

```json
{
    "decQuantity": 66.234,
    "gListID": "5b6d093d-cf88-4070-b089-bb23b5d5d714",
    "oArticle": {
        "decQuantityPackage": null,
        "decSalesPrice1": 603.16,
        "lngSalesPriceUnit": 1,
        "sArticleCode1": "Sony",
        "sArticleCode2": "Peripherie",
        "sArticleCode3": "Monitore",
        "sArticleID": "2000045H",
        "sEAN": "",
        "sGTIN": {
            "isNotNull": false,
            "value": ""
        },
        "sName": "Monitor 15 sony TFT HS53 Blue\"",
        "sQuantityUnitPackage": "",
        "sQuantityUnitSales": "Stk",
        "shtPlanningCode": 4,
        "shtStatus": 2
    },
    "shtItemID": 8
}
```

## Update favorite-item

This endpoint allows you to update a favorite

**URL** : `/favorites/:id/items/:id`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    "decQuantity": 66.234,
    "gListID": "5b6d093d-cf88-4070-b089-bb23b5d5d714",
    "oArticle": {
        "decQuantityPackage": null,
        "decSalesPrice1": 532.00,
        "lngSalesPriceUnit": 1,
        "sArticleCode1": "Quark",
        "sArticleCode2": "Software",
        "sArticleCode3": "Grafik - DTP",
        "sArticleID": "7600165E",
        "sEAN": "",
        "sGTIN": {
            "isNotNull": false,
            "value": ""
        },
        "sName": "QuarkXPress Passport Mac UV",
        "sQuantityUnitPackage": "",
        "sQuantityUnitSales": "Stk",
        "shtPlanningCode": 4,
        "shtStatus": 2
    },
    "shtItemID": 9
}
```

### Success Response

**Condition** : If the favorite is updated successfully.

**Code** : `200 OK`

**Content example**

```json
{
    "decQuantity": 66.234,
    "gListID": "5b6d093d-cf88-4070-b089-bb23b5d5d714",
    "oArticle": {
        "decQuantityPackage": null,
        "decSalesPrice1": 532.00,
        "lngSalesPriceUnit": 1,
        "sArticleCode1": "Quark",
        "sArticleCode2": "Software",
        "sArticleCode3": "Grafik - DTP",
        "sArticleID": "7600165E",
        "sEAN": "",
        "sGTIN": {
            "isNotNull": false,
            "value": ""
        },
        "sName": "QuarkXPress Passport Mac UV",
        "sQuantityUnitPackage": "",
        "sQuantityUnitSales": "Stk",
        "shtPlanningCode": 4,
        "shtStatus": 2
    },
    "shtItemID": 9
}
```

## Delete favorite-item

This endpoint allows you to delete a favorite

**URL** : `/favorites/:id/items/:id`

**Method** : <img src="https://img.shields.io/badge/DELETE%20-%23323330.svg?&style=flat&color=red"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```
None
```

### Success Response

**Condition** : If the favorite is deleted successfully.

**Code** : `200 OK`

**Content example**

```
None
```