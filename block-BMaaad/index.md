writeCode

Write command to

- List collections from a database.
  -- show collections

- create a new collection in your country database which you created recently.
  -- use India
  -- db.createCollection("states")

Write code to:-

- crate a database named `weather`
  -- use weather

- create a capped collection named `temperature` with maximum of 3 documents and try inserting more than 3 to see the result.
  -- db.createCollection("temperature", { capped: true, max:3, size: 10000})
  -- db.temperature.insertOne({type : 'Celcius', degree : 37.5})
  -- db.temperature.insertOne({type : 'Celcius', degree : 42.5})
  -- db.temperature.insertOne({type : 'Fahrenheit', degree : 98.6})
  -- db.temperature.insertOne({type : 'Fahrenheit', degree : 104})
  -- db.temperature.find()
  --- [
  {
  _id: ObjectId("6449a38dbb3b78ea0cdd36a2"),
  type: 'Celcius',
  degree: 42.5
  },
  {
  _id: ObjectId("6449a39bbb3b78ea0cdd36a3"),
  type: 'Fahrenheit',
  degree: 98.6
  },
  {
  _id: ObjectId("6449a3a3bb3b78ea0cdd36a4"),
  type: 'Fahrenheit',
  degree: 104
  }
  ]

// The oldest entry gets deleted when I insert a 4th document into this collection

- create a simple collection named `humidity`
  -- db.createCollection("humidity")

- check whether `temperature` collection is capped or not ?
  -- db.temperature.isCapped()
  --- true

- Delete `humidity` collection and then the entire database(weather).
  -- db.humidity.drop()
  -- db.dropDatabase()
