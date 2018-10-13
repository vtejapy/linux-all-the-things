# Reverse Capture the Flag
In this exercise, you will go through the steps of administering users on a system and implementing basic security hardening procedures.
****

### Objectives
1. Start your Ubuntu lab image or create a cloned image.

2. Within that system, implement all of the following administration and security related tasks.

3. Once completed, use the Export functionality of VirtualBox to submit your work to an instructor to validate completion.
****

### Password Policy
* Set the following password policy on the system
    * Minimum length is 12 characters
    * Require at least 1 1 upper case character
    * Require at least 1 lower case character
    * Require at least 2 numbers
    * Require at least 2 special characters
****

### User Configuration
* Add the following users
    * `tony`
    * `bob`
    * `sarah`
    * `jenny`
    * `toto`
    * `boss`

* Make sure that all users have to reset their password the next time they log in

* Create the following groups
    * `admin`
    * `developer`
    * `auditor`

* Add the users to the following groups
    * `admin`
      * `tony`
      * `sarah`

    * `developer`
      * `bob`
      * `tony`
      * `sarah`
      * `jenny`

    * `auditor`
      * `toto`
    
    * `sudo`
      * `boss`

* Create a directory in the `/share` directory for each group and ensure that only users in that group can access that directory

* Create a directory in `/share` that the `admin` and `developer` groups can access but **not** the `auditor` group

* Create a directory in `/share` that `tony`, `sarah` and `toto` can access but **no one** else

* Create a directory called `/share/legal` that only the `auditor` group can edit files but that all other groups can view the files

* Make sure that each created user has the following directory structures in their home directories:
    * .ssh (user read/write/executable permissions)
      - generate an SSH key pair for each user in their directory
      - authorized_keys (user read/write permissions)

    * mysupersecret.txt (user read/write permissions)

    * mypublicsecret.txt (user read/write permissions, read for everyone)

* Make sure that each users home directory are **only** accessible by them

* Add 3 secret hidden files somewhere on the file system :
    * 1 that has the setid bit set (owned by root)
    * 1 that has the setuid and setgid bit set (owned by root)
    * 1 that has a flag in it with the following format: flag{sometexthere} (owned by any user)

****
### Patch Management
* Make sure your operating system has all the latest security patches for installed software

****
### Firewall
* Ensure that you have enabled a firewall on the system

****
### SSH Hardening
* Enable and harden SSH in the following ways:
    * Change default port
    * Disable root login
    * Don't allow any SSH password logins

****

### Removal of unused/potentially abused tools and services
* Make sure the following programs are removed:
    * ftp
    * netcat

****
#### Resources
* [https://www.networkworld.com/article/2726217/endpoint-protection/how-to-enforce-password-complexity-on-linux.html]()