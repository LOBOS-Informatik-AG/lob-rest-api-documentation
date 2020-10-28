# Users

## Get users

This endpoint allows you to select all E-Users from eNVenta (filtered by customer-Id)

**URL** : `/users`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters**

```
// TODO
```

### Success Response

**Condition** : If users are found.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "dtLastLogin": 1602846058000,
        "dtRegistration": 1601465682000,
        "lngContactID": 95253,
        "lngCustomerID": 10010,
        "sEmail": "info@lobos.ch",
        "sFirstName": "Remo",
        "sFormOfAdress": "Herr",
        "sLastName": "Vetterli",
        "sMobilePhone": "",
        "sPhone": "",
        "sUserName": "info@lobos.ch",
        "shtLanguageID": 1
    },
    ...
]
```

**or**

**Condition** : no users are found.

**Content example**

```json
{
    "text": "Kein(e) User(s) gefunden."
}
```

## Get user by id

This endpoint allows you to get a user by id

**URL** : `/users/:id`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

### Success Response

**Condition** : If the user is found.

**Code** : `200 OK`

**Content example**

```json
{
    "dtLastLogin": 1602846058000,
    "dtRegistration": 1601465682000,
    "lngContactID": 95253,
    "lngCustomerID": 10010,
    "sEmail": "info@lobos.ch",
    "sFirstName": "Remo",
    "sFormOfAdress": "Herr",
    "sLastName": "Vetterli",
    "sMobilePhone": "",
    "sPhone": "",
    "sUserName": "info@lobos.ch",
    "shtLanguageID": 1
}
```

**or**

**Condition** : if no user is found.

**Content example**

```json
{
    "text": "Keinen Benutzer gefunden."
}
```


## Create user

This endpoint allows you to create a user

**URL** : `/users/:id`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    "dtLastLogin": null,
    "dtRegistration": 1581951949000,
    "lngContactID": 103211,
    "lngCustomerID": 10010,
    "sEmail": "rbormolini@lobos.ch",
    "sFirstName": "Reto",
    "sFormOfAdress": "Herr",
    "sLastName": "Bormolini",
    "sMobilePhone": "+41 79 253 46 18",
    "sPhone": "+41 44 825 77 41",
    "sUserName": "rbormolini@lobos.ch",
    "shtLanguageID": 1
}
```

### Success Response

**Condition** : If the user is successfully created.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

### Error Response

**Condition** : If the there is an error during creation.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "text": "Fehler beim Erstellen des Benutzers"
}
```

## Update user

This endpoint allows you to update a user

**URL** : `/users/:id`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    "dtLastLogin":null,
    "dtRegistration":1581948349000,
    "lngContactID":308,
    "lngCustomerID":200645,
    "sEmail":"rvetterli@lobos.ch",
    "sFirstName":"Remo",
    "sFormOfAdress":"Herr",
    "sLastName":"Vetterli",
    "sMobilePhone":"",
    "sPhone":"0448257777",
    "sUserName":"rvetterli@lobos.ch",
    "shtLanguageID":2
}
```

### Success Response

**Condition** : If the user is successfully updated.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

## Delete user

This endpoint allows you to delete a user

**URL** : `/users/:id`

**Method** : <img src="https://img.shields.io/badge/DELETE%20-%23323330.svg?&style=flat&color=red"/>

**Auth required** : Yes

**Permissions required** : No

### Success Response

**Condition** : If the user is successfully deleted.

**Code** : `200 OK`
