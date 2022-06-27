 # AWS Dynamo DB

## Features

### Tables
- Like a regular DB Table
- Stores items

### Items

- correspond to tuples/rows
- schemaless, can store a variety of data


### Attributes
- 

### Primary Key

1. Partition Key ( Hash Attribute )
  - Simple primary key
  - composed of one attribute
  - Used as input for the internal `hash` function
  - Output from hash function determines the partition in which the item will be stored

2. Partition + Sort Key (Range Attribute)
  - Composite primary key
  - Partition Key -> Input for internal hash function
  - Sort key -> Used to sort the values inside a partition


### Secondary Index

- Lets us query the data in the table using alternate key
- `Global Secondary Index`: Index with a partition key and sort key that can be different than original table (Max 20)
- `Local Secondary Index`: Index that has same partition key as the table, but different sort key (Max 5)


## DyanmoDB Streams
- Captures data modification events in DynamoDB Tables
- Each event is represented by a Stream Record
- If streams are enabled on a table, DynamoDB Streams write a stream record whenever on of the following events occurs
  - Item is added
  - Item is Updated
  - Item is deleted

