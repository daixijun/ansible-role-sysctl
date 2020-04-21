# daixijun.sysctl

[![Build Status](https://github.com/daixijun/ansible-role-sysctl/workflows/build/badge.svg)](https://github.com/daixijun/ansible-role-sysctl/actions)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-daixijun.sysctl-660198.svg?style=flat)](https://galaxy.ansible.com/daixijun/ansible-role-sysctl/)
[![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/daixijun/ansible-role-sysctl?sort=semver)](https://github.com/daixijun/ansible-role-sysctl/tags)

系统内核优化，默认内核配置内容参考[sysctl_commons](./defaults/main.yml)

## 环境要求

- RHEL/CentOS 6 及以上版本
- ansible 2.7 及以上版本

## 变量

```yaml
# 需要修改的配置项
sysctl_items: {}
  # net.ipv4.ip_forward:
  #   value: 1
```

## 依赖

无

## 使用示例

```yaml
- hosts: servers
  roles:
    - role: daixijun.sysctl
      sysctl_items:
        net.ipv4.ip_forward:
          value: 1
```

## License

BSD

## 维护者

- Xijun Dai <daixijun1990@gmail.com>
