ansible-basic-server-setup
=========

A role to do basic setup of a debian based server. This role will install
essential packages and do basic security.

Requirements
------------

None.

Role Variables
--------------

By default, this role will install the following packages:

* build-essential
* git-core
* python-setuptools
* python-software-properties
* python-pip
* aptitude
* fail2ban
* unattended-upgrades
* vim

You can specify additional packages to install by setting the variable
`additional_packages_to_install` to a list of additional packages to install.

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: webservers
  roles:
    - role: ansible-basic-server-setup
      additional_packages_to_install:
        - postgresql-server
        - nodejs
        - ruby
```

Author
------

Rick Apichairuk

License
-------

BSD 3-Clause License

Copyright (c) 2017, Rick Apichairuk
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this
  list of conditions and the following disclaimer.

* Redistributions in binary form must reproduce the above copyright notice,
  this list of conditions and the following disclaimer in the documentation
  and/or other materials provided with the distribution.

* Neither the name of the copyright holder nor the names of its
  contributors may be used to endorse or promote products derived from
  this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
