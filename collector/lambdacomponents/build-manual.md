# Build AWS Lambda with Datadog exporter and connector

## Prerequisites

* AWS CLI
* install golang 1.21

## Add Datadog modules and build

* Switch dir 
```
cd collector
```
* Install Datadog exporter and connector go modules
```
go get github.com/open-telemetry/opentelemetry-collector-contrib/exporter/datadogexporter
go get github.com/open-telemetry/opentelemetry-collector-contrib/connector/datadogconnector
go get go.opentelemetry.io/collector/connector
```
* Check Datadog exporter and connector wired up on `collector/lambdacomponents/default.go`
* Run build, this will publish to AWS account
```
make publish-layer
```