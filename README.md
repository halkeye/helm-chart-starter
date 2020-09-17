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
$ git clone https://github.com/halkeye/helm-chart-starter ${HOME}/.local/share/helm/starters/halkeye/charts
```

## Updates

If you need to fetch the newer version, cd into the directory and run the git pull.

```bash
$ cd ${HOME}/.local/share/helm/starters/halkeye/charts
$ git pull
```

## Usage

Helm allows the usage of a "template" chart when creating other charts, as follows:

```bash
$ helm create ${CHART_NAME} --starter=halkeye/chart
```

## Placeholders

* `<CHARTNAME>`: The reference of the chart of the form `/a-z/` e.g. `linkerd`.
