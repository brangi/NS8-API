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
POST /signup
```

```json
{
  "email": "test@test.com",
  "password": "test",
  "phone": "444-333-1111"
}
```

- Return all events for all users:

```bash
POST /events/all
```

```json
{
  "email": "test@test.com",
  "password": "test",
  "phone": "444-333-1111"
}
```


- return all events for a single user
- return all events for the last day
