### Setup kafka on Ubuntu 20.04 ###

#### Test playbook on a Virtualbox VM managed by Vagrant ####

##### 1. Install Virtualbox & Vagrant #####
`sudo apt-get update && sudo apt-get install virtualbox`
`curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -`
`sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"`
`sudo apt-get update && sudo apt-get install vagrant`

##### 2. Go to local project path  #####

##### 3. Start VM with Vagrant  #####
`cd vagrant && vagrant up && cd ..`

##### 4. Run the Ansible playbook #####
`time ansible-playbook -i inventories/local playbooks/setup-kafka.yml`
`# Vault password for the local environment is 'local'`
