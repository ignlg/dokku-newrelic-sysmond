# New Relic's Server Monitoring plugin for Dokku

Sets up and starts [New Relic's server monitoring](http://newrelic.com/server-monitoring) daemon `sysmond` into the docker container that runs your app.

## Installation

On your _dokku_ server:
```sh
git clone https://github.com/ignlg/dokku-newrelic-sysmond.git /var/lib/dokku/plugins/newrelic-sysmond
```

## Configuration

`NEW_RELIC_LICENSE_KEY` environment variable.
