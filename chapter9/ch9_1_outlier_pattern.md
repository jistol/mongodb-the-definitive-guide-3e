## Outlier Pattern
```json
// normal case
{
    "_id": ObjectID("507f1f77bcf86cd799439011")
    "title": "A Genealogical Record of a Line of Alger",
    "author": "Ken W. Alger",
    ...,
    "customers_purchased": ["user00", "user01", "user02"]

}
```

```json
// case of 'customers_purchased' field count exceeds 1000
// "has_extras" field set to true
{
    "_id": ObjectID("507f191e810c19729de860ea"),
    "title": "Harry Potter, the Next Chapter",
    "author": "J.K. Rowling",
    ...,
   "customers_purchased": ["user00", "user01", "user02", ..., "user999"],
   "has_extras": "true"
}
```

Reference : [Building with Patterns: The Outlier Pattern](https://www.mongodb.com/developer/how-to/outlier-pattern/) 
