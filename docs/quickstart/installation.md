# Installation

Enough background info, let's get into the technical steps. Here's a high-level overview of the process to get your range up and running:

1. Clone the project locally from Github
1. Install 
1. Use the CLI to deploy your range
1. Reference the User Guide at [thremulation.io](https://thremulation.io)
1. Use the CLI to perform cleanup / reset tasks


## Installing Dependencies

Let's kick the process off by installing the required software for your host platform!

!!! note ""
      A simple and unified user experience is our goal, so we're working to build the dependency installation process into the [Station Control CLI](/support/stationctl.md), stay tuned. More on `stationctl` in a bit!

<br>

=== "macOS"
      
      <br>
      We have used macOS for the lion's share of the development and testing of the project (and currently provides the most validated experience).

      1. Ensure you have the [Homebrew](https://brew.sh/) package manager, which is used for all subsequent installs
      1. Update your new brew install by running: $ `brew update`
      1. Install Virtualbox: > `brew install --cask virtualbox`
      1. Install Vagrant: > `brew install --cask vagrant`
      1. Install Git: > `brew install git`
      1. Install Vagrant plugins: $ `vagrant plugin install vagrant-disksize vagrant-vbguest`

=== "Windows10"
  
      1. We strongly recommend installing the [Chocolatey](https://chocolatey.org/) package manager, which is used for all subsequent installs
      1. Install Virtualbox: $ `choco install virtualbox`
      1. Install Vagrant: $ `choco install vagrant`
      1. Install Git: $ `choco install git`
      1. Install Vagrant plugins: > `vagrant plugin install vagrant-disksize vagrant-vbguest`
      <br>
      
      > **Note:** Vagrant requires a restart as part of the installation!.

=== "Centos 7"

      This section assumes that you're using a fully updated Centos 7 box. All listed are run from a root shell (`sudo -s`).
      
      1. Install requirements
            ```sh
            yum groupinstall -y "Development Tools"

            yum install -y \
            kernel-devel \
            kernel-devel-3.10.0-1127.el7.x86_64 \
            epel-release \

            yum install -y git
            ```
      1. VirtualBox:
      a. add repo file: `curl -o /etc/yum.repos.d/virtualbox.repo http://download.virtualbox.org/virtualbox/rpm/rhel/virtualbox.repo`  
      b. import key: `rpm --import https://www.virtualbox.org/download/oracle_vbox.asc`  
      c. install: `yum install -y VirtualBox-6.0`
      d. grant permissions: `sudo usermod -aG vboxusers "$(whoami)"` 
      1. Vagrant:
      a. install: `yum install -y https://releases.hashicorp.com/vagrant/2.2.10/vagrant_2.2.10_x86_64.rpm`  
      b. install required plugins: `vagrant plugin install vagrant-disksize vagrant-vbguest`

=== "Fedora 33"

      This section assumes that you're using a fully updated Fedora 33 box. All listed are run from a root shell (`sudo -s`).

      1. Install requirements
            ```sh
            sudo dnf install -y \
              binutils \
              gcc \
              make \
              patch \
              libgomp \
              glibc-headers \
              glibc-devel \
              kernel-headers \
              kernel-devel \
              dkms \
              qt5-qtx11extras \
              libxkbcommon \
              rpmrebuild
            ```
      1. VirtualBox:  
      a. Add repo file: `curl -o ~/VirtualBox-6.1-6.1.16_140961_fedora32-1.x86_64.rpm http://download.virtualbox.org/virtualbox/rpm/fedora/32/x86_64/VirtualBox-6.1-6.1.16_140961_fedora32-1.x86_64.rpm`  
      b. Rebuild for Fedora: `rpmrebuild --change-spec-preamble='sed -e "s/6.1.16_140961_fedora32/6.1.16_140961_fedora33/"' --change-spec-requires='sed -e "s/python(abi) = 3.8/python(abi) >= 3.8/"' --package VirtualBox-6.1-6.1.16_140961_fedora32-1.x86_64.rpm`  
      c. Install package: `dnf install -y ~/rpmbuild/RPMS/x86_64/VirtualBox-6.1-6.1.16_140961_fedora33-1.x86_64.rpm`      
      d. Grant permissions: `sudo usermod -aG vboxusers "$(whoami)"`
      1. Vagrant:  
      a. Install package: `dnf install -y https://releases.hashicorp.com/vagrant/2.2.10/vagrant_2.2.10_x86_64.rpm`  
      b. Install required plugins: `vagrant plugin install vagrant-disksize vagrant-vbguest`


!!! note "Note:"
      If you don't see your OS flavor listed, please consider contributing!

## Getting the Project

Now that you have all the requirements installed, it's time to clone the project code locally:  

1. Clone the repo: $ `git clone https://github.com/thremulation-station/thremulation-station.git`
1. Move into the new project folder: $ `cd thremulation-station`


<br>

---
The next page will cover deploying your VM range.
