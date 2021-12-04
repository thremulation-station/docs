# Tool Usage

At the end of the day, this project builds some fantastic open source  lego pieces together to solve a problem. Here's
what is being leveraged to make locally-served thremulation magic happen:


## Infrastructure

- VirtualBox
  - This serves as the "hypervisor" that your virtual machines will be built on

- Vagrant (and assorted plugins)
  - This is an automation and orchestration platform to build the VMs that will be used for the project


## Threat Emulation
Threat Emulation (or red teaming) is an attack simulation designed to measure how well defenders can detect an attack from a real-life adversary.

To put threat emulation in layman’s terms, it’s “ethical hacking” — a way for teams to test how well defenders would fare in the face of a real attack.

The premise of red teaming is comparable to the old sports saying, "the best offense is a good defense." Red teaming helps defenders learn about new adversary techniques.

To provide threat emulation, we are using Prelude Operator: https://www.prelude.org/


### Prelude Operator
Preldue Operator has a library of simple tests that every security team can execute to test their defenses. Tests are focused, have few dependencies, and are defined in a structured format that can be used by automation frameworks. Additionally, Operator can take advantage of other libraries of TTP's such as Atomic Red Team. If you/your team is taking advantage of Pro TTP's you may sign in with your account for Prelude as well to get additional functionality. 


## Threat Logging & Detection
Threat detection (or blue teaming) is the process of defending assets and infrastructure from adversaries. This is achieved through a combination of signature-based detections and also access to all available log data to find activity that does not trigger any known signatures.

To provide logging and detection, we are using the Elastic Stack - [Elasticsearch](https://www.elastic.co/elasticsearch/), [Kibana](https://www.elastic.co/kibana/), [Beats](https://www.elastic.co/beats/), and [Agents](https://www.elastic.co/guide/en/fleet/current/elastic-agent-installation-configuration.html).


### Elasticsearch
Elasticsearch is a distributed, RESTful search and analytics engine capable of addressing a growing number of use cases. As the heart of the Elastic Stack, it centrally stores your data for lightning fast search, fine‑tuned relevancy, and powerful analytics that scale with ease.

We store and organize our data here.


### Kibana
Kibana is a free and open user interface that lets you visualize your Elasticsearch data and navigate the Elastic Stack. Do anything from tracking query load to understanding the way requests flow through your apps.

We use Kibana to visualize our data


### Elastic Security
Everything you love about the free and open Elastic Stack — geared toward security information and event management (SIEM). Leverage the speed, scale, and relevance of Elasticsearch for SIEM use cases to drive your security operations.

We use the Elastic Security (SIEM) to organize all of our security relevant data.


### Elastic Agent
The Elastic Agent is a wrapper for centralized management of endpoint collection. We use the Elastic Agent to collect endpoint logs. This replaces Elastic "Beats" (which are now folded into the Agent).
