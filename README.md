# New Relic's Server Monitoring plugin for Dokku

**Warning**: This is just an _experiment_ so use it carefully and at your own risk. Any contribution will be really appreciated.

Sets up and starts a [New Relic's server monitoring](http://newrelic.com/server-monitoring) daemon `sysmond` into the docker container that runs the app.

## Installation

On the _dokku_ server:
```sh
git clone https://github.com/ignlg/dokku-newrelic-sysmond.git /var/lib/dokku/plugins/newrelic-sysmond
dokku plugins-install
```

## Setup
### Required environment variables

`NEW_RELIC_LICENSE_KEY` with your New Relic License Key.

`NEW_RELIC_SYSMOND_DOKKU` set to `1` to start the daemon on deploy.

## Issues
* Runs a new monitor with every new container, even for a `docker run ... ls`
* Unnamed containers/servers
* No process list