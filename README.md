# ansible-nodejs [![Build Status](https://travis-ci.org/pbonrad/ansible-nodejs.svg?branch=master)](https://travis-ci.org/pbonrad/ansible-nodejs)

Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient. Node.js' package ecosystem, npm, is the largest ecosystem of open source libraries in the world.

More information about NodeJS can be found here:
[https://nodejs.org](https://nodejs.org)

This role installs NodeJS on the target server using the `apt-get` package manager. It works for Ubuntu and Debian servers and was tested with the help of docker containers. In comparison to other Ansible role tests where Ansible runs inside the container and is connecting to localhost, I decided to use the [Ansible docker connection](http://docs.ansible.com/ansible/intro_inventory.html#non-ssh-connection-types) (`ansible_connection=docker`). The build which run at [Travis CI](https://travis-ci.org/pbonrad/ansible-nodejs) uses this functionality.

See also:
* GitHub project with Dockerfiles:  [https://github.com/pbonrad/ansible-docker-base](https://github.com/pbonrad/ansible-docker-base)
* Role on Ansible Galaxy:  [https://galaxy.ansible.com/pbonrad/nodejs/](https://galaxy.ansible.com/pbonrad/nodejs/)

## Role Variables

    # versions available: 0.12 | 4.x | 5.x | 6.x
    nodejs_version: "6.x"

## Dependencies

There are no dependencies to other roles. If you want to run the test, you need to install [Docker](https://www.docker.com/).

## Example Playbook

An example playbook is included in the `test.yml` file. You can use `run.sh` for running a test locally, which starts a docker container as the target.

    - hosts: all
      roles:
         - role: ansible-nodejs

## Contributions and Feedback

Any contributions are welcome. For any bugs or feature requests, please open an issue through [Github](https://github.com/pbonrad/ansible-nodejs/issues).

## License

MIT

## Author Information

Peter Bonrad - [pbonrad](https://github.com/pbonrad) - 2016
