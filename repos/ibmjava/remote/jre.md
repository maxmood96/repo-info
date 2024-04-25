## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:16b05236ec0fe54b6dc8fd989aa5720d5d0a41ad37d7fab639fd1bcbbc74dfab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:1f0fff4fadd9c6546366f096a3246620345a25072ce00e8881e8ce2c555c54e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166882895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54d9e03881a580baf2a20e8139374319c806062ef3f401d002de8750292e3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 06:34:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 16 Apr 2024 06:34:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:34:31 GMT
ENV JAVA_VERSION=8.0.8.21
# Tue, 16 Apr 2024 06:35:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a381d174001bbc558c8911b952c30c2a4fe6dea78a9ff6a25a2db9ac5e7fd952';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7e1ee0174aea6cd2a41a561beb4e9b61b7b1d73bc3b8bf68a7d47c2f6ba7e555';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='80aed9b6510c2cdc2484435d44d7a50fb744ce4f2ae673fa090eddb222cf66fc';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e7f5d2623a6932095deb2320b3eaa8fd70cf4131653113eb7ff950e276af1cfb';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Tue, 16 Apr 2024 06:35:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dd05ee810a78053e6c2291e4a2022e0022a992e91619f69ce2c91a4894bb1f`  
		Last Modified: Tue, 16 Apr 2024 06:37:01 GMT  
		Size: 1.5 MB (1469699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64933aeed68ec0eb833ffad316192d0ff0be882718e32b83b6d1fafd7188705a`  
		Last Modified: Tue, 16 Apr 2024 06:37:10 GMT  
		Size: 135.0 MB (134973418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:b990146082e211760f9ac4704af7f797cc81a74d28c6113eeb2b03626101ca0b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172578431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf0d35aa15c623ac23c79a12886f609d14b740f11b662b4c061d72320200be3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:51:23 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:51:27 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Wed, 17 Apr 2024 17:51:27 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 20:39:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 25 Apr 2024 20:39:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 20:39:55 GMT
ENV JAVA_VERSION=8.0.8.21
# Thu, 25 Apr 2024 20:40:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a381d174001bbc558c8911b952c30c2a4fe6dea78a9ff6a25a2db9ac5e7fd952';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7e1ee0174aea6cd2a41a561beb4e9b61b7b1d73bc3b8bf68a7d47c2f6ba7e555';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='80aed9b6510c2cdc2484435d44d7a50fb744ce4f2ae673fa090eddb222cf66fc';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e7f5d2623a6932095deb2320b3eaa8fd70cf4131653113eb7ff950e276af1cfb';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Thu, 25 Apr 2024 20:40:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a9466735f8829921e05503ca4d4d92bb6f06facd77aa4b2feb86645d7c27b1ba`  
		Last Modified: Thu, 25 Apr 2024 20:35:05 GMT  
		Size: 35.6 MB (35588305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1237c9d276ff8da25f3202c30bf0b3bc184f62553cdeb8ff720cfb523780fe3f`  
		Last Modified: Thu, 25 Apr 2024 20:40:58 GMT  
		Size: 1.6 MB (1574868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589cec98a41a8b753231317ab1a31bba0bfd8bb839b4821f9af7136b37debc8`  
		Last Modified: Thu, 25 Apr 2024 20:41:09 GMT  
		Size: 135.4 MB (135415258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:bdde1043463f8430a8ed77476271204c54c6aedfdfab696f6c1d5a8288580dca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162070693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8a4753f05aa7fd537cd11432acdb5238267817a5c31eb2b2120e4089614510`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:42:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:42:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:42:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:42:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:42:34 GMT
ADD file:f721f8e69988c4a423ddfb143b1001213ba52ffe029e8623c2f62e210d611fbc in / 
# Wed, 17 Apr 2024 18:42:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:01:41 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 25 Apr 2024 21:01:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:01:58 GMT
ENV JAVA_VERSION=8.0.8.21
# Thu, 25 Apr 2024 21:02:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a381d174001bbc558c8911b952c30c2a4fe6dea78a9ff6a25a2db9ac5e7fd952';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7e1ee0174aea6cd2a41a561beb4e9b61b7b1d73bc3b8bf68a7d47c2f6ba7e555';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='80aed9b6510c2cdc2484435d44d7a50fb744ce4f2ae673fa090eddb222cf66fc';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='e7f5d2623a6932095deb2320b3eaa8fd70cf4131653113eb7ff950e276af1cfb';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Thu, 25 Apr 2024 21:02:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a9e3c76851ed4cb17ff69f864b6230094c69b50fc344074f5cccf18cabee6dbf`  
		Last Modified: Thu, 25 Apr 2024 20:58:17 GMT  
		Size: 28.6 MB (28637471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb724c0ee7f1c025722daf9f246fc7c1302d7dafbd952205d1077ec2e1c7de`  
		Last Modified: Thu, 25 Apr 2024 21:04:54 GMT  
		Size: 1.5 MB (1477703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d090dfb3329dbb03231384e0aeb9a8056fe210f47146a413334828634a4ba0`  
		Last Modified: Thu, 25 Apr 2024 21:05:04 GMT  
		Size: 132.0 MB (131955519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
