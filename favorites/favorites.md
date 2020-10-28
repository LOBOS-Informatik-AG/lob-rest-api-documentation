# Favorites

## Get favorite-lists

This endpoint allows you to get all the favorites-list

**URL** : `/favorites`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters**

``` json
// TODO
```

### Success Response

**Condition** : If favorites are found.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

**or**

**Condition** : no favorites are found.

**Content example**

```json
{
    "text": "Keine Favoritenlisten gefunden."
}
```

## Get favorite-list by id

This endpoint allows you to get a favorites-list by id

**URL** : `/favorites/:id`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters**

``` json
// TODO
```

### Success Response

**Condition** : If favorites are found.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

**or**

**Condition** : no favorites are found.

**Content example**

```json
{
    "text": "Keine Favoritenliste gefunden."
}
```


## Create favorite-list

This endpoint allows you to create a favorites-list

**URL** : `/favorites/:id`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    "gListID": null,
    "sListname": "Test 1453"
}
```

### Success Response

**Condition** : If the favorite-list is successfully created.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

## Update favorite-list

This endpoint allows you to update a favorites-list

**URL** : `/favorites/:id`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
        "gListID": "086FEB83-A7C9-4171-B37C-73ED1E89DFFA",
        "sListname": "changed name"
}
```

### Success Response

**Condition** : If the favorite-list is successfully updated.

**Code** : `200 OK`

**Content example**

```json
// TODO
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

```json
None
```

## Get favorite-items

This endpoint allows you to get all the favorites-list

**URL** : `/favorites/:id/items`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters**

``` json
// TODO
```

### Success Response

**Condition** : If favorites are found.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

**or**

**Condition** : no favorites are found.

**Content example**

```json
{
    "text": "Keine Favoriten gefunden."
}
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
// TODO
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
    "shtItemID": 5
}
```

### Success Response

**Condition** : If the favorite is updated successfully.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

## Delete favorite-item

This endpoint allows you to delete a favorite

**URL** : `/favorites/:id/items/:id`

**Method** : <img src="https://img.shields.io/badge/DELETE%20-%23323330.svg?&style=flat&color=red"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
None
```

### Success Response

**Condition** : If the favorite is deleted successfully.

**Code** : `200 OK`

**Content example**

```json
None
```