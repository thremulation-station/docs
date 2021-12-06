# Prelude Operator Basic Usage


### Goals
At the end of this lab you will be able to: 

1. Start Prelude Operator
2. Understand how to use Prelude Operator
3. Start Pneuma agents that have been staged on the "victim" hosts. 


### Pre-Reqs

Let's get set up for this lab:

1. Vagrant up the redops and windows10 box:

    - `vagrant up ts.redops ts.windows10`

2. Establish an RDP session with the redops box with the RDPclient of your choice, with the following data:

    ```
    host:192.168.56.14
    user:vagrant
    pass:vagrant
    ```

---

## Startup

Operator comes pre-installed on the redops host, and is located in the /home/vagrant/Desktop directory. In order to utilize it you only need to start Operator, so let’s do that.

1. Click `Operator.appimage` on the Desktop. Accept the TOS. Operator will do the rest and will be ready for connections in 15-20 seconds after launch. 

## Agents

To get agents communicating with Operator, we need to start the Windows agent. 

Establish an RDP session with the windows10 box with RDP client of your choice with the following data: 

	```
	host:192.168.56.11
	user:vagrant
	pass:vagrant
	```
	
Navigate to `C:\Pneuma` and run `start-pneuma.ps1`

After a few seconds the agent will connect to Operator and you will receive a notification of the check-in. 

A number of options can be changed with the Agent such as the communication method, the check-in interval, etc. 

The docs for Operator are within the application itself but a good quickstart guide is also available on their GitHub here: [Operator Docs](https://github.com/preludeorg/operator-support/blob/master/docs/quickstart.md)

## Demo
TODO