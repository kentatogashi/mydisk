# mydisk

## centos7 kickstart config
```sh
#version=RHEL7

cmdline
install
url --url=ftp://example.com/centos/7/os/x86_64/

lang en_US.UTF-8
keyboard --vckeymap=jp106 --xlayouts=jp
timezone Asia/Tokyo --isUtc --nontp

network --bootproto=dhcp --ipv6=auto --activate --hostname=unknown

#rootpw --plaintext password
rootpw --iscrypted $1$2c5VfLZS$WKO3i5/aJrKMDe9fudZ/p0

zerombr
bootloader --location=mbr

```
