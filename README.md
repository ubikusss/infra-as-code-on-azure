# Infrastructure as Code on Azure demos

This repository contains various demos presented on DevOps Bootcamp Praha 2018 by Tomas Kubica. 

Each example contains deploy.ps1 or deploy.sh with instructions how to deploy that demo.

# ARM basics (arm-language)

This demonstrates some basic ARM syntax principles described here:

TBD

# Multiple Web Apps with Azure SQL in SaaS scenario (arm-webapps)

Using ARM templates to deploy infrastructure for SaaS solution where each customer has separate instance (Web App) and separate Azure SQL DB (part of elastic pool). Object parameter is used to provide complete list of customers (instances). Certificate is deployed (make sure you put there your own as parameter - contents of your PFX file with base64 encoding; in Bash you can use cat mycert.pfx | base64 -w 0). Also host binding is created and DNS registered in Azure DNS (make sure you have some DNS zone of your own). Staging slot is also deployed with SQL DB, but not registered with custom domain or certificate.

# ARM IaaS (arm-iaas)

Template creates multiple frontend VMs with public IP load balancer and multiple backend VMs with private IP load balancer. Number of VMs in each tier is specified as parameter.

# Terraform as multi-cloud infrastructure deployment solution (terraform)

TBD

# Deploy Windows configuration with ARM and DSC extension (extension-dsc-iis)

Simple ARM template deployes Windows VM and than DSC extension is used to configure OS. Follow instructions in deploy.ps1 in order to get your DSC file uploaded to storage location and referenced by ARM. Purpose of this demo is to leverage DSC to configure IIS on target system.

# Configure Domain Services via DSC and automaticaly join new VM to domain (extension-joindomain)

In first part of our demo we will use again ARM with DSC extension to deploy Windows machine and configure it. This time to enable Domain Services, DNS role and promote machine to DC role. Next we will deploy another Windows VM and use Join Domain Extension to make it automatically joined as part of our ARM deployment process.

# Prepare Azure Automation DSC and use it to manage VM configurations (automation-dsc)

First we will deploy Azure Automation account with ARM template and prepare it for IIS configurations by importing proper Modules, Configurations and make it compiled. As part of template plain Windows VM will be deployed. Next use Azure portal to register this VM with Azure Automation and apply IIS configuration to it.

# Automate Linux OS during first start with multi-cloud cloud-init (cloud-init)

In this demo you will se usage of standard cloud-init to configure Linux system after first start. In our case we will register new repositories, install various packages and run script to do configurations. Purpose of this demo is to automatically create workstation (jump-server) to operate Kubernetes such as AKS (installs GUI, remote desktop, kubectl, Helm, Docker, VS Code with various plugins). 

# Deploy infrastructure and configure Linux VMs with Ansible roles

TBD

# Leverage Low-priority VMs to lower your cost of batch operations (batch-transcoding)

TBD

# Prepare Managed Application and publish it to your internal app catalog in Azure (managedapp)

TBD

# Trial workflow for your SaaS app using ARM, containers and Logic Apps (trial-workflow)

TBD



