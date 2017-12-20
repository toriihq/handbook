# Feature Flags

> Feature Flags (or Feature Toggles) are a powerful technique, allowing teams to modify system behavior without changing code.

## Why

Using feature flags allows us to test features in production without releasing it to our entire user base.

Once a feature is ready to be fully released, we can turn the Feature Flag on. Feature flags can also target specific users or segments of users.

## How

We currently use hardcoded values in our codebase, which isn't perfect. It allows us to have feature flags, but requires a commit and deployment for changing the feature flag's state.

Possible solutions are:
* Storing the flags on an external database
* Using a third-party "Feature Flags" SaaS service

