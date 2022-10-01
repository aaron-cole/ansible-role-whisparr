# ansible-role-whisparr

=========

Ansible Role to install whisparr, an automated downloader, watchlist, monitoring program for adult movies.

Requirements
------------

Minimum Ansible version required is Ansible 2.9

Role Variables
--------------
Role variables have good defined defaults, which are located in `defaults/main.yml`.
Current version includes the following variables with default values:

### Defaults
| Name               | Default Value | Description                  |
|--------------------|---------------|------------------------------|
| `whisparr_user`       | whisparr | The primary user to run whisparr  |
| `whisparr_uid`        | *optional* | Commented out by default |
| `whisparr_group`      | media | The primary group for `whisparr_user` |
| `whisparr_group_gid`  | *optional* | Commented out by default |
| `whisparr_base_install_dir` | /opt | Base Install directory for whisparr |
| `whisparr_config_dir` |  /opt/data/whisparr | Data directory to store configuration |
| `whisparr_download_url` | https://whisparr.servarr.com/v1/update/nightly/updatefile?os=linux&runtime=netcore&arch=x64 | Link to the latest release |
| `whisparr_port` | 6969 | Port in which whisparr operates on, to add to Firewalld |
| `whisparr_packages` |   ```- curl```  ```- sqlite``` | List of Packages Required to install and run whisparr |

Dependencies
------------

None

Example Playbook
----------------

   - hosts: whisparr_servers
      roles:
        - aaron-cole.ansible_role_whisparr


License
-------

GPLv3

Author Information
------------------

Created by Aaron Cole


