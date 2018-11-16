# NS8-API

## Description
API to serve data over RESTful calls for a user tracking software. The server uses lokijs, a in-memory JavaScript Datastore with Persistence.

## Install and run the server

### Development

```bash
npm install
npm run dev
```

## API calls

Firstly, To create users :

```bash
POST localhost:4999/signup
```

```json
{
  "email": "test@test.com",
  "password": "test",
  "phone": "444-333-1111"
}
```

Login (generate events):

```bash
POST localhost:4999/login
```

```json
{
  "email": "test@test.com",
  "password": "test",
}
```
Response:
```json
{
  "message": "Created user with email test@test.com"
}

```

- Return all events for all users:

```bash
GET /events/all
```

```json
[
  {
    "type": "LOGIN",
    "created": 1542332153301
  },
  {
    "type": "LOGIN",
    "created": 1542332534616
  },
  {
    "type": "LOGIN",
    "created": 1542332535460
  },
  {
    "type": "LOGIN",
    "created": 1542332537243
  },
.....
]
```

- Return all events for a single user

```bash
GET localhost:4999/events/user?email=test@test.com
```

- Return all events for the last day

```bash
GET localhost:4999/events/lastday
```
