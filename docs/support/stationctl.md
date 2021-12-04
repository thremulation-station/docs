# Station Control Usage Guide

The `stationctl` CLI aims to be the unified interface for most tasks a user would need to accomplish in TS. 

The CLI is powered by a bash script that can be found in `<project>/vagrant`, and must be executed from that directory. At the end of the day, it's (mostly) a user-experience wrapper around ***existing vagrant commands***. There's a bit of dancing with danger when using a CLI that wraps a CLI, so bear with us...

!!! warning
    If something in `stationctl` does not work, your first step should be to reference the [Vagrant CLI Docs](https://www.vagrantup.com/docs/cli).


<br>

> Remember Luke, runnning `vagrant --help` is your friend. Always. 

<!-- Let's get into the functionality of Station Control and how to use it. -->

## Setup

This (currently experimental) menu will attempt to script out the dependency installation for some major operating system choices.

Under construction!


## Deploy

1. Quick Deployment - _deploy all target boxes_
2. Custom Deployment - _choose targets you want_
3. Staged Deployment - _download boxes you want_


## Status

The "Status" menu will show the state of a running deployment.  

<br>
<p align="center">
<img src="/images/ts-access1.png" width="75%" alt="">
</p>
<br>

This provides some basic information on the status of a TS deployment:

1. Virtualbox machine state
1. Elasticsearch API availability
1. Kibana web interface availability

> **Note:** Because Elasticsearch is a single node installation, the status will show "yellow". Everything is fine.


## Management

This menu will see some heavy use, and it's broken down into 2 sections:

### Maintenance

1. List - _list all current boxes_
2. Startup - _start all local boxes up_
3. Shutdown - _halt running boxes shutdown range_
4. Update - _update boxes to latest version_
5. Reboot - _restart boxes (troubleshooting)_


### Data Reset and Troubleshooting

6. Clear Data - _delete data in all indexes_
7. Clear Alerts - _delete all open signals in the siem index_
8. Soft Reset - _revert to original snapshots_
9. Hard Reset - _destroy all vms_
10. Nuke and Pave - _destroy all vms and boxes_