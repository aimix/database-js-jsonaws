# database-js-jsonaws
Database-js driver for JSON files stored on AWS.
## Usage

```js
let connection, statement;
let file_name = "data.json";
connection = new Connection('jsonaws://'+ACCESSKEYID+':'+SECRETACCESSKEY+'@'+BUCKET_NAME+'/'+file_name);
statement = connection.prepareStatement('INSERT VALUES { "yolo" : "swag" }');
statement.execute().then((results) => {
    connection.close();
}).catch((reason) => {
    connection.close();
});

```
