# Serverless API Server

## Why

Using AWS Gateway + AWS Lambda allows to easily deploy and scale APIs. There are no servers to SSH into, install security updates or scale.

Pros:

- SSL termination is taken care by the AWS Gateway
- Supports multiple environments
- Supports versioning and rollbacks
- Cost is low

Cons:

- Cold starts can make the API slow (during scaling)
- Version of Node.js is controlled by AWS (not the latest one currently)

## How

We use [apex/up](https://github.com/apex/up)

> Deploy infinitely scalable serverless apps, apis, and sites in seconds to AWS.

See [documentation](https://up.docs.apex.sh)

`up` is a command line utility that uploads a full API server as a single Lambda function and creates an API Gateway that routes requests to it.

Everything happens on our AWS account and our [CI tool](cicd.md) uses it to deploy the API server on each successful commit to `master`.