# Role Name
=========
This role is used to create EC2 instances of different types of AMIs, including one Linux and two Ubuntu instances.

## Requirements
------------
Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

- Ansible 2.9 or higher
- AWS credentials configured
- `boto3` and `botocore` packages installed

## Role Variables
--------------
A description of the settable variables for this role should go here, including any variables that are in `defaults/main.yml`, `vars/main.yml`, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (i.e., hostvars, group vars, etc.) should be mentioned here as well.

### defaults/main.yml
```yaml
# AWS region
aws_region: "us-east-1"

# EC2 instance details
ec2_instance_type: "t2.micro"
ec2_key_name: "my-key"

# AMI IDs
linux_ami_id: "ami-0abcdef1234567890"
ubuntu_ami_id_1: "ami-0abcdef1234567891"
ubuntu_ami_id_2: "ami-0abcdef1234567892"

## Dependencies
   ------------
A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

## Example Playbook
   ----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

