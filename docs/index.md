# Welcome

<br>
<p align="center">
<img src="images/ts-logo.png" width="70%" alt="">
</p>
<br>

<h2 align="center"><b>Threat emulation and detection for your laptop</b></h2>

<p align="center">
   Collection of open source tools working together to enable a reasonably capable machine to serve as a local cyber range.
</p>

<p align="center"><b>
    <a href="https://thremulation.io">Thremulation.io</a> |
    <a href="https://github.com/thremulation-station/thremulation-station">Github</a> |
    <a href="https://twitter.com/thremulation">Twitter</a> |
    <a href="https://join.slack.com/t/thremulation/shared_invite/zt-w1v1hijr-r9LYdOOna9p8YuldKxjy_w">Slack</a>
    <br /><br />
</b></p>


<hr />
<br>
Thremulation Station is an approachable small-scale threat emulation and detection range. It leans on Prelude Operator for ***emulating*** threats, and the Elastic Endpoint Agent for ***detection***.

!!! info "TL;DR"
    If you're ready to skip the reading and jump into things, head to the [Quickstart / Installation](https://docs.thremulation.io/quickstart/installation/) section.

There are a lot of tools and moving pieces, but the main building blocks are:

- Virtualbox
- Vagrant
- Elasticsearch
- Kibana
- Elastic Endpoint Agent
- Prelude Operator


## Project Goals

Our goal from the very beginning has been to provide the following:

1. lightweight range that can operate on a laptop with a _minimum_ of 4 threads and 8G of RAM
1. support the big 3 host operating systems (initial linux path is RHEL-based)
1. present users a smooth path to execute threats and observe them with Elastic 
1. provide a singular TUI (Station Control) that can be used to manage all aspects

!!! note "Note"
    You'll be introduced to `./stationctl` early in the [Getting Started](https://docs.thremulation.io/quickstart/deployment/#station-control-intro) section and use it to deploy boxes, get status, manage and clear data, and much more. A full reference guide is located at [support / stationctl](https://docs.thremulation.io/support/stationctl/).


<!-- ## Contribution

How can I help, you ask? We welcome contributions, so check out the project repo [contribution page](https://github.com/thremulation-station/thremulation-station/blob/devel/CONTRIBUTING.md) on Github. -->
