# Archive

Via the archive document interface, documents can be displayed and downloaded directly from the archive stored in eNVenta.

## Get documents

This endpoint returns all archive documents of the searched process from eNVenta

**URL** : `/archive-documents`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : YES

**Permissions required** : None

**Body parameters**

The sProgram and lngReferenceID field is required to search for archive documents

`/archive-documents?sProgram=Call&lngReferenceID=123456`

### Success Response

**Condition** : if at least one document has been found

**Code** : `200 OK`

**Content example**

```json
[
    {
        "dtEntryDate": null,
        "id": "4181186b-4241-45f7-a9fe-3e6f8cf29f1c",
        "lngReferenceID": 123456,
        "lngSize": 27,
        "sDocumentID": "178146",
        "sExtensionType": "txt",
        "sName": "Test",
        "sProgram": "Call"
    },
    ...
]
```

### Empty Response (no documents found)

**Code** : `200 OK`

```json
[]
```

## Get document

This endpoint allows you to get a archive document from eNVenta

**URL** : `/archive-documents`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : YES

**Permissions required** : None

**Body parameters**

The follwing fields are required to successfully get a document for the process (sPgroram="Call")

```json
{
    "sProgram": "Call",
    "lngReferenceID": "123456",
    "sDocumentID": "132465",
}
```

Possible values for sProgram:
* "Call"
* "Customer"

There is a special way to get sales-documents and not knowing the sDocumentID:

```json
{
    "sProgram": "SalesDocument",
    "lngReferenceID": "123456",
    "sBelegart": "VKLS",
}
```

Possible values for sBelegart:
* "VKLS" => delivery note
* "VKRG" => invoice

### Success Response

**Condition** : If the login was successfull.

**Code** : `200 OK`

**Content example**

The Document mostly PDF is returned

### Error Responses

**Condition** : if the process or the document is not found

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "text": "Es wurde kein Dokument gefunden"
}
```

## Post document

This endpoint allows you to upload files to the eNVenta archive

**URL** : `/archive-documents`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : YES

**Permissions required** : None

**Body parameters**

The params have to be sent as form-data with the following params

```json
{
    "sLocation": "1",
    "sProgram": "Call",
    "lngReferenceID": "123456",
    "file": File,
}
```

### Success Response

**Condition** : If the login was successfull.

**Code** : `200 OK`

**Content example**

```json
// TODO
```

### Error Responses

**Condition** : if there was an error during the file-upload

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "text": "Fehler beim File-Upload"
}
```

**Condition** : if the file was to large

**Code** : `413 REQUEST ENTITY TOO LARGE`
