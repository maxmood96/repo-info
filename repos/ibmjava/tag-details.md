<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ibmjava`

-	[`ibmjava:11`](#ibmjava11)
-	[`ibmjava:11-jdk`](#ibmjava11-jdk)
-	[`ibmjava:8`](#ibmjava8)
-	[`ibmjava:8-jre`](#ibmjava8-jre)
-	[`ibmjava:8-jre-alpine`](#ibmjava8-jre-alpine)
-	[`ibmjava:8-sdk`](#ibmjava8-sdk)
-	[`ibmjava:8-sdk-alpine`](#ibmjava8-sdk-alpine)
-	[`ibmjava:8-sfj`](#ibmjava8-sfj)
-	[`ibmjava:8-sfj-alpine`](#ibmjava8-sfj-alpine)
-	[`ibmjava:jre`](#ibmjavajre)
-	[`ibmjava:jre-alpine`](#ibmjavajre-alpine)
-	[`ibmjava:latest`](#ibmjavalatest)
-	[`ibmjava:sdk`](#ibmjavasdk)
-	[`ibmjava:sdk-alpine`](#ibmjavasdk-alpine)
-	[`ibmjava:sfj`](#ibmjavasfj)
-	[`ibmjava:sfj-alpine`](#ibmjavasfj-alpine)

## `ibmjava:11`

```console
$ docker pull ibmjava@sha256:3c15b400cb018901969b56dd2efc39c7fd7807c246bd45f98704f1cacc73804d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:11` - linux; amd64

```console
$ docker pull ibmjava@sha256:81a1f13a4bf4801a8453c697b458416bbea78971ddf2096c474bb36da7934003
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261982927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e40af7c25d7426615a9df141dec871efce3dd1e1e75630156a1f9a563845efd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:21:30 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:21:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:21:37 GMT
ENV JAVA_VERSION=11.0.11.0
# Tue, 13 Jul 2021 23:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='037363b1dd35d7b6a67137baf1c73589b4f7b4e177d40394897726ad6056babd';          YML_FILE='11.0/jdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='717d3c0427d34af710f10f62be68cc78576ebb80523ff65ab3e8c1fe6a785569';          YML_FILE='11.0/jdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='b2e64a73dab3fed0a845144377a9cd2945b87c005ba2418f1abbefea45321167';          YML_FILE='11.0/jdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     mv /opt/ibm/jdk-11* /opt/ibm/java;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:22:37 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e9588864a6125e99ac0d8a1845f653e1d3c704c5bcd165877901941358b920`  
		Last Modified: Tue, 13 Jul 2021 23:24:12 GMT  
		Size: 3.0 MB (3038956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3917773edf6147f39043b8b628ff6da2cea63bd5761843239cc7a0fc92ac0f`  
		Last Modified: Tue, 13 Jul 2021 23:24:32 GMT  
		Size: 230.4 MB (230378108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:11` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:adc037d394997f46bfe36765c48dda9ceed248ab08dbdbdca182c75d4f21e55d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267885941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211fad5facc116182143f4cc37e5846169cf388e444e6d605206fa3504b8ee20`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:43:22 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Jul 2021 04:44:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:44:41 GMT
ENV JAVA_VERSION=11.0.11.0
# Wed, 14 Jul 2021 04:45:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='037363b1dd35d7b6a67137baf1c73589b4f7b4e177d40394897726ad6056babd';          YML_FILE='11.0/jdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='717d3c0427d34af710f10f62be68cc78576ebb80523ff65ab3e8c1fe6a785569';          YML_FILE='11.0/jdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='b2e64a73dab3fed0a845144377a9cd2945b87c005ba2418f1abbefea45321167';          YML_FILE='11.0/jdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     mv /opt/ibm/jdk-11* /opt/ibm/java;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 14 Jul 2021 04:46:08 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c025b44975aec895d0939de4760d4933a2b1e003c6ca6fb32160f377842df54c`  
		Last Modified: Wed, 14 Jul 2021 04:48:07 GMT  
		Size: 3.3 MB (3292553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb2ea47bfc77eab220abd4307578ffca026d6c4ffba60f55f956e4b1fe7e332`  
		Last Modified: Wed, 14 Jul 2021 04:48:35 GMT  
		Size: 231.3 MB (231305542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:11` - linux; s390x

```console
$ docker pull ibmjava@sha256:a25351a76e397fd3114ca20e74cb977946482ec97b477f254d88da0bdeb5b24d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258594432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8181370f52ea733c195d6c7b0afc84e0e2a9cc869314e41c5bbd0f35da4aeda`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:14:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:15:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:15:07 GMT
ENV JAVA_VERSION=11.0.11.0
# Tue, 13 Jul 2021 23:16:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='037363b1dd35d7b6a67137baf1c73589b4f7b4e177d40394897726ad6056babd';          YML_FILE='11.0/jdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='717d3c0427d34af710f10f62be68cc78576ebb80523ff65ab3e8c1fe6a785569';          YML_FILE='11.0/jdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='b2e64a73dab3fed0a845144377a9cd2945b87c005ba2418f1abbefea45321167';          YML_FILE='11.0/jdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     mv /opt/ibm/jdk-11* /opt/ibm/java;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:16:17 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81ddb90e2adcfb5b79ecf14dc4d1038e5b93b21dc1d94217a3922baacbd7a4e`  
		Last Modified: Tue, 13 Jul 2021 23:17:52 GMT  
		Size: 2.7 MB (2737698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5403a01294827b8472ce25a25b8d10dc327522811b5af9a39e38260067ed3c43`  
		Last Modified: Tue, 13 Jul 2021 23:18:08 GMT  
		Size: 228.7 MB (228707416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:11-jdk`

```console
$ docker pull ibmjava@sha256:3c15b400cb018901969b56dd2efc39c7fd7807c246bd45f98704f1cacc73804d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:11-jdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:81a1f13a4bf4801a8453c697b458416bbea78971ddf2096c474bb36da7934003
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261982927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e40af7c25d7426615a9df141dec871efce3dd1e1e75630156a1f9a563845efd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:21:30 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:21:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:21:37 GMT
ENV JAVA_VERSION=11.0.11.0
# Tue, 13 Jul 2021 23:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='037363b1dd35d7b6a67137baf1c73589b4f7b4e177d40394897726ad6056babd';          YML_FILE='11.0/jdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='717d3c0427d34af710f10f62be68cc78576ebb80523ff65ab3e8c1fe6a785569';          YML_FILE='11.0/jdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='b2e64a73dab3fed0a845144377a9cd2945b87c005ba2418f1abbefea45321167';          YML_FILE='11.0/jdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     mv /opt/ibm/jdk-11* /opt/ibm/java;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:22:37 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e9588864a6125e99ac0d8a1845f653e1d3c704c5bcd165877901941358b920`  
		Last Modified: Tue, 13 Jul 2021 23:24:12 GMT  
		Size: 3.0 MB (3038956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3917773edf6147f39043b8b628ff6da2cea63bd5761843239cc7a0fc92ac0f`  
		Last Modified: Tue, 13 Jul 2021 23:24:32 GMT  
		Size: 230.4 MB (230378108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:11-jdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:adc037d394997f46bfe36765c48dda9ceed248ab08dbdbdca182c75d4f21e55d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267885941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211fad5facc116182143f4cc37e5846169cf388e444e6d605206fa3504b8ee20`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:43:22 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Jul 2021 04:44:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:44:41 GMT
ENV JAVA_VERSION=11.0.11.0
# Wed, 14 Jul 2021 04:45:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='037363b1dd35d7b6a67137baf1c73589b4f7b4e177d40394897726ad6056babd';          YML_FILE='11.0/jdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='717d3c0427d34af710f10f62be68cc78576ebb80523ff65ab3e8c1fe6a785569';          YML_FILE='11.0/jdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='b2e64a73dab3fed0a845144377a9cd2945b87c005ba2418f1abbefea45321167';          YML_FILE='11.0/jdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     mv /opt/ibm/jdk-11* /opt/ibm/java;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 14 Jul 2021 04:46:08 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c025b44975aec895d0939de4760d4933a2b1e003c6ca6fb32160f377842df54c`  
		Last Modified: Wed, 14 Jul 2021 04:48:07 GMT  
		Size: 3.3 MB (3292553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb2ea47bfc77eab220abd4307578ffca026d6c4ffba60f55f956e4b1fe7e332`  
		Last Modified: Wed, 14 Jul 2021 04:48:35 GMT  
		Size: 231.3 MB (231305542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:11-jdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:a25351a76e397fd3114ca20e74cb977946482ec97b477f254d88da0bdeb5b24d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258594432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8181370f52ea733c195d6c7b0afc84e0e2a9cc869314e41c5bbd0f35da4aeda`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:14:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:15:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:15:07 GMT
ENV JAVA_VERSION=11.0.11.0
# Tue, 13 Jul 2021 23:16:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='037363b1dd35d7b6a67137baf1c73589b4f7b4e177d40394897726ad6056babd';          YML_FILE='11.0/jdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='717d3c0427d34af710f10f62be68cc78576ebb80523ff65ab3e8c1fe6a785569';          YML_FILE='11.0/jdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='b2e64a73dab3fed0a845144377a9cd2945b87c005ba2418f1abbefea45321167';          YML_FILE='11.0/jdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     mv /opt/ibm/jdk-11* /opt/ibm/java;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:16:17 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81ddb90e2adcfb5b79ecf14dc4d1038e5b93b21dc1d94217a3922baacbd7a4e`  
		Last Modified: Tue, 13 Jul 2021 23:17:52 GMT  
		Size: 2.7 MB (2737698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5403a01294827b8472ce25a25b8d10dc327522811b5af9a39e38260067ed3c43`  
		Last Modified: Tue, 13 Jul 2021 23:18:08 GMT  
		Size: 228.7 MB (228707416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8`

```console
$ docker pull ibmjava@sha256:6031b65f580331de808d3cfa9b28e5b17fea5fe8c2fcdd6a3b9deaf1eec61ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:1f28207dfb86672ecaf28edb45dd61ae11e91ecd1d3fd2800721f2405e3d8ec6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159201377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6539f6a0b29d00ebd0edf13b0873c577ad6242c3d42153e9cdc8396279a749`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; 386

```console
$ docker pull ibmjava@sha256:2e94f1e3997a99d5e10b78237dc06f478625f57c9a7561d0ce51ecf4d5bc5a07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147871707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6671f78cf86f4ef4e886d6348c40dd9e13b01c850c020df9118958936bbe4e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:39:15 GMT
ADD file:2478887c0caae58ac755f71306211decbf5e69b832b9939974a93743e5c440f5 in / 
# Tue, 13 Jul 2021 22:39:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:05:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:05:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:05:35 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:06:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:06:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4c0067b0d84ac31443135f34e6bf8eacb1e1da0b388d042fbdd498858738047f`  
		Last Modified: Tue, 13 Jul 2021 22:40:10 GMT  
		Size: 27.2 MB (27153547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbe1128ef2eac594ca8c851354f334bde2c6c46096bbce3775054be4560ce98`  
		Last Modified: Tue, 13 Jul 2021 23:08:30 GMT  
		Size: 3.0 MB (2988008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f07fa3bc6e26fbbdd63243b676e05d77449077a5155d677b2fa3eebac501bf`  
		Last Modified: Tue, 13 Jul 2021 23:08:41 GMT  
		Size: 117.7 MB (117730152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0d29ca9bc193f393687a1b86662e161781ac76d8ea7f71b3b787fccee3f2bea8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162570715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50683a1bfb2ed72753dbd28d92fe6ec36c220a981e1d20d4abf43cfbcbce37d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:38:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Jul 2021 04:38:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:38:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Wed, 14 Jul 2021 04:40:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 14 Jul 2021 04:40:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ab9a4a9b7968cedcece7ccbd278b539ab11dc1c8c1b32042f293b4152f52fd`  
		Last Modified: Wed, 14 Jul 2021 04:46:40 GMT  
		Size: 3.1 MB (3082897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654092c12995657dfaf42c2272ad3fca06270848c145de4fff056a37c3928dbb`  
		Last Modified: Wed, 14 Jul 2021 04:46:55 GMT  
		Size: 129.1 MB (129059831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:285403a5bb76dad4e36b6667e043e843420ace79aa20f635d4b0646c4f589c03
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154719007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1d5649a4ec20c1bfac6ca894acdcdc0ccbd85172ac62e3cb296717552dff95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:6031b65f580331de808d3cfa9b28e5b17fea5fe8c2fcdd6a3b9deaf1eec61ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:1f28207dfb86672ecaf28edb45dd61ae11e91ecd1d3fd2800721f2405e3d8ec6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159201377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6539f6a0b29d00ebd0edf13b0873c577ad6242c3d42153e9cdc8396279a749`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; 386

```console
$ docker pull ibmjava@sha256:2e94f1e3997a99d5e10b78237dc06f478625f57c9a7561d0ce51ecf4d5bc5a07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147871707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6671f78cf86f4ef4e886d6348c40dd9e13b01c850c020df9118958936bbe4e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:39:15 GMT
ADD file:2478887c0caae58ac755f71306211decbf5e69b832b9939974a93743e5c440f5 in / 
# Tue, 13 Jul 2021 22:39:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:05:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:05:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:05:35 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:06:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:06:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4c0067b0d84ac31443135f34e6bf8eacb1e1da0b388d042fbdd498858738047f`  
		Last Modified: Tue, 13 Jul 2021 22:40:10 GMT  
		Size: 27.2 MB (27153547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbe1128ef2eac594ca8c851354f334bde2c6c46096bbce3775054be4560ce98`  
		Last Modified: Tue, 13 Jul 2021 23:08:30 GMT  
		Size: 3.0 MB (2988008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f07fa3bc6e26fbbdd63243b676e05d77449077a5155d677b2fa3eebac501bf`  
		Last Modified: Tue, 13 Jul 2021 23:08:41 GMT  
		Size: 117.7 MB (117730152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0d29ca9bc193f393687a1b86662e161781ac76d8ea7f71b3b787fccee3f2bea8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162570715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50683a1bfb2ed72753dbd28d92fe6ec36c220a981e1d20d4abf43cfbcbce37d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:38:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Jul 2021 04:38:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:38:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Wed, 14 Jul 2021 04:40:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 14 Jul 2021 04:40:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ab9a4a9b7968cedcece7ccbd278b539ab11dc1c8c1b32042f293b4152f52fd`  
		Last Modified: Wed, 14 Jul 2021 04:46:40 GMT  
		Size: 3.1 MB (3082897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654092c12995657dfaf42c2272ad3fca06270848c145de4fff056a37c3928dbb`  
		Last Modified: Wed, 14 Jul 2021 04:46:55 GMT  
		Size: 129.1 MB (129059831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:285403a5bb76dad4e36b6667e043e843420ace79aa20f635d4b0646c4f589c03
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154719007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1d5649a4ec20c1bfac6ca894acdcdc0ccbd85172ac62e3cb296717552dff95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre-alpine`

```console
$ docker pull ibmjava@sha256:f1752a725461929b425728e7413aef10e927ff3383e3a1cfe3139d1a95a291c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-jre-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:8e808a67bdda727109aba805b626e34816afdb466ff86dab6bf885c490d5eb4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137893422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c67fe1857a7c18788046285d2790966a7667e36f7537613222a3bbd3bad514`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:52:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Apr 2021 22:52:22 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 14 Apr 2021 22:52:39 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 03 Jun 2021 21:24:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Thu, 03 Jun 2021 21:25:28 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 03 Jun 2021 21:25:28 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2473651455a528e12a77a3f77634a9edcf271c6673a5d553738621ea93c7f661`  
		Last Modified: Wed, 14 Apr 2021 22:54:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a476c88f89042a64d394f56be791c17d185be12546f3f0be1966502a0643c`  
		Last Modified: Wed, 14 Apr 2021 22:55:01 GMT  
		Size: 5.5 MB (5539744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6854ed6de97957a8d470b8cbf8da87faffaf82b788ed64a016fd365e0e2a74f6`  
		Last Modified: Thu, 03 Jun 2021 21:28:54 GMT  
		Size: 129.6 MB (129552572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:35b300068b472e9b508d7d0039297b3c74d5bea7a323801f275b693f91c96978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:8db94a9754c1835a85e101d2cad2ff693aaad91dd46cea0affedf3bb0b7b1169
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196346158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b181dfcc736e12b80770de3d4ece682e3bf251316885fd6e0a8c16becc1962`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:21:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:21:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90295c40970bbb17ff1570addc7017c9b85451a44f5e27176685bcda6cf7bf5`  
		Last Modified: Tue, 13 Jul 2021 23:23:59 GMT  
		Size: 166.7 MB (166681009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:99bfb3c1e9ac6d5d2f7156e6a17d1655afb9687d06329f24150f1b9419a4806e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184888403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb09774b59ae1577827d685da33cf783b581188caeb7648d2690a6381785fe50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:39:15 GMT
ADD file:2478887c0caae58ac755f71306211decbf5e69b832b9939974a93743e5c440f5 in / 
# Tue, 13 Jul 2021 22:39:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:05:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:05:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:05:35 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:07:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:07:55 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4c0067b0d84ac31443135f34e6bf8eacb1e1da0b388d042fbdd498858738047f`  
		Last Modified: Tue, 13 Jul 2021 22:40:10 GMT  
		Size: 27.2 MB (27153547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbe1128ef2eac594ca8c851354f334bde2c6c46096bbce3775054be4560ce98`  
		Last Modified: Tue, 13 Jul 2021 23:08:30 GMT  
		Size: 3.0 MB (2988008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537c0e8e38af1c8a98d2d59ecc6e896e11d7e64e6c7066c66282ec2de913d704`  
		Last Modified: Tue, 13 Jul 2021 23:09:34 GMT  
		Size: 154.7 MB (154746848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5a049e080f2fff391a8b96fa0a63500c7e02fb1cf30ee1a244a24fd97da1865c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199849894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feeee59847dc8fea2fd0c9fe842369b6d68ce79bd1cbf1a71c4b06956492776f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:38:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Jul 2021 04:38:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:38:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Wed, 14 Jul 2021 04:42:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 14 Jul 2021 04:43:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ab9a4a9b7968cedcece7ccbd278b539ab11dc1c8c1b32042f293b4152f52fd`  
		Last Modified: Wed, 14 Jul 2021 04:46:40 GMT  
		Size: 3.1 MB (3082897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b321c58cb0c42d32e508e0ff76b7d9451ab38b7992af894e4ee8451b723ea460`  
		Last Modified: Wed, 14 Jul 2021 04:47:55 GMT  
		Size: 166.3 MB (166339010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:e041d9bff40ba18629634b87c4cd85f8afbc575620ab955213c5df6c36daa06b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185001939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7355cb28b9d13df1936d6c3f13d34fb1460f3cfb730eaf379c2049ea2b92e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:14:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e107d093f0ddb6173da707d07364554373c98b1e6f85874cd83d11687d60ac1c`  
		Last Modified: Tue, 13 Jul 2021 23:17:43 GMT  
		Size: 157.0 MB (156959462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk-alpine`

```console
$ docker pull ibmjava@sha256:1fe4106ffc54495c215ee6a3c8bac11a7ad34e82b2f9950d834e0705d2e37c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-sdk-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:7bb1ec5f0be168dec4797885c0dfb53d98886dfd01879bfed592a44349d0ef63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (175033632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeda7a451479203ef04c1f4077208a2607832862a6a722ac5bfc7bf36c04b9b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:52:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Apr 2021 22:52:22 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 14 Apr 2021 22:52:39 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 03 Jun 2021 21:24:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Thu, 03 Jun 2021 21:27:55 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 03 Jun 2021 21:27:56 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2473651455a528e12a77a3f77634a9edcf271c6673a5d553738621ea93c7f661`  
		Last Modified: Wed, 14 Apr 2021 22:54:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a476c88f89042a64d394f56be791c17d185be12546f3f0be1966502a0643c`  
		Last Modified: Wed, 14 Apr 2021 22:55:01 GMT  
		Size: 5.5 MB (5539744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8169a114fdc61189630b383edeffe0f6190a90494d0f4f86f22da251624963`  
		Last Modified: Thu, 03 Jun 2021 21:30:11 GMT  
		Size: 166.7 MB (166692782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:0b980a6275e78178189f035cc25358bba8550e07c6cd5dfdb17a1988cf986fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:9a2391efb9b4152daeb6867186c6c3ff320d78024d6a57a902fdeeb3e4495611
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94035661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebabe592bb7443cb609a85d65d5067282c4ae2f900b61f95d9c17ac22025827`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:20:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:20:29 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76d35690198d2592eef10baa51062473dbf9635abc81fef63eb4aa9eb63dbfc`  
		Last Modified: Tue, 13 Jul 2021 23:23:35 GMT  
		Size: 64.4 MB (64370512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:896c5b46fc5a91b2c0dde6e426132fa9deb23212711574d18f490e6aea2b60d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93878655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e8cc15d2afd7fbc238e86b1476fe2e2f42342dee3df092783fc82c2495dfe9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:39:15 GMT
ADD file:2478887c0caae58ac755f71306211decbf5e69b832b9939974a93743e5c440f5 in / 
# Tue, 13 Jul 2021 22:39:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:05:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:05:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:05:35 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:07:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:07:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4c0067b0d84ac31443135f34e6bf8eacb1e1da0b388d042fbdd498858738047f`  
		Last Modified: Tue, 13 Jul 2021 22:40:10 GMT  
		Size: 27.2 MB (27153547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbe1128ef2eac594ca8c851354f334bde2c6c46096bbce3775054be4560ce98`  
		Last Modified: Tue, 13 Jul 2021 23:08:30 GMT  
		Size: 3.0 MB (2988008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e121d23e1afcf0579dfcfc6cc82bf9f6b37594e83b710df3f350dfa48de2dceb`  
		Last Modified: Tue, 13 Jul 2021 23:09:08 GMT  
		Size: 63.7 MB (63737100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:da64748a60ee5be441ede534145404f7ca1fadfbd24567b39eb084ab180d45bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103229086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca35aa1e774d4c707aa84aa3a41a539a86f2613c1243cc576348b505d4d333`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:38:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Jul 2021 04:38:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:38:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Wed, 14 Jul 2021 04:41:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 14 Jul 2021 04:41:27 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ab9a4a9b7968cedcece7ccbd278b539ab11dc1c8c1b32042f293b4152f52fd`  
		Last Modified: Wed, 14 Jul 2021 04:46:40 GMT  
		Size: 3.1 MB (3082897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e575ef18593a4591a7b17be251c5c1b49fd5956290149fc58433dffce5f9f`  
		Last Modified: Wed, 14 Jul 2021 04:47:23 GMT  
		Size: 69.7 MB (69718202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:f6b31a9d71ee9746f2f420e4b6111fef4338cae3f1e8329d6c843519053dc82c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93510658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63b7c02a34ba4c27ae8639330e649e62e3d71e80abc0c0c6184f6dc1de658c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffda74c5d06c573f1001bc58b41bf8ced98133bfb16efeb134cd98948786009`  
		Last Modified: Tue, 13 Jul 2021 23:17:24 GMT  
		Size: 65.5 MB (65468181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj-alpine`

```console
$ docker pull ibmjava@sha256:262e9812cc0f11c41e15218cc64a4ab9a9cadb899c8112659b2730dd435112be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-sfj-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:f20484e24cee6fefbd379345f6296e334948933bdacbd1cc577157cd055fa053
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72730682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f698c6b09cd03fb877f7156778ebe0de810f7ec8eb5d5e741371befa41e6e6cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:52:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Apr 2021 22:52:22 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 14 Apr 2021 22:52:39 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 03 Jun 2021 21:24:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Thu, 03 Jun 2021 21:26:31 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 03 Jun 2021 21:26:31 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2473651455a528e12a77a3f77634a9edcf271c6673a5d553738621ea93c7f661`  
		Last Modified: Wed, 14 Apr 2021 22:54:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a476c88f89042a64d394f56be791c17d185be12546f3f0be1966502a0643c`  
		Last Modified: Wed, 14 Apr 2021 22:55:01 GMT  
		Size: 5.5 MB (5539744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82faec9364eaa46bdef7684300da3856f837389a970f23de2f4391af423bbd2`  
		Last Modified: Thu, 03 Jun 2021 21:29:27 GMT  
		Size: 64.4 MB (64389832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:6031b65f580331de808d3cfa9b28e5b17fea5fe8c2fcdd6a3b9deaf1eec61ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:1f28207dfb86672ecaf28edb45dd61ae11e91ecd1d3fd2800721f2405e3d8ec6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159201377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6539f6a0b29d00ebd0edf13b0873c577ad6242c3d42153e9cdc8396279a749`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; 386

```console
$ docker pull ibmjava@sha256:2e94f1e3997a99d5e10b78237dc06f478625f57c9a7561d0ce51ecf4d5bc5a07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147871707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6671f78cf86f4ef4e886d6348c40dd9e13b01c850c020df9118958936bbe4e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:39:15 GMT
ADD file:2478887c0caae58ac755f71306211decbf5e69b832b9939974a93743e5c440f5 in / 
# Tue, 13 Jul 2021 22:39:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:05:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:05:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:05:35 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:06:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:06:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4c0067b0d84ac31443135f34e6bf8eacb1e1da0b388d042fbdd498858738047f`  
		Last Modified: Tue, 13 Jul 2021 22:40:10 GMT  
		Size: 27.2 MB (27153547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbe1128ef2eac594ca8c851354f334bde2c6c46096bbce3775054be4560ce98`  
		Last Modified: Tue, 13 Jul 2021 23:08:30 GMT  
		Size: 3.0 MB (2988008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f07fa3bc6e26fbbdd63243b676e05d77449077a5155d677b2fa3eebac501bf`  
		Last Modified: Tue, 13 Jul 2021 23:08:41 GMT  
		Size: 117.7 MB (117730152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0d29ca9bc193f393687a1b86662e161781ac76d8ea7f71b3b787fccee3f2bea8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162570715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50683a1bfb2ed72753dbd28d92fe6ec36c220a981e1d20d4abf43cfbcbce37d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:38:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Jul 2021 04:38:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:38:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Wed, 14 Jul 2021 04:40:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 14 Jul 2021 04:40:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ab9a4a9b7968cedcece7ccbd278b539ab11dc1c8c1b32042f293b4152f52fd`  
		Last Modified: Wed, 14 Jul 2021 04:46:40 GMT  
		Size: 3.1 MB (3082897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654092c12995657dfaf42c2272ad3fca06270848c145de4fff056a37c3928dbb`  
		Last Modified: Wed, 14 Jul 2021 04:46:55 GMT  
		Size: 129.1 MB (129059831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:285403a5bb76dad4e36b6667e043e843420ace79aa20f635d4b0646c4f589c03
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154719007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1d5649a4ec20c1bfac6ca894acdcdc0ccbd85172ac62e3cb296717552dff95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre-alpine`

```console
$ docker pull ibmjava@sha256:f1752a725461929b425728e7413aef10e927ff3383e3a1cfe3139d1a95a291c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:jre-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:8e808a67bdda727109aba805b626e34816afdb466ff86dab6bf885c490d5eb4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137893422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c67fe1857a7c18788046285d2790966a7667e36f7537613222a3bbd3bad514`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:52:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Apr 2021 22:52:22 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 14 Apr 2021 22:52:39 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 03 Jun 2021 21:24:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Thu, 03 Jun 2021 21:25:28 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 03 Jun 2021 21:25:28 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2473651455a528e12a77a3f77634a9edcf271c6673a5d553738621ea93c7f661`  
		Last Modified: Wed, 14 Apr 2021 22:54:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a476c88f89042a64d394f56be791c17d185be12546f3f0be1966502a0643c`  
		Last Modified: Wed, 14 Apr 2021 22:55:01 GMT  
		Size: 5.5 MB (5539744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6854ed6de97957a8d470b8cbf8da87faffaf82b788ed64a016fd365e0e2a74f6`  
		Last Modified: Thu, 03 Jun 2021 21:28:54 GMT  
		Size: 129.6 MB (129552572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:6031b65f580331de808d3cfa9b28e5b17fea5fe8c2fcdd6a3b9deaf1eec61ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:1f28207dfb86672ecaf28edb45dd61ae11e91ecd1d3fd2800721f2405e3d8ec6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159201377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6539f6a0b29d00ebd0edf13b0873c577ad6242c3d42153e9cdc8396279a749`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; 386

```console
$ docker pull ibmjava@sha256:2e94f1e3997a99d5e10b78237dc06f478625f57c9a7561d0ce51ecf4d5bc5a07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147871707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6671f78cf86f4ef4e886d6348c40dd9e13b01c850c020df9118958936bbe4e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:39:15 GMT
ADD file:2478887c0caae58ac755f71306211decbf5e69b832b9939974a93743e5c440f5 in / 
# Tue, 13 Jul 2021 22:39:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:05:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:05:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:05:35 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:06:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:06:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4c0067b0d84ac31443135f34e6bf8eacb1e1da0b388d042fbdd498858738047f`  
		Last Modified: Tue, 13 Jul 2021 22:40:10 GMT  
		Size: 27.2 MB (27153547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbe1128ef2eac594ca8c851354f334bde2c6c46096bbce3775054be4560ce98`  
		Last Modified: Tue, 13 Jul 2021 23:08:30 GMT  
		Size: 3.0 MB (2988008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f07fa3bc6e26fbbdd63243b676e05d77449077a5155d677b2fa3eebac501bf`  
		Last Modified: Tue, 13 Jul 2021 23:08:41 GMT  
		Size: 117.7 MB (117730152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0d29ca9bc193f393687a1b86662e161781ac76d8ea7f71b3b787fccee3f2bea8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162570715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50683a1bfb2ed72753dbd28d92fe6ec36c220a981e1d20d4abf43cfbcbce37d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:38:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Jul 2021 04:38:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:38:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Wed, 14 Jul 2021 04:40:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 14 Jul 2021 04:40:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ab9a4a9b7968cedcece7ccbd278b539ab11dc1c8c1b32042f293b4152f52fd`  
		Last Modified: Wed, 14 Jul 2021 04:46:40 GMT  
		Size: 3.1 MB (3082897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654092c12995657dfaf42c2272ad3fca06270848c145de4fff056a37c3928dbb`  
		Last Modified: Wed, 14 Jul 2021 04:46:55 GMT  
		Size: 129.1 MB (129059831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:285403a5bb76dad4e36b6667e043e843420ace79aa20f635d4b0646c4f589c03
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154719007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1d5649a4ec20c1bfac6ca894acdcdc0ccbd85172ac62e3cb296717552dff95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:35b300068b472e9b508d7d0039297b3c74d5bea7a323801f275b693f91c96978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:8db94a9754c1835a85e101d2cad2ff693aaad91dd46cea0affedf3bb0b7b1169
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196346158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b181dfcc736e12b80770de3d4ece682e3bf251316885fd6e0a8c16becc1962`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:21:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:21:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90295c40970bbb17ff1570addc7017c9b85451a44f5e27176685bcda6cf7bf5`  
		Last Modified: Tue, 13 Jul 2021 23:23:59 GMT  
		Size: 166.7 MB (166681009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:99bfb3c1e9ac6d5d2f7156e6a17d1655afb9687d06329f24150f1b9419a4806e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184888403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb09774b59ae1577827d685da33cf783b581188caeb7648d2690a6381785fe50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:39:15 GMT
ADD file:2478887c0caae58ac755f71306211decbf5e69b832b9939974a93743e5c440f5 in / 
# Tue, 13 Jul 2021 22:39:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:05:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:05:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:05:35 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:07:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:07:55 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4c0067b0d84ac31443135f34e6bf8eacb1e1da0b388d042fbdd498858738047f`  
		Last Modified: Tue, 13 Jul 2021 22:40:10 GMT  
		Size: 27.2 MB (27153547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbe1128ef2eac594ca8c851354f334bde2c6c46096bbce3775054be4560ce98`  
		Last Modified: Tue, 13 Jul 2021 23:08:30 GMT  
		Size: 3.0 MB (2988008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537c0e8e38af1c8a98d2d59ecc6e896e11d7e64e6c7066c66282ec2de913d704`  
		Last Modified: Tue, 13 Jul 2021 23:09:34 GMT  
		Size: 154.7 MB (154746848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5a049e080f2fff391a8b96fa0a63500c7e02fb1cf30ee1a244a24fd97da1865c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199849894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feeee59847dc8fea2fd0c9fe842369b6d68ce79bd1cbf1a71c4b06956492776f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:38:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Jul 2021 04:38:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:38:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Wed, 14 Jul 2021 04:42:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 14 Jul 2021 04:43:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ab9a4a9b7968cedcece7ccbd278b539ab11dc1c8c1b32042f293b4152f52fd`  
		Last Modified: Wed, 14 Jul 2021 04:46:40 GMT  
		Size: 3.1 MB (3082897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b321c58cb0c42d32e508e0ff76b7d9451ab38b7992af894e4ee8451b723ea460`  
		Last Modified: Wed, 14 Jul 2021 04:47:55 GMT  
		Size: 166.3 MB (166339010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:e041d9bff40ba18629634b87c4cd85f8afbc575620ab955213c5df6c36daa06b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185001939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7355cb28b9d13df1936d6c3f13d34fb1460f3cfb730eaf379c2049ea2b92e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:14:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e107d093f0ddb6173da707d07364554373c98b1e6f85874cd83d11687d60ac1c`  
		Last Modified: Tue, 13 Jul 2021 23:17:43 GMT  
		Size: 157.0 MB (156959462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk-alpine`

```console
$ docker pull ibmjava@sha256:1fe4106ffc54495c215ee6a3c8bac11a7ad34e82b2f9950d834e0705d2e37c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:sdk-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:7bb1ec5f0be168dec4797885c0dfb53d98886dfd01879bfed592a44349d0ef63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (175033632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeda7a451479203ef04c1f4077208a2607832862a6a722ac5bfc7bf36c04b9b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:52:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Apr 2021 22:52:22 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 14 Apr 2021 22:52:39 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 03 Jun 2021 21:24:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Thu, 03 Jun 2021 21:27:55 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 03 Jun 2021 21:27:56 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2473651455a528e12a77a3f77634a9edcf271c6673a5d553738621ea93c7f661`  
		Last Modified: Wed, 14 Apr 2021 22:54:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a476c88f89042a64d394f56be791c17d185be12546f3f0be1966502a0643c`  
		Last Modified: Wed, 14 Apr 2021 22:55:01 GMT  
		Size: 5.5 MB (5539744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8169a114fdc61189630b383edeffe0f6190a90494d0f4f86f22da251624963`  
		Last Modified: Thu, 03 Jun 2021 21:30:11 GMT  
		Size: 166.7 MB (166692782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:0b980a6275e78178189f035cc25358bba8550e07c6cd5dfdb17a1988cf986fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:9a2391efb9b4152daeb6867186c6c3ff320d78024d6a57a902fdeeb3e4495611
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94035661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebabe592bb7443cb609a85d65d5067282c4ae2f900b61f95d9c17ac22025827`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:20:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:20:29 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76d35690198d2592eef10baa51062473dbf9635abc81fef63eb4aa9eb63dbfc`  
		Last Modified: Tue, 13 Jul 2021 23:23:35 GMT  
		Size: 64.4 MB (64370512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:896c5b46fc5a91b2c0dde6e426132fa9deb23212711574d18f490e6aea2b60d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93878655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e8cc15d2afd7fbc238e86b1476fe2e2f42342dee3df092783fc82c2495dfe9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:39:15 GMT
ADD file:2478887c0caae58ac755f71306211decbf5e69b832b9939974a93743e5c440f5 in / 
# Tue, 13 Jul 2021 22:39:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:05:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:05:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:05:35 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:07:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:07:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4c0067b0d84ac31443135f34e6bf8eacb1e1da0b388d042fbdd498858738047f`  
		Last Modified: Tue, 13 Jul 2021 22:40:10 GMT  
		Size: 27.2 MB (27153547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbe1128ef2eac594ca8c851354f334bde2c6c46096bbce3775054be4560ce98`  
		Last Modified: Tue, 13 Jul 2021 23:08:30 GMT  
		Size: 3.0 MB (2988008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e121d23e1afcf0579dfcfc6cc82bf9f6b37594e83b710df3f350dfa48de2dceb`  
		Last Modified: Tue, 13 Jul 2021 23:09:08 GMT  
		Size: 63.7 MB (63737100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:da64748a60ee5be441ede534145404f7ca1fadfbd24567b39eb084ab180d45bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103229086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca35aa1e774d4c707aa84aa3a41a539a86f2613c1243cc576348b505d4d333`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:38:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Jul 2021 04:38:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:38:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Wed, 14 Jul 2021 04:41:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 14 Jul 2021 04:41:27 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ab9a4a9b7968cedcece7ccbd278b539ab11dc1c8c1b32042f293b4152f52fd`  
		Last Modified: Wed, 14 Jul 2021 04:46:40 GMT  
		Size: 3.1 MB (3082897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e575ef18593a4591a7b17be251c5c1b49fd5956290149fc58433dffce5f9f`  
		Last Modified: Wed, 14 Jul 2021 04:47:23 GMT  
		Size: 69.7 MB (69718202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:f6b31a9d71ee9746f2f420e4b6111fef4338cae3f1e8329d6c843519053dc82c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93510658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63b7c02a34ba4c27ae8639330e649e62e3d71e80abc0c0c6184f6dc1de658c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffda74c5d06c573f1001bc58b41bf8ced98133bfb16efeb134cd98948786009`  
		Last Modified: Tue, 13 Jul 2021 23:17:24 GMT  
		Size: 65.5 MB (65468181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj-alpine`

```console
$ docker pull ibmjava@sha256:262e9812cc0f11c41e15218cc64a4ab9a9cadb899c8112659b2730dd435112be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:sfj-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:f20484e24cee6fefbd379345f6296e334948933bdacbd1cc577157cd055fa053
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72730682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f698c6b09cd03fb877f7156778ebe0de810f7ec8eb5d5e741371befa41e6e6cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:52:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Apr 2021 22:52:22 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 14 Apr 2021 22:52:39 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 03 Jun 2021 21:24:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Thu, 03 Jun 2021 21:26:31 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 03 Jun 2021 21:26:31 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2473651455a528e12a77a3f77634a9edcf271c6673a5d553738621ea93c7f661`  
		Last Modified: Wed, 14 Apr 2021 22:54:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a476c88f89042a64d394f56be791c17d185be12546f3f0be1966502a0643c`  
		Last Modified: Wed, 14 Apr 2021 22:55:01 GMT  
		Size: 5.5 MB (5539744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82faec9364eaa46bdef7684300da3856f837389a970f23de2f4391af423bbd2`  
		Last Modified: Thu, 03 Jun 2021 21:29:27 GMT  
		Size: 64.4 MB (64389832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
