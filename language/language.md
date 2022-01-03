## Get languages

This endpoint allows you to get all the languages defined by the app params

**URL** : `/languages`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : No

**Permissions required** : No

**Query parameters**

```
None
```

### Success Response

**Code** : `200 OK`

**Content example**

```json
[
    {
        "sIsoCode": "de",
        "sLanguageName": "Deutsch",
        "shtIsDefault": 1,
        "shtLanguageID": 1
    },
    {
        "sIsoCode": "fr",
        "sLanguageName": "Französisch",
        "shtIsDefault": 0,
        "shtLanguageID": 3
    },
    {
        "sIsoCode": "en",
        "sLanguageName": "Englisch",
        "shtIsDefault": 0,
        "shtLanguageID": 2
    }
]
```