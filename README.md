# Ansible-LikewiseOpen
====================

Ansible playbook for deploying PowerBroker Identity Services PBIS Open Edition for RedHat/CentOS

## Ubuntu PBIS package
The Ubuntu support adds and installs from the http://repo.pbis.beyondtrust.com/apt.html repo

## Distributing PBIS package

The Easiest way for distributing the PBIS Open packages is using local `yum` repository.

1. Download the package from [BeyondTrust Website](http://download1.beyondtrust.com/Technical-Support/Downloads/PowerBroker-Identity-Services-Open-Edition/?Pass=True)
2. Exctract the package and move the rpm files `pbis-open-8.2.1-2979.x86_64.rpm pbis-open-gui-8.2.1-2979.x86_64.rpm pbis-open-upgrade-8.2.1-2979.x86_64.rpm` to  for example `/var/www/packages/pbis` folder (nginx or apache)
3. create/update the repo with `createrepo /var/www/packages/pbis`   `(--update)`


## Variables
* `domain_user:` and `domain_pass:` of a domain user with granted add/remove computers to the domain
* `domain_fqdn:` Full qualified domain name of your domain, e.g. office.contoso.com
* `domain_netbios:` NetBIOS domain name, e.g. CONTOSO
* `url:` http adress of your yum repo if using Redhat

## Supported platforms
* Redhat/CentOS 6.x
* Ubuntu 14.04


## todo
* add a module or sh script to download pbis and update rpm repository
