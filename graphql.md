
# Graph QL

- Specification built around HTTP
- Used to define payload in a request/response
- Query Language for APIs + Runtime for fulfilling those queries with existing data

> Solves the problem of `underfetching` and `overfetching`

## Schema

- Need to define a schema, for the `graphql server` to accept and respond to requests with responses 
- `SDL` : Schema Definition Language
- Describes the capabilities of a GraphQL Server and is used to deremine if a query is valid.

## Type System

- Define `types` and specify those types in a structure.

## Operations

- The list of allowed operations are:

### Query
- To lookup something from the database

### Mutation
- Create/Update/Delete object from database

### Subscription

- Subscribe to any changes in an object

### Input
- Defined with the `input` keyword
- Used to define input with multiple fields


## Resolver

- Connector between GraphQL and Data Source
- Translate incoming GraphQL Request into instructions for Backend Data Source + Translate response from data source into a GraphQL Response
- Written in [Apache VTL](./apache_vtl.md)
- Mechanism by which requests are fulfilled


