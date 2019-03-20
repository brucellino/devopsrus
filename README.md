# DevOps-R-Us

Infrastructure code for delivering a DevOps pipeline in the ☁️

## Purpose

This repository is for hosting the code necessary to stand up an automation environment for DevOps teams.
It is a purely personal project.

### Assumptions

The following assumptions are made:

- Multiple teams are working on multiple projects, not all of them need to be integrated with each other
- products are deployed across cloud infrastructures, to arbitrary endpoints (AWS, Azure, _etc_).
  - By corollary, I assume that you have access to these platforms.

### Workflow

<!-- insert workflow diagrams here -->

## Toolset

I use the following toolset to build, test, deploy and hopefully monitor the platform.

### Core tools and Orchestration

- Jenkins
- Jenkins plugins
- git

Core to the toolset is the automation engine: [Jenkins](https://jenkins.io).
Jenkins itself represents a bootstrap problem, since something is needed to run the initial deployment, and test the outcome.
For the moment, I'm going to ignore this problem and assume that some perfect robot is testing and running the robot.
See below in [configuration and provisioning](#configuration-and-provisioning) for discussion on the deployment.

### Configuration and Provisioning

Application configuration is done with the relevant toolset of the project language(s) and no
