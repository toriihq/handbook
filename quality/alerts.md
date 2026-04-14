# Monitoring & Alerts

## Why?

Since we have the ability to ship code quickly and rollback changes, setting up good alerts are critical to catch problems in production.

## How?

Good alerts starts with good logging. Always log errors and warning and provide good context.

All errors are reported in real time by `datadog` (backend) and `sentry` (frontend) to `Slack` and each one requires attention. New alerts can be setup in `datadog` based on search terms.

We encourage setting up AI Agents automations in the Cloud that will monitor these alerts and provide initial triage and if possible, a PR fix.
