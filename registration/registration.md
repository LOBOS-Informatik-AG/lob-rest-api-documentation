# Registration

## Register

This endpoint allows new users to register an account

**URL** : `/registration`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : No

**Permissions required** : None

**Body parameters**

The following fields are required to successfully register

```json
{
    "sCompany1": "TestFirma5",
    "sStreet": "Teststrasse 123",
    "sZipCode": "1234",
    "sCity": "Testort",
    "sContactFormOfAddress": "Herr",
    "sContactFirstName": "Tester",
    "sContactLastName": "Muster",
    "sContactEmail": "TestEmail5@test.test",
    "sPassword": "123456",
    "sCountryCode": "AT",
    "sCountry": "Österreich",
    "sVATRegNo": "111222"
}
```