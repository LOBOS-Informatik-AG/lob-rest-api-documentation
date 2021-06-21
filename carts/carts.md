# Carts

## Get carts

This endpoint allows you to get the carts for the authenticated user

**URL** : `/carts`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters** : Default filters

### Success Response

**Condition** : If carts are found.

**Code** : `200 OK`

**Content example**

```json
[
    ...
]
```

**or**

**Condition** : no carts have been found.

**Content example**

```json
{
    "text": "Keine Warenkörbe gefunden."
}
```

## Get cart by id

This endpoint allows you to get a cart by id

**URL** : `/carts/:id`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

### Success Response

**Condition** : If the cart is found.

**Code** : `200 OK`

**Content example**

```json
{
    ...
}
```

**or**

**Condition** : if no cart is found.

**Content example**

```json
{
    "text": "Kein Warenkorb gefunden"
}
```


## Create cart

This endpoint allows you to create a cart

**URL** : `/carts`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    ...
}
```

### Success Response

**Condition** : If the cart is successfully created.

**Code** : `200 OK`

**Content example**

```json
{
    ...
}
```

## Update cart

This endpoint allows you to update a cart

**URL** : `/carts/:id`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    ...
}
```

### Success Response

**Condition** : If the cart is successfully updated.

**Code** : `200 OK`

**Content example**

```json
{
    ...
}
```

## Delete cart

This endpoint allows you to delete a cart

**URL** : `/carts/:id`

**Method** : <img src="https://img.shields.io/badge/DELETE%20-%23323330.svg?&style=flat&color=red"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
None
```

### Success Response

**Condition** : If the cart is deleted successfully.

**Code** : `200 OK`

**Content example**

```json
None
```

## Get cart-items

This endpoint allows you to get all the cart-items

**URL** : `/carts/:id/items`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Query parameters** : Default filters

### Success Response

**Condition** : If cart-items are found.

**Code** : `200 OK`

**Content example**

```json
[
    ...
]
```

**or**

**Condition** : no cart-items are found.

**Content example**

```json
{
    "text": "Keine Warenkorbpositionen gefunden."
}
```

## Create cart-item

This endpoint allows you create a cart-item

**URL** : `/carts/:id/items`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    ...
}
```

### Success Response

**Condition** : If the item is succesfully created.

**Code** : `200 OK`

**Content example**

```json
{
    ...
}
```

## Update cart-item

This endpoint allows you to update a item

**URL** : `/carts/:id/items/:id`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
{
    ...
}
```

### Success Response

**Condition** : If the cart is updated successfully.

**Code** : `200 OK`

**Content example**

```json
{
    ...
}
```

## Delete cart-item

This endpoint allows you to delete a cart-item

**URL** : `/carts/:id/items/:id`

**Method** : <img src="https://img.shields.io/badge/DELETE%20-%23323330.svg?&style=flat&color=red"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

``` json
None
```

### Success Response

**Condition** : If the cart-item is deleted successfully.

**Code** : `200 OK`

**Content example**

```json
None
```