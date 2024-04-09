# User API Spec

## Register User

Endpoint: `POST /api/users`

Request Body :

```json
{
  "username": "muhammadlutfi",
  "name": "Muhammad Lutfi",
  "password": "password"
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "muhammadlutfi",
    "name": "Muhammad Lutfi"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "username must not blank, ..."
}
```

## Login User

Endpoint: `POST /api/users/login`

Request Body :

```json
{
  "username": "muhammadlutfi",
  "password": "password"
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "muhammadlutfi",
    "name": "Muhammad Lutfi",
    "token" : "uuid"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "username or password wrong, ..."
}
```

## Get User

Endpoint: `GET /api/users/current`

Request Header :
- `X-API-TOKEN`: token

Response Body (Success) :

```json
{
  "data": {
    "username": "muhammadlutfi",
    "name": "Muhammad Lutfi"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized, ..."
}
```

## Update User

Endpoint: `PATCH /api/users/current`

Request Header :
- `X-API-TOKEN`: token

Request Body :

```json
{
  "username": "muhammadlutfi", // tidak wajib
  "name": "Muhammad Lutfi", // tidak wajib
  "password": "password" // tidak wajib
}
```

Response Body :

```json
{
  "data": {
    "username": "muhammadlutfi",
    "name": "Muhammad Lutfi"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized, ..."
}
```

## Logout User

Endpoint: `DELETE /api/users/current`

Request Header :
- `X-API-TOKEN`: token

Response Body :

```json
{
  "data": "OK"
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized, ..."
}
```