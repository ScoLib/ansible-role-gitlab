Ansible Role: GitLab
=========

Install GitLab 

Requirements
------------

None

Role Variables
--------------

```
gitlabVer: "v12.6.2"
gitlabRunnerVer: "alpine-v12.6.0"
gitlabShellVer: "v10.3.0"
kubectlVer: "1.13.12"
exporterVer: "5.1.0"
certificatesVer: "20171114-r3"

# 离线镜像tar包
gitlab_ee_offline: "gitlab_ee_{{ gitlabVer }}.tar"
gitlab_shell_offline: "gitlab_shell_{{ gitlabShellVer }}.tar"
gitlab_kubectl_offline: "gitlab_kubectl_{{ kubectlVer }}.tar"
gitlab_exporter_offline: "gitlab_exporter_{{ exporterVer }}.tar"
gitlab_certificates_offline: "gitlab_certificates_{{ certificatesVer }}.tar"
gitlab_runner_offline: "gitlab_runner_{{ gitlabRunnerVer }}.tar"
gitlab_gitaly_offline: "gitlab_gitaly_latest.tar"


docker_bin: "/opt/kube/bin/docker"
helm_bin: "/opt/kube/bin/helm"

base_dir: "/etc/ansible"

helm_set: ""
```



Dependencies
------------

- Docker
- Helm V3

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: gitlab }

License
-------

MIT

Author Information
------------------

Created by [klgd](https://github.com/klgd)