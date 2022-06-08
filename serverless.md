# Serverless

DOC: [Here](https://www.serverless.com/)

- helps to develop and deploy AWS Lambda functions, along with the AWS infrastructure resources they require
- allows to build event-driven, serverless architectures, comprised of `Functions` and `Events`
- manages both `code` and `infrastructure`


## Services

- Equivalent to 1 project.
- Configured via `serverless.yml` --> (Configuration File)
- define functions, events and AWS Resources in here

### serverless.yml

- One service configuration is managed in one `serverless.yml` file
- Declares/Defines the following
  - Declare a `serverless service`
  - define cloud provider
  - define functions
  - define events that trigger each function
  - allow events listed in `events` section to automatically create resources required for event upon deployment
  - define AWS Resources
  - define plugins
  - use `variables`

#### Variables

- allows to dynamically replace config values in `serverless.yml` file
- > Can not use variables in `keys`
- Use as follows

```yaml
key: ${variableSource} # resolves value of the variable
key: ${variableSource, defaultValue} # resolved value of the variable, with a fallback

key: ${self:variable_name} # property inside same `serverless.yml` file
key: ${sls:variable_name} # core variables provided by serverless framework (ex instanceID = random id)
key: ${env:variable_name} # environment variables
key: ${param:variable_name} # parameter defined under `params` key
key: ${opt:variable_name} # CLI arguments
key: ${aws:variable_name} # AWS arguments
key: ${file(/path/to/file):variable_name} # arguments defined in other YAML/JSON files
```

### Deployment

- On `serverless deploy` command, functions + events + resources are translated to `AWS CloudFormation Template` and deployed as a stack
- Can deploy entire configuration or a single function (faster)

## Functions

- Independent unit of execution and deployment
- Performs a single job
- If `Provider==AWS`, all functions defined inside the service are `AWS Lambda` Functions
- `handler` property of a `function` key, points to a file/module containing the code we want to run for this function
- functions inherit settings from `provider` property
- can specify environment variables under `environment` property
- `versionFunctions` : If false, will not create function version for each deploy



## Events

- Functions are **triggered** by events
- Events can come from any AWS Resources
  - HTTP Request
  - CloudWatch Schedule
  - SNS Topic
  - S3 Bucket Upload
- This is an array, as it's possible for functions to be triggered by multiple events

## Resources

- AWS infrastructure components which the `functions` use
  - DynamoDB Table
  - S3 Bucket
  - SNS Topic
