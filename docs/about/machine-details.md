# Node Details
This section provices details on each node and what surface area is available. So just what is going on on each virtual machine?

## Elastic
The "`elastic`" node is the first and only _required_ node, and is the crux of the entire project. It's essentially a SIEM that is used to capture logs of attacks carried out by the red box `redops`.

#### Features

* Elasticsearch
* Kibana
* Prelude Operator UI
* Powershell

#### Enabled Services

* Elasticsearch
* Kibana

## Windows10 Workstation

The Windows10 node acts as the primary _target system_ to execute effects against, in
order to generate security event data.

#### Features

* Built from Windows 10 x64 Enterprise trial ISO
* WinRM Enable (unauthenticated mode, for Packer/Vagrant to use)
* One user `vagrant`
* All updates applied during build process
* Includes VM guest additions
* Turn on RDP
* Set the network type for the virtual adapter to 'Home' and not bug you about it
* Turns autologin *off*

#### Enabled Services

* Elastic Agent
* Sysmon

## Centos Server

The intent of the `ts.centos7` box is emulate hosting the typical services hosted on a small enterprise environment and provided another OS attack surface.

#### Features

* Built from CentOS 7 ISO
* SELinux enforced
* One user `vagrant`
* All updates applied during build process
* Includes VM guest additions
* Turns autologin *off*

#### Enabled Services

* Auditbeat
* Auditd
* Filebeat
* Cockpit
* Nginx
* Rsyslog
* Samba

## Redops

The intent of the redops box is a Red Team box that is used to execute attacks against the victim machines.

#### Features

* Built from Debian 11 ISO
* One user `vagrant`
* All updates applied during build process
* Includes VM guest additions

#### Enabled Services

* Prelude Operator

> More details on the usage of each tool can be found in the [Tool Usage Section](https://docs.thremulation.io/tool-usage/).