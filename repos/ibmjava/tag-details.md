<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ibmjava`

-	[`ibmjava:8`](#ibmjava8)
-	[`ibmjava:8-jre`](#ibmjava8-jre)
-	[`ibmjava:8-sdk`](#ibmjava8-sdk)
-	[`ibmjava:8-sfj`](#ibmjava8-sfj)
-	[`ibmjava:jre`](#ibmjavajre)
-	[`ibmjava:latest`](#ibmjavalatest)
-	[`ibmjava:sdk`](#ibmjavasdk)
-	[`ibmjava:sfj`](#ibmjavasfj)

## `ibmjava:8`

```console
$ docker pull ibmjava@sha256:65c6d8dc6142e41613bd11a2c98116fa316945f11193879ccc7c8bad29910b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:31c6cce656c7e8f8e452112b393c9f6f1a9ba249ab61328d78d59cde6645edb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165752327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a992dbde4f54fb71e3f2f14da67901c4e97729803dd3fa654c9ff3f27abf38e`
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
# Fri, 02 Jun 2023 01:03:45 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 01:04:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 01:04:44 GMT
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
	-	`sha256:060ad4d2c434c002e4380df3db7baa322a92ab810729556c82fffdfefc8182d0`  
		Last Modified: Fri, 02 Jun 2023 01:07:25 GMT  
		Size: 133.9 MB (133853336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:abc7efe7899afcd66f54579192b33701976a32ef9c735d5184cd518494836a12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0cc550973d6f28c3f44e9012b319ee5cc2db56095947fd57b9a50587f3ac0d`
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
# Fri, 02 Jun 2023 00:42:21 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 00:44:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 00:44:51 GMT
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
	-	`sha256:04c9d356bbc6d8e3b217e7967abd09ac74f3489f6be5b5138ff24edd20a17ebb`  
		Last Modified: Fri, 02 Jun 2023 00:50:32 GMT  
		Size: 133.6 MB (133555947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:9e6cd0c4cdea2701c5e56bfd06052ec75f9d1f801ad66e7f53b74213e36d33f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160756394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3726b9e3624cd26699c2b609d0d0f0e9c831289ab538f33c6eeabb41725517`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:44:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 08:44:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:44:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 08:45:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 08:45:49 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:78722793f0008ff8422830a0106f21e8bc168fb9aac12cc99fb223799951759e`  
		Last Modified: Wed, 03 May 2023 22:33:36 GMT  
		Size: 28.6 MB (28647905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9459c54d841fa6f6b374fa6fe3230943f4104eb1c43155f1255ff1c9e735443`  
		Last Modified: Thu, 04 May 2023 08:48:50 GMT  
		Size: 1.5 MB (1452439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f1a3330c7bf0b93483213fd37e7f563f9c48a90f30d9ec27d5b01cf032a5af`  
		Last Modified: Thu, 04 May 2023 08:48:59 GMT  
		Size: 130.7 MB (130656050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:65c6d8dc6142e41613bd11a2c98116fa316945f11193879ccc7c8bad29910b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:31c6cce656c7e8f8e452112b393c9f6f1a9ba249ab61328d78d59cde6645edb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165752327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a992dbde4f54fb71e3f2f14da67901c4e97729803dd3fa654c9ff3f27abf38e`
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
# Fri, 02 Jun 2023 01:03:45 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 01:04:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 01:04:44 GMT
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
	-	`sha256:060ad4d2c434c002e4380df3db7baa322a92ab810729556c82fffdfefc8182d0`  
		Last Modified: Fri, 02 Jun 2023 01:07:25 GMT  
		Size: 133.9 MB (133853336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:abc7efe7899afcd66f54579192b33701976a32ef9c735d5184cd518494836a12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0cc550973d6f28c3f44e9012b319ee5cc2db56095947fd57b9a50587f3ac0d`
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
# Fri, 02 Jun 2023 00:42:21 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 00:44:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 00:44:51 GMT
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
	-	`sha256:04c9d356bbc6d8e3b217e7967abd09ac74f3489f6be5b5138ff24edd20a17ebb`  
		Last Modified: Fri, 02 Jun 2023 00:50:32 GMT  
		Size: 133.6 MB (133555947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:9e6cd0c4cdea2701c5e56bfd06052ec75f9d1f801ad66e7f53b74213e36d33f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160756394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3726b9e3624cd26699c2b609d0d0f0e9c831289ab538f33c6eeabb41725517`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:44:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 08:44:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:44:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 08:45:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 08:45:49 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:78722793f0008ff8422830a0106f21e8bc168fb9aac12cc99fb223799951759e`  
		Last Modified: Wed, 03 May 2023 22:33:36 GMT  
		Size: 28.6 MB (28647905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9459c54d841fa6f6b374fa6fe3230943f4104eb1c43155f1255ff1c9e735443`  
		Last Modified: Thu, 04 May 2023 08:48:50 GMT  
		Size: 1.5 MB (1452439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f1a3330c7bf0b93483213fd37e7f563f9c48a90f30d9ec27d5b01cf032a5af`  
		Last Modified: Thu, 04 May 2023 08:48:59 GMT  
		Size: 130.7 MB (130656050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:5d03d0359244f02a27e35451d9690830ba8847edaf5275a289c6df97ad66a796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:24e3878e912fef5ee5917498cd05eb41910fb7d22c8b17a588599b14fae11dac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202902135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4fcf418f9b1638c12795ea7075784fdc7bda199fd2463f30d331b45b73c361`
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
# Fri, 02 Jun 2023 01:03:45 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 01:06:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a1dfef941fc2e43fcd8143960d2c3a82e283695eff893923cb05c226bcdd0a0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5a3d2ef0ad3687b34e1df3854b45d2e00a034724fe70a0e5bf14b2eebca1fe9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f361174227db6e6e1b067b8085549fd2f7ba63a73752a2db7be260e438ef39eb';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='974c339555e219ea93198316f6a33ee8243481e568a730d68b467c79f7caa5bc';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 01:06:56 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:7fb50ccd6b8bf20b7e441e078623ad18278a8eecc9ad3f0cee157bd88f8a4c97`  
		Last Modified: Fri, 02 Jun 2023 01:08:00 GMT  
		Size: 171.0 MB (171003144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:219645c3a69340ee6824d03fc4fb9cfcd1ce08714aff2643aaea7a88cf07004a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208127326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780b997db9350af0750e5fad0a33adaf5171b6c697177ad7989229a66868c074`
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
# Fri, 02 Jun 2023 00:42:21 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 00:49:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a1dfef941fc2e43fcd8143960d2c3a82e283695eff893923cb05c226bcdd0a0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5a3d2ef0ad3687b34e1df3854b45d2e00a034724fe70a0e5bf14b2eebca1fe9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f361174227db6e6e1b067b8085549fd2f7ba63a73752a2db7be260e438ef39eb';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='974c339555e219ea93198316f6a33ee8243481e568a730d68b467c79f7caa5bc';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 00:49:46 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:66c4067630032554977fbfae179ff7a5954ab7694f1ac475eb5e32bba070262f`  
		Last Modified: Fri, 02 Jun 2023 00:51:25 GMT  
		Size: 170.8 MB (170838365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:3984863e5b0159fb3ba0ff7817898a37c8828c24a8f17174d515e9cbb46f2402
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191054927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30122011018027b7603fd79ac1603d1399a1d88acf6944a5587335ce4ba7a6f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:44:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 08:44:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:44:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 08:48:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a1dfef941fc2e43fcd8143960d2c3a82e283695eff893923cb05c226bcdd0a0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5a3d2ef0ad3687b34e1df3854b45d2e00a034724fe70a0e5bf14b2eebca1fe9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f361174227db6e6e1b067b8085549fd2f7ba63a73752a2db7be260e438ef39eb';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='974c339555e219ea93198316f6a33ee8243481e568a730d68b467c79f7caa5bc';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 08:48:21 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:78722793f0008ff8422830a0106f21e8bc168fb9aac12cc99fb223799951759e`  
		Last Modified: Wed, 03 May 2023 22:33:36 GMT  
		Size: 28.6 MB (28647905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9459c54d841fa6f6b374fa6fe3230943f4104eb1c43155f1255ff1c9e735443`  
		Last Modified: Thu, 04 May 2023 08:48:50 GMT  
		Size: 1.5 MB (1452439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec537f63976b3afc1a38ef002078bd6db8ec68729ad89795f237dab27ed975bc`  
		Last Modified: Thu, 04 May 2023 08:49:28 GMT  
		Size: 161.0 MB (160954583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:5a547449d6bb9527dc9042a34480cd3a0173fb7227e5e5d9c821db5c8417fcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:9819342e50417e768d5d1be0bd09db065ebfbb8170e2e7e2046dc347c6cb13b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101138578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bede7e30780f33e6d1e7548e2b9a8d94f0e7201939385b3aa03f26252c8fe8`
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
# Fri, 02 Jun 2023 01:03:45 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 01:05:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='83aa5cbbf7706def8564c57e92afe8cbd76bfe8af58e03f50cbe4154e9feecc7';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cef1f4a87e4dcd97fb8e99f2c2ddcf18c90b7712e3cb65a561ee3e0013052dd8';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='26833e7defe3fc1705d0068f530bbedbe0d9a12c38db8c4bc0837b595827a62e';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='85ab8a83e67d515a48638c58d9e4931ceecafb6f05e2c9f02cf8d9ff4dbfc116';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 01:05:38 GMT
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
	-	`sha256:20482074d738da9d09cf3cc8c31260ec76842807a7ac5d7c7d104494713be260`  
		Last Modified: Fri, 02 Jun 2023 01:07:41 GMT  
		Size: 69.2 MB (69239587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:eb0ed9515b6974dbf6dfccbb8b6acd1a2a44385fda6aaf52b2d26d75992239ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106883174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32dec7dcfbebd431a04f1ac400b4cc50406f23899aedd190509dc962a7195e8`
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
# Fri, 02 Jun 2023 00:42:21 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 00:46:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='83aa5cbbf7706def8564c57e92afe8cbd76bfe8af58e03f50cbe4154e9feecc7';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cef1f4a87e4dcd97fb8e99f2c2ddcf18c90b7712e3cb65a561ee3e0013052dd8';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='26833e7defe3fc1705d0068f530bbedbe0d9a12c38db8c4bc0837b595827a62e';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='85ab8a83e67d515a48638c58d9e4931ceecafb6f05e2c9f02cf8d9ff4dbfc116';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 00:46:50 GMT
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
	-	`sha256:317cfa0e6b14514a9ec0b11e357afb8f67c33a554f6ab45e73220f0be609a8a7`  
		Last Modified: Fri, 02 Jun 2023 00:50:56 GMT  
		Size: 69.6 MB (69594213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:7032004252ac333b786812a8c64d8978845c368090eaedf7354c1de827e9f807
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100170032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57c1f68afc1b0754a6757611e58281f3e492fd77bc9756a51a2d58d028c2a40`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:44:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 08:44:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:44:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 08:46:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='83aa5cbbf7706def8564c57e92afe8cbd76bfe8af58e03f50cbe4154e9feecc7';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cef1f4a87e4dcd97fb8e99f2c2ddcf18c90b7712e3cb65a561ee3e0013052dd8';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='26833e7defe3fc1705d0068f530bbedbe0d9a12c38db8c4bc0837b595827a62e';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='85ab8a83e67d515a48638c58d9e4931ceecafb6f05e2c9f02cf8d9ff4dbfc116';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 08:46:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:78722793f0008ff8422830a0106f21e8bc168fb9aac12cc99fb223799951759e`  
		Last Modified: Wed, 03 May 2023 22:33:36 GMT  
		Size: 28.6 MB (28647905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9459c54d841fa6f6b374fa6fe3230943f4104eb1c43155f1255ff1c9e735443`  
		Last Modified: Thu, 04 May 2023 08:48:50 GMT  
		Size: 1.5 MB (1452439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e309f4f98bde0b724a481fb7c27d8c745d9eb4c6d56254003e084df449d08b61`  
		Last Modified: Thu, 04 May 2023 08:49:12 GMT  
		Size: 70.1 MB (70069688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:65c6d8dc6142e41613bd11a2c98116fa316945f11193879ccc7c8bad29910b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:31c6cce656c7e8f8e452112b393c9f6f1a9ba249ab61328d78d59cde6645edb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165752327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a992dbde4f54fb71e3f2f14da67901c4e97729803dd3fa654c9ff3f27abf38e`
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
# Fri, 02 Jun 2023 01:03:45 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 01:04:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 01:04:44 GMT
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
	-	`sha256:060ad4d2c434c002e4380df3db7baa322a92ab810729556c82fffdfefc8182d0`  
		Last Modified: Fri, 02 Jun 2023 01:07:25 GMT  
		Size: 133.9 MB (133853336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:abc7efe7899afcd66f54579192b33701976a32ef9c735d5184cd518494836a12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0cc550973d6f28c3f44e9012b319ee5cc2db56095947fd57b9a50587f3ac0d`
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
# Fri, 02 Jun 2023 00:42:21 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 00:44:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 00:44:51 GMT
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
	-	`sha256:04c9d356bbc6d8e3b217e7967abd09ac74f3489f6be5b5138ff24edd20a17ebb`  
		Last Modified: Fri, 02 Jun 2023 00:50:32 GMT  
		Size: 133.6 MB (133555947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:9e6cd0c4cdea2701c5e56bfd06052ec75f9d1f801ad66e7f53b74213e36d33f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160756394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3726b9e3624cd26699c2b609d0d0f0e9c831289ab538f33c6eeabb41725517`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:44:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 08:44:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:44:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 08:45:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 08:45:49 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:78722793f0008ff8422830a0106f21e8bc168fb9aac12cc99fb223799951759e`  
		Last Modified: Wed, 03 May 2023 22:33:36 GMT  
		Size: 28.6 MB (28647905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9459c54d841fa6f6b374fa6fe3230943f4104eb1c43155f1255ff1c9e735443`  
		Last Modified: Thu, 04 May 2023 08:48:50 GMT  
		Size: 1.5 MB (1452439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f1a3330c7bf0b93483213fd37e7f563f9c48a90f30d9ec27d5b01cf032a5af`  
		Last Modified: Thu, 04 May 2023 08:48:59 GMT  
		Size: 130.7 MB (130656050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:65c6d8dc6142e41613bd11a2c98116fa316945f11193879ccc7c8bad29910b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:31c6cce656c7e8f8e452112b393c9f6f1a9ba249ab61328d78d59cde6645edb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165752327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a992dbde4f54fb71e3f2f14da67901c4e97729803dd3fa654c9ff3f27abf38e`
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
# Fri, 02 Jun 2023 01:03:45 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 01:04:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 01:04:44 GMT
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
	-	`sha256:060ad4d2c434c002e4380df3db7baa322a92ab810729556c82fffdfefc8182d0`  
		Last Modified: Fri, 02 Jun 2023 01:07:25 GMT  
		Size: 133.9 MB (133853336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:abc7efe7899afcd66f54579192b33701976a32ef9c735d5184cd518494836a12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0cc550973d6f28c3f44e9012b319ee5cc2db56095947fd57b9a50587f3ac0d`
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
# Fri, 02 Jun 2023 00:42:21 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 00:44:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 00:44:51 GMT
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
	-	`sha256:04c9d356bbc6d8e3b217e7967abd09ac74f3489f6be5b5138ff24edd20a17ebb`  
		Last Modified: Fri, 02 Jun 2023 00:50:32 GMT  
		Size: 133.6 MB (133555947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:9e6cd0c4cdea2701c5e56bfd06052ec75f9d1f801ad66e7f53b74213e36d33f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160756394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3726b9e3624cd26699c2b609d0d0f0e9c831289ab538f33c6eeabb41725517`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:44:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 08:44:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:44:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 08:45:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='39cf0ebeda2461c0ee81636d745643713a37863d729784c46a48b4eded4717fb';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bef3e93e4b1025e8350492fed0f6a5a743a2d35fbacdb7820cc539d24c891a4e';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='87d22ee3d2e20faa9854044aa46bf6be5d39f8ceb9ccf91574c7518f2535dfcb';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='227ada7516542c170a920bc78a416c1dc492cba4321a23f42bd7e640ddc890e5';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 08:45:49 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:78722793f0008ff8422830a0106f21e8bc168fb9aac12cc99fb223799951759e`  
		Last Modified: Wed, 03 May 2023 22:33:36 GMT  
		Size: 28.6 MB (28647905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9459c54d841fa6f6b374fa6fe3230943f4104eb1c43155f1255ff1c9e735443`  
		Last Modified: Thu, 04 May 2023 08:48:50 GMT  
		Size: 1.5 MB (1452439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f1a3330c7bf0b93483213fd37e7f563f9c48a90f30d9ec27d5b01cf032a5af`  
		Last Modified: Thu, 04 May 2023 08:48:59 GMT  
		Size: 130.7 MB (130656050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:5d03d0359244f02a27e35451d9690830ba8847edaf5275a289c6df97ad66a796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:24e3878e912fef5ee5917498cd05eb41910fb7d22c8b17a588599b14fae11dac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202902135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4fcf418f9b1638c12795ea7075784fdc7bda199fd2463f30d331b45b73c361`
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
# Fri, 02 Jun 2023 01:03:45 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 01:06:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a1dfef941fc2e43fcd8143960d2c3a82e283695eff893923cb05c226bcdd0a0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5a3d2ef0ad3687b34e1df3854b45d2e00a034724fe70a0e5bf14b2eebca1fe9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f361174227db6e6e1b067b8085549fd2f7ba63a73752a2db7be260e438ef39eb';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='974c339555e219ea93198316f6a33ee8243481e568a730d68b467c79f7caa5bc';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 01:06:56 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:7fb50ccd6b8bf20b7e441e078623ad18278a8eecc9ad3f0cee157bd88f8a4c97`  
		Last Modified: Fri, 02 Jun 2023 01:08:00 GMT  
		Size: 171.0 MB (171003144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:219645c3a69340ee6824d03fc4fb9cfcd1ce08714aff2643aaea7a88cf07004a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208127326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780b997db9350af0750e5fad0a33adaf5171b6c697177ad7989229a66868c074`
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
# Fri, 02 Jun 2023 00:42:21 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 00:49:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a1dfef941fc2e43fcd8143960d2c3a82e283695eff893923cb05c226bcdd0a0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5a3d2ef0ad3687b34e1df3854b45d2e00a034724fe70a0e5bf14b2eebca1fe9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f361174227db6e6e1b067b8085549fd2f7ba63a73752a2db7be260e438ef39eb';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='974c339555e219ea93198316f6a33ee8243481e568a730d68b467c79f7caa5bc';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 00:49:46 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:66c4067630032554977fbfae179ff7a5954ab7694f1ac475eb5e32bba070262f`  
		Last Modified: Fri, 02 Jun 2023 00:51:25 GMT  
		Size: 170.8 MB (170838365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:3984863e5b0159fb3ba0ff7817898a37c8828c24a8f17174d515e9cbb46f2402
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191054927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30122011018027b7603fd79ac1603d1399a1d88acf6944a5587335ce4ba7a6f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:44:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 08:44:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:44:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 08:48:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a1dfef941fc2e43fcd8143960d2c3a82e283695eff893923cb05c226bcdd0a0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5a3d2ef0ad3687b34e1df3854b45d2e00a034724fe70a0e5bf14b2eebca1fe9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f361174227db6e6e1b067b8085549fd2f7ba63a73752a2db7be260e438ef39eb';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='974c339555e219ea93198316f6a33ee8243481e568a730d68b467c79f7caa5bc';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 08:48:21 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:78722793f0008ff8422830a0106f21e8bc168fb9aac12cc99fb223799951759e`  
		Last Modified: Wed, 03 May 2023 22:33:36 GMT  
		Size: 28.6 MB (28647905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9459c54d841fa6f6b374fa6fe3230943f4104eb1c43155f1255ff1c9e735443`  
		Last Modified: Thu, 04 May 2023 08:48:50 GMT  
		Size: 1.5 MB (1452439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec537f63976b3afc1a38ef002078bd6db8ec68729ad89795f237dab27ed975bc`  
		Last Modified: Thu, 04 May 2023 08:49:28 GMT  
		Size: 161.0 MB (160954583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:5a547449d6bb9527dc9042a34480cd3a0173fb7227e5e5d9c821db5c8417fcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:9819342e50417e768d5d1be0bd09db065ebfbb8170e2e7e2046dc347c6cb13b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101138578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bede7e30780f33e6d1e7548e2b9a8d94f0e7201939385b3aa03f26252c8fe8`
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
# Fri, 02 Jun 2023 01:03:45 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 01:05:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='83aa5cbbf7706def8564c57e92afe8cbd76bfe8af58e03f50cbe4154e9feecc7';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cef1f4a87e4dcd97fb8e99f2c2ddcf18c90b7712e3cb65a561ee3e0013052dd8';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='26833e7defe3fc1705d0068f530bbedbe0d9a12c38db8c4bc0837b595827a62e';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='85ab8a83e67d515a48638c58d9e4931ceecafb6f05e2c9f02cf8d9ff4dbfc116';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 01:05:38 GMT
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
	-	`sha256:20482074d738da9d09cf3cc8c31260ec76842807a7ac5d7c7d104494713be260`  
		Last Modified: Fri, 02 Jun 2023 01:07:41 GMT  
		Size: 69.2 MB (69239587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:eb0ed9515b6974dbf6dfccbb8b6acd1a2a44385fda6aaf52b2d26d75992239ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106883174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32dec7dcfbebd431a04f1ac400b4cc50406f23899aedd190509dc962a7195e8`
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
# Fri, 02 Jun 2023 00:42:21 GMT
ENV JAVA_VERSION=8.0.8.0
# Fri, 02 Jun 2023 00:46:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='83aa5cbbf7706def8564c57e92afe8cbd76bfe8af58e03f50cbe4154e9feecc7';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cef1f4a87e4dcd97fb8e99f2c2ddcf18c90b7712e3cb65a561ee3e0013052dd8';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='26833e7defe3fc1705d0068f530bbedbe0d9a12c38db8c4bc0837b595827a62e';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='85ab8a83e67d515a48638c58d9e4931ceecafb6f05e2c9f02cf8d9ff4dbfc116';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Jun 2023 00:46:50 GMT
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
	-	`sha256:317cfa0e6b14514a9ec0b11e357afb8f67c33a554f6ab45e73220f0be609a8a7`  
		Last Modified: Fri, 02 Jun 2023 00:50:56 GMT  
		Size: 69.6 MB (69594213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:7032004252ac333b786812a8c64d8978845c368090eaedf7354c1de827e9f807
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100170032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57c1f68afc1b0754a6757611e58281f3e492fd77bc9756a51a2d58d028c2a40`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:44:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 04 May 2023 08:44:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:44:58 GMT
ENV JAVA_VERSION=8.0.8.0
# Thu, 04 May 2023 08:46:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='83aa5cbbf7706def8564c57e92afe8cbd76bfe8af58e03f50cbe4154e9feecc7';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cef1f4a87e4dcd97fb8e99f2c2ddcf18c90b7712e3cb65a561ee3e0013052dd8';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='26833e7defe3fc1705d0068f530bbedbe0d9a12c38db8c4bc0837b595827a62e';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='85ab8a83e67d515a48638c58d9e4931ceecafb6f05e2c9f02cf8d9ff4dbfc116';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 04 May 2023 08:46:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:78722793f0008ff8422830a0106f21e8bc168fb9aac12cc99fb223799951759e`  
		Last Modified: Wed, 03 May 2023 22:33:36 GMT  
		Size: 28.6 MB (28647905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9459c54d841fa6f6b374fa6fe3230943f4104eb1c43155f1255ff1c9e735443`  
		Last Modified: Thu, 04 May 2023 08:48:50 GMT  
		Size: 1.5 MB (1452439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e309f4f98bde0b724a481fb7c27d8c745d9eb4c6d56254003e084df449d08b61`  
		Last Modified: Thu, 04 May 2023 08:49:12 GMT  
		Size: 70.1 MB (70069688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
