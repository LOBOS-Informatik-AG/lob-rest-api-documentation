# Price

## Get price by article id

This endpoint allows you to get a price for the given article id

**URL** : `/price`

**Method** : <img src="https://img.shields.io/badge/GET%20-%23323330.svg?&style=flat&color=green"/>

**Auth required** : No

**Permissions required** : No

**Query parameters**

``` json
{
    "articleId": "0101008H",
    "unit": "Stk",
    "currency": "CHF"
}
```

### Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "Query": null,
    "Status": null,
    "decBasePriceGross": 892.83,
    "decBasePriceNet": 829.00,
    "decBasePriceTax": 63.83,
    "decPriceGross": 829.00,
    "decPriceNet": 829.00,
    "decPriceTax": 0.00,
    "decResalePriceGross": 0,
    "decResalePriceNet": 0,
    "decResalePriceTax": 0,
    "decSpecialPriceGross": 0,
    "decSpecialPriceNet": 0,
    "decSpecialPriceTax": 0,
    "decTaxRate": 7.70,
    "lngCustomerID": 10124,
    "lngSalesPriceUnit": 1,
    "oPriceScaleInfoList": [],
    "sArticleID": "0101008H",
    "sCurrencyCode": "CHF",
    "sQuantityUnit": "Stk",
    "sTaxCode": "M7.7",
    "shtPriceGroup": 1
}
```

**or**

**Condition** : if the article is not found.

**Content example**

```json
{
    "text": "Artikelnr erforderlich '0101008Htest'"
}
```