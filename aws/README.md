# Amazon Web Services

## AppSync

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
