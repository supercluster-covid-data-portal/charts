# Supercluster Helm Chart Repository

## How it works

GitHub Pages is pointed to the `/docs` folder. A typical workflow from creating to publishing a chart is described below.

> NOTE: Make sure to use Helm 3

```shell
$ helm create mychart # Create a new chart
$ helm package mychart # Turn a chart into a versioned chart archive file
$ mv mychart-0.1.0.tgz /docs # move the new chart file to the charts folder
$ helm repo index ./docs --url https://supercluster-covid-data-portal.github.io/charts/ # Generate an index file in docs folder
```

## Add repository

To add this repository to a kubernetes cluster:

```shell
helm repo add supercluster https://supercluster-covid-data-portal.github.io/charts/
```
