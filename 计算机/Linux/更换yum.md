---
title: 更换yum
updated: 2024-11-20T03:30:13
created: 2024-11-20T03:28:13
---

更换yum
2024年11月20日
3:28

cd /etc/yum.repos.d/
mkdir repo_bak
mv \*.repo repo_bak/
wget <http://mirrors.aliyun.com/repo/Centos-7.repo>
yum clean all
yum makecache
yum list | grep epel-release
yum install -y epel-release
wget -O /etc/yum.repos.d/epel-7.repo <http://mirrors.aliyun.com/repo/epel-7.repo>
yum clean all
yum makecache

**

