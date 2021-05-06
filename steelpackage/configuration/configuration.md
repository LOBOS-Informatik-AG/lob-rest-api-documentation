# Configuration

## Post configuration

This endpoint allows you to create an initial steel configuration based on the *ConfigurationParam* object that ist passed in the body.

**URL** : `/configuration`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : No

**Permissions required** : No

**Body** *ConfigurationParam*

``` json
{
    "decBO3Factor1": 0,
    "decBO3Factor2": 0,
    "decBO3Factor3": 0,
    "decBO3QuantityInput": 3,
    "sArticleID": "HEA100",
    "sBO3QuantityUnitInput": "2-Stk"
}
```

### Success Response

**Condition** : If configuration can be created.

**Code** : `200 OK`

**Content example**

```json
{
  "decBO3Factor1": 0,
  "decBO3Factor2": 0,
  "decBO3Factor3": 0,
  "decBO3QuantityInput": 3,
  "decPrice": 0,
  "decPriceConfiguration": 0,
  "oFigureListColl": [
    {
      "binTakePositionImage": "...",
      "decFrontAngle": 0,
      "decFrontAngleFrom": 0,
      "decFrontAngleTo": 0,
      "decRearAngle": 0,
      "decRearAngleFrom": -60,
      "decRearAngleTo": 0,
      "sFigureID": "11",
      "sName": "Figur 11",
      "sProfileType": "H"
    },
    {
      "binTakePositionImage": "...",
      "decFrontAngle": 0,
      "decFrontAngleFrom": -60,
      "decFrontAngleTo": 0,
      "decRearAngle": 0,
      "decRearAngleFrom": -60,
      "decRearAngleTo": 0,
      "sFigureID": "12",
      "sName": "Figur 12",
      "sProfileType": "H"
    },
    {
      "binTakePositionImage": "...",
      "decFrontAngle": 0,
      "decFrontAngleFrom": 0,
      "decFrontAngleTo": 60,
      "decRearAngle": 0,
      "decRearAngleFrom": -60,
      "decRearAngleTo": 0,
      "sFigureID": "13",
      "sName": "Figur 13",
      "sProfileType": "H"
    },
    {
      "binTakePositionImage": "...",
      "decFrontAngle": 0,
      "decFrontAngleFrom": 0,
      "decFrontAngleTo": 0,
      "decRearAngle": 0,
      "decRearAngleFrom": -60,
      "decRearAngleTo": 0,
      "sFigureID": "21",
      "sName": "Figur 21",
      "sProfileType": "H"
    },
    {
      "binTakePositionImage": "...",
      "decFrontAngle": 0,
      "decFrontAngleFrom": -60,
      "decFrontAngleTo": 0,
      "decRearAngle": 0,
      "decRearAngleFrom": -60,
      "decRearAngleTo": 0,
      "sFigureID": "22",
      "sName": "Figur 22",
      "sProfileType": "H"
    },
    {
      "binTakePositionImage": "...",
      "decFrontAngle": 0,
      "decFrontAngleFrom": 0,
      "decFrontAngleTo": 60,
      "decRearAngle": 0,
      "decRearAngleFrom": -60,
      "decRearAngleTo": 0,
      "sFigureID": "23",
      "sName": "Figur 23",
      "sProfileType": "H"
    }
  ],
  "oFigureSelected": {
    "binTakePositionImage": "...",
    "decFrontAngle": 0,
    "decFrontAngleFrom": 0,
    "decFrontAngleTo": 0,
    "decRearAngle": 0,
    "decRearAngleFrom": 0,
    "decRearAngleTo": 0,
    "sFigureID": "",
    "sName": "",
    "sProfileType": ""
  },
  "oP48APIRoutingDetailColl": [
    {
      "bBO3Execute": false,
      "decPrice": 0,
      "decQuantity": 0,
      "sBO3SteelProcessingArticleID": "309001",
      "sBO3SteelProcessingArticleName": "Zuschnitt",
      "sUnit": ""
    },
    {
      "bBO3Execute": false,
      "decPrice": 0,
      "decQuantity": 0,
      "sBO3SteelProcessingArticleID": "309006",
      "sBO3SteelProcessingArticleName": "Bohren",
      "sUnit": ""
    },
    {
      "bBO3Execute": false,
      "decPrice": 0,
      "decQuantity": 0,
      "sBO3SteelProcessingArticleID": "309004",
      "sBO3SteelProcessingArticleName": "Klinken",
      "sUnit": ""
    },
    {
      "bBO3Execute": false,
      "decPrice": 0,
      "decQuantity": 0,
      "sBO3SteelProcessingArticleID": "309007",
      "sBO3SteelProcessingArticleName": "Grundieren",
      "sUnit": ""
    },
    {
      "bBO3Execute": false,
      "decPrice": 0,
      "decQuantity": 0,
      "sBO3SteelProcessingArticleID": "309008",
      "sBO3SteelProcessingArticleName": "Stahlstrahlen",
      "sUnit": ""
    }
  ],
  "sArticleID": "HEA100",
  "sBO3QuantityUnitInput": "2-Stk"
}
```

**or**

**Condition** : no configuration could be created.

**Content example**

```json
{
    "text": "Eine Konfiguration anhand der übergebenen Parameter konnte nicht erstellt werden."
}
```

## PUT configuration

This endpoint allows you to update a configuration that is passed in the body. According to the transferred configuration, the quantities and prices of the configuration are adjusted. In addition to the selected processings, the units, quantities and selected figures are also taken into account. The following information is taken into account for input:
* The unit of the configuration is taken into account, e.g *'trM/kg'* ```  $.sBO3QuantityUnitInput = 'trM/kg' ```
* The factor1 of the configuration is taken into account, e.g *18000* ```  $.decBO3Factor1 = 18000 ```
* The factor2 of the configuration is taken into account, e.g *0* ```  $.decBO3Factor2 = 0 ```
* The factor3 of the configuration is taken into account, e.g *0* ```  $.decBO3Factor3 = 0 ```
* The quantity of the configuration is taken into account, e.g. *3* ```  $.decBO3QuantityInput = 3 ```
* Processings can be selected or deselected, e.g. *true* ```  $.oP48APIRoutingDetailColl[*].bBO3Execute = true ```
* The selected Figure along with the front/rear angle ```  $.oFigureSelected = ```
```json
{
    "binTakePositionImage": ...,
    "decFrontAngle": 30,
    "decFrontAngleFrom": 0,
    "decFrontAngleTo": 60,
    "decRearAngle": -30,
    "decRearAngleFrom": -60,
    "decRearAngleTo": 0,
    "sFigureID": "23",
    "sName": "Figur 23",
    "sProfileType": "H"
    }
 
}
```

**URL** : `/configuration`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : No

**Permissions required** : No

**Body**

```json
{
    "sArticleID": "HEA 100",
    "decBO3Factor1": 18000,
    "decBO3Factor2": 0,
    "decBO3Factor3": 0,
    "decBO3QuantityInput": 3,
    "oFigureListColl": [
        {
            "binTakePositionImage": "",
            "decFrontAngleFrom": 0,
            "decFrontAngleTo": 0,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "11",
            "sName": "Figur 11",
            "sProfileType": "H"
        },
        {
            "binTakePositionImage": "",
            "decFrontAngleFrom": -60,
            "decFrontAngleTo": 0,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "12",
            "sName": "Figur 12",
            "sProfileType": "H"
        },
        {
            "binTakePositionImage": "",
            "decFrontAngleFrom": 0,
            "decFrontAngleTo": 60,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "13",
            "sName": "Figur 13",
            "sProfileType": "H"
        },
        {
            "binTakePositionImage": "",
            "decFrontAngleFrom": 0,
            "decFrontAngleTo": 0,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "21",
            "sName": "Figur 21",
            "sProfileType": "H"
        },
        {
            "binTakePositionImage": "",
            "decFrontAngleFrom": -60,
            "decFrontAngleTo": 0,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "22",
            "sName": "Figur 22",
            "sProfileType": "H"
        },
        {
            "binTakePositionImage": "",
            "decFrontAngleFrom": 0,
            "decFrontAngleTo": 60,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "23",
            "sName": "Figur 23",
            "sProfileType": "H"
        }
    ],
    "oFigureSelected": null,
    "oP48APIRoutingDetailColl": [
        {
            "bBO3Execute": false,
            "sBO3SteelProcessingArticleID": "309001",
            "sBO3SteelProcessingArticleName": "Zuschnitt"
        },
        {
            "bBO3Execute": true,
            "sBO3SteelProcessingArticleID": "309006",
            "sBO3SteelProcessingArticleName": "Bohren"
        },
        {
            "bBO3Execute": true,
            "sBO3SteelProcessingArticleID": "309004",
            "sBO3SteelProcessingArticleName": "Klinken"
        },
        {
            "bBO3Execute": true,
            "sBO3SteelProcessingArticleID": "309007",
            "sBO3SteelProcessingArticleName": "Grundieren"
        },
        {
            "bBO3Execute": false,
            "sBO3SteelProcessingArticleID": "309008",
            "sBO3SteelProcessingArticleName": "Stahlstrahlen"
        }
    ],
    "sBO3QuantityUnitInput": "trM/kg"
}
```

### Success Response

**Condition** : If configuration can be updated.

**Code** : `200 OK`

**Content example**

```json
{
    "decBO3Factor1": 18000,
    "decBO3Factor2": 0,
    "decBO3Factor3": 0,
    "decBO3QuantityInput": 3,
    "decPrice": 1875.75,
    "decPriceConfiguration": 2590.90,
    "oFigureListColl": [
        {
            "binTakePositionImage": null,
            "decFrontAngle": 0,
            "decFrontAngleFrom": 0,
            "decFrontAngleTo": 0,
            "decRearAngle": 0,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "11",
            "sName": "Figur 11",
            "sProfileType": "H"
        },
        {
            "binTakePositionImage": null,
            "decFrontAngle": 0,
            "decFrontAngleFrom": -60,
            "decFrontAngleTo": 0,
            "decRearAngle": 0,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "12",
            "sName": "Figur 12",
            "sProfileType": "H"
        },
        {
            "binTakePositionImage": null,
            "decFrontAngle": 0,
            "decFrontAngleFrom": 0,
            "decFrontAngleTo": 60,
            "decRearAngle": 0,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "13",
            "sName": "Figur 13",
            "sProfileType": "H"
        },
        {
            "binTakePositionImage": null,
            "decFrontAngle": 0,
            "decFrontAngleFrom": 0,
            "decFrontAngleTo": 0,
            "decRearAngle": 0,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "21",
            "sName": "Figur 21",
            "sProfileType": "H"
        },
        {
            "binTakePositionImage": null,
            "decFrontAngle": 0,
            "decFrontAngleFrom": -60,
            "decFrontAngleTo": 0,
            "decRearAngle": 0,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "22",
            "sName": "Figur 22",
            "sProfileType": "H"
        },
        {
            "binTakePositionImage": null,
            "decFrontAngle": 0,
            "decFrontAngleFrom": 0,
            "decFrontAngleTo": 60,
            "decRearAngle": 0,
            "decRearAngleFrom": -60,
            "decRearAngleTo": 0,
            "sFigureID": "23",
            "sName": "Figur 23",
            "sProfileType": "H"
        }
    ],
    "oFigureSelected": {
        "binTakePositionImage": null,
        "decFrontAngle": 0,
        "decFrontAngleFrom": 0,
        "decFrontAngleTo": 0,
        "decRearAngle": 0,
        "decRearAngleFrom": 0,
        "decRearAngleTo": 0,
        "sFigureID": "",
        "sName": "",
        "sProfileType": ""
    },
    "oP48APIRoutingDetailColl": [
        {
            "bBO3Execute": false,
            "decPrice": 0,
            "decQuantity": 0,
            "sBO3SteelProcessingArticleID": "309001",
            "sBO3SteelProcessingArticleName": "Zuschnitt",
            "sUnit": ""
        },
        {
            "bBO3Execute": true,
            "decPrice": 75.00,
            "decQuantity": 3,
            "sBO3SteelProcessingArticleID": "309006",
            "sBO3SteelProcessingArticleName": "Bohren",
            "sUnit": "Stk"
        },
        {
            "bBO3Execute": true,
            "decPrice": 54.00,
            "decQuantity": 3,
            "sBO3SteelProcessingArticleID": "309004",
            "sBO3SteelProcessingArticleName": "Klinken",
            "sUnit": "Stk"
        },
        {
            "bBO3Execute": true,
            "decPrice": 586.15,
            "decQuantity": 901.800,
            "sBO3SteelProcessingArticleID": "309007",
            "sBO3SteelProcessingArticleName": "Grundieren",
            "sUnit": "kg"
        },
        {
            "bBO3Execute": false,
            "decPrice": 0,
            "decQuantity": 0,
            "sBO3SteelProcessingArticleID": "309008",
            "sBO3SteelProcessingArticleName": "Stahlstrahlen",
            "sUnit": ""
        }
    ],
    "sArticleID": "HEA 100",
    "sBO3QuantityUnitInput": "trM/kg"
}
```

**or**

**Condition** : no configuration could be updated.

**Content example**

```json
{
    "text": "Fehler beim Ändern der Konfiguration."
}
```

