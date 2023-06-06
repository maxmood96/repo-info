## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:9a59bfdb7a69c4ec510465dd68a22b0033aced93b3161bbb42dfd4ba7b40ca64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:b12dc1a1d9c64dc8b7fc3748ccd44c15f95322c33c956bc13770f43e634125c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101238239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a07ec6eaaa2996ee6f3bf36f59b8f339d9b1c3f4d0c2a41181a439801d1452`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:03:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Jun 2023 01:03:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Jun 2023 22:19:43 GMT
ENV JAVA_VERSION=8.0.8.5
# Tue, 06 Jun 2023 22:21:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5f03c22c39ef4d70836921da7993378ae0c2aab2f0b3b278f6b31cfc6177c816';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40362ca241d3597ba7177c84c61fd8b3a6e424602fece0788badd30ca186cfdb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3b4778739116009174a860c075a5e08a16a403abead3b0af7b420631219d0f0c';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='489e72d5c9f93b6db6653b5246f3c08999dc53dcf11c8210ab9783b062a728e4';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Jun 2023 22:21:33 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db07816b3aab4d393ea40ce80939a39026f25e04db32332ddbf7503eb707995`  
		Last Modified: Fri, 02 Jun 2023 01:07:16 GMT  
		Size: 1.5 MB (1468716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11377baee3ba9f41750334baad3afe39a119ec48104b03063c1a965475ca118d`  
		Last Modified: Tue, 06 Jun 2023 22:23:38 GMT  
		Size: 69.3 MB (69339248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:00785ab2717b98279deb048bab125ddb26d7d11d076af599baa7644cefedb732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (106968724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccc79d6a1b5ccc42123d922be07daade02709e3360d35b5579b6bd25c2f2b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:39:12 GMT
ARG RELEASE
# Mon, 22 May 2023 17:39:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:39:16 GMT
ADD file:5b5967ce188eac9717526ca9f6cf6679cbae6ee4b17b207cc3d640c78d9a9788 in / 
# Mon, 22 May 2023 17:39:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:42:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Jun 2023 00:42:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Jun 2023 22:16:33 GMT
ENV JAVA_VERSION=8.0.8.5
# Tue, 06 Jun 2023 22:21:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5f03c22c39ef4d70836921da7993378ae0c2aab2f0b3b278f6b31cfc6177c816';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40362ca241d3597ba7177c84c61fd8b3a6e424602fece0788badd30ca186cfdb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3b4778739116009174a860c075a5e08a16a403abead3b0af7b420631219d0f0c';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='489e72d5c9f93b6db6653b5246f3c08999dc53dcf11c8210ab9783b062a728e4';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Jun 2023 22:21:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e39d2517f3d915af1b821fe306b14eba12466c4cae87efe57eaa0b749503166e`  
		Last Modified: Thu, 01 Jun 2023 23:48:51 GMT  
		Size: 35.7 MB (35712704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6f4fea813cd170474c7af294c8efaf91f3ef2901fe2005f9c7f0ad10a868d5`  
		Last Modified: Fri, 02 Jun 2023 00:50:16 GMT  
		Size: 1.6 MB (1576257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ea59b865d0008a1cf010b2c093f678de19388f23626187d0abb60938db1281`  
		Last Modified: Tue, 06 Jun 2023 22:25:34 GMT  
		Size: 69.7 MB (69679763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:8edb50bdda4417dd251ade7b314eca4ba926eb9ee3abfc2b2342b8ce71382c5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100033748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c1739ff4ecbddc9a619930cef0394c422a68a2a65b4253ff93eb106634d546`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:46:45 GMT
ARG RELEASE
# Mon, 22 May 2023 17:46:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:46:47 GMT
ADD file:7bf1b7a1484e37f289d40f5c1c1cbe321ef337f898dd3d5809193c848a9a3dc2 in / 
# Mon, 22 May 2023 17:46:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 14:39:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Jun 2023 14:39:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Jun 2023 22:44:26 GMT
ENV JAVA_VERSION=8.0.8.5
# Tue, 06 Jun 2023 22:47:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5f03c22c39ef4d70836921da7993378ae0c2aab2f0b3b278f6b31cfc6177c816';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40362ca241d3597ba7177c84c61fd8b3a6e424602fece0788badd30ca186cfdb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3b4778739116009174a860c075a5e08a16a403abead3b0af7b420631219d0f0c';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='489e72d5c9f93b6db6653b5246f3c08999dc53dcf11c8210ab9783b062a728e4';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Jun 2023 22:47:33 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f2957179c3a13374d05630725d1d996f8083efadf7d2da999c9b4ca53ab7c98f`  
		Last Modified: Thu, 01 Jun 2023 23:19:06 GMT  
		Size: 28.6 MB (28648005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc2efbbc357d3180a9037577b3e9ef5404409073cff3477f88ad10630fec864`  
		Last Modified: Fri, 02 Jun 2023 14:46:59 GMT  
		Size: 1.5 MB (1476762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97befa971d7f6b39dfd4e4bd8a47a13e524cf179eae4b63afcd0a71558fe6b29`  
		Last Modified: Tue, 06 Jun 2023 22:53:01 GMT  
		Size: 69.9 MB (69908981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
