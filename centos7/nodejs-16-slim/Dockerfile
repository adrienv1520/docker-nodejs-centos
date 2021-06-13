FROM centos:7

MAINTAINER adrienv1520 (adrienvalcke@icloud.com)

RUN (curl -fsSL https://rpm.nodesource.com/setup_16.x | bash -) \
  && yum clean all -y \
  && yum update -y \
  && yum install -y nodejs \
  && yum autoremove -y \
  && yum clean all -y \
  && npm install npm --global
