# Bending

## Get buildingsites

This endpoint allows you to GET all buildingsites who have set the attribute `Show in banding App`

**URL** : `/buildingsites`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters**

``` json
None
```

### Success Response

**Condition** : If contacts are found.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "dtAlterationDate": "1520416939000",
        "dtEntryDate": "1511255659000",
        "lngContactId": 101381,
        "sDepartmentName": "2",
        "sEmail": "awidmer@lobos.ch",
        "sFirstName": "Alexander",
        "sFormOfAdress": "Herr",
        "sLastName": "Widmer",
        "sMobilePhone": "",
        "sPhone": "044 825 77 77",
        "sPosition": "",
        "shtInactive": null
    },
    ...
]
```

**or**

**Condition** : no contacts are found.

**Content example**

```json
{
    "text": "Keine Kontakte gefunden."
}
```

