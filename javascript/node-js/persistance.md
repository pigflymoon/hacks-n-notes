# Persistence

## Filesystem Persistence

- never trust an uploaded file
- verify that the filename is alphanumeric
- the file could be a malicious executable
- save the file in a cloud storage eg. **S3**

## Cloud Persistence

- AWS S3

```js
aws.putObject({
  ACL: 'private',
  Bucket: 'uploads',
  Key: filename,
  Body: fs.readFileSync(__dirname + '/tmp/' + filename)
})
```

## Database Persistence

### Types of NoSQL DB

- document DB
- key-value DB
- NoSQL databases support concurrency to scale performance

#### Document DB

- document DB excel at storing objects 
- great fit for Node and JS
- MongoDB is the leading document DB

##### MongoDB DBaaS

- [mlab](www.mlab.com)
- [MongoHQ](https://www.compose.com/mongodb)
- AWS DynamoDB

##### MongoDB npm packages

- mongodb - low-level driver for MongoDB
- mongoose - Object Document Mapper (ODM)
- session-mongoose - to manage session storage

#### Key-value DB

- are good for data schemas that are easily mapped into key-value pairs

##### Redis npm packages
- connect-redis