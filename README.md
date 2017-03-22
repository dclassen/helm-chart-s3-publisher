# helm-chart-s3-publisher
A web server to broker the upkeeping of chart objects and helm index manifest grooming between your CI build process.  

Lead Maintainer: [Lam Chan](https://github.com/lamchakchan)

## Introduction
[`helm`](https://github.com/kubernetes/helm) is a package manager for [Kubernetes](https://github.com/kubernetes).  The runtime for `helm` consist of a CLI which helps with `chart` package scafolding, manifest generation and can act as a stand alone chart repository.  For long term storage of `chart` packages, it is desirable to use AWS S3 as the storage backing.  `helm-chart-s3-publisher` acts as the shuttle for you to push new `chart`s or update existing `chart`s to AWS S3.  This broker will also manage the updates of the `index.yaml` manifest file when a file is pushed remotely.

## Installation

```
npm install -g helm-chart-s3-publisher
```

Or using Docker
```
docker pull xogroup/helm-chart-s3-publisher
```

## Usage

```
helm-chart-publisher
```

Or using Docker
```
docker run -d xogroup/helm-chart-s3-publisher
```

## Documentation


### API

See the [API Reference](http://github.com/xogroup/helm-chart-s3-publisher/blob/master/API.md).

### Examples

Check out the [Examples]
(http://github.com/xogroup/helm-chart-s3-publisher/blob/master/Example.md).

## Contributing

We love community and contributions! Please check out our [guidelines](http://github.com/xogroup/helm-chart-s3-publisher/blob/master/.github/CONTRIBUTING.md) before making any PRs.

## Setting up for development

1. Clone this project and `cd` into the project directory
2. Run the commands below

```
npm install
npm test
```