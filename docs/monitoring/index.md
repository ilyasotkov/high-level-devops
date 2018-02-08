# Monitoring and alerting

Once your software is running in a production environment, our job is finished! Well, not quite.

Ideally, we don't ever want to face failure in production, because that's what staging environments are for. We don't live in an ideal world though. So, in case a mistake happens, we want to:

- Quickly get notified of the problem
- Quickly fix the problem

## Monitoring

Monitoring is done to predict and prevent systems failure. It also helps us understand how our systems work.

## Alerting

It would be expensive and boring to spend all day staring at a monitoring system. Human resources should focus on adding value to the system, not maintaining it. That's why our deployments must have health checks and auto-healing features enabled.

But when the system cannot fix itself, an alerting system will make sure there's no delay between (imminent) failure and human intervention.
