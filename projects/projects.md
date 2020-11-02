# Projects

## Get projects

This endpoint allows you to get all the projects

**URL** : `/projects`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters** : Default filters

### Success Response

**Condition** : If projects are found.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "dtEntryDate": 1301484937000,
        "lngCustomerID": 10010,
        "lngProjectID": 10010,
        "sCity": "",
        "sCompany1": "",
        "sCompany2": "",
        "sCountry": "",
        "sCountryCode": "",
        "sProjectName": "LOBOS E-Commerce Shop",
        "sStreet": "",
        "sZipCode": "",
        "shtStatus": 0
    }
]
```

**or**

**Condition** : no projects are found.

**Content example**

```json
{
    "text": "Keine Projekte gefunden."
}
```