# Feature Flags

> Feature Flags (or Feature Toggles) are a powerful technique, allowing teams to modify system behavior without changing code.

## Why

Using feature flags allows us to test features in production without releasing it to our entire user base.

Once a feature is ready to be fully released, we can turn the Feature Flag on. Feature flags can also target specific users or segments of users.

## How

Feature flags for each customer can be set in the MySQL DB table `feature_flag`. These are sent to the client and processed on the web application.

