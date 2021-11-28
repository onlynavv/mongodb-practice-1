# mongodb-practice-1

1)
```
db.products.find({})
```

2)
```
db.products.find({product_price: {$gte:400, $lt:800}})
```

3)
```
db.products.find({$not: { product_price: {$gte: 400, $lt:800} }}).pretty()
```

4)
```
db.products.find({products_price:{$gt:500}}).limit(4).pretty()
```

5)
```
db.products.find({},{product_name:1, product_material:1})
```

6)
```
db.products.find({id: "10"})
```

7)

```
db.products.find({},{product_name:1, product_material:1})
```

8)
```
db.products.find({product_material:"Soft"})
```
```
db.products.aggregate([{$match:{product_material:"Soft"}},{$group:{_id:"$product_name"}}])
```

9)
```
db.products.find({product_color:"indigo", product_price:492.00})
```

10)
```
db.products.deleteMany({product_price:36})
```
