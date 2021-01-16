# Node Details
This section provices details on each node and what surface area is available. So just what is going on on each virtual machine?

## Elastomic
The "`elastomic`" node is the first and only _required_ node, and is the crux of the entire project. It's essentially a "Purple Teaming" control box that is used to **both** _execute attacks and capture logs of those attacks_.

#### Features

* Elasticsearch
* Kibana
* Atomic Redteam UI
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

> More details on the usage of each tool can be found in the [Tool Usage Section](../tool-usage/index.md).