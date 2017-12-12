# Environment Variables

## The one rule

> Never check-in sensitive data to the GitHub repo (such as passwords, or secret API keys).

If sensitive data was pushed to GitHub, follow the following guide to remove it: [Removing sensitive data from GitHub](https://help.github.com/articles/removing-sensitive-data-from-a-repository/).

## Use `.env` files for local development

`.env` files are ignored with `.gitignore` and are read by the application when developing locally.

For production, we use [AWS Parameter store](http://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-paramstore.html) to encrypt/decrypt all environment variables and secrets. Only assigned AWS resources can decrypt the secrets.
