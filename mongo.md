# Mongo DB

## Criar Collection

```mongodb
db.createCollection("collection")
```

## Adicionar Valor

```mongodb
db.collection.insert({
    "campo": "valor",
    "campo2": new Date(30,11,1998)
})
```

*OBS*: existem alguns tipos que podem ser passados como valor.

## Buscar Valor

```mongodb
db.collection.find({
    "campo": "valor"
})
```

### Join

```mongodb
db.collection.find({
    "campo.subcampo": "valor"
})
```

### And , $or, $in

```mongodb
db.collection.find(
    {"campo": "valor"},
    {"campo": "valor"}
)
```

```mongodb
db.collection.find([
    $or: [
        {"campo": "valor"},
        {"campo": "valor"}
    ]
])
```

```mongodb
db.collection.find([
    "campo": {
        $in: ["valor1", "valor2"]
    }
])
```

