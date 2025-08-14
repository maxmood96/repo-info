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
