# Customers

## Get customers

This endpoint allows you to get all the customers

**URL** : `/customers`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : Yes `isSalesForce = true`

**Pagination** : Yes

**Query parameters**

``` json
// TODO
```

### Success Response

**Condition** : If customers are found.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

**or**

**Condition** : if no customer are found.

**Content example**

```json
{
    "text": "Keine Kunden gefunden."
}
```

## Get customer by id

This endpoint allows you to get a specific customer by id

**URL** : `/customers/:id`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : Yes `isSalesForce = true`

### Success Response

**Condition** : If customer is found.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

**or**

**Condition** : if no customer is found.

**Content example**

```json
{
    "text": "Kein Kunde gefunden."
}
```