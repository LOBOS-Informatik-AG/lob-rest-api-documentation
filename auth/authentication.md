# Authentication

Authentication is the verification of the credentials of the connection attempt. This process consists of sending the credentials from the remote access client to the remote access server in an either plaintext or encrypted form by using an authentication protocol.

### Error Responses

**Condition** : if the session was not found.

**Code** : `401 UNAUTHORIZED`

**Content example**

```json
{
    "text": "Ungültige Sitzung."
}
```
## Login

This endpoint allows you to get an authentication token by providing the user credentials

**URL** : `/auth/login/`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : No

**Permissions required** : None

**Body parameters**

The username and password field is required to successfully login

```json
{
    "username": "info@lobos.ch",
    "password": "xxxxxxxx"
}
```

### Success Response

**Condition** : If the login was successfull.

**Code** : `200 OK`

**Content example**

```json
{
    "oUser": {
        "dtLastLogin": 1601456845000,
        "dtRegistration": 1600249405000,
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
    "oAuthorizations": [
        {
            "bIsAuthorized": true,
            "sName": "Download",
            "shtID": 1
        },
        {
            "bIsAuthorized": true,
            "sName": "Belege",
            "shtID": 2
        },
        {
            "bIsAuthorized": false,
            "sName": "Benutzerverwaltung",
            "shtID": 3
        }
    ],
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1bmlxdWVfbmFtZSI6ImluZm9AbG9ib3MuY2giLCJzU2Vzc2lvbklEIjoiM2FlYmIxY2QxMzEyNGQ0NzhiZmU0Yzc5ZmRlYzkwNTciLCJuYmYiOjE2MDE0NDk2NDUsImV4cCI6MTYwMTQ1MDI0NSwiaWF0IjoxNjAxNDQ5NjQ1fQ.RQmh5TOk3QbSIJr8TeKHLE4JRJTEWmIlX8dm8g-3S90"
}
```

### Error Responses

**Condition** : if the username or password aren't valid.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "text": "Ungültiges Passwort"
}
```
or
```json
{
    "text": "Benutzer ungültig"
}
```

## Logout

This endpoint allows you to remove the active session on the server

**URL** : `/auth/logout`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : None

### Success Response

**Condition** : If the logout was successfull.

**Code** : `200 OK`

### Error Responses

**Condition** : if the session was not found.

**Code** : `401 UNAUTHORIZED`

**Content example**

```json
{
    "text": "Ungültige Sitzung."
}
```

## New-pass

This endpoint allows signed in users to set a new password.

**URL** : `/auth/new-pass`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : None

**Body parameters**

The "sNewPassword" field is required to set a new password

```json
{
    "sNewPassword": "xxxxxxxxx"
}
```

### Success Response

**Condition** : If the new password has been successfully set.

**Code** : `200 OK`

**Content example**

```json
{
    "oUser": {
        "dtLastLogin": 1601459178000,
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
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1bmlxdWVfbmFtZSI6ImluZm9AbG9ib3MuY2giLCJzU2Vzc2lvbklEIjoiZWUxYWYzZjAzMmFhNDA0NWIzYjk2YWUxNTljMTIxY2UiLCJuYmYiOjE2MDE0NTE5ODYsImV4cCI6MTYwMTQ1MjU4NiwiaWF0IjoxNjAxNDUxOTg2fQ.3DbH895sEQL9S1ik7Zewk2seFxWZmg-H98bk0mbZG3k"
}
```

### Error Responses

**Condition** : if the session was not found.

**Code** : `401 UNAUTHORIZED`

**Content example**

```json
{
    "text": "Ungültige Sitzung."
}
```

## Refresh-token

This endpoint allows you to refresh the active session

**URL** : `/auth/refresh-token`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : YES

**Permissions required** : None

**Body parameters**

The username and password field is required to successfully login

```json
{
    "username": "info@lobos.ch",
    "password": "xxxxxxxx"
}
```

### Success Response

**Condition** : If the token refresh was successfull.

**Code** : `200 OK`

**Content example**

```json
{
    "oUser": {
        "dtLastLogin": 1601458094000,
        "dtRegistration": 1600249405000,
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
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1bmlxdWVfbmFtZSI6ImluZm9AbG9ib3MuY2giLCJzU2Vzc2lvbklEIjoiMWEzYjY5OWExNDFjNGY3ZTg4NmQ5NDA2YzAzNmI5NTkiLCJuYmYiOjE2MDE0NTA4OTYsImV4cCI6MTYwMTQ1MTQ5NiwiaWF0IjoxNjAxNDUwODk2fQ.znGDJKVw25Pmpyg9U9AHGNBiwcBskPJZD8Jac-GyHWU"
}
```

### Error Responses

**Condition** : if the session was not found.

**Code** : `401 UNAUTHORIZED`

**Content example**

```json
{
    "text": "Ungültige Sitzung."
}
```

## Request-pass

This endpoint allows you to request the possibility to set a new password

**URL** : `/auth/request-pass`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : No

**Permissions required** : None

**Body parameters**

The "sEmail" field is required to request the possibility to set a new password

```json
{
    "sEmail": "awidmer@lobos.ch"
}
```

### Success Response

**Condition** : If the token (link) has been sent to the given email.

**Code** : `200 OK`

### Error Responses

**Condition** : if the user has not been found with the given email.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "text": "eMail existiert nicht"
}
```

## Reset-pass

This endpoint allows you to reset the password

**URL** : `/auth/reset-pass`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : No

**Permissions required** : None

**Body parameters**

The "sRegID" and "sNewPassword" field are required to successfully change the password

```json
{
    "sNewPassword": "xxxxxxxxxx",
    "sRegID": "8d71227207914c7daf5362e6864c0052"
}
```

### Success Response

**Condition** : If the password reset was successfull.

**Code** : `200 OK`

**Content example**

``` json
{
    "oUser": {
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
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1bmlxdWVfbmFtZSI6ImF3aWRtZXJAbG9ib3MuY2giLCJzU2Vzc2lvbklEIjoiNzk1N2ZiMDQ1MmNkNDUxNTljYmM2NGU1ODBlM2JmOTIiLCJuYmYiOjE2MDM5ODQzNjgsImV4cCI6MTYwMzk4NDk2OCwiaWF0IjoxNjAzOTg0MzY4fQ.herMsSuCsBOilgkCYLJW7zothJcs0zD4hF-stdIMBv0"
}
```

### Error Responses

**Condition** : if the username or password aren't valid.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "text": "Entsperren nicht erfolgreich"
}
```