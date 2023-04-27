writeCode

Write code to:-

- create a database named `mountains`
  -- use mountains

- a collection inside that database named `himalayas`
  -- db.createCollection("himalayas")

- insert 1 document into that collection `{name: 'Dhauldhar range', height: '4000 mtrs'}`
  -- db.himalayas.insertOne({name: 'Dhauldhar range', height: '4000 mtrs'})

- insert multiple document using insertMany command
  -- db.himalayas.insertMany([
  {
  name : 'Mount Everest',
  height : '8,848 mtrs'
  },
  {
  name : 'Kangchenjunga',
  height : '8,586 mtrs'
  },
  {
  name : 'Nanda Devi',
  height : '7,816 mtrs'
  },
  ])

- find all documents from mountains
  -- db.himalayas.find().pretty()

- find a single document using name
  -- db.himalayas.findOne({name: 'Nanda Devi'})
