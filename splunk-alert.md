# Splunk Detector Gate

Gating your releases based on active alerts in Splunk Observability Cloud can help protect against unintended impacts of a software release during an active incident or outage. If a release is required during an outage or incident the release gate can be easily ignored.

For detailed quick start instructions please visit this extension's [Github Repo](https://github.com/splunk/azure-devops-splunk-alert-gate)

## Additional information on Splunk Observability Cloud API interactions

Check [the API docs](https://dev.splunk.com/observability/reference/api/detectors/latest#endpoint-retrieve-events-single-detector) for more information on interacting with Detectors.

Token used must be an **API** token.