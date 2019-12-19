# VotingAppAnsible
## Introduction
In order to keep this demo project as real as posible i built an Application in a non-monolitic approach, for this we have an **UI** (user interface) and a **Backend**, this application is deplyed using **Docker containers** with docker-compose all of this over **AWS infrastrcutre** deployed using **Ansible** so a the end of the day we have four repositories.
1. **UI:** https://github.com/jpablo1286/VotingAppUI
2. **Backend:** https://github.com/jpablo1286/VotingAppBackend
3. **Docker containers :** https://github.com/jpablo1286/VotingAppDocker
4. **Ansible Playbooks:** https://github.com/jpablo1286/VotingAppAnsible

## Check the working app visiting this link http://votingapp.juanrivera.org/ ##


# Ansible
This repository contains two playbooks:
 1. **Playbook.yml** Creates a Security group deploy an EC2 instance and installs all dependencies, build images and deploy the containers, finally it attaches an Elastic IP pointed by the DNS record **votingapp.juanrivera.org** sumairizing this playbook deploys from scratch the application and let it fully working and available.
 2. **DecomisionPlaybook.yml** it terminates the EC2 instances deployed for the app and remove the security group and related resources, it is just a tool for cleaning up, mainly for testing purposes.


### Usage: ###
> ansible-playbook -i ec2.py Playbook.yml
