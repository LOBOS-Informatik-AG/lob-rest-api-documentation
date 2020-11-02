# Countries

## Get countries

This endpoint allows you to get all countries with the attribute `ecomm = true`

**URL** : `/countries`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : No

**Permissions required** : No

**Query parameters** : Default filters

### Success Response

**Condition** : If countries with the flag `ecomm = true` are found.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "sCountryCode": "CH",
        "sIsoCode": "CH",
        "sName": "Schweiz",
        "shtCountryID": 41,
        "shtLanguageID": 1
    },
    ...
]
```

**or**

**Condition** : no countries are found.

**Content example**

```json
{
    "text": "Keine Länder gefunden."
}
```

