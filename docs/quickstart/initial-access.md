# Initial Access

If you've just completed a [Deployment](https://docs.thremulation.io/quickstart/deployment/), it's time to really get into things by accessing the primary user interfaces in the project.


## Getting Status

First, let's make sure everything is up and running. Let's fire `stationctl` back up and use the "Status" menu:

- Run the CLI: $ `./stationctl`
- Select option 3: "`show current deployment`"

This will run through a check of you new Vagrant boxes to see if they're up and communicating over all the necessary channels.

<br>
<p align="center">
<img src="/images/ts-access1.png" width="75%" alt="">
</p>
<br>

This provides some very valuable information on the status of our local range:

1. Virtualbox machine state
1. Elasticsearch API availability
1. Kibana web interface availability

> **Note:** Because Elasticsearch is a single node installation, the status will show "yellow". Everything is fine.


## Interface Login

The environment is designed for users to interact with 2 primary interfaces:

- Prelude Operator - **execute** threats
- Kibana WebUI - **detect** threats


### Prelude Operator

This adversary emulation toolset is accessed by rdp'ing into the `ts.redops` box and starting up `Operator.appimage` on the Desktop.

1. From the vagrant/ directory:
    - $ `vagrant rdp ts.redops`
1. Start Operator:
    - $ `cd ~/Desktop` 
    - $ `./Operator.appimage`
    - Click `Operator.appimage` and accept the TOS


### Kibana Web Interface

1. To reach Kibana browse to `localhost:5601`
1. Login with the credentials:
    - user: `vagrant`
    - pass: `vagrant`

1. Once in Kibana click the hamburger menu in the upper left corner of the UI and select the "Discover" tab.


<br>

---
Now that you've set up the primary user interfaces, it's time to move on to running a functions check!
