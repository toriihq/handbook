# Alerts

## Why?

Since we have the ability to ship code quickly and rollback changes, setting up good alerts are critical to catch problems in production.

## How?

Good alerts starts with good logging. Always log errors and warning and provide good context.

All errors are reported in real time by `logz.io` (backend) and `sentry` (frontend) to `Slack` and each one requires attention. New alerts can be setup in `logz.io` based on search terms.
