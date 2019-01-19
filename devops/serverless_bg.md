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

We use [apex/apex](https://github.com/apex/apex)

> Build, deploy, and manage AWS Lambda functions with ease

See [documentation](http://apex.run)

`apex` is a command line utility that uploads functions and manages their life-cycle of configuration, updates and logging.

Everything happens on our AWS account.
