# New Relic's Server Monitoring plugin for Dokku

Sets up and starts [New Relic's server monitoring](http://newrelic.com/server-monitoring) daemon `sysmond` into the docker container that runs your app.

## Installation

On your _dokku_ server:
```sh
git clone https://github.com/ignlg/dokku-newrelic-sysmond.git /var/lib/dokku/plugins/newrelic-sysmond
```

## Files

`.newrelic-sysmond` file in the root directory of the application to run this plugin.

## Environment variables

`NEW_RELIC_SYSMOND_DOKKU` with `1` to run the daemon.

`NEW_RELIC_LICENSE_KEY` with your New Relic License Key.
