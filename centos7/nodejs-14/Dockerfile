FROM centos:7

MAINTAINER adrienv1520 (adrienvalcke@icloud.com)

RUN (curl -fsSL https://rpm.nodesource.com/setup_14.x | bash -) \
  && yum clean all -y \
  && yum update -y \
  && yum install -y nodejs \
  && yum groupinstall -y "Development Tools" \
  && yum install -y libtool autoconf automake wget gettext which python3 \
  && yum reinstall -y kernel-core-4.18.0-193.28.1.el7.aarch64 2>/dev/null \
  ; yum autoremove -y \
  && yum clean all -y \
  && npm install npm --global
