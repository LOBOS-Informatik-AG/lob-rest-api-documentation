# SO-Carts

## Get carts

This endpoint allows you to get the cart headers for the authenticated user

**URL** : `/so-carts`

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
  {
    "bCollectiveInvoice": false,
    "decTotalOrderGrossAmount": 0,
    "decTotalOrderNetAmount": 0,
    "decTotalOrderTax": 0,
    "dtDeliveryDate": 1639958400000,
    "dtEntryDate": 1640007900000,
    "dtOrderDate": 1640007900000,
    "lngCampaignID": 0,
    "lngContactID": 0,
    "lngCustomerID": 123456,
    "lngOrderID": 111222333,
    "lngPayConnectionID": 0,
    "lngProjectID": 0,
    "oContact": {
      "dtAlterationDate": "",
      "dtEntryDate": "",
      "lngContactId": null,
      "sDepartmentName": "",
      "sEmail": "",
      "sFirstName": "",
      "sFormOfAdress": "",
      "sLastName": "",
      "sMobilePhone": "",
      "sPhone": "",
      "sPosition": "",
      "shtInactive": null
    },
    "oDeliveryAddress": {
      "lngAddressID": null,
      "lngContactID": null,
      "lngCustomerID": null,
      "lngRouteBaseID": null,
      "sCity": "",
      "sCompany1": "",
      "sCompany2": "",
      "sContact": "",
      "sCountry": "",
      "sCountryCode": "",
      "sMemo": "",
      "sPostBox": "",
      "sStreet": "",
      "sZipBox": "",
      "sZipCode": ""
    },
    "oInvoiceAddress": {
      "lngAddressID": null,
      "lngContactID": null,
      "lngCustomerID": null,
      "lngRouteBaseID": null,
      "sCity": "testCity",
      "sCompany1": "testCompany",
      "sCompany2": "",
      "sContact": "",
      "sCountry": "testCountry",
      "sCountryCode": "AT",
      "sMemo": "",
      "sPostBox": "",
      "sStreet": "testStreet 123",
      "sZipBox": "",
      "sZipCode": "1234"
    },
    "oShippingCondition": {
      "sName": "01 - Abholung",
      "shtP48APICollection": null,
      "shtP48APIDeliveryOptions": null,
      "shtShippingTypeID": 1
    },
    "sCartName": "testCartName",
    "sContactName": "",
    "sIContact": "",
    "sMemo": "",
    "sOrderKind": "Onlineshop",
    "sOrderText": "",
    "sOrderType": "A100",
    "sPaymentID": "",
    "sPaymentIDType": "",
    "sShippingMemo": "",
    "shtBlocked": 0,
    "shtOfferStatus": 0,
    "shtPaymentCondition": 5,
    "shtShippingCondition": 1,
    "shtStatus": 1
  },
  { }
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

**URL** : `/so-carts/:id` (`/so-carts/123456` in example)

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : No

### Success Response

**Condition** : If the cart is found.

**Code** : `200 OK`

**Content example**

```json
{
  "oSalesItemList": [
    {
      "bAlternativeItem": false,
      "bBlockDelivery": false,
      "bPartialDelivery": false,
      "decFactorSalesPrice": 1.000000000000000,
      "decItemGrossAmountFC": 0.00,
      "decItemNetAmountFC": 0.00,
      "decItemTaxAmountFC": 0,
      "decPrice": 0.00,
      "decPriceFactor": 1.00000000000000,
      "decPricePG": 0,
      "decQuantity": 0,
      "decQuantityDelivered": 3.000,
      "decQuantityDelivered2": 0,
      "decQuantityOrdered": 3.000,
      "decSalesPrice": 0,
      "decTaxRate": 20.00,
      "dtDeliveryDate": 1640649600000,
      "dtDeliveryNoteIDDate": 0,
      "dtInvoiceDate": 0,
      "dtRequestedDate": 1640649600000,
      "lngCampaignID": 0,
      "lngCustomerOrderID": 0,
      "lngDeliveryNoteID": 0,
      "lngGoodsReceiptID": 0,
      "lngInvoiceID": 0,
      "lngOrderID": 123456,
      "lngPackingListID": 0,
      "lngSalesPriceUnit": 0,
      "lngSupplierID": 112233,
      "oArticle": {},
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
      "oSteelConfiguration": null,
      "sArticleID": "TESTARTICLE",
      "sArticleIDOfDataSupplier": null,
      "sArticleName": "testName",
      "sCustomerArticleID": "",
      "sItemText": "",
      "sItemType": "P",
      "sItemsListID": "",
      "sOfferStatus": null,
      "sOrderStatus": "offen",
      "sOrderText": null,
      "sOrderType": "A100",
      "sPurchOrderNumber": null,
      "sQuantityUnit": "mt",
      "sTaxCode": "MAT20",
      "sUniformNumber": "777777",
      "shtBranchID": 0,
      "shtFixedItemID": 1,
      "shtHasAdditionalItems": 0,
      "shtIsAdditionalToItem": 0,
      "shtItemID": 1,
      "shtItemsList": 0,
      "shtOfferStatus": 0,
      "shtPlanningCode": 0,
      "shtProcessedItem": 0,
      "shtRestOfItem": 0,
      "shtStatus": 1,
      "shtSteelprocessing": 0,
      "shtStorageID": 1000
    },
    { }
  ],
  "oSalesMaster": {
    "bCollectiveInvoice": false,
    "decTotalOrderGrossAmount": 0,
    "decTotalOrderNetAmount": 0,
    "decTotalOrderTax": 0,
    "dtDeliveryDate": 1640649600000,
    "dtEntryDate": 1640707728000,
    "dtOrderDate": 1640707728000,
    "lngCampaignID": 0,
    "lngContactID": 0,
    "lngCustomerID": 112233,
    "lngOrderID": 123456,
    "lngPayConnectionID": 0,
    "lngProjectID": 0,
    "oContact": {
      "dtAlterationDate": "",
      "dtEntryDate": "",
      "lngContactId": null,
      "sDepartmentName": "",
      "sEmail": "",
      "sFirstName": "",
      "sFormOfAdress": "",
      "sLastName": "",
      "sMobilePhone": "",
      "sPhone": "",
      "sPosition": "",
      "shtInactive": null
    },
    "oDeliveryAddress": {
      "lngAddressID": null,
      "lngContactID": null,
      "lngCustomerID": null,
      "lngRouteBaseID": null,
      "sCity": "",
      "sCompany1": "",
      "sCompany2": "",
      "sContact": "",
      "sCountry": "",
      "sCountryCode": "",
      "sMemo": "",
      "sPostBox": "",
      "sStreet": "",
      "sZipBox": "",
      "sZipCode": ""
    },
    "oInvoiceAddress": {
      "lngAddressID": null,
      "lngContactID": null,
      "lngCustomerID": null,
      "lngRouteBaseID": null,
      "sCity": "testCity",
      "sCompany1": "testCompany",
      "sCompany2": "",
      "sContact": "",
      "sCountry": "testCountry",
      "sCountryCode": "AT",
      "sMemo": "",
      "sPostBox": "",
      "sStreet": "testStreet 123",
      "sZipBox": "",
      "sZipCode": "1234"
    },
    "oShippingCondition": {
      "sName": "01 - Abholung",
      "shtP48APICollection": null,
      "shtP48APIDeliveryOptions": null,
      "shtShippingTypeID": 1
    },
    "sCartName": "testCartName",
    "sContactName": "",
    "sIContact": "",
    "sMemo": "",
    "sOrderKind": "Onlineshop",
    "sOrderText": "",
    "sOrderType": "A100",
    "sPaymentID": "",
    "sPaymentIDType": "",
    "sShippingMemo": "",
    "shtBlocked": 0,
    "shtOfferStatus": 0,
    "shtPaymentCondition": 5,
    "shtShippingCondition": 1,
    "shtStatus": 1
  }
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

**URL** : `/so-carts`

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```json
{
    "lngCampaignID": 0,
    "lngProjectId": 0,
    "sCartName": "testcartName",
    "oDeliveryAddress":
    {
        "sCity": "deliverCity",
        "sCompany1": "deliverTest1",
        "sCompany2": "deliverTest2",
        "sContact": "deliverContact",
        "sCountry": "Österreich",
        "sCountryCode": "AT",
        "sStreet": "deliverStreet 123",
        "sZipCode": "4321"
    }
}
```

### Success Response

**Condition** : If the cart is successfully created.

**Code** : `200 OK`

**Content example**

```json
{
  "bCollectiveInvoice": false,
  "decTotalOrderGrossAmount": 0,
  "decTotalOrderNetAmount": 0,
  "decTotalOrderTax": 0,
  "dtDeliveryDate": 1640736000000,
  "dtEntryDate": 1640794279000,
  "dtOrderDate": 1640794279000,
  "lngCampaignID": 0,
  "lngContactID": 0,
  "lngCustomerID": 999999,
  "lngOrderID": 123456,
  "lngPayConnectionID": 0,
  "lngProjectID": 0,
  "oContact": {
    "dtAlterationDate": "",
    "dtEntryDate": "",
    "lngContactId": null,
    "sDepartmentName": "",
    "sEmail": "",
    "sFirstName": "",
    "sFormOfAdress": "",
    "sLastName": "",
    "sMobilePhone": "",
    "sPhone": "",
    "sPosition": "",
    "shtInactive": null
  },
  "oDeliveryAddress": {
    "lngAddressID": null,
    "lngContactID": null,
    "lngCustomerID": null,
    "lngRouteBaseID": null,
    "sCity": "deliverCity",
    "sCompany1": "deliverTest1",
    "sCompany2": "deliverTest2",
    "sContact": "deliverContact",
    "sCountry": "Österreich",
    "sCountryCode": "AT",
    "sMemo": "",
    "sPostBox": "",
    "sStreet": "deliverStreet 123",
    "sZipBox": "",
    "sZipCode": "4321"
  },
  "oInvoiceAddress": {
    "lngAddressID": null,
    "lngContactID": null,
    "lngCustomerID": null,
    "lngRouteBaseID": null,
    "sCity": "testCity",
    "sCompany1": "testCompany",
    "sCompany2": "",
    "sContact": "",
    "sCountry": "Österreich",
    "sCountryCode": "AT",
    "sMemo": "",
    "sPostBox": "",
    "sStreet": "testStreet 12",
    "sZipBox": "",
    "sZipCode": "1234"
  },
  "oShippingCondition": {
    "sName": "01 - Abholung",
    "shtP48APICollection": null,
    "shtP48APIDeliveryOptions": null,
    "shtShippingTypeID": 1
  },
  "sCartName": "testcartName",
  "sContactName": "",
  "sIContact": "",
  "sMemo": "",
  "sOrderKind": "Onlineshop",
  "sOrderText": "",
  "sOrderType": "A100",
  "sPaymentID": "",
  "sPaymentIDType": "",
  "sShippingMemo": "",
  "shtBlocked": 0,
  "shtOfferStatus": 0,
  "shtPaymentCondition": 5,
  "shtShippingCondition": 1,
  "shtStatus": 1
}
```

## Update cart

This endpoint allows you to update a cart

**URL** : `/so-carts/:id` (`/so-carts/123456` in example)

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```json
{
"oSalesMaster": {
        "bCollectiveInvoice": true,
        "dtDeliveryDate": 1636549916000,
        "dtEntryDate": 1635343921000,
        "dtOrderDate": 1635336716000,
        "lngCampaignID": 0,
        "lngContactID": 0,
        "lngCustomerID": 888888,
        "lngOrderID": 123456,
        "lngPayConnectionID": 0,
        "lngProjectID": 0,
        "sCartName": "testcart 200",
        "sContactName": "",
        "sDCity": "deliverCitytestchange",
        "sDCompany1": "deliverTest1",
        "sDCompany2": "deliverTest2",
        "sDCompany3": "deliverTest3",
        "sDCompany4": "deliverTest4",
        "sDContact": "deliverContact",
        "sDCountry": "Österreich",
        "sDCountryCode": "AT",
        "sDStreet": "deliverStreet 123",
        "sDZipCode": "4321",
        "sICity": "invoiceCity",
        "sICompany1": "invoiceTest1",
        "sICompany2": "invoiceTest2",
        "sICompany3": "invoiceTest3",
        "sICompany4": "invoiceTest4",
        "sIContact": "invoiceContact",
        "sICountry": "Schweiz",
        "sICountryCode": "CH",
        "sIPostBox": "",
        "sIStreet": "invoiceStreet",
        "sIZipBox": "",
        "sIZipCode": "5678",
        "sMemo": "",
        "sOrderKind": "Onlineshop",
        "sOrderText": "",
        "sOrderType": "A300",
        "sPaymentID": "",
        "sPaymentIDType": "",
        "shtBlocked": 1,
        "shtOfferStatus": 0,
        "shtPaymentCondition": 2,
        "shtShippingCondition": 1,
        "shtStatus": 1
    }
}
```

### Success Response

**Condition** : If the cart is successfully updated.

**Code** : `200 OK`

**Content example**

```json
{
  "oSalesItemList": [],
  "oSalesMaster": {
    "bCollectiveInvoice": false,
    "decTotalOrderGrossAmount": 0,
    "decTotalOrderNetAmount": 0,
    "decTotalOrderTax": 0,
    "dtDeliveryDate": 1636549916000,
    "dtEntryDate": 1640794279000,
    "dtOrderDate": 1640794279000,
    "lngCampaignID": 0,
    "lngContactID": 0,
    "lngCustomerID": 888888,
    "lngOrderID": 123456,
    "lngPayConnectionID": 0,
    "lngProjectID": 0,
    "oContact": {
      "dtAlterationDate": "",
      "dtEntryDate": "",
      "lngContactId": 0,
      "sDepartmentName": "",
      "sEmail": "",
      "sFirstName": "",
      "sFormOfAdress": "",
      "sLastName": "",
      "sMobilePhone": "",
      "sPhone": "",
      "sPosition": "",
      "shtInactive": null
    },
    "oDeliveryAddress": {
      "lngAddressID": null,
      "lngContactID": null,
      "lngCustomerID": null,
      "lngRouteBaseID": null,
      "sCity": "deliverCity",
      "sCompany1": "deliverTest1",
      "sCompany2": "deliverTest2",
      "sContact": "deliverContact",
      "sCountry": "Österreich",
      "sCountryCode": "AT",
      "sMemo": "",
      "sPostBox": "",
      "sStreet": "deliverStreet 123",
      "sZipBox": "",
      "sZipCode": "4321"
    },
    "oInvoiceAddress": {
      "lngAddressID": null,
      "lngContactID": null,
      "lngCustomerID": null,
      "lngRouteBaseID": null,
      "sCity": "testCity",
      "sCompany1": "testCompany",
      "sCompany2": "",
      "sContact": "",
      "sCountry": "testCountry",
      "sCountryCode": "AT",
      "sMemo": "",
      "sPostBox": "",
      "sStreet": "testStreet 12",
      "sZipBox": "",
      "sZipCode": "1234"
    },
    "oShippingCondition": {
      "sName": "01 - Abholung",
      "shtP48APICollection": null,
      "shtP48APIDeliveryOptions": null,
      "shtShippingTypeID": 1
    },
    "sCartName": "testcart 200",
    "sContactName": "",
    "sIContact": "invoiceContact",
    "sMemo": "",
    "sOrderKind": "Onlineshop",
    "sOrderText": "",
    "sOrderType": "A100",
    "sPaymentID": "",
    "sPaymentIDType": "",
    "sShippingMemo": "",
    "shtBlocked": 0,
    "shtOfferStatus": 0,
    "shtPaymentCondition": 2,
    "shtShippingCondition": 1,
    "shtStatus": 1
  }
}
```


## Activate cart

This endpoint allows you to activate a cart

**URL** : `/so-carts/:id/activate`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```
None
```

### Success Response

**Condition** : If the cart is activated successfully.

**Code** : `200 OK`

**Content example**

```json
{
  "oSalesItemList": [],
  "oSalesMaster": {}
}
```

## Submit cart

This endpoint allows you to submit a cart

**URL** : `/so-carts/:id/submit`

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```
None
```

### Success Response

**Condition** : If the cart is submitted successfully.

**Code** : `200 OK`

**Content example**

```json
{
  "oSalesItemList": [],
  "oSalesMaster": {}
}
```


## Delete cart

This endpoint allows you to delete a cart

**URL** : `/so-carts/:id`

**Method** : <img src="https://img.shields.io/badge/DELETE%20-%23323330.svg?&style=flat&color=red"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```
None
```

### Success Response

**Condition** : If the cart is deleted successfully.

**Code** : `200 OK`

**Content example**

```
None
```

## Create cart-item

This endpoint allows you to create a cart-item

**URL** : `/so-carts/:id/items` (`/so-carts/123456/items` in example)

**Method** : <img src="https://img.shields.io/badge/POST%20-%23323330.svg?&style=flat&color=blue"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```json
{
  "sArticleID": "TESTARTICLE",
  "decQuantityOrdered": 777.000,
  "sQuantityUnit": "kg"
}
```

### Success Response

**Condition** : If the item is successfully created.

**Code** : `200 OK`

**Content example**

```json
{
  "oSalesItemList": [
    {
      "bAlternativeItem": false,
      "bBlockDelivery": false,
      "bPartialDelivery": false,
      "decFactorSalesPrice": 1.000000000000000,
      "decItemGrossAmountFC": 0,
      "decItemNetAmountFC": 0,
      "decItemTaxAmountFC": 0,
      "decPrice": 0,
      "decPriceFactor": 1.00000000000000,
      "decPricePG": 0,
      "decQuantity": 0,
      "decQuantityDelivered": 777.000,
      "decQuantityDelivered2": 0,
      "decQuantityOrdered": 777.000,
      "decSalesPrice": 0,
      "decTaxRate": 0.00,
      "dtDeliveryDate": 1640736000000,
      "dtDeliveryNoteIDDate": 0,
      "dtInvoiceDate": 0,
      "dtRequestedDate": 1640736000000,
      "lngCampaignID": 0,
      "lngCustomerOrderID": 0,
      "lngDeliveryNoteID": 0,
      "lngGoodsReceiptID": 0,
      "lngInvoiceID": 0,
      "lngOrderID": 123456,
      "lngPackingListID": 0,
      "lngSalesPriceUnit": 0,
      "lngSupplierID": 333333,
      "oArticle": {},
      "oDiscount1": {
        "decDiscountAmount": 0,
        "decDiscountPercent": 0,
        "decDiscountValue": 0,
        "lngDiscountID": 0,
        "sDiscountText": "",
        "sDiscountType": ""
      },
      "oDiscount2": {
        "decDiscountAmount": 0,
        "decDiscountPercent": 0,
        "decDiscountValue": 0,
        "lngDiscountID": 0,
        "sDiscountText": "",
        "sDiscountType": ""
      },
      "oDiscount3": {
        "decDiscountAmount": 0,
        "decDiscountPercent": 0,
        "decDiscountValue": 0,
        "lngDiscountID": 0,
        "sDiscountText": "",
        "sDiscountType": ""
      },
      "oDiscount4": {
        "decDiscountAmount": 0,
        "decDiscountPercent": 0,
        "decDiscountValue": 0,
        "lngDiscountID": 0,
        "sDiscountText": "",
        "sDiscountType": ""
      },
      "oDiscount5": {
        "decDiscountAmount": 0,
        "decDiscountPercent": 0,
        "decDiscountValue": 0,
        "lngDiscountID": 0,
        "sDiscountText": "",
        "sDiscountType": ""
      },
      "oDiscount6": {
        "decDiscountAmount": 0,
        "decDiscountPercent": 0,
        "decDiscountValue": 0,
        "lngDiscountID": 0,
        "sDiscountText": "",
        "sDiscountType": ""
      },
      "sArticleID": "TESTARTICLE",
      "sArticleIDOfDataSupplier": null,
      "sArticleName": "testName",
      "sCustomerArticleID": "",
      "sItemText": "",
      "sItemType": "P",
      "sItemsListID": "",
      "sOfferStatus": null,
      "sOrderStatus": "offen",
      "sOrderText": null,
      "sOrderType": "A100",
      "sPurchOrderNumber": null,
      "sQuantityUnit": "kg",
      "sTaxCode": "MATRCS",
      "sUniformNumber": "222222",
      "shtBranchID": 0,
      "shtFixedItemID": 1,
      "shtHasAdditionalItems": 0,
      "shtIsAdditionalToItem": 0,
      "shtItemID": 1,
      "shtItemsList": 0,
      "shtOfferStatus": 0,
      "shtPlanningCode": 0,
      "shtProcessedItem": 0,
      "shtRestOfItem": 0,
      "shtStatus": 1,
      "shtSteelprocessing": 0,
      "shtStorageID": 1000
    }
  ],
  "oSalesMaster": {}
}
```

## Update cart-item

This endpoint allows you to update an item (quantity, item-text and article-name only)

**URL** : `/so-carts/:id/items/:fixedItemId` (`/so-carts/123456/items/1` in example)

**Method** : <img src="https://img.shields.io/badge/PUT%20-%23323330.svg?&style=flat&color=yellow"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```json
{
  "decQuantityOrdered": 888,
  "sItemText": "testItemText",
  "sArticleName": "testArticleName"
}
```

### Success Response

**Condition** : If the cart-item is updated successfully.

**Code** : `200 OK`

**Content example**

```json
{
  "oSalesItemList": [
    {
      "bAlternativeItem": false,
      "bBlockDelivery": false,
      "bPartialDelivery": false,
      "decFactorSalesPrice": 1.000000000000000,
      "decItemGrossAmountFC": 0.00,
      "decItemNetAmountFC": 0.00,
      "decItemTaxAmountFC": 0,
      "decPrice": 0.00,
      "decPriceFactor": 1.00000000000000,
      "decPricePG": 0,
      "decQuantity": 0,
      "decQuantityDelivered": 888,
      "decQuantityDelivered2": 0,
      "decQuantityOrdered": 888,
      "decSalesPrice": 0,
      "decTaxRate": 0.00,
      "dtDeliveryDate": 1640736000000,
      "dtDeliveryNoteIDDate": 0,
      "dtInvoiceDate": 0,
      "dtRequestedDate": 1640736000000,
      "lngCampaignID": 0,
      "lngCustomerOrderID": 0,
      "lngDeliveryNoteID": 0,
      "lngGoodsReceiptID": 0,
      "lngInvoiceID": 0,
      "lngOrderID": 123456,
      "lngPackingListID": 0,
      "lngSalesPriceUnit": 0,
      "lngSupplierID": 666666,
      "oArticle": {},
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
      "sArticleID": "TESTARTICLE",
      "sArticleIDOfDataSupplier": null,
      "sArticleName": "testArticleName",
      "sCustomerArticleID": "",
      "sItemText": "testItemText",
      "sItemType": "P",
      "sItemsListID": "",
      "sOfferStatus": null,
      "sOrderStatus": "offen",
      "sOrderText": null,
      "sOrderType": "A100",
      "sPurchOrderNumber": null,
      "sQuantityUnit": "kg",
      "sTaxCode": "MATRCS",
      "sUniformNumber": "222222",
      "shtBranchID": 0,
      "shtFixedItemID": 1,
      "shtHasAdditionalItems": 0,
      "shtIsAdditionalToItem": 0,
      "shtItemID": 1,
      "shtItemsList": 0,
      "shtOfferStatus": 0,
      "shtPlanningCode": 0,
      "shtProcessedItem": 0,
      "shtRestOfItem": 0,
      "shtStatus": 1,
      "shtSteelprocessing": 0,
      "shtStorageID": 1000
    }
  ],
  "oSalesMaster": {}
}
```

## Delete cart-item

This endpoint allows you to delete a cart-item

**URL** : `/so-carts/:id/items/:fixedItemId`

**Method** : <img src="https://img.shields.io/badge/DELETE%20-%23323330.svg?&style=flat&color=red"/>

**Auth required** : Yes

**Permissions required** : No

**Body**

```
None
```

### Success Response

**Condition** : If the cart-item is deleted successfully.

**Code** : `200 OK`

**Content example**

```
None
```