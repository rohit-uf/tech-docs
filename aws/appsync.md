# AppSync

- Managed serverless GraphQL Service
- Connect to data sources in your account
- Data Sync, Real Time and Offline Capabilities
- Can be used as `facade` for any AWS Service

> Application and Data Service, with Real-Time + Offline capabilities + Built-In Authorization + Conflict Resolution

### Data

- AppSync API can access Data directly via DynamoDB tables, elasticsearch clusters, lambda functions etc
- `Resolver(s)`
  - It is a collection of functions that generate response for a GraphQL query
  - Acts as a bridge between data defined in schema and data available in actual sources
  - Map any fields with a data sources 

### VTL : Velocity Template Language

- `Request Mapping`: Used to resolve GraphQL queries into requests to actual data sources
- `Response Mapping`: Used to resolve data from data sources into GraphQL response
    
## `context` Object reference

### `arguments`

- map that contains all graphql **arguments** passed in the request

### `identity`

= object that contains information about the caller

### `source`

- Map that contains resolution of parent field

### `stash`

- Map that is available inside each resolver and function mapping template
- Single instance of stash lives throught a single resolver execution
- Can be used to pass arbitrary data across request and response mapping templates

### `result`

- container for the results of this resolver
- available only to `response` mapping templates

### `prev.result`

- result of wahtever previous operation executed in a pipeline resolver

### `info`

- contains information about the graphql request
  - fieldName: name of field that is currently being resolved
  - parentTypeName: name of the parent type for the field that is currently being resolved
  - variables: All variables passed into graphql request 
