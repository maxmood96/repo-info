## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:d712c39469d11e80c97806609a6a72b3e98fe5545056364b5ef3426696ba5f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:ffb662a75277faba3442b7726cb2f8cfc6f6c1b1d19e81993a16ed02684338ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101253900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39b37b344d542f3242fc4c5a99dd37296cc67b8b5eff9efa918a38f747044d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Thu, 17 Aug 2023 06:43:31 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 17 Aug 2023 06:43:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 06:43:41 GMT
ENV JAVA_VERSION=8.0.8.6
# Thu, 17 Aug 2023 06:45:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d795b429c31b76e28e96848ad66a2749314c498a2c744f41d1fa7bf032ccc495';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75f234bd86768a7cd4aa0cf6b62f88f62f79a9d0455c3e49adf97cf363391170';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3d2eceb6ff09b2663c312f0c11955372198cfd85dc693c4188875300aefae6ac';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='9e7f8f163eddd1d8c7781a11bc7e6a2d428063ac1d3054184227b172d95cef56';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 17 Aug 2023 06:45:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d80cb2eef8352f8d51cee0579d0d7e53c9b3089f0aedb190b60897ae6b2e9c9`  
		Last Modified: Thu, 17 Aug 2023 06:47:15 GMT  
		Size: 1.5 MB (1469099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59e262fddbaeb9e51273183024c1010faf6f79ccc781e22caa21bd8e07605b3`  
		Last Modified: Thu, 17 Aug 2023 06:47:45 GMT  
		Size: 69.3 MB (69346841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:72e696e9b518d59f583cbceeabe021036f707d3fb601a8b4c2aa552eebc8c631
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (106974319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c36241c7d7585eed0b09727d09995f376d0df3f5268526d0529e5c713f1872`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 00:34:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 05 Jul 2023 00:34:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 00:34:51 GMT
ENV JAVA_VERSION=8.0.8.6
# Wed, 05 Jul 2023 00:40:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d795b429c31b76e28e96848ad66a2749314c498a2c744f41d1fa7bf032ccc495';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75f234bd86768a7cd4aa0cf6b62f88f62f79a9d0455c3e49adf97cf363391170';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3d2eceb6ff09b2663c312f0c11955372198cfd85dc693c4188875300aefae6ac';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='9e7f8f163eddd1d8c7781a11bc7e6a2d428063ac1d3054184227b172d95cef56';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Jul 2023 00:40:47 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536d286660db27a2dfe5334aaf1b48fcb9672ab1c6c043ae843eb0b98fa0524d`  
		Last Modified: Wed, 05 Jul 2023 00:44:32 GMT  
		Size: 1.6 MB (1576543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081a7ece352e38a70c9a9b931906fbf67b251fc6a303bf302beb0572decd5b8a`  
		Last Modified: Wed, 05 Jul 2023 00:45:16 GMT  
		Size: 69.7 MB (69686307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:68c8c035f96278e43decdbeca3c94184fa4de9fc9d113d051b453d8e04270751
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100040799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf64c1c81cbb290ee8f819ff3625f7633e85d6ae34033cc4bbe7ffaa477782e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:16 GMT
ADD file:d5b5687c046ca0689ccc4f42ddcc27543404ae2273aa12241e6636a2b3d675df in / 
# Fri, 04 Aug 2023 05:03:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 09:47:06 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 16 Aug 2023 09:47:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 09:47:12 GMT
ENV JAVA_VERSION=8.0.8.6
# Wed, 16 Aug 2023 09:49:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d795b429c31b76e28e96848ad66a2749314c498a2c744f41d1fa7bf032ccc495';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75f234bd86768a7cd4aa0cf6b62f88f62f79a9d0455c3e49adf97cf363391170';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3d2eceb6ff09b2663c312f0c11955372198cfd85dc693c4188875300aefae6ac';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='9e7f8f163eddd1d8c7781a11bc7e6a2d428063ac1d3054184227b172d95cef56';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 16 Aug 2023 09:49:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:de1d106061fc0332ca262e39ed7d2aa6384ae341a084b39449e21c742802df9c`  
		Last Modified: Wed, 16 Aug 2023 04:39:02 GMT  
		Size: 28.6 MB (28644373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481198287db5a00cd86f00bf03a07297476d96af9492766f7515b515bd7486fa`  
		Last Modified: Wed, 16 Aug 2023 09:51:24 GMT  
		Size: 1.5 MB (1477116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e85f829f8c8235a499842044e6828bbdc33f03cc6f44177597050d9bff68dd`  
		Last Modified: Wed, 16 Aug 2023 09:51:48 GMT  
		Size: 69.9 MB (69919310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
