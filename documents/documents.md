# Documents

## Get sales-documents

This endpoint allows you to get all documents

**URL** : `/sales-documents`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : None

**Pagination** : Yes

**Query parameters** : Default filters

### Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 3,
    "lastPage": "13",
    "currentPage": "1",
    "total": 37,
    "data": [
        {
            "decDiscountAmount1": null,
            "decDiscountAmount2": null,
            "decDiscountAmount3": null,
            "decDiscountPercent1": null,
            "decDiscountPercent2": null,
            "decDiscountPercent3": null,
            "decPacking": null,
            "decPostage": null,
            "dtDeliveryDate": null,
            "dtEntryDate": 1041845619000,
            "dtOrderDate": 1041811200000,
            "dtPrintDate": 1041848980000,
            "lngContactID": 0,
            "lngCustomerID": 10010,
            "lngDocumentID": 390739,
            "lngOrderID": 390739,
            "lngProjectID": null,
            "oDeliveryAddress": {
                "sCity": "",
                "sCompany1": "",
                "sCompany2": "",
                "sContact": "",
                "sCountry": "",
                "sCountryCode": "",
                "sPostBox": "",
                "sStreet": "",
                "sZipBox": "",
                "sZipCode": ""
            },
            "oInvoiceAddress": {
                "sCity": "Schwerzenbach",
                "sCompany1": "LOBOS Informatik AG",
                "sCompany2": "",
                "sContact": "Herrn Werner Locher",
                "sCountry": "",
                "sCountryCode": "",
                "sPostBox": "",
                "sStreet": "Bahnstrasse 25",
                "sZipBox": "",
                "sZipCode": "8603"
            },
            "sClerkID": "LO",
            "sCurrencyCode": "",
            "sDiscountText1": "",
            "sDiscountText2": "",
            "sDiscountText3": "",
            "sDocumentType": "O",
            "sDocumentTypeName": "Angebot",
            "sMemo": "",
            "sOrderSource": "",
            "sOrderText": "",
            "sOrderType": "A",
            "sPaymentID": "",
            "sPaymentIDType": "",
            "shtBlocked": 0,
            "shtCompleteDelivery": null,
            "shtDeliveryConditionID": null,
            "shtPaymentConditionID": 2,
            "shtShippingConditionID": null,
            "shtValidityPeriod": null,
            "shtValueCreditNote": 0
        },
        {
            "decDiscountAmount1": null,
            "decDiscountAmount2": null,
            "decDiscountAmount3": null,
            "decDiscountPercent1": null,
            "decDiscountPercent2": null,
            "decDiscountPercent3": null,
            "decPacking": null,
            "decPostage": null,
            "dtDeliveryDate": null,
            "dtEntryDate": 1041853937000,
            "dtOrderDate": 1041811200000,
            "dtPrintDate": 1041853941000,
            "lngContactID": 0,
            "lngCustomerID": 10010,
            "lngDocumentID": 390740,
            "lngOrderID": 390740,
            "lngProjectID": null,
            "oDeliveryAddress": {
                "sCity": "",
                "sCompany1": "",
                "sCompany2": "",
                "sContact": "",
                "sCountry": "",
                "sCountryCode": "",
                "sPostBox": "",
                "sStreet": "",
                "sZipBox": "",
                "sZipCode": ""
            },
            "oInvoiceAddress": {
                "sCity": "Schwerzenbach",
                "sCompany1": "LOBOS Informatik AG",
                "sCompany2": "",
                "sContact": "Herrn Werner Locher",
                "sCountry": "",
                "sCountryCode": "",
                "sPostBox": "",
                "sStreet": "Bahnstrasse 25",
                "sZipBox": "",
                "sZipCode": "8603"
            },
            "sClerkID": "AS1",
            "sCurrencyCode": "",
            "sDiscountText1": "",
            "sDiscountText2": "",
            "sDiscountText3": "",
            "sDocumentType": "O",
            "sDocumentTypeName": "Angebot",
            "sMemo": "",
            "sOrderSource": "",
            "sOrderText": "",
            "sOrderType": "A",
            "sPaymentID": "",
            "sPaymentIDType": "",
            "shtBlocked": 0,
            "shtCompleteDelivery": null,
            "shtDeliveryConditionID": null,
            "shtPaymentConditionID": 2,
            "shtShippingConditionID": null,
            "shtValidityPeriod": null,
            "shtValueCreditNote": 0
        },
        {
            "decDiscountAmount1": null,
            "decDiscountAmount2": null,
            "decDiscountAmount3": null,
            "decDiscountPercent1": null,
            "decDiscountPercent2": null,
            "decDiscountPercent3": null,
            "decPacking": null,
            "decPostage": null,
            "dtDeliveryDate": 1192665600000,
            "dtEntryDate": 1066043089000,
            "dtOrderDate": 1066003200000,
            "dtPrintDate": 1132826859000,
            "lngContactID": 85950,
            "lngCustomerID": 10010,
            "lngDocumentID": 390927,
            "lngOrderID": 390927,
            "lngProjectID": null,
            "oDeliveryAddress": {
                "sCity": "Schwerzenbach",
                "sCompany1": "LOBOS Informatik AG",
                "sCompany2": "",
                "sContact": "",
                "sCountry": "Schweiz",
                "sCountryCode": "CH",
                "sPostBox": "",
                "sStreet": "Bahnstrasse 25",
                "sZipBox": "",
                "sZipCode": "8603"
            },
            "oInvoiceAddress": {
                "sCity": "Schwerzenbach",
                "sCompany1": "LOBOS Informatik AG",
                "sCompany2": "",
                "sContact": "Herr François Berger",
                "sCountry": "Schweiz",
                "sCountryCode": "CH",
                "sPostBox": "",
                "sStreet": "Bahnstrasse 25",
                "sZipBox": "",
                "sZipCode": "8603"
            },
            "sClerkID": "FB",
            "sCurrencyCode": "",
            "sDiscountText1": "",
            "sDiscountText2": "",
            "sDiscountText3": "",
            "sDocumentType": "O",
            "sDocumentTypeName": "Angebot",
            "sMemo": "",
            "sOrderSource": "",
            "sOrderText": "",
            "sOrderType": "A",
            "sPaymentID": "",
            "sPaymentIDType": "",
            "shtBlocked": 0,
            "shtCompleteDelivery": null,
            "shtDeliveryConditionID": null,
            "shtPaymentConditionID": 2,
            "shtShippingConditionID": null,
            "shtValidityPeriod": null,
            "shtValueCreditNote": 0
        }
    ]
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

```json
{
    "sDocumentType": "O",
    "lngDocumentID": 123456
}

```

### Success Response

**Condition** : If documents are found.

**Code** : `200 OK`

**Content** : File download

**or**

**Condition** : if no documents are found.

**Content example**

```json
{
    "text": "Kein Dokument gefunden."
}
```