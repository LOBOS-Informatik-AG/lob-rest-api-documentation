# Tickets (Call-Center)

## Get tickets

This endpoint allows you to get the tickets by the specified filters

**URL** : `/tickets`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

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



## Get ticket by id

This endpoint allows you to get a ticket by id

**URL** : `/tickets/:id`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

### Success Response

**Condition** : If a ticket is found.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

**or**

**Condition** : if no ticket is found.

**Content example**

```json
{
    "text": "Kein Ticket gefunden."
}
```

## Create ticket

This endpoint allows you to create a ticket

**URL** : `/tickets`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    "dtAlterationDate": null,
    "dtEntryDate": 1592838793,
    "lngCategory": null,
    "lngContactID": null,
    "lngPriority": 1,
    "lngStatus": 1,
    "sAlterationUser": null,
    "sB22Description": "Test 2110",
    "sB22Responsible": "",
    "sEntryUser": "SYSADM"
}
```

### Success Response

**Condition** : If the ticket is successfully created.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

## Update ticket

This endpoint allows you to update a ticket

**URL** : `/tickets/:id`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    "dtAlterationDate": null,
    "dtEntryDate": 1592845993,
    "id": 2020090329,
    "lngCategory": null,
    "lngContactID": null,
    "lngPriority": 1,
    "lngStatus": 1,
    "sAlterationUser": "SYSADM",
    "sB22Description": "TEST 13:53",
    "sB22Responsible": "",
    "sEntryUser": "SYSADM"
}
```

### Success Response

**Condition** : If the ticket is successfully updated.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

## Get ticket-messages

This endpoint allows you to get all the messages of the specified ticket

**URL** : `/tickets/:id/messages`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

### Success Response

**Condition** : If messages are found.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

**or**

**Condition** : if no messages are found.

**Content example**

```json
{
    "text": "Keine Nachrichten gefunden."
}
```

## Create ticket-message

This endpoint allows you create a ticket-message

**URL** : `/tickets/:id/messages`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
        "lngTicketId": 2020090329,
        "sClerkID": "TF",
        "sText": "Das ist eine Antwort via API.",
        "sTextType": "T"
}
```

### Success Response

**Condition** : If the message is created.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

## Get ticket-categories

This endpoint allows you to get all ticket categories

**URL** : `/ticket-categories`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : None

**Pagination** : No

### Success Response

**Condition** : If categories are found.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "lngCategoryID": 15,
        "lngParentCategoryID": 2,
        "sName": "LOBOS"
    },
    ...
]
```

**or**

**Condition** : if no categories are found.

**Content example**

```json
{
    "text": "Keine Ticket-Kategorien gefunden."
}
```

## Get ticket-priorities

This endpoint allows you to get all ticket priorities

**URL** : `/ticket-priorities`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : None

**Pagination** : No

### Success Response

**Condition** : If priorities are found.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "lngPriorityID": 1,
        "sName": "Normal"
    },
    ...
]
```

**or**

**Condition** : if no priorities are found.

**Content example**

```json
{
    "text": "Keine Ticket-Prioritäten gefunden."
}
```

## Get ticket-types

This endpoint allows you to get all ticket priorities

**URL** : `/ticket-types`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : None

**Pagination** : No

### Success Response

**Condition** : If types are found.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "lngTypeID": 314,
        "sName": "Anlagebuchhaltung"
    },
    ...
]
```

**or**

**Condition** : if no types are found.

**Content example**

```json
{
    "text": "Keine Ticket-Typen gefunden."
}
```

## Get ticket-stats

This endpoint allows you to get the ticket-statistic the statistic shows always the history of the last three years.</br>
The stats data is grouped by the months.

**URL** : `/ticket-stats`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : None

**Pagination** : No

### Success Response

**Condition** : If the stats are successfully researched.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "iarrData": [
            3,
            2,
            3,
            1,
            2,
            0,
            1,
            1,
            2,
            2,
            2,
            1
        ],
        "sYear": "2018"
    },
    {
        "iarrData": [
            1,
            1,
            0,
            1,
            0,
            0,
            1,
            0,
            1,
            0,
            1,
            0
        ],
        "sYear": "2019"
    },
    {
        "iarrData": [
            1,
            2,
            0,
            1,
            1,
            2,
            1,
            0,
            0,
            2
        ],
        "sYear": "2020"
    }
]
```