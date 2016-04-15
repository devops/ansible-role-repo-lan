# Ansible Role: repo-lan

Configure a LAN Repo for RedHat/CentOS.

## Requirements

None.

## Role Variables

`defaults/main.yml`

* `repo_lan_baseurl: http://mirrors.aliyun.com/centos/7.1.1503/os/x86_64/`
* `repo_lan_repos:`
    ```
      - { name: "base", baseurl: "http://mirrors.ustc.edu.cn/centos/7/os/x86_64/" }
    ```
* `repo_lan_backup: yes`

## Dependencies

None.

## Example Playbook

    - name: Configure Repo.
      hosts: servers
      roles:
        - role: ansible-role-repo-lan
          repo_lan_repos:
            - { name: "base", baseurl:  "http://mirrors.ustc.edu.cn/centos/7/os/x86_64/" }
            - { name: "extras", baseurl: "http://mirrors.ustc.edu.cn/centos/7/extras/x86_64/" }

## License

MIT / BSD

## Author Information

z
