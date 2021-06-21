# Basics

# App-Id

The interface can be configured for different applications. For this purpose, the App-Id must be specified in the header (for all requests)

- `webshopId` (appId)

# Localization

// TODO

# Branches

The interface can be configured for different branches. For this purpose, the "branchkey" must be specified in the header (for all requests)

- `businessUnit` (branchkey)

# Pagination

All the endpoints which expose a list of items include pagination functionality

To work with the pagination on the client side you have to add attributes to the query params

- `intPageIndex` (the current page number)
- `intPageSize` (the page size)
- `intMaxRows` (max rows, default is 1000)

``` json
{
    "perPage": 8,
    "lastPage": "1",
    "currentPage": "1",
    "total": 1,
    "data": [
        ...
    ]
}
```

# Filters

All the attributes defined by an entity can be used as an filter.
The filter can be exact like `/customers?sCustomerGroup=3` or you can enhance the filter using an operator like `/customers?sCustomerGroup[gt]=3`

The following operators can be used:
- [gt] = " > "
- [gte] = " >= "
- [lt] = " < "
- [lte] =" <= "
- [like] = " LIKE "

It is also possible to use the same attribute multiple times

`/customers?sCustomerGroup[gt]=3&sCustomerGroup[lt]=9`

If you need to work with datetimes you have to use UTC as date format
Be aware to not use the LIKE operator with dates!

`/tickets?dtEntryDate[lte]=15996625521448`