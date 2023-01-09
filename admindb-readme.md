
# AdminDB

An easy way to communicate with backend database through admin panel


## API Reference

#### Get all items

```http
  query_opperation: 
```

| Function | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `query` | `object, string, string` | **Required**. Retrieve all matching [objects] from [table] in [database] |
| `queryLimit` | `object, string, string` | **Required**. retrieve [int] items from [table] in [database] |
| `findOne` | `object` | **Required**. Retrieve a single [object] from [table] in [database] |
| `insertMany` | `array of objects` | **Required**. insert multiple items into [table] in [database] |
| `insertOne` | `object` | **Required**. insert one item into [table] in [database] |
| `pagination` | `object, int, int, string, string` | **Required**. retrieve [int] results from [table] in [database] starting at index [int] |
| `deleteOne` | `object, string, string` | **Required**. delete item from [table] in [database] |
| `deleteMany` | `object (regex match), string, string` | **Required**. delete all items from [table] in [database] where [key value] matches [regex string] |
| `updateOne` | `object, string, string` | **Required**. update item from [table] in [database] |
| `updateMany` | `object (regex match), string, string` | **Required**. update all items from [table] in [database] where [key value] matches [regex string] |
| `collectionCount` | `string, string` | **Required**. get number of items in [table] in [database] |
| `countDocuments` | `string, string, object` | **Required**. get number of documents that match [key value] equals [any] from [table] in [database] |

#### Params

```http
  query_params:
```

| Function | Example    | Description
| :-------- | :------- | :------ |
| `query`      | `{ username: 'admin' }` | `get all items where [username] = [admin]` | 
| `queryLimit`      | `[{ username: 'admin' }, 10]` | `get top 10 results where [username] = [admin]` | 
| `findOne`      | `{ username: 'admin' }` | `get first result where [username] = [admin]` | 
| `insertMany`      | `[{ id: 1 }, { id: 2 }]` | `insert two items { id: 1 } and { id: 2 }` | 
| `insertOne`      | `{ id: 1 }` | `insert one item {id: 1}` | 
| `pagination`      | `[{ username: 'admin' }, 10, 10]` | `get top 10 results where [username] = [admin] starting at the tenth index (item) -- items 10-20` | 
| `deleteOne`      | `{ username: 'admin' }` | `delete one record where [username] = [admin]` | 
| `deleteMany`      | `{ username: 'admin' }` | `delete all records where [username] = [admin]` | 
| `updateOne`      | `[{ username: 'admin' }, { $set: { username: 'justpics-admin' }}]` | `get one result where [username] = [admin] and set username to justpics-admin` | 
| `updateMany`      | `[{ username: /^a/ }, { $set: { username: 'justpics-admin'}}]` | `get all results where [username] starts with [a] and update them to [justpics-admin]` | 
| `collectionCount`      | `` | `get top 10 results where [username] = [admin]` | 
| `countDocuments`      | `{ username: 'admin' }` | `count how many records have the [username] = [admin]` | 

#### query_table:
Table to query, for example table "users" in database...

#### query_database:
Database to query for example FileUploadingSiteDB

## Usage/Examples



```json
{ 
    query_opperation: 'findOne', 
    query_table: 'carts', 
    query_db: 'TestNextAuth', 
    query_params: [
        {
          username: 'admin'
        }
    ]
}
```


## API Reference

#### Get all items

```http
  query_opperation: 
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `query` | `object` | **Required**. Retrieve multiple items from database |
| `findOne` | `object` | **Required**. Retrieve a single item from database where value matches key |
| `insertMany` | `array of objects` | **Required**. insert multiple items into table |
| `insertOne` | `object` | **Required**. insert one item into table |
| `query` | `object` | **Required**. Retrieve multiple items from database |


#### Get item

```http
  GET /api/items/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |

#### add(num1, num2)

Takes two numbers and returns the sum.


## Usage/Examples



```json
{ 
    query_opperation: 'findOne', 
    query_table: 'carts', 
    query_db: 'TestNextAuth', 
    query_params: [
        {
          SessionID: "cs_test_b1fuuiAKDqNwBMABWjjwkhDgyhIYzIBKHE4kukEZLPqpWPnYe1lBgy9Lp6"
        }
    ]
}
```

