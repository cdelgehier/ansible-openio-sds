# Ansible role `openio-sds`

[![Build Status](https://travis-ci.org/cdelgehier/ansible-role-openio-sds.svg?branch=master)](https://travis-ci.org/cdelgehier/ansible-role-openio-sds)

An Ansible role for [OPENIO-SDS](http://docs.openio.io/install-guide-centos). Specifically, the responsibilities of this role are to:

- add the openio repository
    - define the right repository for your distrubution
    - add repository key
- install the openio-sds
- generate the manifest puppet to install the openio-sds
- run the manifest (soon)

This role supports Centos 7 and Ubuntu Xenial.

If you like/use this role, please consider giving it a star or reviewing it on Ansible Galaxy. Thanks!


## Requirements

No specific requirements

## Role Variables


| Variable      	| Default 					| Comments (type)  |
| :---          	| :---    					| :---             |
| `sds_version` 	| `16.10`     					| The SDS version to install |
| `cluster_ip`		| `['127.1.1.1', '127.2.2.2', '127.3.3.3']`	| List of IP addresses of the servers composing the cluster |
| `conscience_ip`	| `'127.1.1.1'`					| IP address where to put the consciousness |
| `redis_ip`		| `'127.2.2.2'`					| IP address of the master Redis |
| `configure`		| `false`					| Determines whether to launch the installation manifest |


## Dependencies

No dependencies.

## Example Playbook

See the test playbooks in either the [Vagrant](https://github.com/cdelgehier/ansible-role-openio-sds/blob/vagrant-tests/test.yml) or [Docker](https://github.com/cdelgehier/ansible-role-openio-sds/blob/docker-tests/test.yml) test environment. See the section Testing for details.

## Testing

There are two types of test environments available. One powered by Vagrant, another by Docker. The latter is suitable for running automated tests on Travis-CI. Test code is kept in separate orphan branches. For details of how to set up these test environments on your own machine, see the README files in the respective branches:

- Vagrant: [vagrant-tests](https://github.com/cdelgehier/ansible-role-openio-sds/tree/vagrant-tests)
- Docker: [docker-tests](https://github.com/cdelgehier/ansible-role-openio-sds/tree/docker-tests)

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.

Pull requests are also very welcome. The best way to submit a PR is by first creating a fork of this Github project, then creating a topic branch for the suggested change and pushing that branch to your own fork. Github can then easily create a PR based on that branch.

## License

BSD

## Contributors

- [Cédric DELGEHIER](https://github.com/cdelgehier/) (maintainer)

