# Downloads

## Get download (tree)

This endpoint allows you to get the downloads as a tree structure

**URL** : `/download-tree`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : No

**Permissions required** : No

### Success Response

**Condition** : If the download structure is found.

**Code** : `200 OK`

**Content example**

```json
[
    {
        "sName": "Alle",
        "sType": "Folder",
        "lngSize": 0,
        "sPath": "/Alle",
        "oChildren": [
            {
                "sName": "subdir",
                "sType": "Folder",
                "lngSize": 0,
                "sPath": "/Alle/subdir",
                "oChildren": [
                    {
                        "sName": "tst.txt",
                        "sType": "txt",
                        "lngSize": 16,
                        "sPath": "/Alle/subdir/tst.txt",
                        "oChildren": null
                    }
                ]
            },
            {
                "sName": "ecommerce-seo-guide.pdf",
                "sType": "pdf",
                "lngSize": 13351874,
                "sPath": "/Alle/ecommerce-seo-guide.pdf",
                "oChildren": null
            },
            {
                "sName": "favoriten.pdf",
                "sType": "pdf",
                "lngSize": 231034,
                "sPath": "/Alle/favoriten.pdf",
                "oChildren": null
            }
        ]
    }
]
```

## Get file

This endpoint allows you to download a specific file

**URL** : `/download-file`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Query params** :

```json
{
    "sPath": "/Alle/ecommerce-seo-guide.pdf"
}
```

### Success Response

**Condition** : If the file is found.

**Code** : `200 OK`

**Content example**

form-data

**or**

**Condition** : if no file is found.

**Content example**

```json
{
  "text": "Datei oder Pfad nicht vorhanden." 
}
```