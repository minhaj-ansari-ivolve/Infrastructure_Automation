# Infrastructure Automation

## Introduction

Heat Orchestration Template is used for creating Infrastructure/Stack on Openstack. There are two scripts, one is template and other is for environment variables. You only have to change the environment variables which will create an infrastructure on Openstack accordingly with the Template file.

## Modules being created via Automation

1. Internal/Private Network
2. Subnet for the Internal/Private Network
3. Internal Router
4. Interface for the Router
5. Security Group
6. New Keypair
7. Group of Instances

## Notes

- External/Public Network can be created however it is commented in Template and Variables scripts both
- If you don't change script for the External/Public Network creation than you have to give an existing External/Public Network in Variables script
- First source the openstack in which you want to create the infrastructure/stack before running CLI commands

## CLI Commands

```
openstack stack create -t Automation_Template.yaml -e Environment_Variables.yaml TEST-STACK --wait
openstack stack update -t Automation_Template.yaml -e Environment_Variables.yaml TEST-STACK --wait
openstack stack delete TEST-STACK --wait
```
