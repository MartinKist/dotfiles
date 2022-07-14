# dotfiles

Dotfiles and ansible playbooks to set up and configure my personal Ubuntu environment.

## Requirements
### Ubuntu
These playbooks have only been tested with Ubuntu 22.04, other versions may work.

### root priviliges
Goes without saying.

### Ansible
Run `$ sudo apt install ansible` if it is not installed already.


## Usage

### Clone this repository
`$ git clone https://github.com/MartinKist/dotfiles.git`

### Create an inventory file
Move into the `dotfiles` folder (`$ cd dotfiles`) and create a new file called `inventory.yaml`.
Put the following into your new file:
```
all:
  vars:
    git:
      user: <your git username>
      email: <your email address>
      editor: vim
      default_branch_name: main
```
Fill in your git username and email and save the file.

### Run the playbook
Run the `up.yaml` playbook using `$ ansible-playbook -i inventory.yaml -K up.yaml`.  
When you get prompted for a BECOME password, type in your unix password and hit enter.
