# Tickets (Call-Center)

## Get tickets

This endpoint allows you to get the tickets by the specified filters

**URL** : `/tickets`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters**

- dtEntryDate[gte] / [lte] example: `/tickets?dtEntryDate[gte]=1596545331448&dtEntryDate[lte]=15996625521448`
- dtAlterationDate[gte] / [lte]
- lngCategory
- lngContactID
- lngPriority
- lngStatus
- sAlterationUser
- sB22Description
- sB22Responsible
- sEntryUser

### Success Response

**Condition** : If tickets are found.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "dtAlterationDate": null,
        "dtEntryDate": 1579701140000,
        "lngCategory": null,
        "lngContactID": 97382,
        "lngPriority": 1,
        "lngStatus": 1,
        "lngTicketID": 2020012148,
        "sAlterationUser": "",
        "sB22Description": "",
        "sB22Responsible": "",
        "sEntryUser": "CFI"
    },
    ...
]
```

**or**

**Condition** : no tickets are found.

**Content example**

```json
{
    "text": "Kein(e) Ticket(s) gefunden."
}
```

### Error Responses

**Condition** : if the username or password aren't valid.

**Code** : `400 BAD REQUEST`

**Content example**

```json
// TODO
```
