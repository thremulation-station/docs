# Contribution

This document aims to provides instructions to set up, develop, and submit updates and
features for this project. Here is a high level overview of the process:

- fork the project
- clone to your local machine
- setup local environment with docker
- use the local container to update documentation

### Github Issue

Please create an Issue the proper repository:

* [Project documentation](https://github.com/thremulation-station/thremulation-docs/issues)
* [Code/additions/anything else](https://github.com/thremulation-station/thremulation-station/issues)

### Community

Please join the [Slack](https://join.slack.com/t/thremulation-station/shared_invite/zt-urwtghsh-GyJp8ENYQgtDQAP0JhcbRw).

### Email

If all else fails, please feel free to send us an email --> `contact [at] thremulation [dot] io`.

## Install Requirements

This section assumes that you are using macOS. Use the [brew](https://brew.sh/)
package manager where noted below (and generally whenever possible).  

1. Install Git: $ `brew install git`
  - instructions for installing brew can be found [here](https://brew.sh/)
ADD

## Git the Things

1. Clone the repo locally by copy / pasting the full command by clicking the "Clone" in the top right corner of the web UI:  
  $ `# example command:  git clone <CLONE_URL>`

2. Change directory into the project folder:
  $ `cd thremulation-station`

3. Create an new branch (alternate timeline) for later pull request / merging operations:
  $ `git branch <BRANCH_NAME>`

4. Jump into your new personal branch:
  $ `git checkout <BRANCH_NAME>`


## Content Development

TODO


## Submitting Changes

After the above workflow is complete, it's time to submit your work for
approval:

1. With all your work committed, push your changes up to your project fork:
  $ `git push`

2. Use the Github graphical interface to submit an official Pull Request to
merge in all your changes.  
