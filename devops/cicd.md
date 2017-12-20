# CI/CD

> `Continuous Integration` is the practice of constantly merging development work with the *master* branch so that you can test changes and test that those changes work with other changes.
>
> `Continuous Deployment` is the deployment or release of code to production as soon as it’s ready.

## Why

1. Eliminate manual and repetitive tasks.
2. Make sure our code is always tested and ready to deploy.
3. Focus on building and testing the product.
4. Build a shipping culture.
5. Improve overall productivity.

## How

An external service is preferred over a local installation of `Jenkins` to reduce operational costs around scaling and extending the local installation.

We use [CircleCI](https://circleci.com) to build and test every commit on every branch. Results are reported to GitHub.

CircleCI also deploys `master` to production. This means that `master` is always ready to deploy and it also matches the deployed version of production.