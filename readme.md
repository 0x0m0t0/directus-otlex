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

## API ROUTER

GET ALL BOOKS

```
/items/books
```

GET BOOKS and related fields (each \* goes one relation deeper)

```
/items/books?fields=*.*.*.*
```

## Context

This project was created to testrun a headless CMS together with a NEXT.js frontend.
