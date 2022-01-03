# Users

## Get users

This endpoint allows you to select all E-Users from eNVenta (filtered by customer-Id)

**URL** : `/users`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters** : default filters

### Success Response

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
    {}
]
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

```json
{
    "dtLastLogin": 1602846058000,
    "dtRegistration": 1601465682000,
    "lngContactID": null,
    "lngCustomerID": 10010,
    "sEmail": "awidmer@lobos.ch",
    "sFirstName": "Alexander",
    "sFormOfAdress": "Herr",
    "sLastName": "Widmer",
    "sMobilePhone": "",
    "sPhone": "",
    "sUserName": "awidmer@lobos.ch",
    "shtLanguageID": 2
}
```

### Success Response

**Condition** : If the user is successfully created.

**Code** : `200 OK`

**Content example**

```json
{
    "dtLastLogin": 1602853258000,
    "dtRegistration": 1603987881000,
    "lngContactID": 103212,
    "lngCustomerID": 10010,
    "sEmail": "awidmer@lobos.ch",
    "sFirstName": "Alexander",
    "sFormOfAdress": "Herr",
    "sLastName": "Widmer",
    "sMobilePhone": "",
    "sPhone": "",
    "sUserName": "awidmer@lobos.ch",
    "shtLanguageID": 2
}
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
    "shtLanguageID": 2
}
```

### Success Response

**Condition** : If the user is successfully updated.

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
    "shtLanguageID": 2
}
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
