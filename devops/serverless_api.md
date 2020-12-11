# Serverless API Server

## Why

Using AWS Gateway + AWS Lambda allows to easily deploy and scale APIs. There are no servers to SSH into, install security updates or scale.

Pros:

- SSL termination is taken care by the AWS Gateway
- Supports multiple environments
- Supports versioning and rollbacks
- Operation cost is low

Cons:

- Cold starts can make the API slow (during scaling)
- 30 seconds HTTP request limit
- Cost may be larger when scaling up

## How

We use [The Serverless Framework](https://github.com/serverless/serverless)

> Build applications comprised of microservices that run in response to events, auto-scale for you, and only charge you when they run. This lowers the total cost of maintaining your apps, enabling you to build more logic, faster.

The `serverless.yml` file includes all the infrastructure definitions to create a full API server as a single Lambda function and creates an API Gateway that routes requests to it.

Everything happens on our AWS account and our [CI tool](cicd.md) uses it to deploy the API server on each successful commit to `master`.
