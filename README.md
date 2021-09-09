Role Name
=========
ansible-asr-redhat

Description
---------------
Ansible role to install the Microsoft Azure Site Recovery (ASR) Agent on a Red Hat Linux system.

This role was developed and tested on a Mint 20.2 system using [Molecule 3](https://molecule.readthedocs.io/en/latest/). Full instructions for setting up this environment are available at [GeoffStratton.com](https://www.geoffstratton.com/test-ansible-roles-molecule-3-and-red-hat-docker-images-linux-mint).

The Azure Site Recovery agent allows a Linux server to connect to a Windows process server for replication into the Azure cloud.

The Azure Site Recovery agent can be placed in the "files" directory here for convenience, but new versions are distributed with the ASR software installed on a Windows process server. The version of the agent **must match** the version of the ASR software on the process server.

Updated agents can be found in c:\%ProgramData%\ASR\home\svsystems\pushinstallsvc\repository on a process server.

Agents must be able to contact a process server on port TCP 443 for successful configuration and startup. TCP 9443 is needed for data replication.

For full documentation, see the [official Microsoft ASR pages](https://docs.microsoft.com/en-us/azure/site-recovery/vmware-azure-install-mobility-service).

To see supported Linux versions, see the [official support matrix](https://docs.microsoft.com/en-us/azure/site-recovery/vmware-physical-azure-support-matrix).

Requirements
--------------
* ansible
* molecule
* python

License
-------
GNU General Public License v3.0

Author Information
------------------
Geoff Stratton
