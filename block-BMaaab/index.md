writeCode

Run these shell commands in mongo shell:

- db.version()
  -- 6.0.5
- db.stats()

-- {
db: 'test',
collections: 0,
views: 0,
objects: 0,
avgObjSize: 0,
dataSize: 0,
storageSize: 0,
indexes: 0,
indexSize: 0,
totalSize: 0,
scaleFactor: 1,
fsUsedSize: 0,
fsTotalSize: 0,
ok: 1
}

- db.help()

Write code to

- create a database of your country name.
  -- use India
  --- switched to db India

- check list of databases to see newly created database.
  -- show dbs
  --- admin 40.00 KiB
  config 60.00 KiB
  local 72.00 KiB

// This doesn't show my currently created db because it needs to have atleast one document.

- check which database you are currently connected to ?
  -- db.getName()
  --- test
