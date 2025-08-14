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
$ docker pull ibmjava@sha256:9626481da11b946704196b63dc021c686cf95027e392f545805c0522a4428eef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:6494d2f1b139f4557657d36a81d52d4b79b4816f5fb0865b0476df6135fdcbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166406112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f73d18f316ea22dd6db3b58c9a9c095effda288fa0ea021e215be4449ff46f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f2eec3d528eb5b5110c2bb9812d5a2c27a080f85b313e063387bfdb6166e8e`  
		Last Modified: Tue, 12 Aug 2025 17:26:04 GMT  
		Size: 1.5 MB (1450029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ad216cec582a4c9420675953629f4cdc5046ba2fecc126a371479369d618a`  
		Last Modified: Tue, 12 Aug 2025 17:59:13 GMT  
		Size: 135.4 MB (135419090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5befd233eb606ca2c38f93db5e80065f47a67d43accc2031e1409761f388a64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5464d9d18132df98ae8bc2b24ec9d560f05f9c18228173eff52e76b4768132d`

```dockerfile
```

-	Layers:
	-	`sha256:c2442617ed8b1550a6eba8f16e0795e994941e7ceb1485c422fa4aefa6c77d85`  
		Last Modified: Tue, 12 Aug 2025 20:01:24 GMT  
		Size: 2.2 MB (2173526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e98a836f1739539f81e16c1702577bcc44500b156a16e89f9f07dd4c9b9186e3`  
		Last Modified: Tue, 12 Aug 2025 20:01:24 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:d08ec4e0d92aa197707efec98f5f6c2a20e280f8e997428c6b24ae8114fae273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172346961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acbe6b6c2592137856f658f477e81176424e1f8f1b5905e63d2c3c4b1953e1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2927a1e71e8665a0426e9c87b474fb1e405fba2f397cd65dfa47740d2204a7b`  
		Last Modified: Tue, 12 Aug 2025 18:23:37 GMT  
		Size: 1.5 MB (1536169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38acb531b224a8c9fbff4a5b8df38d3d05236be9b6ece3c83de72a8e11e1997`  
		Last Modified: Tue, 12 Aug 2025 20:18:48 GMT  
		Size: 136.4 MB (136367647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3e75a160b189532295764764c0c4c0f6da7085127009e15023e1b72426818938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f86379c07a583c6b4d2cda730067fd39c55759ad0b53a845a80d0ed1e4e918`

```dockerfile
```

-	Layers:
	-	`sha256:147a62d352cf78f202afc96c5da922c9887cda49c41d8361aea522230e478a38`  
		Last Modified: Tue, 12 Aug 2025 20:01:29 GMT  
		Size: 2.2 MB (2176816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be0156c28bdbd4005e2aaaddaa2a84801c57027018e6f11ec1c4fa445ddfc5b8`  
		Last Modified: Tue, 12 Aug 2025 20:01:30 GMT  
		Size: 13.3 KB (13281 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:b17eee212c1c210609cd565ace2921d4f51f0f558a0496bb231c2950154f072d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161749926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26e70e8ebd202849ee12a68aa118a3cafb84ced4322b51c0a63e4e677e731f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f8a63a7a987fdc761e7e8968ba27654e47f55b299e1e97fe6e51a2c4940f6`  
		Last Modified: Tue, 12 Aug 2025 18:03:01 GMT  
		Size: 1.5 MB (1455837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b282bb47e354fef0c2bcd88a6519010f31c0cb841b9d18790126035171dc4c2`  
		Last Modified: Tue, 12 Aug 2025 21:17:31 GMT  
		Size: 132.3 MB (132290870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a7266ee04452817b08fa29b0fbebd35e50f8c52e3c43404713d121b709a773db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871ca65a6cc062486ec644ccc2475fb782c5f34d8dbed69e36047adf57ec4ee6`

```dockerfile
```

-	Layers:
	-	`sha256:13e98e9c08d9ba46883f71213872667798b4bbee447ba410ee562fc0619e6aae`  
		Last Modified: Tue, 12 Aug 2025 20:01:34 GMT  
		Size: 2.2 MB (2173487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e7acb1f40aad1a6b9562ac8e788e8119165682383980dea21e0d2a7d4a518f`  
		Last Modified: Tue, 12 Aug 2025 20:01:35 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:9626481da11b946704196b63dc021c686cf95027e392f545805c0522a4428eef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:6494d2f1b139f4557657d36a81d52d4b79b4816f5fb0865b0476df6135fdcbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166406112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f73d18f316ea22dd6db3b58c9a9c095effda288fa0ea021e215be4449ff46f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f2eec3d528eb5b5110c2bb9812d5a2c27a080f85b313e063387bfdb6166e8e`  
		Last Modified: Tue, 12 Aug 2025 17:26:04 GMT  
		Size: 1.5 MB (1450029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ad216cec582a4c9420675953629f4cdc5046ba2fecc126a371479369d618a`  
		Last Modified: Tue, 12 Aug 2025 17:59:13 GMT  
		Size: 135.4 MB (135419090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5befd233eb606ca2c38f93db5e80065f47a67d43accc2031e1409761f388a64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5464d9d18132df98ae8bc2b24ec9d560f05f9c18228173eff52e76b4768132d`

```dockerfile
```

-	Layers:
	-	`sha256:c2442617ed8b1550a6eba8f16e0795e994941e7ceb1485c422fa4aefa6c77d85`  
		Last Modified: Tue, 12 Aug 2025 20:01:24 GMT  
		Size: 2.2 MB (2173526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e98a836f1739539f81e16c1702577bcc44500b156a16e89f9f07dd4c9b9186e3`  
		Last Modified: Tue, 12 Aug 2025 20:01:24 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:d08ec4e0d92aa197707efec98f5f6c2a20e280f8e997428c6b24ae8114fae273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172346961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acbe6b6c2592137856f658f477e81176424e1f8f1b5905e63d2c3c4b1953e1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2927a1e71e8665a0426e9c87b474fb1e405fba2f397cd65dfa47740d2204a7b`  
		Last Modified: Tue, 12 Aug 2025 18:23:37 GMT  
		Size: 1.5 MB (1536169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38acb531b224a8c9fbff4a5b8df38d3d05236be9b6ece3c83de72a8e11e1997`  
		Last Modified: Tue, 12 Aug 2025 20:18:48 GMT  
		Size: 136.4 MB (136367647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3e75a160b189532295764764c0c4c0f6da7085127009e15023e1b72426818938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f86379c07a583c6b4d2cda730067fd39c55759ad0b53a845a80d0ed1e4e918`

```dockerfile
```

-	Layers:
	-	`sha256:147a62d352cf78f202afc96c5da922c9887cda49c41d8361aea522230e478a38`  
		Last Modified: Tue, 12 Aug 2025 20:01:29 GMT  
		Size: 2.2 MB (2176816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be0156c28bdbd4005e2aaaddaa2a84801c57027018e6f11ec1c4fa445ddfc5b8`  
		Last Modified: Tue, 12 Aug 2025 20:01:30 GMT  
		Size: 13.3 KB (13281 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:b17eee212c1c210609cd565ace2921d4f51f0f558a0496bb231c2950154f072d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161749926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26e70e8ebd202849ee12a68aa118a3cafb84ced4322b51c0a63e4e677e731f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f8a63a7a987fdc761e7e8968ba27654e47f55b299e1e97fe6e51a2c4940f6`  
		Last Modified: Tue, 12 Aug 2025 18:03:01 GMT  
		Size: 1.5 MB (1455837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b282bb47e354fef0c2bcd88a6519010f31c0cb841b9d18790126035171dc4c2`  
		Last Modified: Tue, 12 Aug 2025 21:17:31 GMT  
		Size: 132.3 MB (132290870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a7266ee04452817b08fa29b0fbebd35e50f8c52e3c43404713d121b709a773db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871ca65a6cc062486ec644ccc2475fb782c5f34d8dbed69e36047adf57ec4ee6`

```dockerfile
```

-	Layers:
	-	`sha256:13e98e9c08d9ba46883f71213872667798b4bbee447ba410ee562fc0619e6aae`  
		Last Modified: Tue, 12 Aug 2025 20:01:34 GMT  
		Size: 2.2 MB (2173487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e7acb1f40aad1a6b9562ac8e788e8119165682383980dea21e0d2a7d4a518f`  
		Last Modified: Tue, 12 Aug 2025 20:01:35 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:02a04134ac3190711716059db09c2b979c136551ba87a6a95f522ad008630ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:71dd3c780e6d7c5d9e2b0679cceae79d306f56cb9940a083cf763fd21f5083aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203659556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccf2b579d7444a130c9628eb1bc3013da3f5fbd8dfbc4a7b684b64fecd2fd68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0551be367fd50b97f502140b9d811f1c3923476f5c9d50f976225fcff67022`  
		Last Modified: Tue, 12 Aug 2025 18:09:15 GMT  
		Size: 1.5 MB (1450024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34774f59a374f39e2b8157f86129828379ae33cd60f4288943a4f58483a0129`  
		Last Modified: Tue, 12 Aug 2025 18:09:36 GMT  
		Size: 172.7 MB (172672539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6cacd89c775ce34719f3eea6c3196f07870f2331513ec42fb3dd3457fa943851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe95e5479e5d256a258f6945f921cb3515e0fd863c73c30c2dfe4845140eae0`

```dockerfile
```

-	Layers:
	-	`sha256:88488c5add82f58c63243bb4ccc8b637bdac3d54637eca5209b5c4f80b390112`  
		Last Modified: Tue, 12 Aug 2025 20:01:35 GMT  
		Size: 3.1 MB (3083846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b1e970f30ce4ceb1f9bd09b82cd795acc572a2b441d0adcdd1d59433d6df5b0`  
		Last Modified: Tue, 12 Aug 2025 20:01:36 GMT  
		Size: 12.6 KB (12641 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1e86e6da9c3d0628c22a79554382f4046073124f8bc7a8bd37572f5c98a1176f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209795573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a7ffdd882315282737991187aa858b558e300b102463d8953f6664a52b688c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2927a1e71e8665a0426e9c87b474fb1e405fba2f397cd65dfa47740d2204a7b`  
		Last Modified: Tue, 12 Aug 2025 18:23:37 GMT  
		Size: 1.5 MB (1536169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a1e9cd76df11cf884d2a1f9ade58772e0f6f878920b9ef002ff05b94bbbe60`  
		Last Modified: Tue, 12 Aug 2025 20:15:54 GMT  
		Size: 173.8 MB (173816259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a98532efc4d173d65a1b144acf49feaf5991d98f2df96e836dc399cc91180c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d8d29c3b9b6e350f085e580acd5348080b29cb99f860b2f27d383dbbfbd2c2`

```dockerfile
```

-	Layers:
	-	`sha256:8b9486f4423ba6c45e98c9d03eb847f33fd7a952a09f4902f2da744e989b73ff`  
		Last Modified: Tue, 12 Aug 2025 20:01:41 GMT  
		Size: 3.1 MB (3069795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f3c0c3c64f6f94b6a5f23f3feedfb4cc76a07070d2f419acb73753beaa32b2`  
		Last Modified: Tue, 12 Aug 2025 20:01:43 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:cdbe31c5a853d1cdbbda046216675e50ee4cdd92a79d7e44dde2b6dc83be8bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192089078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce384e75bfbbc061a912960fe4538008d58daaeb67fa309d1c3fe7452cf25d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f8a63a7a987fdc761e7e8968ba27654e47f55b299e1e97fe6e51a2c4940f6`  
		Last Modified: Tue, 12 Aug 2025 18:03:01 GMT  
		Size: 1.5 MB (1455837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397ca2c90bb4662b9b3e972a6aac6702d5fa9aa6d3bab89fbf5f367416c6f7d2`  
		Last Modified: Tue, 12 Aug 2025 19:02:25 GMT  
		Size: 162.6 MB (162630022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c4f4af4678045deb56e7a72f930f14f5fd5c0591a45bf57cb029521408e52cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2769803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153e32ae64130eb38337d1b8bac21f5e1b9844a7c5c46b2433d2a8bf796b506d`

```dockerfile
```

-	Layers:
	-	`sha256:da1a452985b329cf02fff48495d6b4cfd7f76825847ed126e837c5d65a3b4eb0`  
		Last Modified: Tue, 12 Aug 2025 20:01:48 GMT  
		Size: 2.8 MB (2757162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf0ea98abc378c80f19f33aa0a0f75e77e40d106b8c8249802dfb4550c89b1d`  
		Last Modified: Tue, 12 Aug 2025 20:01:49 GMT  
		Size: 12.6 KB (12641 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:fc1ac1b535770add2d6c973709bac8a4c9db14df9e2aead3ec156aa1a6e5f04f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:54bb953981048a74381518f07c825002bfb6e64044490e340bc3bb198542e1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101766532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbc9424a617e5020ffd85e33b3e0f4e22d756ec4fe5a1041c8b0aa13c43a2e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e82fa24af564814fde5b9935935ddcee4a20f1a264469802f41069e3b38f8bf8';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3ccbe3ca1ffd097f40b06e7c4f31f4a38de361e5c8116ffd4a030df5f5303519';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bcf97b069ac7fbc7dffee303e1934917668d73af2a9b426ccb1b91e76e46eee0';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4185aac8297b90cd44b5b3d2584f9dd03e25f1834e93bb9b0f59da6c16bb8f3`  
		Last Modified: Tue, 12 Aug 2025 17:25:40 GMT  
		Size: 1.5 MB (1450096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2588de7108140d8c28ea836579bce61d2a2f8bf9f6d6271c638ae2f3fbb23159`  
		Last Modified: Tue, 12 Aug 2025 17:25:46 GMT  
		Size: 70.8 MB (70779443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:18d0f40a7f6185ae46775029d6ef14aa4f17601153d07d29bdd0a516e735ae57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3627e520f8675050cb7e7a3211660e1ce0657f6e4ca81c6186264c829f6aaf`

```dockerfile
```

-	Layers:
	-	`sha256:06ef88c71a526377d1bf2ab3fc947fb91ad60263d1539682d8988edf6fe6e522`  
		Last Modified: Tue, 12 Aug 2025 20:01:44 GMT  
		Size: 2.2 MB (2155957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4315e02f1c2733e9b508891f71a29bb8e531126c0a1e2d8d1d65794e24cc48de`  
		Last Modified: Tue, 12 Aug 2025 20:01:45 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1c8748796d625abd66e9b5cc79ca70e7a5ab61f15dc92f278b0330f531da70c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107698269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de451c6b226fdf22be432565c59f3e4846ace77e934be13d56f88cacc9601dae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e82fa24af564814fde5b9935935ddcee4a20f1a264469802f41069e3b38f8bf8';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3ccbe3ca1ffd097f40b06e7c4f31f4a38de361e5c8116ffd4a030df5f5303519';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bcf97b069ac7fbc7dffee303e1934917668d73af2a9b426ccb1b91e76e46eee0';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2927a1e71e8665a0426e9c87b474fb1e405fba2f397cd65dfa47740d2204a7b`  
		Last Modified: Tue, 12 Aug 2025 18:23:37 GMT  
		Size: 1.5 MB (1536169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f5e673ca196e9434dbf8bf58d7e62169c42935620c154b6db579b0620bb667`  
		Last Modified: Wed, 13 Aug 2025 04:00:54 GMT  
		Size: 71.7 MB (71718955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:65191572d2ad45f88577167c0882c79a00d04d5f91855a15d803a6d73653083f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9635f81d1ee5374ccd0f856f8ff7735687f4fbcf27f39b4984bb437503c030f5`

```dockerfile
```

-	Layers:
	-	`sha256:39fbbedafeed61727ea9f7efe3da4c19baa82f5e15303003b3a275ea7ed40448`  
		Last Modified: Tue, 12 Aug 2025 20:01:49 GMT  
		Size: 2.2 MB (2160458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6e20f5edb7ca943c5703954963cbff2096538a0225d27c2e26c2409c31dfa8`  
		Last Modified: Tue, 12 Aug 2025 20:01:50 GMT  
		Size: 12.7 KB (12677 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:06d848e6e143fee8c47ee90f0f530a9fc0cf8621b831cd089dcb1b5c251a5c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100736932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5058f7727ce3136116d875dacf8d95a5496198851cb5964d4d355caa17b68936`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e82fa24af564814fde5b9935935ddcee4a20f1a264469802f41069e3b38f8bf8';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3ccbe3ca1ffd097f40b06e7c4f31f4a38de361e5c8116ffd4a030df5f5303519';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bcf97b069ac7fbc7dffee303e1934917668d73af2a9b426ccb1b91e76e46eee0';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f8a63a7a987fdc761e7e8968ba27654e47f55b299e1e97fe6e51a2c4940f6`  
		Last Modified: Tue, 12 Aug 2025 18:03:01 GMT  
		Size: 1.5 MB (1455837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c41df9e93244c5db11d8c38190d7c3a2277266bcee1539276a8f8046150d9f`  
		Last Modified: Tue, 12 Aug 2025 18:03:52 GMT  
		Size: 71.3 MB (71277876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ba3c040b155eebce6a54645deaa27fbd301696c7e50d6a6769aaa112b678536e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ef2320d1fec929d66ca694b7221e6d967979102f7c2b229cfd764bac5d0840`

```dockerfile
```

-	Layers:
	-	`sha256:dff5993b2c233316904b716d5e05b20400fd02a256c815f0462acf75ebf52ff4`  
		Last Modified: Tue, 12 Aug 2025 20:01:55 GMT  
		Size: 2.2 MB (2159579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35de9795555730ef8b1c91e2b2ed3ca8412f7f965cb46d54d6e186354169ea40`  
		Last Modified: Tue, 12 Aug 2025 20:01:56 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:9626481da11b946704196b63dc021c686cf95027e392f545805c0522a4428eef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:6494d2f1b139f4557657d36a81d52d4b79b4816f5fb0865b0476df6135fdcbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166406112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f73d18f316ea22dd6db3b58c9a9c095effda288fa0ea021e215be4449ff46f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f2eec3d528eb5b5110c2bb9812d5a2c27a080f85b313e063387bfdb6166e8e`  
		Last Modified: Tue, 12 Aug 2025 17:26:04 GMT  
		Size: 1.5 MB (1450029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ad216cec582a4c9420675953629f4cdc5046ba2fecc126a371479369d618a`  
		Last Modified: Tue, 12 Aug 2025 17:59:13 GMT  
		Size: 135.4 MB (135419090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5befd233eb606ca2c38f93db5e80065f47a67d43accc2031e1409761f388a64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5464d9d18132df98ae8bc2b24ec9d560f05f9c18228173eff52e76b4768132d`

```dockerfile
```

-	Layers:
	-	`sha256:c2442617ed8b1550a6eba8f16e0795e994941e7ceb1485c422fa4aefa6c77d85`  
		Last Modified: Tue, 12 Aug 2025 20:01:24 GMT  
		Size: 2.2 MB (2173526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e98a836f1739539f81e16c1702577bcc44500b156a16e89f9f07dd4c9b9186e3`  
		Last Modified: Tue, 12 Aug 2025 20:01:24 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:d08ec4e0d92aa197707efec98f5f6c2a20e280f8e997428c6b24ae8114fae273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172346961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acbe6b6c2592137856f658f477e81176424e1f8f1b5905e63d2c3c4b1953e1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2927a1e71e8665a0426e9c87b474fb1e405fba2f397cd65dfa47740d2204a7b`  
		Last Modified: Tue, 12 Aug 2025 18:23:37 GMT  
		Size: 1.5 MB (1536169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38acb531b224a8c9fbff4a5b8df38d3d05236be9b6ece3c83de72a8e11e1997`  
		Last Modified: Tue, 12 Aug 2025 20:18:48 GMT  
		Size: 136.4 MB (136367647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3e75a160b189532295764764c0c4c0f6da7085127009e15023e1b72426818938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f86379c07a583c6b4d2cda730067fd39c55759ad0b53a845a80d0ed1e4e918`

```dockerfile
```

-	Layers:
	-	`sha256:147a62d352cf78f202afc96c5da922c9887cda49c41d8361aea522230e478a38`  
		Last Modified: Tue, 12 Aug 2025 20:01:29 GMT  
		Size: 2.2 MB (2176816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be0156c28bdbd4005e2aaaddaa2a84801c57027018e6f11ec1c4fa445ddfc5b8`  
		Last Modified: Tue, 12 Aug 2025 20:01:30 GMT  
		Size: 13.3 KB (13281 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:b17eee212c1c210609cd565ace2921d4f51f0f558a0496bb231c2950154f072d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161749926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26e70e8ebd202849ee12a68aa118a3cafb84ced4322b51c0a63e4e677e731f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f8a63a7a987fdc761e7e8968ba27654e47f55b299e1e97fe6e51a2c4940f6`  
		Last Modified: Tue, 12 Aug 2025 18:03:01 GMT  
		Size: 1.5 MB (1455837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b282bb47e354fef0c2bcd88a6519010f31c0cb841b9d18790126035171dc4c2`  
		Last Modified: Tue, 12 Aug 2025 21:17:31 GMT  
		Size: 132.3 MB (132290870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a7266ee04452817b08fa29b0fbebd35e50f8c52e3c43404713d121b709a773db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871ca65a6cc062486ec644ccc2475fb782c5f34d8dbed69e36047adf57ec4ee6`

```dockerfile
```

-	Layers:
	-	`sha256:13e98e9c08d9ba46883f71213872667798b4bbee447ba410ee562fc0619e6aae`  
		Last Modified: Tue, 12 Aug 2025 20:01:34 GMT  
		Size: 2.2 MB (2173487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e7acb1f40aad1a6b9562ac8e788e8119165682383980dea21e0d2a7d4a518f`  
		Last Modified: Tue, 12 Aug 2025 20:01:35 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:9626481da11b946704196b63dc021c686cf95027e392f545805c0522a4428eef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:6494d2f1b139f4557657d36a81d52d4b79b4816f5fb0865b0476df6135fdcbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166406112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f73d18f316ea22dd6db3b58c9a9c095effda288fa0ea021e215be4449ff46f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f2eec3d528eb5b5110c2bb9812d5a2c27a080f85b313e063387bfdb6166e8e`  
		Last Modified: Tue, 12 Aug 2025 17:26:04 GMT  
		Size: 1.5 MB (1450029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ad216cec582a4c9420675953629f4cdc5046ba2fecc126a371479369d618a`  
		Last Modified: Tue, 12 Aug 2025 17:59:13 GMT  
		Size: 135.4 MB (135419090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5befd233eb606ca2c38f93db5e80065f47a67d43accc2031e1409761f388a64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5464d9d18132df98ae8bc2b24ec9d560f05f9c18228173eff52e76b4768132d`

```dockerfile
```

-	Layers:
	-	`sha256:c2442617ed8b1550a6eba8f16e0795e994941e7ceb1485c422fa4aefa6c77d85`  
		Last Modified: Tue, 12 Aug 2025 20:01:24 GMT  
		Size: 2.2 MB (2173526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e98a836f1739539f81e16c1702577bcc44500b156a16e89f9f07dd4c9b9186e3`  
		Last Modified: Tue, 12 Aug 2025 20:01:24 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:d08ec4e0d92aa197707efec98f5f6c2a20e280f8e997428c6b24ae8114fae273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172346961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acbe6b6c2592137856f658f477e81176424e1f8f1b5905e63d2c3c4b1953e1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2927a1e71e8665a0426e9c87b474fb1e405fba2f397cd65dfa47740d2204a7b`  
		Last Modified: Tue, 12 Aug 2025 18:23:37 GMT  
		Size: 1.5 MB (1536169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38acb531b224a8c9fbff4a5b8df38d3d05236be9b6ece3c83de72a8e11e1997`  
		Last Modified: Tue, 12 Aug 2025 20:18:48 GMT  
		Size: 136.4 MB (136367647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3e75a160b189532295764764c0c4c0f6da7085127009e15023e1b72426818938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f86379c07a583c6b4d2cda730067fd39c55759ad0b53a845a80d0ed1e4e918`

```dockerfile
```

-	Layers:
	-	`sha256:147a62d352cf78f202afc96c5da922c9887cda49c41d8361aea522230e478a38`  
		Last Modified: Tue, 12 Aug 2025 20:01:29 GMT  
		Size: 2.2 MB (2176816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be0156c28bdbd4005e2aaaddaa2a84801c57027018e6f11ec1c4fa445ddfc5b8`  
		Last Modified: Tue, 12 Aug 2025 20:01:30 GMT  
		Size: 13.3 KB (13281 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:b17eee212c1c210609cd565ace2921d4f51f0f558a0496bb231c2950154f072d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161749926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26e70e8ebd202849ee12a68aa118a3cafb84ced4322b51c0a63e4e677e731f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ad3486554724df92b79d08ac15460631e2ef3ff44dabb50a1b8c3a3ad7e645f4';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='55de3054399a593a8561a9a6a8d4ebb3820acd0309da1974a51db184f4ab88f2';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8094b571b52e9a77a693ca7130fa1267187bced19fcb1ba7a20bf33bb30eca41';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f8a63a7a987fdc761e7e8968ba27654e47f55b299e1e97fe6e51a2c4940f6`  
		Last Modified: Tue, 12 Aug 2025 18:03:01 GMT  
		Size: 1.5 MB (1455837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b282bb47e354fef0c2bcd88a6519010f31c0cb841b9d18790126035171dc4c2`  
		Last Modified: Tue, 12 Aug 2025 21:17:31 GMT  
		Size: 132.3 MB (132290870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a7266ee04452817b08fa29b0fbebd35e50f8c52e3c43404713d121b709a773db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871ca65a6cc062486ec644ccc2475fb782c5f34d8dbed69e36047adf57ec4ee6`

```dockerfile
```

-	Layers:
	-	`sha256:13e98e9c08d9ba46883f71213872667798b4bbee447ba410ee562fc0619e6aae`  
		Last Modified: Tue, 12 Aug 2025 20:01:34 GMT  
		Size: 2.2 MB (2173487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e7acb1f40aad1a6b9562ac8e788e8119165682383980dea21e0d2a7d4a518f`  
		Last Modified: Tue, 12 Aug 2025 20:01:35 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:02a04134ac3190711716059db09c2b979c136551ba87a6a95f522ad008630ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:71dd3c780e6d7c5d9e2b0679cceae79d306f56cb9940a083cf763fd21f5083aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203659556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccf2b579d7444a130c9628eb1bc3013da3f5fbd8dfbc4a7b684b64fecd2fd68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0551be367fd50b97f502140b9d811f1c3923476f5c9d50f976225fcff67022`  
		Last Modified: Tue, 12 Aug 2025 18:09:15 GMT  
		Size: 1.5 MB (1450024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34774f59a374f39e2b8157f86129828379ae33cd60f4288943a4f58483a0129`  
		Last Modified: Tue, 12 Aug 2025 18:09:36 GMT  
		Size: 172.7 MB (172672539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6cacd89c775ce34719f3eea6c3196f07870f2331513ec42fb3dd3457fa943851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe95e5479e5d256a258f6945f921cb3515e0fd863c73c30c2dfe4845140eae0`

```dockerfile
```

-	Layers:
	-	`sha256:88488c5add82f58c63243bb4ccc8b637bdac3d54637eca5209b5c4f80b390112`  
		Last Modified: Tue, 12 Aug 2025 20:01:35 GMT  
		Size: 3.1 MB (3083846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b1e970f30ce4ceb1f9bd09b82cd795acc572a2b441d0adcdd1d59433d6df5b0`  
		Last Modified: Tue, 12 Aug 2025 20:01:36 GMT  
		Size: 12.6 KB (12641 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1e86e6da9c3d0628c22a79554382f4046073124f8bc7a8bd37572f5c98a1176f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209795573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a7ffdd882315282737991187aa858b558e300b102463d8953f6664a52b688c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2927a1e71e8665a0426e9c87b474fb1e405fba2f397cd65dfa47740d2204a7b`  
		Last Modified: Tue, 12 Aug 2025 18:23:37 GMT  
		Size: 1.5 MB (1536169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a1e9cd76df11cf884d2a1f9ade58772e0f6f878920b9ef002ff05b94bbbe60`  
		Last Modified: Tue, 12 Aug 2025 20:15:54 GMT  
		Size: 173.8 MB (173816259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a98532efc4d173d65a1b144acf49feaf5991d98f2df96e836dc399cc91180c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d8d29c3b9b6e350f085e580acd5348080b29cb99f860b2f27d383dbbfbd2c2`

```dockerfile
```

-	Layers:
	-	`sha256:8b9486f4423ba6c45e98c9d03eb847f33fd7a952a09f4902f2da744e989b73ff`  
		Last Modified: Tue, 12 Aug 2025 20:01:41 GMT  
		Size: 3.1 MB (3069795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f3c0c3c64f6f94b6a5f23f3feedfb4cc76a07070d2f419acb73753beaa32b2`  
		Last Modified: Tue, 12 Aug 2025 20:01:43 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:cdbe31c5a853d1cdbbda046216675e50ee4cdd92a79d7e44dde2b6dc83be8bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192089078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce384e75bfbbc061a912960fe4538008d58daaeb67fa309d1c3fe7452cf25d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f8a63a7a987fdc761e7e8968ba27654e47f55b299e1e97fe6e51a2c4940f6`  
		Last Modified: Tue, 12 Aug 2025 18:03:01 GMT  
		Size: 1.5 MB (1455837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397ca2c90bb4662b9b3e972a6aac6702d5fa9aa6d3bab89fbf5f367416c6f7d2`  
		Last Modified: Tue, 12 Aug 2025 19:02:25 GMT  
		Size: 162.6 MB (162630022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c4f4af4678045deb56e7a72f930f14f5fd5c0591a45bf57cb029521408e52cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2769803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153e32ae64130eb38337d1b8bac21f5e1b9844a7c5c46b2433d2a8bf796b506d`

```dockerfile
```

-	Layers:
	-	`sha256:da1a452985b329cf02fff48495d6b4cfd7f76825847ed126e837c5d65a3b4eb0`  
		Last Modified: Tue, 12 Aug 2025 20:01:48 GMT  
		Size: 2.8 MB (2757162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf0ea98abc378c80f19f33aa0a0f75e77e40d106b8c8249802dfb4550c89b1d`  
		Last Modified: Tue, 12 Aug 2025 20:01:49 GMT  
		Size: 12.6 KB (12641 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:fc1ac1b535770add2d6c973709bac8a4c9db14df9e2aead3ec156aa1a6e5f04f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:54bb953981048a74381518f07c825002bfb6e64044490e340bc3bb198542e1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101766532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbc9424a617e5020ffd85e33b3e0f4e22d756ec4fe5a1041c8b0aa13c43a2e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e82fa24af564814fde5b9935935ddcee4a20f1a264469802f41069e3b38f8bf8';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3ccbe3ca1ffd097f40b06e7c4f31f4a38de361e5c8116ffd4a030df5f5303519';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bcf97b069ac7fbc7dffee303e1934917668d73af2a9b426ccb1b91e76e46eee0';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4185aac8297b90cd44b5b3d2584f9dd03e25f1834e93bb9b0f59da6c16bb8f3`  
		Last Modified: Tue, 12 Aug 2025 17:25:40 GMT  
		Size: 1.5 MB (1450096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2588de7108140d8c28ea836579bce61d2a2f8bf9f6d6271c638ae2f3fbb23159`  
		Last Modified: Tue, 12 Aug 2025 17:25:46 GMT  
		Size: 70.8 MB (70779443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:18d0f40a7f6185ae46775029d6ef14aa4f17601153d07d29bdd0a516e735ae57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3627e520f8675050cb7e7a3211660e1ce0657f6e4ca81c6186264c829f6aaf`

```dockerfile
```

-	Layers:
	-	`sha256:06ef88c71a526377d1bf2ab3fc947fb91ad60263d1539682d8988edf6fe6e522`  
		Last Modified: Tue, 12 Aug 2025 20:01:44 GMT  
		Size: 2.2 MB (2155957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4315e02f1c2733e9b508891f71a29bb8e531126c0a1e2d8d1d65794e24cc48de`  
		Last Modified: Tue, 12 Aug 2025 20:01:45 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1c8748796d625abd66e9b5cc79ca70e7a5ab61f15dc92f278b0330f531da70c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107698269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de451c6b226fdf22be432565c59f3e4846ace77e934be13d56f88cacc9601dae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e82fa24af564814fde5b9935935ddcee4a20f1a264469802f41069e3b38f8bf8';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3ccbe3ca1ffd097f40b06e7c4f31f4a38de361e5c8116ffd4a030df5f5303519';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bcf97b069ac7fbc7dffee303e1934917668d73af2a9b426ccb1b91e76e46eee0';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2927a1e71e8665a0426e9c87b474fb1e405fba2f397cd65dfa47740d2204a7b`  
		Last Modified: Tue, 12 Aug 2025 18:23:37 GMT  
		Size: 1.5 MB (1536169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f5e673ca196e9434dbf8bf58d7e62169c42935620c154b6db579b0620bb667`  
		Last Modified: Wed, 13 Aug 2025 04:00:54 GMT  
		Size: 71.7 MB (71718955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:65191572d2ad45f88577167c0882c79a00d04d5f91855a15d803a6d73653083f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9635f81d1ee5374ccd0f856f8ff7735687f4fbcf27f39b4984bb437503c030f5`

```dockerfile
```

-	Layers:
	-	`sha256:39fbbedafeed61727ea9f7efe3da4c19baa82f5e15303003b3a275ea7ed40448`  
		Last Modified: Tue, 12 Aug 2025 20:01:49 GMT  
		Size: 2.2 MB (2160458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6e20f5edb7ca943c5703954963cbff2096538a0225d27c2e26c2409c31dfa8`  
		Last Modified: Tue, 12 Aug 2025 20:01:50 GMT  
		Size: 12.7 KB (12677 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:06d848e6e143fee8c47ee90f0f530a9fc0cf8621b831cd089dcb1b5c251a5c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100736932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5058f7727ce3136116d875dacf8d95a5496198851cb5964d4d355caa17b68936`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 06:32:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 05 Aug 2025 06:32:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_VERSION=8.0.8.50
# Tue, 05 Aug 2025 06:32:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e82fa24af564814fde5b9935935ddcee4a20f1a264469802f41069e3b38f8bf8';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3ccbe3ca1ffd097f40b06e7c4f31f4a38de361e5c8116ffd4a030df5f5303519';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bcf97b069ac7fbc7dffee303e1934917668d73af2a9b426ccb1b91e76e46eee0';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 05 Aug 2025 06:32:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f8a63a7a987fdc761e7e8968ba27654e47f55b299e1e97fe6e51a2c4940f6`  
		Last Modified: Tue, 12 Aug 2025 18:03:01 GMT  
		Size: 1.5 MB (1455837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c41df9e93244c5db11d8c38190d7c3a2277266bcee1539276a8f8046150d9f`  
		Last Modified: Tue, 12 Aug 2025 18:03:52 GMT  
		Size: 71.3 MB (71277876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ba3c040b155eebce6a54645deaa27fbd301696c7e50d6a6769aaa112b678536e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ef2320d1fec929d66ca694b7221e6d967979102f7c2b229cfd764bac5d0840`

```dockerfile
```

-	Layers:
	-	`sha256:dff5993b2c233316904b716d5e05b20400fd02a256c815f0462acf75ebf52ff4`  
		Last Modified: Tue, 12 Aug 2025 20:01:55 GMT  
		Size: 2.2 MB (2159579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35de9795555730ef8b1c91e2b2ed3ca8412f7f965cb46d54d6e186354169ea40`  
		Last Modified: Tue, 12 Aug 2025 20:01:56 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.in-toto+json
