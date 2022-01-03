# Shipping addresses

## Get shipping-addresses

This endpoint allows you to get all the shipping-addresses

**URL** : `/shipping-addresses`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters** : default filters

### Success Response

**Condition** : If shipping-addresses are found.

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 5,
    "lastPage": "1",
    "currentPage": "1",
    "total": 4,
    "data": [
        {
            "lngAddressID": 13,
            "lngContactID": null,
            "lngCustomerID": 10896,
            "lngRouteBaseID": null,
            "sCity": "Zürich",
            "sCompany1": "LOBOS Informatik AG",
            "sCompany2": "",
            "sContact": "",
            "sCountry": "Schweiz",
            "sCountryCode": "CH",
            "sPostBox": "",
            "sStreet": "Auenstrasse 4",
            "sZipBox": "",
            "sZipCode": "8600"
        },
      {}
    ]
}
```

## Get shipping-address by id

This endpoint allows you to get a shipping-address by id

**URL** : `/shipping-addresses/:id`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

### Success Response

**Condition** : If a shipping-address is found.

**Code** : `200 OK`

**Content example**

```json
{
    "lngAddressID": 13,
    "lngContactID": null,
    "lngCustomerID": 10896,
    "lngRouteBaseID": null,
    "sCity": "Zürich",
    "sCompany1": "LOBOS Informatik AG",
    "sCompany2": "",
    "sContact": "",
    "sCountry": "Schweiz",
    "sCountryCode": "CH",
    "sPostBox": "",
    "sStreet": "Auenstrasse 4",
    "sZipBox": "",
    "sZipCode": "8600"
}
```

**or**

**Condition** : if no shipping-address is found.

**Content example**

```json
{
    "text": "Versand-Adresse nicht gefunden"
}
```


## Create shipping-address

This endpoint allows you to create a shipping-address

**URL** : `/shipping-addresses`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```json
{
    "lngAddressID": null,
    "lngContactID": 100955,
    "lngCustomerID": 11722,
    "lngRouteBaseID": null,
    "sCity": "Dübendorf",
    "sCompany1": "LOBOS Informatik AG",
    "sCompany2": "",
    "sContact": "Alexander Widmer",
    "sCountry": "Schweiz",
    "sCountryCode": "CH",
    "sPostBox": "",
    "sStreet": "Auenstrasse 4",
    "sZipBox": "",
    "sZipCode": "8600"
}
```

### Success Response

**Condition** : If the shipping-address is successfully created.

**Code** : `200 OK`

**Content example**

```json
{
    "lngAddressID": 18,
    "lngContactID": 100955,
    "lngCustomerID": 11722,
    "lngRouteBaseID": null,
    "sCity": "Dübendorf",
    "sCompany1": "LOBOS Informatik AG",
    "sCompany2": "",
    "sContact": "Alexander Widmer",
    "sCountry": "Schweiz",
    "sCountryCode": "CH",
    "sPostBox": "",
    "sStreet": "Auenstrasse 4",
    "sZipBox": "",
    "sZipCode": "8600"
}
```

## Update shipping-address

This endpoint allows you to update a shipping-address

**URL** : `/shipping-addresses/:id`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```json
{
    "lngAddressID": 18,
    "lngContactID": 100955,
    "lngCustomerID": 11722,
    "lngRouteBaseID": null,
    "sCity": "Dübendorf",
    "sCompany1": "LOBOS Informatik AG",
    "sCompany2": "",
    "sContact": "Andrea Erni",
    "sCountry": "Schweiz",
    "sCountryCode": "CH",
    "sPostBox": "",
    "sStreet": "Auenstrasse 6",
    "sZipBox": "",
    "sZipCode": "8600"
}
```

### Success Response

**Condition** : If the shipping-address is successfully updated.

**Code** : `200 OK`

**Content example**

```json
{
    "lngAddressID": 18,
    "lngContactID": 100955,
    "lngCustomerID": 11722,
    "lngRouteBaseID": null,
    "sCity": "Dübendorf",
    "sCompany1": "LOBOS Informatik AG",
    "sCompany2": "",
    "sContact": "Andrea Erni",
    "sCountry": "Schweiz",
    "sCountryCode": "CH",
    "sPostBox": "",
    "sStreet": "Auenstrasse 6",
    "sZipBox": "",
    "sZipCode": "8600"
}
```

## Delete shipping-address

This endpoint allows you to delete a shipping-address

**URL** : `/shipping-addresses/:id`

**Method** : <img src="https://img.shields.io/badge/DELETE%20-%23323330.svg?&style=flat&color=red"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```
None
```

### Success Response

**Condition** : If the shipping-address is deleted successfully.

**Code** : `200 OK`

**Content example**

```
None
```
