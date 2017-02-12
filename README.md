# Example of building an openio cluster
---

A set of playbook to build an opneio cluster.

This demo supports Openstack and Centos 7 for the moment

## Requirements

- Epel repository : 

```yum install --enablerepo=extras epel-release```
    
- Devel packages :

```yum install --enablerepo=epel gcc python-setuptools python-pip python-devel openssl-devel```
    
- A pip up-to-date:

```pip install --upgrade pip```

Please refer to the [requirements.txt](https://github.com/cdelgehier/ansible-openio-sds/blob/master/requirements.txt) file for the python environment

```pip install -r requirements.txt```

- Some ansible roles: ```./install_roles_dependencies.sh```



## Usage

Look the [inventory](https://github.com/cdelgehier/ansible-openio-sds/blob/master/inventory) file 

| Variable 		| Comments (type)  |
| :---     		| :---             |
| `os_image`    	| The Openstack image to use |
| `flavor`    		| The Openstack flavor to use |
| `netid`    		| The Openstack network ID to use |
| `upgrade_system`    	| Need an operating system up-to-date |

These variables can be defined in the inventory but also in a file in the [host_vars](https://github.com/cdelgehier/ansible-openio-sds/blob/master/host_vars) folder

### Openstack: Deployment

For the use of openstack, you must fill the file [openstackrc](https://github.com/cdelgehier/ansible-openio-sds/blob/master/openstackrc) with your identifiers and the endpoint keystone

```. openstackrc```


### Openstack: Rollback

To remove all VM in openstack

```. openstackrc```

```ansible-playbook  mrproper.yml```

## Run

```ansible-playbook site.yml```

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.

Pull requests are also very welcome. The best way to submit a PR is by first creating a fork of this Github project, then creating a topic branch for the suggested change and pushing that branch to your own fork. Github can then easily create a PR based on that branch.

## License

BSD

## Contributors

- [Cédric DELGEHIER](https://github.com/cdelgehier/) (maintainer)
