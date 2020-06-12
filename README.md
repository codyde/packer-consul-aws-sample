# What is this dark magic? 
## It's Packer of Course! 

This combination of files will help you quickly a Consul enabled "client" up and running quickly in AWS. It builds quickly and after deployment you can deploy the AMI and have it automatically join your Consul environment.  

## Consul Configuration Includes... 

* Consul binary (1.7.3 currently)
* Consul systemd service (enabled)
* Envoy binary 
* Envoy service created (disabled)

## Requirements 

* Ensure you've configured your AWS authentication on the workstation this is being ran from 
* Update the `ansiblevars.yml` file with the details from your Consul deployment. 
* Update the `ca.pem` and the `consul.config.json` file with the information provided to you from your Consul environment. 
* Update `packer.json` with the name you want to use for your AMI

## Building 

Execute the build by running 

`packer build packer.json` (remember to add -force if you have already built this AMI before)