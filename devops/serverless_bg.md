# Serverless Background jobs

## Why

Using AWS Lambda, we can create a function that handles one (or more) background jobs such as syncing data from 3rd party apps, sending emails, calculating scores and more.

Pros:

- Can be scheduled like cron jobs
- Can be triggered by AWS events such as: S3 file uploads, Simple Notification Service (SNS) events and other triggers
- Supports versioning and rollbacks
- Cost is low

Cons:

- 15 minutes limit

## How

We use [The Serverless Framework](https://github.com/serverless/serverless)

> Build applications comprised of microservices that run in response to events, auto-scale for you, and only charge you when they run. This lowers the total cost of maintaining your apps, enabling you to build more logic, faster.

The `serverless.yml` file includes all the infrastructure definitions for each function.

Everything happens on our AWS account and our [CI tool](cicd.md) uses it to deploy the API server on each successful commit to `master`.
