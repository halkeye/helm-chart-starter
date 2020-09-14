# Helm Chart Starter

## Project Outline

### Project Goals

Make it simple to produce the necessary boilerplate for Kubernetes helm charts

### Similar Work

https://github.com/sitewards/helm-chart
https://github.com/kubernetes/helm/blob/master/pkg/chartutil/create.go

### Summary

* License: MIT
* Language: en-CA

## Installation

```bash
$ git clone https://github.com/halkeye/helm-chart-starter ${HOME}/.helm/starters/halkeye/chart
```

## Updates

If you need to fetch the newer version, cd into the directory and run the git pull.

```bash
$ cd ${HOME}/.helm/starters/halkeye/chart
$ git pull
```

## Usage

Helm allows the usage of a "template" chart when creating other charts, as follows:

```bash
$ helm create ${CHART_NAME} --starter=halkeye/chart
```

This lets us "pre-populate" a chart with much of the boilerplate that is repeated across all projects. Anything that
we know to be unique has a placeholder of the format `__PLACEHOLDER__`, and anything that needs further attention
once the chart has been generated should have a `todo` and extensive documentation.

Not all documentation has been finished.

A list of the `__` placeholders and their intended purpose is below:

* `__NAME__`: The human readable name of the chart of the form `/A-Za-z-_ /` e.g. `Sitewards GmbH`
* `__CHART__`: The reference of the chart of the form `/a-z/` e.g. `linkerd`.
* `__CONTAINER_NAME__`:  The name of the application container of the form `a-z` e.g. `kubectl`
* `__CONTAINER_IMAGE__`: The image ref of the container to be used of the form `/a-z.\//-_` e.g. `quay.io/littlemanco/apache-php`
