writeCode

#### Import data from json file to mongodb database using `mongoimport`

```
mongoimport --host <host_name> --username <user_name> --password <password> --db
DB_NAME --collection COLLECTION_NAME --file cities.json(file location) --jsonArray
(an array of json data)
```

host, username and password are optional fields.

- --host : hostname // defaults to localhost:27017
- --username and --password: optional username and password for db user
- --db: database name
- --collection: Collection name
- --file: file location
- --jsonArray: Passed an array of json objects

## BLOCK-writeCode

Go to `https://www.json-generator.com/`

- generate 40 random json document using the format

```js
// paste this on left panel
[
  "{{repeat(30)}}",
  {
    _id: "{{objectId()}}",
    age: "{{integer(20, 40)}}",
    name: "{{firstName()}} {{surname()}}",
    gender: "{{gender()}}",
    company: "{{company().toUpperCase()}}",
    email: "{{email()}}",
    phone: "+1 {{phone()}}",
    tags: ["{{repeat(2)}}", '{{lorem(1, "words")}}'],
  },
];
```

- download it on `Desktop`
- import it into mongodb `test` database into a collection named `users`

-- mongoimport "E:\JSON\users.json" -d test -c users --jsonArray --drop

#### Export data from mongodb server to local system in json format using

`mongoexport`command.

```
mongoexport --db state --collection cities --out ~/Desktop/states/city.json --jsonArray
```

-- mongoexport -d society -c users --out C:\Users\DELL\Desktop\society\users.json --jsonArray
--- 2023-04-28T15:37:35.635+0530 connected to: mongodb://localhost/
--- 2023-04-28T15:37:35.658+0530 exported 30 records

## BLOCK-writeCode

Export `users` collection from `test` database onto `Desktop` in a file named `exported.json`.

-- mongoexport -d test -c users --out C:\Users\DELL\Desktop\exported.json --jsonArray

#### Import from csv file

```
mongoimport -d DB_NAME -c COLLECTION_NAME --type csv --file elections.csv(file location) --headerline(including header)
```

## BLOCK-writeCode

Generate mock csv data from `https://www.convertcsv.com/generate-test-data.htm`

- insert this mock csv data into `test` database into a collection named `students`

-- mongoimport -d test -c students --type csv --file "C:\Users\DELL\Desktop\data.json" --headerline
