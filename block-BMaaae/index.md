writeCode

Write code to:-

- create a database named `sports`.
  -- use sports

- list all databases present in local mongod server.
  -- use mongod
  -- show dbs
  --- admin 40.00 KiB
  config 108.00 KiB
  local 72.00 KiB

- create 3 collections named `cricket`, `football`, `TT` in sports databse.
  -- db.createCollection("cricket")
  -- db.createCollection("football")
  -- db.createCollection("TT")

- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.
  -- db.cricket.insertMany([ {name: "Barry", age: 32, "bid_price" : 14500}, {name: "Pete", age: 29, "bid_price" : 16900},{name: "Stephan", age: 35, "bid_price" : 21343}])
  -- db.football.insertMany([ {name: "Ted", age: 35, "bid_price" : 12980}, {name: "John", age: 25, "bid_price" : 15720},{name: "Garrison", age: 31, "bid_price" : 23563}])
  -- db.TT.insertMany([ {name: "Stella", age: 32, "bid_price" : 12980}, {name: "Marie", age: 27, "bid_price" : 15720},{name: "Hella", age: 25, "bid_price" : 21553}])

- list all collections in sports database.
  -- show collections
  --- cricket
  football
  TT

- rename `TT` collection to `tennis`.
  -- db.TT.renameCollection("tennis")

- create a capped collection called `khokho` which should have max 3 documents.
  -- db.createCollection("khokho", {capped: true, size: 10000, max: 3})

Try inserting more than 3 and see what happens?
Ans : If I add more than 3 documents the oldest entry gets overwritten by the new one.

- check whether a collection is capped or not?
  -- db.sports.isCapped()
  -- db.khokho.isCapped()

- drop all documents from `football` collection.
  -- db.football.remove({})

- delete cricket collection completely.
  -- db.cricket.drop()

- delete sports database.
  -- db.dropDatabase()

- check which database you are connected to ?
  -- db

- connect to test database
  -- use test
