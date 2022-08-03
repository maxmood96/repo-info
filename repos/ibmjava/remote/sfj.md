## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:17fea063a15a7ba83cdd7ce668d3a39b6060f51a16fc1d745690b6a1fd8d12ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:f1be0da02b2c973016ba78c06cbec1706f22c487ddbaefa9c2671b573d1ed81e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94532625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af6074e5cbdc5fc21a3181c8ea3c5747be67e9fe20c36de640152e4f703473a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:09:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 20:10:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:10:01 GMT
ENV JAVA_VERSION=8.0.7.11
# Tue, 02 Aug 2022 20:11:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='68d93db98bfde238b8a53089a2e89eb9927ae7a46dc2a20e41a1655e882ebe18';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='5732b958332885e1bea39105018ac23297bc871ba78c29ce92b208ed87967b17';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c3f53130efb66f541aa0492c471187176d2eb5cbb6aa12ae8ddbdc818de28e9a';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e06fe432da13c9e5fd082f9d16f59d7d7f0198a819393f392bc9b1f08050fb20';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3e3a577a8322001d73fde8144f7a7a9400f73bc0e709f8057ece0432386143b1';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 02 Aug 2022 20:11:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6715a1bb89fcf5e91403be2bc6130f23e6b3cfd0da73e6b09e937d028409d3`  
		Last Modified: Tue, 02 Aug 2022 20:13:24 GMT  
		Size: 3.0 MB (2957815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0506387839b0c98f93d2a0bb7bc8edfa104c7dae17aea02db93c40b4410d1d`  
		Last Modified: Tue, 02 Aug 2022 20:13:55 GMT  
		Size: 64.9 MB (64864540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:cfab585f99f61e322ebfa0b03e392659526b24402e24f674193b96ce3be3b398
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94402024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756f57c832853ebea518c8a46ac78ef880199834f8f4438b6681abc1e99c98f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:55 GMT
ADD file:6d22c6318075d01068d0a9213f33655abf6c251f8a71d98c17b857b9021b43bd in / 
# Tue, 02 Aug 2022 00:50:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:23:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 16:23:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:23:28 GMT
ENV JAVA_VERSION=8.0.7.11
# Tue, 02 Aug 2022 16:25:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='68d93db98bfde238b8a53089a2e89eb9927ae7a46dc2a20e41a1655e882ebe18';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='5732b958332885e1bea39105018ac23297bc871ba78c29ce92b208ed87967b17';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c3f53130efb66f541aa0492c471187176d2eb5cbb6aa12ae8ddbdc818de28e9a';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e06fe432da13c9e5fd082f9d16f59d7d7f0198a819393f392bc9b1f08050fb20';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3e3a577a8322001d73fde8144f7a7a9400f73bc0e709f8057ece0432386143b1';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 02 Aug 2022 16:25:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:5496b4c91dece81ce997c62cf2e1ef6f1764e612c6e8f0b385722c6645e4ad30`  
		Last Modified: Tue, 02 Aug 2022 00:51:39 GMT  
		Size: 27.2 MB (27164268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0dd584134d885dc07df56cb1531c30c56e50d96a7cc1cb92c61c41813d18e0`  
		Last Modified: Tue, 02 Aug 2022 16:27:10 GMT  
		Size: 3.0 MB (2983285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8f33dd275115477b5029186dfdd39c3bd9b1d7d028d5b18a9bd57963e3895b`  
		Last Modified: Tue, 02 Aug 2022 16:27:51 GMT  
		Size: 64.3 MB (64254471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:04f67d0bae589450460500d5a5302f3115b3c95cc47dca0f1e325b7d5f56e5dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98523030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8deae41e620e0f9335ef3a2da317bb92a72c949e145699d158ffff5ded1cf04`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 03:44:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 03 Aug 2022 03:44:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 03:44:53 GMT
ENV JAVA_VERSION=8.0.7.11
# Wed, 03 Aug 2022 03:49:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='68d93db98bfde238b8a53089a2e89eb9927ae7a46dc2a20e41a1655e882ebe18';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='5732b958332885e1bea39105018ac23297bc871ba78c29ce92b208ed87967b17';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c3f53130efb66f541aa0492c471187176d2eb5cbb6aa12ae8ddbdc818de28e9a';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e06fe432da13c9e5fd082f9d16f59d7d7f0198a819393f392bc9b1f08050fb20';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3e3a577a8322001d73fde8144f7a7a9400f73bc0e709f8057ece0432386143b1';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 03 Aug 2022 03:49:17 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99970d1735353adabddaef52faa1237908c9cdf39198088cf543cb21ecb3fa69`  
		Last Modified: Wed, 03 Aug 2022 03:52:54 GMT  
		Size: 3.1 MB (3075943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d9610565ff84cd816561ec2bf5b2d7ae08711f00d96b60245c911cfb0641c0`  
		Last Modified: Wed, 03 Aug 2022 03:53:37 GMT  
		Size: 65.0 MB (65005617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:13ea274de2a8ab0eff9e2af257249057b60ddeb4125a0234771763e542677d02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93964502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb80f98c987f43ffa1aaa4e6ae721fb27e1b455d827d43bd5860273b33ff54e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:01:57 GMT
ADD file:3d2e9b401524527b395347bc3847be7c9cb465b9a214a1a1d31e74330e293c45 in / 
# Tue, 02 Aug 2022 01:01:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:19:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 13:19:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:19:25 GMT
ENV JAVA_VERSION=8.0.7.11
# Tue, 02 Aug 2022 13:21:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='68d93db98bfde238b8a53089a2e89eb9927ae7a46dc2a20e41a1655e882ebe18';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='5732b958332885e1bea39105018ac23297bc871ba78c29ce92b208ed87967b17';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c3f53130efb66f541aa0492c471187176d2eb5cbb6aa12ae8ddbdc818de28e9a';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e06fe432da13c9e5fd082f9d16f59d7d7f0198a819393f392bc9b1f08050fb20';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3e3a577a8322001d73fde8144f7a7a9400f73bc0e709f8057ece0432386143b1';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 02 Aug 2022 13:21:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be3ed498266c519f84268ff1f02085fa249c0e32fb60a59466e24c862b5f094b`  
		Last Modified: Tue, 02 Aug 2022 01:03:25 GMT  
		Size: 25.4 MB (25369584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ed0adcefe11b30e3dff027bcb1cb9fe759f39f50b008bafb3644d3d2fcba8`  
		Last Modified: Tue, 02 Aug 2022 13:22:41 GMT  
		Size: 2.7 MB (2671706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a08b2fa3615a60e5ad800d32866fa0f1bf8d14981a6a3b0c820b723e6ae21ae`  
		Last Modified: Tue, 02 Aug 2022 13:23:04 GMT  
		Size: 65.9 MB (65923212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
