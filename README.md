# restson
Simple JSON REST server

## Install

```
npm i -d
```

### Running The "Server"

```
npm run server
```

### GET

```
curl http://localhost:3000/pais
```

```
curl http://localhost:3000/pais/2
```

### PUT

```
curl -H 'Content-Type: application/json' -X PUT -d '{"nombre": "Bolivia"}' http://localhost:3000/pais/2
```

### POST

```
curl -H 'Content-Type: application/json' -X POST -d '{"nombre": "Paraguay"}' http://localhost:3000/pais
```

### DELETE

```
curl -X DELETE http://localhost:3000/pais/6
```
