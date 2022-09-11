# Lesson 13: Vital Production Metrics

Metrics are data points that tell you how healthy production is 

If log aggregation is the first tool to set up for production monitoring, metrics monitoring should be the second

Log aggregation primarily deals with text - logs are textual of couse. In contrast, metric aggregation deals with numbers

- How long did something take?
- Is memory being used?


## Ideas for metrics to collect:
- Request fulfillment times
- Request counts
- Service resources

## Server resource metric examples:
- Database size and maximum database size
- Web server memory (currently used as well as maximum)
- Network throughput and capacity (900mb/s out of 1gb/s)
- TLS certificate expiry time and life left

### Production faults rarely look like "no user can access anything", often they are a gradula ramp - certain APIs taking longer and longer to load until everything falls apart, for example

## Quartile analysis
- Quartile analysis is an easy way to pare down production time statistics into something actionable. A website might measure how long it takes visitors to fully load their landing page to notice when there is a production issue. 
- With quartile analysis, they would split the request times into many different buckets:
    - How long did the slowest 1% of requests take?
    - How long did the slowest 5% of requests take?
    - How long did the slowest 25% of requests take?

## Common production metrics tools: 
- Promethus/Grafana - OSS, often seen in cloud native (Kubernetes/Docker) settings
- Datadog - newer, primarily SaaS, often described as expensive
- New Relic - older, perhaps more reliable and mature
- AWS CloudWatch Metrics - common choice for AWS users
- Google Cloud Monitoring - less mature version of CloudWatch Metrics
- Azure Monitor Metrics - perhaps the best interface and experience of the three top cloud providers