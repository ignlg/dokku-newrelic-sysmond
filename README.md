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

### Required patch
In order to avoid running a new monitor with every `dokku run APP COMMAND`, the [Dokku's PR #645 patch](https://github.com/progrium/dokku/pull/645) must be applied.

## Issues
* Unnamed containers/servers <-- fixable with [dokku-name](https://github.com/alex-sherwin/dokku-name) plugin