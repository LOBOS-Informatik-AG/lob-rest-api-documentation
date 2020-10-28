# Documents

## Get sales-documents

This endpoint allows you to get all documents with the attribute `ecomm = true`

**URL** : `/sales-documents`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : None

**Pagination** : Yes

**Query parameters**

``` json
// TODO
```

### Success Response

**Condition** : If documents are found.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

**or**

**Condition** : no documents are found.

**Content example**

```json
{
    "text": "Keine Kontakte gefunden."
}
```

## Get printed sales-document

This endpoint allows you to reprint the document

**URL** : `/sales-documents`

**Example** : `sales-documents?sDocumentType=O&lngDocumentID=1293701`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : None

**Pagination** : Yes

**Query parameters**

``` json
// TODO
```

### Success Response

**Condition** : If documents are found.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

**or**

**Condition** : no documents are found.

**Content example**

```json
{
    "text": "Keine Kontakte gefunden."
}
```