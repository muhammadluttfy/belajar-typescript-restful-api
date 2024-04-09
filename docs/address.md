# Address API Spec

## Create Address
Endpoint : `POST /api/contact/:idContact/addresses`

Request Header :
- `X-API-TOKEN`: token

Request Body :
```json
{
  "street" : "jln. example",
  "city" : "City example",
  "province" : "Province example",
  "country" : "Country example",
  "postal_code" : "22256",
}
```

Response Body (Success) :
```json
{
  "data" : {
    "id" : 1
    "street" : "jln. example",
    "city" : "City example",
    "province" : "Province example",
    "country" : "Country example",
    "postal_code" : "22256",
  }
}
```

Response Body (Failed) :
```json
{
  "errors" : "street must not blank, ..."
}
```

## Get Address
Endpoint : `GET /api/contact/:idContact/addresses/:idAddress`

Request Header :
- `X-API-TOKEN`: token

Response Body (Success) :
```json
{
  "data" : {
    "id" : 1
    "street" : "jln. example",
    "city" : "City example",
    "province" : "Province example",
    "country" : "Country example",
    "postal_code" : "22256",
  }
}
```

Response Body (Failed) :
```json
{
  "errors" : "street must not blank, ..."
}
```

## Update Address
Endpoint : `PUT /api/contact/:idContact/addresses/:idAddress`

Request Header :
- `X-API-TOKEN`: token

Request Body :
```json
{
  "street" : "jln. example",
  "city" : "City example",
  "province" : "Province example",
  "country" : "Country example",
  "postal_code" : "22256",
}
```

Response Body (Success) :
```json
{
  "data" : {
    "id" : 1
    "street" : "jln. example",
    "city" : "City example",
    "province" : "Province example",
    "country" : "Country example",
    "postal_code" : "22256",
  }
}
```

Response Body (Failed) :
```json
{
  "errors" : "street must not blank, ..."
}
```

## Remove Address
Endpoint : `DELETE /api/contact/:idContact/addresses/:idAddress`

Request Header :
- `X-API-TOKEN`: token

Response Body (Success) :
```json
{
  "data" : "OK"
}
```

Response Body (Failed) :
```json
{
  "errors" : "address is not found, ..."
}
```

## List Address
Endpoint : `GET /api/contact/:idContact/addresses`

Request Header :
- `X-API-TOKEN`: token

Response Body (Success) :
```json
{
  "data" : [
    {
      "id" : 1
      "street" : "jln. example",
      "city" : "City example",
      "province" : "Province example",
      "country" : "Country example",
      "postal_code" : "22256",
    },
    {
      "id" : 2
      "street" : "jln. example",
      "city" : "City example",
      "province" : "Province example",
      "country" : "Country example",
      "postal_code" : "22256",
    }
  ]
}
```

Response Body (Failed) :
```json
{
  "errors" : "contact is not found, ..."
}
```