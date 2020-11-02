# Customers

## Get customers

This endpoint allows you to get all the customers

**URL** : `/customers`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : Yes

**Permissions required** : Yes `isSalesForce = true`

**Pagination** : Yes

**Query parameters** : Default filters

### Success Response

**Condition** : If customers are found.

**Code** : `200 OK`

**Content example**

```json
{
    "perPage": 5,
    "lastPage": "3",
    "currentPage": "1",
    "total": 15,
    "data": [
        {
            "bNoShippingExpenses": false,
            "bPrivateCustomer": false,
            "decCreditLimit": null,
            "lngAccountID": 10001,
            "lngAssociationID": null,
            "lngCentralPayerID": null,
            "lngCustomerID": 10001,
            "lngILN": null,
            "lngRouteBaseID": null,
            "lngSalesRepID": null,
            "sCity": "Dübendorf",
            "sCode1": "",
            "sCode2": "",
            "sCode3": "",
            "sCompany1": "LOBOS Informatik AG",
            "sCompany2": "",
            "sCompanyID": "",
            "sCountry": "Schweiz",
            "sCountryCode": "CH",
            "sCurrency": "CHF",
            "sCustomerGroup": "3",
            "sEMail": "info@lobos.ch",
            "sExtSupplierID": "",
            "sFax": "+41 44 825 77 77",
            "sIndustrySector": "",
            "sLanguageCode": "de",
            "sMatchCode": "LOBOS",
            "sOrderType": "",
            "sPhone": "+41 44 825 77 77",
            "sPostBox": "",
            "sStreet": "Auenstrasse 4",
            "sTaxNumber": "",
            "sVATRegNo": "",
            "sWebsite": "www.lobos.ch",
            "sZipBox": "8600",
            "sZipCode": "8600",
            "shtDeliveryConditionID": null,
            "shtPaymentConditionID": 1,
            "shtPriceGroup": 2,
            "shtShippingConditionID": null
        },
        ...
    ]
}
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
{
    "bNoShippingExpenses": false,
    "bPrivateCustomer": false,
    "decCreditLimit": 1000.00,
    "lngAccountID": 10896,
    "lngAssociationID": null,
    "lngCentralPayerID": null,
    "lngCustomerID": 10896,
    "lngILN": null,
    "lngRouteBaseID": null,
    "lngSalesRepID": 11,
    "sCity": "Dübendorf",
    "sCode1": "",
    "sCode2": "",
    "sCode3": "",
    "sCompany1": "LOBOS Informatik AG",
    "sCompany2": "",
    "sCompanyID": "",
    "sCountry": "Schweiz",
    "sCountryCode": "CH",
    "sCurrency": "CHF",
    "sCustomerGroup": "1",
    "sEMail": "",
    "sExtSupplierID": "",
    "sFax": "044 825 77 77",
    "sIndustrySector": "",
    "sLanguageCode": "de",
    "sMatchCode": "LOBOS",
    "sOrderType": "",
    "sPhone": "+41 44 825 77 77",
    "sPostBox": "",
    "sStreet": "Auenstrasse 4",
    "sTaxNumber": "",
    "sVATRegNo": "",
    "sWebsite": "www.lobos.ch",
    "sZipBox": "8600",
    "sZipCode": "8600",
    "shtDeliveryConditionID": null,
    "shtPaymentConditionID": 1,
    "shtPriceGroup": 2,
    "shtShippingConditionID": null
}
```

**or**

**Condition** : if no customer is found.

**Content example**

```json
{
    "text": "Kein Kunde gefunden."
}
```