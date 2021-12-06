# Requirements

Thremulation Station aims to be as lightweight as possible, in order to deliver on the promise of running a "range on a laptop". In order to achive this, we have to establish some minimum standards.

## Hardware Capability

Bottom line: this project should provide a usable range on a _relatively modern_ laptop:

- 4 CPU threads (i5 / i7 proc) 
- 8G of memory
- Virtualization support (VTd etc.)


## Virtual Resources

The listing of resources allocated to each virtual machine are listed below (note that virtual cpus == threads):

- Elastic:
    - virtual memory = `4G`
    - virtual cpus = `2`
- Windows:
    - virtual memory = `2G`
    - virtual cpus = `2`
- Centos7:
    - virtual memory = `1G`
    - virtual cpus = `1`
- Redops
    - virtual memory = `2G`
    - virtual cpus = `2G`

 These values are certainly tunable, but this is a good starting point. All details can be found in the [Vagrantfile](https://github.com/thremulation-station/thremulation-station/blob/devel/vagrant/Vagrantfile).

!!! warning "Warning"
    Make sure you know what your doing before changing things in the Vagrantfile. You break it, you buy it ;)

<br>

---
The next page will cover details on the packages, tools, and running services on each box.