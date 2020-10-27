# User

## Get users

This endpoint allows you to select all E-Users from eNVenta (filtered by customer-Id)

**URL** : `/users`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters**

```
// TODO
```

### Success Response

**Condition** : If tickets are found.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "dtLastLogin": 1601630878000,
        "dtRegistration": 1601458482000,
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

