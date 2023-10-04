<h1 align="center">Otlex backend: Directus Headless CMS</h1>

<p align="center">
  Headless CMS for <a href="https://github.com/0x0m0t0/otlex-next">Otlex</a>, a personal library management tool.

</p>

<br>

<br>

## Installation

npm:

```
npm i
```

```
npm run start
```

## API ROUTES

### POST Users
```
/users
```


```json
{
  "first_name": "OOOOO",
  "last_name": "User",
  "email": "admin@example.com",
  "password": "**********",
  "location": "New York City",
  "title": "CTO",
  "description": null,
  "tags": null,
  "avatar": null,
  "language": "en-US",
  "theme": "auto",
  "tfa_secret": null,
  "status": "active",
  "role":"b63fab4b-9966-47ba-b35a-eed418bb2d56",
  "token": null,
  "last_access": "2021-02-05T10:18:13-05:00",
  "last_page": "/settings/roles/653925a9-970e-487a-bfc0-ab6c96affcdc"
}
```


### GET Users
```
/users
```




### GET ALL BOOKS

```
/items/books
```

### GET BOOKS and related fields (each \* goes one relation deeper)

```
/items/books?fields=*.*.*.*
```


### GET Specific books + categories

```
/items/books?fields=Name,Year,Authors.authors_id.name,categories.categories_id.name&filter[_and][0][categories][categories_id][name][_eq]=Sci-Fi&filter[_and][1][categories][categories_id][name][_eq]=fiction
```

### POST BOOKS

- Authorization

```
/items/books
```

```json
{
  "Name": "Book of Books",
  "status": "published",
  "Authors": [
    {
      "authors_id": {
        "name": "Michael The Writer",
        "description": "A writer amongst writers"
      }
    }
  ],
  "Users": [
    {
      "users_id": {
        "id": 1
      }
    }
  ]
}
```

## Context

This project was created to testrun a headless CMS together with a NEXT.js frontend.
