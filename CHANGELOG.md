# CHANGELOG

## 1.0.2 - delivery @14/06/2021

- add `;` in docker files after `yum reinstall -y kernel-core-4.18.0-193.28.1.el7.aarch64 2>/dev/null` so what comes next is always chained whatever the result of the command

## 1.0.1 - delivery @14/06/2021

- add `yum reinstall -y kernel-core-4.18.0-193.28.1.el7.aarch64 2>/dev/null` to support `arm64` builds
- add documentation regarding multi architecture builds

## 1.0.0 - delivery @13/06/2021

- first delivery
- target x86 builds only but can fix yum autoremove for arm64 in centos 7 by adding `yum reinstall -y kernel-core-4.18.0-193.28.1.el7.aarch64` wich will not be listed as dependency to remove
