# Sales-Order \ -Offer \ -Credit-Note

## Get sales-orders

This endpoint allows you to GET sales-orders for the authenticated user (Customer)

**URL** : `/sales-orders`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters** : default filters

### Success Response

**Condition** : If sales-orders are found.

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 3,
    "lastPage": "8",
    "currentPage": "1",
    "total": 22,
    "data": [
        {
            "bCollectiveInvoice": false,
            "dtDeliveryDate": 1219228678000,
            "dtEntryDate": 1219228678000,
            "dtOrderDate": 1219228678000,
            "lngCampaignID": 0,
            "lngContactID": 0,
            "lngCustomerID": 10010,
            "lngOrderID": 825774,
            "lngProjectID": 0,
            "sContactName": "",
            "sDCity": "",
            "sDCompany1": "",
            "sDCompany2": "",
            "sDCompany3": "",
            "sDCompany4": "",
            "sDContact": "",
            "sDCountry": "",
            "sDCountryCode": "",
            "sDStreet": "",
            "sDZipCode": "",
            "sICity": "Schwerzenbach",
            "sICompany1": "LOBOS Informatik AG",
            "sICompany2": "",
            "sICompany3": "",
            "sICompany4": "",
            "sIContact": "",
            "sICountry": "Schweiz",
            "sICountryCode": "CH",
            "sIPostBox": "",
            "sIStreet": "Bahnstrasse 25",
            "sIZipBox": "",
            "sIZipCode": "8603",
            "sOrderText": "",
            "sOrderType": "6",
            "shtBlocked": 0,
            "shtOfferStatus": 0,
            "shtPaymentCondition": 1,
            "shtShippingCondition": 0,
            "shtStatus": 5
        },
        {
            "bCollectiveInvoice": false,
            "dtDeliveryDate": 1439251200000,
            "dtEntryDate": 1439286710000,
            "dtOrderDate": 1439286711000,
            "lngCampaignID": 0,
            "lngContactID": 0,
            "lngCustomerID": 10010,
            "lngOrderID": 1550882,
            "lngProjectID": 0,
            "sContactName": "",
            "sDCity": "Frauenfeld",
            "sDCompany1": "Andreas Ammann",
            "sDCompany2": "",
            "sDCompany3": "",
            "sDCompany4": "",
            "sDContact": "",
            "sDCountry": "Schweiz",
            "sDCountryCode": "CH",
            "sDStreet": "Kleiberweg 20",
            "sDZipCode": "8500",
            "sICity": "Frauenfeld",
            "sICompany1": "Andreas Ammann",
            "sICompany2": "",
            "sICompany3": "",
            "sICompany4": "",
            "sIContact": "",
            "sICountry": "Schweiz",
            "sICountryCode": "CH",
            "sIPostBox": "",
            "sIStreet": "Kleiberweg 20",
            "sIZipBox": "",
            "sIZipCode": "8500",
            "sOrderText": "",
            "sOrderType": "5",
            "shtBlocked": 0,
            "shtOfferStatus": 0,
            "shtPaymentCondition": 13,
            "shtShippingCondition": 0,
            "shtStatus": 3
        },
        {
            "bCollectiveInvoice": false,
            "dtDeliveryDate": 1514764800000,
            "dtEntryDate": 1513003199000,
            "dtOrderDate": 1513003199000,
            "lngCampaignID": 0,
            "lngContactID": 0,
            "lngCustomerID": 10010,
            "lngOrderID": 1761636,
            "lngProjectID": 0,
            "sContactName": "",
            "sDCity": "Dübendorf",
            "sDCompany1": "LOBOS Informatik AG",
            "sDCompany2": "",
            "sDCompany3": "",
            "sDCompany4": "",
            "sDContact": "",
            "sDCountry": "Schweiz",
            "sDCountryCode": "CH",
            "sDStreet": "Auenstrasse 4",
            "sDZipCode": "8600",
            "sICity": "Dübendorf",
            "sICompany1": "LOBOS Informatik AG",
            "sICompany2": "",
            "sICompany3": "",
            "sICompany4": "",
            "sIContact": "",
            "sICountry": "Schweiz",
            "sICountryCode": "CH",
            "sIPostBox": "",
            "sIStreet": "Auenstrasse 4",
            "sIZipBox": "",
            "sIZipCode": "8600",
            "sOrderText": "",
            "sOrderType": "7",
            "shtBlocked": 1,
            "shtOfferStatus": 0,
            "shtPaymentCondition": 1,
            "shtShippingCondition": 0,
            "shtStatus": 1
        }
    ]
}
```
**or**

**Condition** : no sales-orders are found.

**Content example**

```json
{
    "text": "Auftrag nicht gefunden."
}
```

## Get sales-orders by id

This endpoint allows you to GET a sales-order by id

**URL** : `/sales-orders/:id`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

### Success Response

**Condition** : If sales-order are found.

**Code** : `200 OK`

**Content example**

```json
{
    "bCollectiveInvoice": false,
    "dtDeliveryDate": 1603324800000,
    "dtEntryDate": 1603367079000,
    "dtOrderDate": 1603367079000,
    "lngCampaignID": 0,
    "lngContactID": 101644,
    "lngCustomerID": 10010,
    "lngOrderID": 2073574,
    "lngProjectID": 0,
    "sContactName": "Herr Andrin Schaufelberger",
    "sDCity": "Dübendorf",
    "sDCompany1": "LOBOS Informatik AG",
    "sDCompany2": "",
    "sDCompany3": "",
    "sDCompany4": "",
    "sDContact": "",
    "sDCountry": "Schweiz",
    "sDCountryCode": "CH",
    "sDStreet": "Auenstrasse 4",
    "sDZipCode": "8600",
    "sICity": "Dübendorf",
    "sICompany1": "LOBOS Informatik AG",
    "sICompany2": "",
    "sICompany3": "",
    "sICompany4": "",
    "sIContact": "Herr Andrin Schaufelberger",
    "sICountry": "Schweiz",
    "sICountryCode": "CH",
    "sIPostBox": "",
    "sIStreet": "Auenstrasse 4",
    "sIZipBox": "",
    "sIZipCode": "8600",
    "sOrderText": "strunz",
    "sOrderType": "6",
    "shtBlocked": 0,
    "shtOfferStatus": 0,
    "shtPaymentCondition": 1,
    "shtShippingCondition": 0,
    "shtStatus": 1
}
```
**or**

**Condition** : no sales-order are found.

**Content example**

```json
{
    "text": "Auftrag nicht gefunden."
}
```

## Get sales-orders items

This endpoint allows you to GET all the sales-order items

**URL** : `/sales-orders/:id/items`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters** : default filters

### Success Response

**Condition** : If sales-order items are found.

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 2,
    "lastPage": "1",
    "currentPage": "1",
    "total": 2,
    "data": [
        {
            "bAlternativeItem": false,
            "bBlockDelivery": false,
            "bPartialDelivery": false,
            "decFactorSalesPrice": 1.000000000000000,
            "decItemGrossAmountFC": 0,
            "decItemNetAmountFC": 0,
            "decItemTaxAmountFC": 0,
            "decPrice": 0.00,
            "decPriceFactor": 1.00000000000000,
            "decPricePG": 0,
            "decQuantityDelivered": 1.000,
            "decQuantityDelivered2": 0,
            "decQuantityOrdered": 1.000,
            "decTaxRate": 7.70,
            "dtDeliveryDate": 1603324800000,
            "dtDeliveryNoteIDDate": 0,
            "dtInvoiceDate": 0,
            "dtRequestedDate": 1603324800000,
            "lngCampaignID": 0,
            "lngCustomerOrderID": 0,
            "lngDeliveryNoteID": 0,
            "lngGoodsReceiptID": 0,
            "lngInvoiceID": 0,
            "lngOrderID": 2073574,
            "lngPackingListID": 0,
            "lngSalesPriceUnit": 0,
            "lngSupplierID": 0,
            "oArticle": {
                "decQuantityPackage": 1.000000000000000,
                "decSalesPrice1": 60.00,
                "lngSalesPriceUnit": 1,
                "oFeatures": [],
                "oPriceInfo": null,
                "oProductInfo": null,
                "oUnitColl": [
                    {
                        "sQuantityUnitInput": "Stk",
                        "sQuantityUnitInputName": "Stk",
                        "shtStandard": 0
                    }
                ],
                "sArticleCode1": "",
                "sArticleCode2": "",
                "sArticleCode3": "",
                "sArticleID": "150900022",
                "sDescription": "Supervisor Smartcard inkl. Smartcard Reader",
                "sEAN": "",
                "sName": "PROXESS Sicherheitspaket",
                "sQuantityUnitPackage": "Stk",
                "sQuantityUnitSales": "Stk",
                "sUrlPath": null,
                "shtPlanningCode": 1,
                "shtStatus": 1
            },
            "oDiscount1": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount2": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount3": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount4": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount5": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount6": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "sArticleID": "150900022",
            "sArticleIDOfDataSupplier": null,
            "sArticleName": "PROXESS Sicherheitspaket",
            "sCustomerArticleID": "",
            "sItemText": "PROXESS Sicherheitspaket\r\nSupervisor Smartcard inkl. Smartcard Reader\r\nSerial-Nr: 20100285",
            "sItemType": "P",
            "sItemsListID": "",
            "sOfferStatus": null,
            "sOrderStatus": "",
            "sOrderText": null,
            "sOrderType": "6",
            "sPurchOrderNumber": null,
            "sQuantityUnit": "Stk",
            "sTaxCode": "M7.7",
            "sUniformNumber": "",
            "shtBranchID": 0,
            "shtFixedItemID": 1,
            "shtHasAdditionalItems": 0,
            "shtIsAdditionalToItem": 0,
            "shtItemID": 1,
            "shtItemsList": 0,
            "shtOfferStatus": 0,
            "shtPlanningCode": 0,
            "shtStatus": 1,
            "shtStorageID": 1
        },
        {
            "bAlternativeItem": false,
            "bBlockDelivery": false,
            "bPartialDelivery": false,
            "decFactorSalesPrice": 1.000000000000000,
            "decItemGrossAmountFC": 0,
            "decItemNetAmountFC": 0,
            "decItemTaxAmountFC": 0,
            "decPrice": 100.00,
            "decPriceFactor": 1.00000000000000,
            "decPricePG": 0,
            "decQuantityDelivered": 5.000,
            "decQuantityDelivered2": 0,
            "decQuantityOrdered": 5.000,
            "decTaxRate": 7.70,
            "dtDeliveryDate": 1603324800000,
            "dtDeliveryNoteIDDate": 0,
            "dtInvoiceDate": 0,
            "dtRequestedDate": 1603324800000,
            "lngCampaignID": 0,
            "lngCustomerOrderID": 0,
            "lngDeliveryNoteID": 0,
            "lngGoodsReceiptID": 0,
            "lngInvoiceID": 0,
            "lngOrderID": 2073574,
            "lngPackingListID": 0,
            "lngSalesPriceUnit": 0,
            "lngSupplierID": 0,
            "oArticle": {
                "decQuantityPackage": 0,
                "decSalesPrice1": 102.00,
                "lngSalesPriceUnit": 1,
                "oFeatures": [
                    {
                        "lngFeatureID": 1,
                        "sFormat": "",
                        "sName": "Akkuspannung (V)",
                        "sValue": "3.6 V",
                        "shtDataType": 1,
                        "shtFCFPos": 0,
                        "shtPos": 0,
                        "shtRepresentationType": 1,
                        "shtWebshopFilter": 1
                    },
                    {
                        "lngFeatureID": 3,
                        "sFormat": "",
                        "sName": "Schrauben-Ø, max. ( mm )",
                        "sValue": "5",
                        "shtDataType": 2,
                        "shtFCFPos": 0,
                        "shtPos": 0,
                        "shtRepresentationType": 2,
                        "shtWebshopFilter": 1
                    },
                    {
                        "lngFeatureID": 5,
                        "sFormat": "",
                        "sName": "Gewicht exkl. Akku ( kg )",
                        "sValue": "0.310",
                        "shtDataType": 3,
                        "shtFCFPos": 0,
                        "shtPos": 0,
                        "shtRepresentationType": 2,
                        "shtWebshopFilter": 1
                    },
                    {
                        "lngFeatureID": 2,
                        "sFormat": "",
                        "sName": "Akkukapazität (Ah)",
                        "sValue": "1.5 Ah",
                        "shtDataType": 1,
                        "shtFCFPos": 0,
                        "shtPos": 0,
                        "shtRepresentationType": 1,
                        "shtWebshopFilter": 1
                    },
                    {
                        "lngFeatureID": 4,
                        "sFormat": "",
                        "sName": "Bohr-Ø Holz, max. ( mm )",
                        "sValue": "5",
                        "shtDataType": 2,
                        "shtFCFPos": 0,
                        "shtPos": 0,
                        "shtRepresentationType": 2,
                        "shtWebshopFilter": 1
                    }
                ],
                "oPriceInfo": null,
                "oProductInfo": [
                    {
                        "Id": "a6d45984-1ebf-11eb-91da-00155d868c02",
                        "decDirectly": 1,
                        "keywords": [],
                        "listHierarchicalCategories": [
                            {
                                "sName": "level0",
                                "sValue": "e-commerce-katalog"
                            },
                            {
                                "sName": "level1",
                                "sValue": "elektrowerkzeuge"
                            },
                            {
                                "sName": "level2",
                                "sValue": "akku-geraete"
                            },
                            {
                                "sName": "level3",
                                "sValue": "akku-bohrschrauber"
                            }
                        ],
                        "lngGroup": 4,
                        "lngItemId": 0,
                        "lngParentGroup": 3,
                        "oArticles": null,
                        "oFeatureClass": [
                            {
                                "lngFeatureID": 1,
                                "sFormat": "",
                                "sName": "Akkuspannung (V)",
                                "sValue": null,
                                "shtDataType": 1,
                                "shtFCFPos": 10,
                                "shtPos": 0,
                                "shtRepresentationType": 1,
                                "shtWebshopFilter": 1
                            },
                            {
                                "lngFeatureID": 2,
                                "sFormat": "",
                                "sName": "Akkukapazität (Ah)",
                                "sValue": null,
                                "shtDataType": 1,
                                "shtFCFPos": 20,
                                "shtPos": 0,
                                "shtRepresentationType": 1,
                                "shtWebshopFilter": 1
                            },
                            {
                                "lngFeatureID": 3,
                                "sFormat": "",
                                "sName": "Schrauben-Ø, max. ( mm )",
                                "sValue": null,
                                "shtDataType": 2,
                                "shtFCFPos": 30,
                                "shtPos": 0,
                                "shtRepresentationType": 2,
                                "shtWebshopFilter": 1
                            },
                            {
                                "lngFeatureID": 4,
                                "sFormat": "",
                                "sName": "Bohr-Ø Holz, max. ( mm )",
                                "sValue": null,
                                "shtDataType": 2,
                                "shtFCFPos": 40,
                                "shtPos": 0,
                                "shtRepresentationType": 2,
                                "shtWebshopFilter": 1
                            }
                        ],
                        "oResources": [
                            {
                                "dtExpirationDate": 0,
                                "lngGroupID": 4,
                                "lngItemID": 1,
                                "lngResourceID": 1,
                                "sHyperlinkUrl": "",
                                "sImageUrl": "",
                                "sMetaDescription": "",
                                "sResourceDescription": "",
                                "sResourceKey": "",
                                "sResourceName": "Pesta_Katalog",
                                "sResourcePath": "Pesta_Katalog.png",
                                "sResourceSource": "ftp://<Portal1 - E-Download>/Kunden/LOBOS Informatik AG_10010/Pesta_Katalog.png",
                                "shtDefault": 0,
                                "shtHTMLText": 0,
                                "shtLanguageID": 0,
                                "shtResourceGroupIDInternal": 2,
                                "shtResourcePos": 0,
                                "shtResourceTypeInternal": 0
                            },
                            {
                                "dtExpirationDate": 0,
                                "lngGroupID": 4,
                                "lngItemID": 1,
                                "lngResourceID": 8,
                                "sHyperlinkUrl": "",
                                "sImageUrl": "",
                                "sMetaDescription": "",
                                "sResourceDescription": "",
                                "sResourceKey": "",
                                "sResourceName": "Installation Document Service",
                                "sResourcePath": "Installation Document Service.pdf",
                                "sResourceSource": "ftp://<Portal1 - E-Download>/Kunden/LOBOS Informatik AG_10010/Installation Document Service.pdf",
                                "shtDefault": 0,
                                "shtHTMLText": 0,
                                "shtLanguageID": 0,
                                "shtResourceGroupIDInternal": 6,
                                "shtResourcePos": 0,
                                "shtResourceTypeInternal": 0
                            }
                        ],
                        "sDescription": "<p style=\"margin-top: 0\">\n      Akku-Bohrschrauber von Bosch sind nicht nur leistungsstark, sondern \n      setzen auch Ma&#223;st&#228;be in Gr&#246;&#223;e und Gewicht. Sie &#252;berzeugen durch \n      optimales Gewicht, Robustheit und lange Akkulaufleistung.\n    </p>",
                        "sDescriptionShort": "",
                        "sNavname": "",
                        "sTitle": "Akku-Bohrschrauber",
                        "sType": "P",
                        "sUrlPath": "/e-commerce-katalog/elektrowerkzeuge/akku-geraete/akku-bohrschrauber/"
                    },
                    {
                        "Id": "a9d3158c-67b8-11eb-91de-00155d868c02",
                        "decDirectly": 1,
                        "keywords": [],
                        "listHierarchicalCategories": [
                            {
                                "sName": "level0",
                                "sValue": "e-commerce-katalog"
                            },
                            {
                                "sName": "level1",
                                "sValue": "elektrowerkzeuge-einzeln"
                            },
                            {
                                "sName": "level2",
                                "sValue": "akku-geraete-test-eae"
                            },
                            {
                                "sName": "level3",
                                "sValue": "akku-bohrschrauber"
                            },
                            {
                                "sName": "level4",
                                "sValue": "bosch-go"
                            }
                        ],
                        "lngGroup": 19,
                        "lngItemId": 0,
                        "lngParentGroup": 16,
                        "oArticles": null,
                        "oFeatureClass": [
                            {
                                "lngFeatureID": 1,
                                "sFormat": "",
                                "sName": "Akkuspannung (V)",
                                "sValue": null,
                                "shtDataType": 1,
                                "shtFCFPos": 10,
                                "shtPos": 0,
                                "shtRepresentationType": 1,
                                "shtWebshopFilter": 1
                            },
                            {
                                "lngFeatureID": 2,
                                "sFormat": "",
                                "sName": "Akkukapazität (Ah)",
                                "sValue": null,
                                "shtDataType": 1,
                                "shtFCFPos": 20,
                                "shtPos": 0,
                                "shtRepresentationType": 1,
                                "shtWebshopFilter": 1
                            },
                            {
                                "lngFeatureID": 3,
                                "sFormat": "",
                                "sName": "Schrauben-Ø, max. ( mm )",
                                "sValue": null,
                                "shtDataType": 2,
                                "shtFCFPos": 30,
                                "shtPos": 0,
                                "shtRepresentationType": 2,
                                "shtWebshopFilter": 1
                            },
                            {
                                "lngFeatureID": 4,
                                "sFormat": "",
                                "sName": "Bohr-Ø Holz, max. ( mm )",
                                "sValue": null,
                                "shtDataType": 2,
                                "shtFCFPos": 40,
                                "shtPos": 0,
                                "shtRepresentationType": 2,
                                "shtWebshopFilter": 1
                            }
                        ],
                        "oResources": [],
                        "sDescription": "",
                        "sDescriptionShort": "",
                        "sNavname": "",
                        "sTitle": "Bosch GO",
                        "sType": "P",
                        "sUrlPath": "/e-commerce-katalog/elektrowerkzeuge-einzeln/akku-geraete-test-eae/akku-bohrschrauber/bosch-go/"
                    }
                ],
                "oUnitColl": [
                    {
                        "sQuantityUnitInput": "Stk",
                        "sQuantityUnitInputName": "Stk",
                        "shtStandard": 0
                    }
                ],
                "sArticleCode1": "",
                "sArticleCode2": "",
                "sArticleCode3": "",
                "sArticleID": "BOSCH GO",
                "sDescription": "Der Bosch GO Akku-Schrauber – Minimaler Aufwand, maximale Wirkung",
                "sEAN": "",
                "sName": "Bosch GO Test22",
                "sQuantityUnitPackage": "",
                "sQuantityUnitSales": "Stk",
                "sUrlPath": [
                    "/e-commerce-katalog/elektrowerkzeuge/akku-geraete/akku-bohrschrauber/",
                    "/e-commerce-katalog/elektrowerkzeuge-einzeln/akku-geraete-test-eae/akku-bohrschrauber/bosch-go/"
                ],
                "shtPlanningCode": 1,
                "shtStatus": 1
            },
            "oDiscount1": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount2": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount3": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount4": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount5": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount6": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "sArticleID": "BOSCH GO",
            "sArticleIDOfDataSupplier": null,
            "sArticleName": "Bosch GO Test22",
            "sCustomerArticleID": "",
            "sItemText": "",
            "sItemType": "P",
            "sItemsListID": "",
            "sOfferStatus": null,
            "sOrderStatus": "",
            "sOrderText": null,
            "sOrderType": "6",
            "sPurchOrderNumber": null,
            "sQuantityUnit": "Stk",
            "sTaxCode": "M7.7",
            "sUniformNumber": "",
            "shtBranchID": 0,
            "shtFixedItemID": 2,
            "shtHasAdditionalItems": 0,
            "shtIsAdditionalToItem": 0,
            "shtItemID": 2,
            "shtItemsList": 0,
            "shtOfferStatus": 0,
            "shtPlanningCode": 0,
            "shtStatus": 1,
            "shtStorageID": 1
        }
    ]
}
```
**or**

**Condition** : no sales-order items are found.

**Content example**

```json
{
    "perPage": 0,
    "lastPage": "-2147483648",
    "currentPage": "1",
    "total": 0,
    "data": []
}
```

## Get sales-offers

This endpoint allows you to GET sales-offers for the authenticated user (Customer)

**URL** : `/sales-offers`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters** : default filters

### Success Response

**Condition** : If sales-offers are found.

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 2,
    "lastPage": "40",
    "currentPage": "1",
    "total": 80,
    "data": [
        {
            "bCollectiveInvoice": false,
            "dtDeliveryDate": 0,
            "dtEntryDate": 1041845619000,
            "dtOrderDate": 1041811200000,
            "lngCampaignID": 0,
            "lngContactID": 0,
            "lngCustomerID": 10010,
            "lngOrderID": 390739,
            "lngProjectID": 0,
            "sContactName": "",
            "sDCity": "",
            "sDCompany1": "",
            "sDCompany2": "",
            "sDCompany3": "",
            "sDCompany4": "",
            "sDContact": "",
            "sDCountry": "",
            "sDCountryCode": "",
            "sDStreet": "",
            "sDZipCode": "",
            "sICity": "Schwerzenbach",
            "sICompany1": "LOBOS Informatik AG",
            "sICompany2": "",
            "sICompany3": "",
            "sICompany4": "",
            "sIContact": "Herrn Werner Locher",
            "sICountry": "",
            "sICountryCode": "",
            "sIPostBox": "",
            "sIStreet": "Bahnstrasse 25",
            "sIZipBox": "",
            "sIZipCode": "8603",
            "sOrderText": "",
            "sOrderType": "A",
            "shtBlocked": 0,
            "shtOfferStatus": 2,
            "shtPaymentCondition": 2,
            "shtShippingCondition": 0,
            "shtStatus": 1
        },
        {
            "bCollectiveInvoice": false,
            "dtDeliveryDate": 0,
            "dtEntryDate": 1041853937000,
            "dtOrderDate": 1041811200000,
            "lngCampaignID": 0,
            "lngContactID": 0,
            "lngCustomerID": 10010,
            "lngOrderID": 390740,
            "lngProjectID": 0,
            "sContactName": "",
            "sDCity": "",
            "sDCompany1": "",
            "sDCompany2": "",
            "sDCompany3": "",
            "sDCompany4": "",
            "sDContact": "",
            "sDCountry": "",
            "sDCountryCode": "",
            "sDStreet": "",
            "sDZipCode": "",
            "sICity": "Schwerzenbach",
            "sICompany1": "LOBOS Informatik AG",
            "sICompany2": "",
            "sICompany3": "",
            "sICompany4": "",
            "sIContact": "Herrn Werner Locher",
            "sICountry": "",
            "sICountryCode": "",
            "sIPostBox": "",
            "sIStreet": "Bahnstrasse 25",
            "sIZipBox": "",
            "sIZipCode": "8603",
            "sOrderText": "",
            "sOrderType": "A",
            "shtBlocked": 0,
            "shtOfferStatus": 3,
            "shtPaymentCondition": 2,
            "shtShippingCondition": 0,
            "shtStatus": 1
        }
    ]
}
```
**or**

**Condition** : no sales-orders are found.

**Content example**

```json
{
    "text": "Auftrag nicht gefunden."
}
```

## Get sales-offers by id

This endpoint allows you to GET a sales-offer by id

**URL** : `/sales-offers/:id`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

### Success Response

**Condition** : If sales-offer are found.

**Code** : `200 OK`

**Content example**

```json
{
    "bCollectiveInvoice": false,
    "dtDeliveryDate": 0,
    "dtEntryDate": 1041853937000,
    "dtOrderDate": 1041811200000,
    "lngCampaignID": 0,
    "lngContactID": 0,
    "lngCustomerID": 10010,
    "lngOrderID": 390740,
    "lngProjectID": 0,
    "sContactName": "",
    "sDCity": "",
    "sDCompany1": "",
    "sDCompany2": "",
    "sDCompany3": "",
    "sDCompany4": "",
    "sDContact": "",
    "sDCountry": "",
    "sDCountryCode": "",
    "sDStreet": "",
    "sDZipCode": "",
    "sICity": "Schwerzenbach",
    "sICompany1": "LOBOS Informatik AG",
    "sICompany2": "",
    "sICompany3": "",
    "sICompany4": "",
    "sIContact": "Herrn Werner Locher",
    "sICountry": "",
    "sICountryCode": "",
    "sIPostBox": "",
    "sIStreet": "Bahnstrasse 25",
    "sIZipBox": "",
    "sIZipCode": "8603",
    "sOrderText": "",
    "sOrderType": "A",
    "shtBlocked": 0,
    "shtOfferStatus": 3,
    "shtPaymentCondition": 2,
    "shtShippingCondition": 0,
    "shtStatus": 1
}
```
**or**

**Condition** : no sales-order are found.

**Content example**

```json
{
    "text": "Auftrag nicht gefunden."
}
```

## Get sales-offers items

This endpoint allows you to GET all the sales-offer items

**URL** : `/sales-offers/:id/items`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters** : default filters

### Success Response

**Condition** : If sales-offer items are found.

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 2,
    "lastPage": "7",
    "currentPage": "1",
    "total": 14,
    "data": [
        {
            "bAlternativeItem": false,
            "bBlockDelivery": false,
            "bPartialDelivery": false,
            "decFactorSalesPrice": 0,
            "decItemGrossAmountFC": 0,
            "decItemNetAmountFC": 0,
            "decItemTaxAmountFC": 0,
            "decPrice": 0,
            "decPriceFactor": 0,
            "decPricePG": 0,
            "decQuantityDelivered": 0,
            "decQuantityDelivered2": 0,
            "decQuantityOrdered": 0,
            "decTaxRate": 0,
            "dtDeliveryDate": 0,
            "dtDeliveryNoteIDDate": 0,
            "dtInvoiceDate": 0,
            "dtRequestedDate": 0,
            "lngCampaignID": 0,
            "lngCustomerOrderID": 0,
            "lngDeliveryNoteID": 0,
            "lngGoodsReceiptID": 0,
            "lngInvoiceID": 0,
            "lngOrderID": 390740,
            "lngPackingListID": 0,
            "lngSalesPriceUnit": 0,
            "lngSupplierID": 0,
            "oArticle": {
                "decQuantityPackage": 0,
                "decSalesPrice1": 0,
                "lngSalesPriceUnit": 0,
                "oFeatures": [],
                "oPriceInfo": null,
                "oProductInfo": null,
                "oUnitColl": [
                    {
                        "sQuantityUnitInput": "##Invalid##",
                        "sQuantityUnitInputName": "##Invalid##",
                        "shtStandard": 0
                    }
                ],
                "sArticleCode1": "",
                "sArticleCode2": "",
                "sArticleCode3": "",
                "sArticleID": " ",
                "sDescription": "",
                "sEAN": "",
                "sName": "",
                "sQuantityUnitPackage": "",
                "sQuantityUnitSales": "",
                "sUrlPath": null,
                "shtPlanningCode": 0,
                "shtStatus": 0
            },
            "oDiscount1": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount2": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount3": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount4": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount5": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount6": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "sArticleID": " ",
            "sArticleIDOfDataSupplier": null,
            "sArticleName": "Lizenzen SQL-Business",
            "sCustomerArticleID": "",
            "sItemText": "",
            "sItemType": "G",
            "sItemsListID": "",
            "sOfferStatus": null,
            "sOrderStatus": "Verloren",
            "sOrderText": null,
            "sOrderType": "A",
            "sPurchOrderNumber": null,
            "sQuantityUnit": "",
            "sTaxCode": "",
            "sUniformNumber": "",
            "shtBranchID": 1,
            "shtFixedItemID": 1,
            "shtHasAdditionalItems": 0,
            "shtIsAdditionalToItem": 0,
            "shtItemID": 1,
            "shtItemsList": 0,
            "shtOfferStatus": 3,
            "shtPlanningCode": 0,
            "shtStatus": 1,
            "shtStorageID": 0
        },
        {
            "bAlternativeItem": false,
            "bBlockDelivery": false,
            "bPartialDelivery": false,
            "decFactorSalesPrice": 0,
            "decItemGrossAmountFC": 0,
            "decItemNetAmountFC": 0,
            "decItemTaxAmountFC": 0,
            "decPrice": 0,
            "decPriceFactor": 0,
            "decPricePG": 0,
            "decQuantityDelivered": 0,
            "decQuantityDelivered2": 0,
            "decQuantityOrdered": 0,
            "decTaxRate": 0,
            "dtDeliveryDate": 0,
            "dtDeliveryNoteIDDate": 0,
            "dtInvoiceDate": 0,
            "dtRequestedDate": 0,
            "lngCampaignID": 0,
            "lngCustomerOrderID": 0,
            "lngDeliveryNoteID": 0,
            "lngGoodsReceiptID": 0,
            "lngInvoiceID": 0,
            "lngOrderID": 390740,
            "lngPackingListID": 0,
            "lngSalesPriceUnit": 0,
            "lngSupplierID": 0,
            "oArticle": {
                "decQuantityPackage": 0,
                "decSalesPrice1": 0,
                "lngSalesPriceUnit": 0,
                "oFeatures": [],
                "oPriceInfo": null,
                "oProductInfo": null,
                "oUnitColl": [
                    {
                        "sQuantityUnitInput": "##Invalid##",
                        "sQuantityUnitInputName": "##Invalid##",
                        "shtStandard": 0
                    }
                ],
                "sArticleCode1": "",
                "sArticleCode2": "",
                "sArticleCode3": "",
                "sArticleID": " ",
                "sDescription": "",
                "sEAN": "",
                "sName": "",
                "sQuantityUnitPackage": "",
                "sQuantityUnitSales": "",
                "sUrlPath": null,
                "shtPlanningCode": 0,
                "shtStatus": 0
            },
            "oDiscount1": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount2": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount3": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount4": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount5": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "oDiscount6": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": ""
            },
            "sArticleID": " ",
            "sArticleIDOfDataSupplier": null,
            "sArticleName": "<F>SQL-Business Verkauf...",
            "sCustomerArticleID": "",
            "sItemText": "<F>SQL-Business Verkauf",
            "sItemType": "T",
            "sItemsListID": "",
            "sOfferStatus": null,
            "sOrderStatus": "Verloren",
            "sOrderText": null,
            "sOrderType": "A",
            "sPurchOrderNumber": null,
            "sQuantityUnit": "",
            "sTaxCode": "",
            "sUniformNumber": "",
            "shtBranchID": 1,
            "shtFixedItemID": 9,
            "shtHasAdditionalItems": 0,
            "shtIsAdditionalToItem": 0,
            "shtItemID": 2,
            "shtItemsList": 0,
            "shtOfferStatus": 3,
            "shtPlanningCode": 0,
            "shtStatus": 1,
            "shtStorageID": 0
        }
    ]
}
```
**or**

**Condition** : no sales-offer items are found.

**Content example**

```json
{
    "perPage": 0,
    "lastPage": "-2147483648",
    "currentPage": "1",
    "total": 0,
    "data": []
}
```

## Get sales-credit-notes

This endpoint allows you to GET sales-credit-notes for the authenticated user (Customer)

**URL** : `/sales-credit-notes`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters** : default filters

### Success Response

**Condition** : If sales-credit-notes are found.

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 1,
    "lastPage": "1",
    "currentPage": "1",
    "total": 1,
    "data": [
        {
            "bCollectiveInvoice": false,
            "dtDeliveryDate": 1219231685000,
            "dtEntryDate": 1219231685000,
            "dtOrderDate": 1219231685000,
            "lngCampaignID": 0,
            "lngContactID": 0,
            "lngCustomerID": 10010,
            "lngOrderID": 850199,
            "lngProjectID": 0,
            "sContactName": "",
            "sDCity": "",
            "sDCompany1": "",
            "sDCompany2": "",
            "sDCompany3": "",
            "sDCompany4": "",
            "sDContact": "",
            "sDCountry": "",
            "sDCountryCode": "",
            "sDStreet": "",
            "sDZipCode": "",
            "sICity": "Schwerzenbach",
            "sICompany1": "LOBOS Informatik AG",
            "sICompany2": "",
            "sICompany3": "",
            "sICompany4": "",
            "sIContact": "",
            "sICountry": "Schweiz",
            "sICountryCode": "CH",
            "sIPostBox": "",
            "sIStreet": "Bahnstrasse 25",
            "sIZipBox": "",
            "sIZipCode": "8603",
            "sOrderText": "",
            "sOrderType": "G",
            "shtBlocked": 0,
            "shtOfferStatus": 0,
            "shtPaymentCondition": 1,
            "shtShippingCondition": 0,
            "shtStatus": 5
        }
    ]
}
```
**or**

**Condition** : no sales-orders are found.

**Content example**

```json
{
    "text": "Auftrag nicht gefunden."
}
```

## Get sales-credit-notes by id

This endpoint allows you to GET a sales-credit-notes by id

**URL** : `/sales-credit-notes/:id`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

### Success Response

**Condition** : If sales-credit-notes are found.

**Code** : `200 OK`

**Content example**

```json
{
    "bCollectiveInvoice": false,
    "dtDeliveryDate": 1219231685000,
    "dtEntryDate": 1219231685000,
    "dtOrderDate": 1219231685000,
    "lngCampaignID": 0,
    "lngContactID": 0,
    "lngCustomerID": 10010,
    "lngOrderID": 850199,
    "lngProjectID": 0,
    "sContactName": "",
    "sDCity": "",
    "sDCompany1": "",
    "sDCompany2": "",
    "sDCompany3": "",
    "sDCompany4": "",
    "sDContact": "",
    "sDCountry": "",
    "sDCountryCode": "",
    "sDStreet": "",
    "sDZipCode": "",
    "sICity": "Schwerzenbach",
    "sICompany1": "LOBOS Informatik AG",
    "sICompany2": "",
    "sICompany3": "",
    "sICompany4": "",
    "sIContact": "",
    "sICountry": "Schweiz",
    "sICountryCode": "CH",
    "sIPostBox": "",
    "sIStreet": "Bahnstrasse 25",
    "sIZipBox": "",
    "sIZipCode": "8603",
    "sOrderText": "",
    "sOrderType": "G",
    "shtBlocked": 0,
    "shtOfferStatus": 0,
    "shtPaymentCondition": 1,
    "shtShippingCondition": 0,
    "shtStatus": 5
}
```
**or**

**Condition** : no sales-credit-notes are found.

**Content example**

```json
{
    "text": "Auftrag nicht gefunden."
}
```

## Get sales-credit-notes items

This endpoint allows you to GET all the sales-credit-note items

**URL** : `/sales-credit-notes/:id/items`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

**Pagination** : Yes

**Query parameters** : default filters

### Success Response

**Condition** : If sales-credit-notes items are found.

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 2,
    "lastPage": "5",
    "currentPage": "1",
    "total": 9,
    "data": [
        {
            "bAlternativeItem": false,
            "bBlockDelivery": false,
            "bPartialDelivery": false,
            "decFactorSalesPrice": 0,
            "decItemGrossAmountFC": 0,
            "decItemNetAmountFC": 0,
            "decItemTaxAmountFC": 0,
            "decPrice": 0,
            "decPriceFactor": 0,
            "decPricePG": 0,
            "decQuantityDelivered": 0,
            "decQuantityDelivered2": 0,
            "decQuantityOrdered": 0,
            "decTaxRate": 0,
            "dtDeliveryDate": 1219231685000,
            "dtDeliveryNoteIDDate": 0,
            "dtInvoiceDate": 1219231715000,
            "dtRequestedDate": 1219228678000,
            "lngCampaignID": 0,
            "lngCustomerOrderID": 0,
            "lngDeliveryNoteID": 0,
            "lngGoodsReceiptID": 0,
            "lngInvoiceID": 22825,
            "lngOrderID": 850199,
            "lngPackingListID": 0,
            "lngSalesPriceUnit": 0,
            "lngSupplierID": 0,
            "oArticle": {
                "decQuantityPackage": 0,
                "decSalesPrice1": 0,
                "lngSalesPriceUnit": 0,
                "oFeatures": [],
                "oPriceInfo": null,
                "oProductInfo": null,
                "oUnitColl": [
                    {
                        "sQuantityUnitInput": "##Invalid##",
                        "sQuantityUnitInputName": "##Invalid##",
                        "shtStandard": 0
                    }
                ],
                "sArticleCode1": "",
                "sArticleCode2": "",
                "sArticleCode3": "",
                "sArticleID": " ",
                "sDescription": "",
                "sEAN": "",
                "sName": "",
                "sQuantityUnitPackage": "",
                "sQuantityUnitSales": "",
                "sUrlPath": null,
                "shtPlanningCode": 0,
                "shtStatus": 0
            },
            "oDiscount1": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "oDiscount2": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "oDiscount3": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "oDiscount4": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "oDiscount5": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "oDiscount6": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "sArticleID": " ",
            "sArticleIDOfDataSupplier": null,
            "sArticleName": "Gruppentitel",
            "sCustomerArticleID": "",
            "sItemText": "",
            "sItemType": "G",
            "sItemsListID": "",
            "sOfferStatus": null,
            "sOrderStatus": "",
            "sOrderText": null,
            "sOrderType": "G",
            "sPurchOrderNumber": null,
            "sQuantityUnit": "",
            "sTaxCode": "",
            "sUniformNumber": "",
            "shtBranchID": 1,
            "shtFixedItemID": 1,
            "shtHasAdditionalItems": 0,
            "shtIsAdditionalToItem": 0,
            "shtItemID": 1,
            "shtItemsList": 0,
            "shtOfferStatus": 0,
            "shtPlanningCode": 0,
            "shtStatus": 6,
            "shtStorageID": 1
        },
        {
            "bAlternativeItem": false,
            "bBlockDelivery": false,
            "bPartialDelivery": false,
            "decFactorSalesPrice": 1.000000000000000,
            "decItemGrossAmountFC": 0,
            "decItemNetAmountFC": 0,
            "decItemTaxAmountFC": 0,
            "decPrice": 300.00,
            "decPriceFactor": 1.00000000000000,
            "decPricePG": 0,
            "decQuantityDelivered": 1.000,
            "decQuantityDelivered2": 0,
            "decQuantityOrdered": 1.000,
            "decTaxRate": 7.60,
            "dtDeliveryDate": 1219231685000,
            "dtDeliveryNoteIDDate": 0,
            "dtInvoiceDate": 1219231715000,
            "dtRequestedDate": 1219228678000,
            "lngCampaignID": 0,
            "lngCustomerOrderID": 0,
            "lngDeliveryNoteID": 0,
            "lngGoodsReceiptID": 0,
            "lngInvoiceID": 22825,
            "lngOrderID": 850199,
            "lngPackingListID": 0,
            "lngSalesPriceUnit": 0,
            "lngSupplierID": 0,
            "oArticle": {
                "decQuantityPackage": 0,
                "decSalesPrice1": 0.00,
                "lngSalesPriceUnit": 1,
                "oFeatures": [],
                "oPriceInfo": null,
                "oProductInfo": null,
                "oUnitColl": [
                    {
                        "sQuantityUnitInput": "%",
                        "sQuantityUnitInputName": "%",
                        "shtStandard": 1
                    },
                    {
                        "sQuantityUnitInput": "Liz",
                        "sQuantityUnitInputName": "Liz",
                        "shtStandard": 0
                    }
                ],
                "sArticleCode1": "",
                "sArticleCode2": "",
                "sArticleCode3": "",
                "sArticleID": "NV-CG-00",
                "sDescription": "eNVenta ERP Crossgrade\n\nAnzahl eNVenta ERP-Benutzer: __\n\nBasis:\n- bestehende SQL-Business Lizenzen\n- gültiger SW-Wartungsvertrag",
                "sEAN": "",
                "sName": "eNVenta ERP Crossgrade",
                "sQuantityUnitPackage": "",
                "sQuantityUnitSales": "Liz",
                "sUrlPath": null,
                "shtPlanningCode": 4,
                "shtStatus": 1
            },
            "oDiscount1": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "oDiscount2": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "oDiscount3": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "oDiscount4": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "oDiscount5": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "oDiscount6": {
                "decDiscountAmount": 0.00,
                "decDiscountPercent": 0.00,
                "decDiscountValue": 0,
                "lngDiscountID": 0,
                "sDiscountText": "",
                "sDiscountType": "M"
            },
            "sArticleID": "NV-CG-00",
            "sArticleIDOfDataSupplier": null,
            "sArticleName": "NVinity® Crossgrade",
            "sCustomerArticleID": "",
            "sItemText": "",
            "sItemType": "P",
            "sItemsListID": "",
            "sOfferStatus": null,
            "sOrderStatus": "",
            "sOrderText": null,
            "sOrderType": "G",
            "sPurchOrderNumber": null,
            "sQuantityUnit": "Liz",
            "sTaxCode": "M7.6",
            "sUniformNumber": "",
            "shtBranchID": 1,
            "shtFixedItemID": 2,
            "shtHasAdditionalItems": 0,
            "shtIsAdditionalToItem": 0,
            "shtItemID": 2,
            "shtItemsList": 0,
            "shtOfferStatus": 0,
            "shtPlanningCode": 0,
            "shtStatus": 6,
            "shtStorageID": 1
        }
    ]
}
```
**or**

**Condition** : no sales-credit-notes items are found.

**Content example**

```json
{
    "perPage": 0,
    "lastPage": "-2147483648",
    "currentPage": "1",
    "total": 0,
    "data": []
}
```