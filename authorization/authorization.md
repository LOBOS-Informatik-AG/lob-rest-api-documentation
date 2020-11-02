# Authorization

## Get roles

This endpoint allows you to get all authorization roles defined in eNVenta

**URL** : `/roles`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : No

**Permissions required** : No

**Query parameters**

```
None
```

### Success Response

**Condition** : If roles are found.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "lngID": 101,
        "sRoleName": "Admin"
    },
    {
        "lngID": 102,
        "sRoleName": "User"
    }
]
```

**or**

**Condition** : no roles are found.

**Content example**

```json
{
    "text": "Keine Berechtigungsgruppen gefunden."
}
```