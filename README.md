Ansible Role: Intel_SGX_PWS
=========

Ansible Role to install the Intel SGX Platform Software (Intel SGX PSW) and Intel SGX DCAP according to the Intel SGX Software Installation Guide For Linux OS

Requirements
------------

Pre-requisites not be covered by Ansible or the role:
- None

Role Variables
--------------

The file `defaults/main.yml` defines the package that are being installed according to the Intel SGX Software Installation Guide.

In the file `vars/main.yml` we additionally define the following two variables to allow you to control whether dev and debug packages will be installed:

```
install_sgx_debug: true # controls if debug packages will be installed, true by default
install_sgx_dev: true # controls if development packages will be installed, true by default
```

Dependencies
------------

Roles hosted on Galaxy and their parameters:
- None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: melhindi.intel_sgx_pws }

License
-------

Apache 2.0

Contribute
-------

To contribute to the development of this role the following setup is recommended:

```
# 1. Clone the repository with the expected role name:
git clone git@github.com:melhindi/ansible-role-intel-sgx-pws.git melhindi.intel_sgx_pws

# 2. Initialize the virtual environment
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt

# 3. Use molecule to test the role
molecule converge
```
*Note*: This setup assumes that you do not have any globally installed ansible or molecule. Sometimes globally installed ansible/molecule can cause package/dependency conflicts.
