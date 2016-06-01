# restson
Simple JSON REST server

## Install

```
npm i -d
```

### Files

```
mkdir -p ./db/ && touch ./db/demo.json
```

*./db/demo.json*

```json
{
  "pais": [
    {
      "nombre": "Argentina",
      "id": 1
    },
    {
      "nombre": "Bolivix",
      "id": 2
    },
    {
      "nombre": "Colombia",
      "id": 3
    },
    {
      "nombre": "Ecuador",
      "id": 4
    },
    {
      "nombre": "Perú",
      "id": 5
    }
  ]
}
```


### Running The "Server"

```
npm run server
```

### GET

```
curl http://localhost:3000/pais
```
*Response: (200)*
```json
[
  {
    "nombre": "Argentina",
    "id": 1
  },
  {
    "nombre": "Bolivix",
    "id": 2
  },
  {
    "nombre": "Colombia",
    "id": 3
  },
  {
    "nombre": "Ecuador",
    "id": 4
  },
  {
    "nombre": "Perú",
    "id": 5
  }
]
```

```
curl http://localhost:3000/pais/2
```
*Response: (200)*
```json
{
  "nombre": "Bolivix",
  "id": 2
}
```

----------

### PUT

```
curl -H 'Content-Type: application/json' -X PUT -d '{"nombre": "Bolivia"}' http://localhost:3000/pais/2
```
*Response: (200)*
```json
{
  "nombre": "Bolivia",
  "id": 2
}
```

----------

### POST

```
curl -H 'Content-Type: application/json' -X POST -d '{"nombre": "Paraguay"}' http://localhost:3000/pais
```
*Response: (201)*
```json
{
  "nombre": "Paraguay",
  "id": 6
}
```

----------

### DELETE

```
curl -X DELETE http://localhost:3000/pais/6
```

*Response: (200)*
```json
{}
```
