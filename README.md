Infinidat Challenge 

# Overview 

Please create a flask application with the following steps:

Create single page flask app with some info about yourself .
Create Ansible role which deploys a Docker container running your app
Create a Terraform role to provision instance in aws
Integrate both (executing terraform should trigger the ansible on the provisioned instance )
(you can use aws free tier https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc)

Expected Result:
Running the Terraform will provision and deploy everything needed for your app to be up & running.

Please zip all created files and send back.

** Note **
If you have any questions regarding the task please contact Maxim at: mlevinzon@infinidat.com

## Introduction


## Pre-face

- local Ansible in Docker to test playbook (grabbed here: https://medium.com/@iced_burn/run-ansible-with-docker-9eb27d75285b )
docker run -v "${PWD}":/work:ro -v ~/.ansible/roles:/root/.ansible/roles -v ~/.ssh:/root/.ssh:ro --rm spy86/ansible:latest ansible-playbook playbook.yml 
** Note ** 
replace ${PWD} with regular windows path if run under Windows Docker client

This one, didn't work for me:
TASK [build container image] ***************************************************
_fatal: [localhost]: FAILED! => {"changed": false, "msg": "Unsupported parameters for (docker_image) module: source found in build.

Going to build custom image d:\develop\docker\dockerfile_ansible ( inspired by https://duffney.io/containers-for-ansible-development/#create-a-dockerfile)
https://docs.ansible.com/ansible/2.4/docker_module.html
docker run -it --name  redis --network infinidat_challenge -h redis --rm redis # 
Run redis-cli docker run -it --network infinidat_challenge --rm redis redis-cli 

_(inspired by https://medium.com/@andreilhicas/provision-docker-containers-with-ansible-30cc5ee6d950) 
### Create Ansible role folders structure (https://docs.ansible.com/ansible/2.7/reference_appendices/galaxy.html) 
docker run -v "d:\Develop\Infinidate_challenge":/work -v ~/.ansible/roles:/root/.ansible/roles -v ~/.ssh:/root/.ssh:ro --rm spy86/ansible:latest ansible-galaxy init docker-role 

Build image and create container 
_d:\Develop\Infinidate_challenge> docker run -v "d:\Develop\Infinidate_challenge":/work -v "d:\Develop\Infinidate_challenge"\.ansible\roles:/root/.ansible/roles -v ~/.ssh:/root/.ssh:ro -w /work -e DOCKER_HOST="tcp://host.docker.internal:2375" --rm myansible_centos:latest ansible-playbook infinidat_playbook.yml


### Terraform 
https://learn.hashicorp.com/collections/terraform/aws-get-started

choco install terraform




