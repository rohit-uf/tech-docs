# Cloud Formation

- [tutorial](https://www.youtube.com/watch?v=YXVCdGyHDSk)

- Infrastructure as code
- Can define an entire application built on AWS via a Template File
- Cloud formation will build the application step-by-step from the provided template

## Templates

- defined in `yaml` or `json`
- contain `resources` which are AWS services linked together to form one application

## Stacks

- Logical grouping of templates + resources
- Can combine multiple independent stacks together, and deploy all at once
- Can also create nested stacks

## Changesets

- DIFF of what cloud formation has from our previous upload and what we are attempting to upload
- It only performs updates on things that have changed
- is applied on a `stack`, to update the stack with latest changes
- We need to create a `changeset` with the updated template file and **execute** it manuallyf

## Drift

- Once `cloudformation` deploys from a template, it keeps track of the state of all AWS Resources involved (via snapshots)
- Snapshots are updated for each deploy
- If after a deployment, we manually change something in one of those resource(s), it creates an out-of-sync issue called `drift`. Where the cloudfront snapshot does not match with the actual state of those resources


## Alternatives

> AWS SAM
> Serverless
> AWS Cloud Development Kit
> Terraform : Platform agnostic
