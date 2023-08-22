## connect to conatiner

``` sh
docker-compose exec mongodb bash
```
## connect with mongosh

``` sh
mongosh "mongodb://myrootuser:myrootpassword@localhost:27017/?authMechanism=DEFAULT&tls=false"
```

``` sh
show dbs
show collections

```

``` sh
use("STORE")

```

``` sh
use("STORE")
db.productos.find()

```
## Drop 

``` sh
db.coleccion.drop()

```

## insertar varios documentos

``` sh
db.coleccion.insertMany([
    {
        name: "cosa1",
        price: 152
    },
    {
        name: "cosa2",
        price: 154
    }
])

```

``` sh
db.coleccion.insertMany([
    {
        name: "cosa1",
        price: 152
    },
    {
        name: "cosa2",
        price: 154
    }
], {
    ordered: false
})

```

## actualizar documentos

``` sh
use("STORE")
db.productos.updateOne(
    {_id:2},
{
    $set:{
        name : 'cambio'
    }
}
)
```

### incrementar 

``` sh
use("STORE")
db.productos.updateOne(
    {_id:2},
{
    $set:{
        prise : 100
    }
}
)
```

### con id de mongo

``` sh
use("STORE")
db.productos.updateOne(
    {_id:ObjectId("665df76341635fdsf")},
{
    $set:{
        prise : 100
    }
}
)
```

