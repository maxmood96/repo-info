## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:b4aae928e9f7d0e34a2b847c0183a3456d6c9398cd2b9bd4ba0df69c6fb83c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:2fc0d750f0dfbeede1f48ef06d637908347223688248a0b089bbf7146af87e95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94250536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8645910307c0607a9f8c90bf8cea8a981d1c7a72726b1a2854b9f8769663f48b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:11:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 04:11:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:11:10 GMT
ENV JAVA_VERSION=8.0.7.5
# Wed, 06 Apr 2022 04:12:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f3d0d6cf854f1cd5c6908be9ab77fa133dee458a11a52220a0b2685a18e69aef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='79c24135b40cbe7e1fa10c8e49192ff87a76547d34d31d07f85b29684212228b';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9635b3d236dfbe32e342d5e5c6e2e29aa323fa5b005dec604c399c711f0053a7';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6240eacc70f4331836349fb52f6327a5a4f4191d89dab1a70a07fc6fd0517ce7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3ceb64e606904c38a45d58fd7917bb2ffb29a107e780aeef6aed5cd678c4c842';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 Apr 2022 04:12:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bfba7ea970cb1c55200b82df4d841cb3aeceb410b11a8979aa633a92e7d236b`  
		Last Modified: Wed, 06 Apr 2022 04:13:29 GMT  
		Size: 3.0 MB (2959903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10415952fc7a726aaac39992a393fd4998976285bc07c065229c86c5848a8682`  
		Last Modified: Wed, 06 Apr 2022 04:13:59 GMT  
		Size: 64.6 MB (64581695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:8147cafd3d6fd8d11606de4458802deb5ca140acf184085d321df01db752e3b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94119410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68801ccd578eafb8b079bbf348ad855167d0836bc69b402f7fc125d7f669712c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:39:01 GMT
ADD file:d9edbb973ba7a0ee377e64ec7b7135478b3259223d5fbb83185ae0653ec0773f in / 
# Tue, 05 Apr 2022 22:39:02 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:56:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 22:56:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 22:56:17 GMT
ENV JAVA_VERSION=8.0.7.5
# Tue, 05 Apr 2022 22:57:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f3d0d6cf854f1cd5c6908be9ab77fa133dee458a11a52220a0b2685a18e69aef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='79c24135b40cbe7e1fa10c8e49192ff87a76547d34d31d07f85b29684212228b';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9635b3d236dfbe32e342d5e5c6e2e29aa323fa5b005dec604c399c711f0053a7';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6240eacc70f4331836349fb52f6327a5a4f4191d89dab1a70a07fc6fd0517ce7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3ceb64e606904c38a45d58fd7917bb2ffb29a107e780aeef6aed5cd678c4c842';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 05 Apr 2022 22:57:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:12d1023794ad0425246985d1a3b4e8ad7a1368a1a6bd0f7a2827dd443349538b`  
		Last Modified: Tue, 05 Apr 2022 13:12:34 GMT  
		Size: 27.2 MB (27162492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7cb5790f060933c43ae1b003f69b6cf1bb7e024de0a59705e22882def104b8`  
		Last Modified: Tue, 05 Apr 2022 22:58:55 GMT  
		Size: 3.0 MB (2988442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d4b837be82f821608eb5605dc4664197bfa6758a4ec2f137baea83b66863ae`  
		Last Modified: Tue, 05 Apr 2022 22:59:39 GMT  
		Size: 64.0 MB (63968476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:47d8556f6f5c06f8d08526303d69e32bed3921ace84e217fbd773b1f4a113a19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98309835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf80d2284636dac6ae6a249aaf009dc783057c775a2b39d9b107756fac054d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:13:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 06 Apr 2022 05:14:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:14:31 GMT
ENV JAVA_VERSION=8.0.7.5
# Wed, 06 Apr 2022 05:17:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f3d0d6cf854f1cd5c6908be9ab77fa133dee458a11a52220a0b2685a18e69aef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='79c24135b40cbe7e1fa10c8e49192ff87a76547d34d31d07f85b29684212228b';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9635b3d236dfbe32e342d5e5c6e2e29aa323fa5b005dec604c399c711f0053a7';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6240eacc70f4331836349fb52f6327a5a4f4191d89dab1a70a07fc6fd0517ce7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3ceb64e606904c38a45d58fd7917bb2ffb29a107e780aeef6aed5cd678c4c842';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 Apr 2022 05:17:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdbaeb83a31ef16299d247a8ff263c6635af307374780bb9be69adac828283a`  
		Last Modified: Wed, 06 Apr 2022 05:19:24 GMT  
		Size: 3.1 MB (3082224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc78aae1fb9221c1fa424c8443c2bf21a2afdc75201015cddf13cb4a698624`  
		Last Modified: Wed, 06 Apr 2022 05:20:06 GMT  
		Size: 64.8 MB (64789182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:cbb86638e78860220ed824f4283ce6c96e469cef1b3d7ddd42263fd95c2e51c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93669220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9d4c16afeaebc0e523634b96f211a1337624192dc462c8f14fef59f498fa1d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:41:55 GMT
ADD file:7da6edcff7f600bf3a5d740cd585065c6b3748ff587c0627def91686d1bfe54d in / 
# Tue, 05 Apr 2022 22:41:57 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:04:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Apr 2022 23:04:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:04:27 GMT
ENV JAVA_VERSION=8.0.7.5
# Tue, 05 Apr 2022 23:06:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f3d0d6cf854f1cd5c6908be9ab77fa133dee458a11a52220a0b2685a18e69aef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='79c24135b40cbe7e1fa10c8e49192ff87a76547d34d31d07f85b29684212228b';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9635b3d236dfbe32e342d5e5c6e2e29aa323fa5b005dec604c399c711f0053a7';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6240eacc70f4331836349fb52f6327a5a4f4191d89dab1a70a07fc6fd0517ce7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3ceb64e606904c38a45d58fd7917bb2ffb29a107e780aeef6aed5cd678c4c842';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 05 Apr 2022 23:06:23 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4b0f8a5e4614be4866f08e8772b57664127164f512df03d05a52607176caa02f`  
		Last Modified: Tue, 05 Apr 2022 13:13:37 GMT  
		Size: 25.4 MB (25365860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df112729db94ceb85cc2f4f1a8a29c4c17240f3414e928932240687367857b`  
		Last Modified: Tue, 05 Apr 2022 23:07:59 GMT  
		Size: 2.7 MB (2676913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4077e1280bbe3270c79502dc6cd3a0923fc44129ef033b0b73053945165558`  
		Last Modified: Tue, 05 Apr 2022 23:08:22 GMT  
		Size: 65.6 MB (65626447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
