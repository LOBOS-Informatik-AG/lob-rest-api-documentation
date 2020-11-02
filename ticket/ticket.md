# Tickets (Call-Center)

## Get tickets

This endpoint allows you to get the tickets by the specified filters

**URL** : `/tickets`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters** : Default filters

### Success Response

**Condition** : If tickets are found.

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 8,
    "lastPage": "1",
    "currentPage": "1",
    "total": 1,
    "data": [
        {
            "dtAlterationDate": 1602166517000,
            "dtEntryDate": 1591380372000,
            "lngCategory": 10,
            "lngContactID": null,
            "lngPriority": 3,
            "lngStatus": 2,
            "lngTicketID": 2020068631,
            "sAlterationUser": "SYSADM",
            "sB22Description": "Einstellungen Druckertreiber flüchtig",
            "sB22Responsible": "MGR",
            "sEntryUser": "MHA"
        },
        ...
    ]
}
```

**or**

**Condition** : no tickets are found.

**Content example**

```json
{
    "text": "Kein(e) Ticket(s) gefunden."
}
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
{
    "dtAlterationDate": 1602166517000,
    "dtEntryDate": 1591380372000,
    "lngCategory": 10,
    "lngContactID": null,
    "lngPriority": 3,
    "lngStatus": 2,
    "lngTicketID": 2020068631,
    "sAlterationUser": "SYSADM",
    "sB22Description": "Einstellungen Druckertreiber flüchtig",
    "sB22Responsible": "MGR",
    "sEntryUser": "MHA"
}
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
    "sB22Description": "Test API",
    "sB22Responsible": "",
    "sEntryUser": "SYSADM"
}
```

### Success Response

**Condition** : If the ticket is successfully created.

**Code** : `200 OK`

**Content example**

```json
{
    "dtAlterationDate": null,
    "dtEntryDate": 1596438000,
    "lngCategory": null,
    "lngContactID": null,
    "lngPriority": 1,
    "lngStatus": 1,
    "lngTicketID": 2020119734,
    "sAlterationUser": "",
    "sB22Description": "Test API",
    "sB22Responsible": "",
    "sEntryUser": "SYSADM"
}
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
    "dtAlterationDate": 1604335734000,
    "dtEntryDate": 1600038000,
    "lngCategory": null,
    "lngContactID": null,
    "lngPriority": 1,
    "lngStatus": 1,
    "lngTicketID": 2020119734,
    "sAlterationUser": "SYSADM",
    "sB22Description": "Test API",
    "sB22Responsible": "",
    "sEntryUser": "SYSADM"
}
```

### Success Response

**Condition** : If the ticket is successfully updated.

**Code** : `200 OK`

**Content example**

```json
{
    "dtAlterationDate": 1604335734000,
    "dtEntryDate": 1600038000,
    "lngCategory": null,
    "lngContactID": null,
    "lngPriority": 1,
    "lngStatus": 1,
    "lngTicketID": 2020119734,
    "sAlterationUser": "SYSADM",
    "sB22Description": "Test API",
    "sB22Responsible": "",
    "sEntryUser": "SYSADM"
}
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
{
    "perPage": 8,
    "lastPage": "1",
    "currentPage": "1",
    "total": 8,
    "data": [
        {
            "dtEntryDate": 1602176483000,
            "id": "2116c63b-0977-11eb-91d9-00155d868c02",
            "lngTicketId": 2020068631,
            "sClerkID": "SYSADM",
            "sText": "Hello Support",
            "sTextType": "T"
        },
        {
            "dtEntryDate": 1602176490000,
            "id": "2116c63c-0977-11eb-91d9-00155d868c02",
            "lngTicketId": 2020068631,
            "sClerkID": "SYSADM",
            "sText": "Hello Customer",
            "sTextType": "A"
        },
        ...
    ]
}
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
        "lngTicketId": 2020068631,
        "sClerkID": "TF",
        "sText": "Hi this is a question",
        "sTextType": "T"
}
```

### Success Response

**Condition** : If the message is created.

**Code** : `200 OK`

**Content example**

```json
{
    "dtEntryDate": 1604335843000,
    "id": "29c83d3d-1d23-11eb-91da-00155d868c02",
    "lngTicketId": 2020068631,
    "sClerkID": "TF",
    "sText": "Hi this is a question",
    "sTextType": "T"
}
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