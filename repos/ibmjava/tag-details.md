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
$ docker pull ibmjava@sha256:0ed49f9fde4a936e3666a3a3c988a0861269213055753bb572fbf064cbef142b
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
$ docker pull ibmjava@sha256:25b999f62b9f2e511af20c8eb5f1267e53712fa5ce9dbe92016cd2f8ad705de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166770465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e467561527b8887a76d4b9bbe553c4c0d945dd580923c4982720c816a13657`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c754e0c069b23f513303e7a7174dfb0bbda6dc9b2182a442c041aeaab3061`  
		Last Modified: Wed, 02 Jul 2025 03:11:27 GMT  
		Size: 1.4 MB (1449992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130dddc1476195e7e0977d2b5625d4904c73bdc63da5b56532136b598baefc8a`  
		Last Modified: Wed, 02 Jul 2025 04:15:17 GMT  
		Size: 135.8 MB (135784787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:eef124806535710dddad9db301376f87c66f0ad791ef4766cfa0169d562756cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24907a5e7483c764122fbfbe3d2a2543f99c0f4c94f546db0af432cd61c9b7b5`

```dockerfile
```

-	Layers:
	-	`sha256:2b7641176a6570be84361accd02e2966a726b640f8c5220fcad66315690bc6eb`  
		Last Modified: Wed, 02 Jul 2025 06:21:13 GMT  
		Size: 2.2 MB (2173508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:062d8aeef74cef1afdc2ed8a0e529914dd991433fb30cf78384896f6e054d7e3`  
		Last Modified: Wed, 02 Jul 2025 06:21:14 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0dfc49e54b96cab01b2d9f0faa2ac9cb8bdd23a307f8cd404b5361d8803d4bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172607671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa126710509d5aad12f8d37bf40215d1e00cc81ff6e7d8b88ebf45461da61da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f581f4e6d076b9a3a2abd7d2780b110e85ed22e65b4361103dcee628dbec2ac6`  
		Last Modified: Wed, 02 Jul 2025 03:54:24 GMT  
		Size: 136.6 MB (136628814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0490dd8aaa1965e6afcc222939705f3e1ced67fc582f169ed11c978716f95ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2dfc34f191c32be6112f2902d9b2aad5a4b67319cb0efebf9ed18a1dacac18`

```dockerfile
```

-	Layers:
	-	`sha256:7f59357e19d60da8dd7a215ac4eef83e815c18200f5322df6251115c864980b7`  
		Last Modified: Wed, 02 Jul 2025 05:01:25 GMT  
		Size: 2.2 MB (2176798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b9ee117cfb64fc03034ecce80400b9922d3c7ac1397bd1dd4b4c9ab95407e1`  
		Last Modified: Wed, 02 Jul 2025 05:01:26 GMT  
		Size: 13.8 KB (13816 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:1af138803ecd97e0d501856dc41f0ab5633080c719cc534ca6d0f4e1c61e2dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162269765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d18314c5e9da7d3fe2e0716583cd8fb02dc271fda569b95a41b74e5066302a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f78588c4bb31985140e15e675b5832054fdf1cef60bb357597ede86a9b3e5`  
		Last Modified: Wed, 02 Jul 2025 04:47:58 GMT  
		Size: 1.5 MB (1455774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd2845940d068d370a18433dcc4e1790d21632c2fbf5aeff078aa7d12b163f6`  
		Last Modified: Wed, 02 Jul 2025 04:47:51 GMT  
		Size: 132.8 MB (132811816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:1a2562601300f9c79b2848e046c0028aa547d6229a0f3fa92d2c66daa76d8f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e934f104fe176504006a48df57848170b0eb7ac3217276138fb5532b4839fcef`

```dockerfile
```

-	Layers:
	-	`sha256:72d93b03b9be0e8f8bcaecda460b1ce76172f9d3b7c869516e56c4dbb384ece2`  
		Last Modified: Wed, 02 Jul 2025 08:01:25 GMT  
		Size: 2.2 MB (2173469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57480cf5c841c8ce1dc982cff99617eebf2c8c8b6c9cc7c9012f85e2065284d`  
		Last Modified: Wed, 02 Jul 2025 08:01:26 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:0ed49f9fde4a936e3666a3a3c988a0861269213055753bb572fbf064cbef142b
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
$ docker pull ibmjava@sha256:25b999f62b9f2e511af20c8eb5f1267e53712fa5ce9dbe92016cd2f8ad705de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166770465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e467561527b8887a76d4b9bbe553c4c0d945dd580923c4982720c816a13657`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c754e0c069b23f513303e7a7174dfb0bbda6dc9b2182a442c041aeaab3061`  
		Last Modified: Wed, 02 Jul 2025 03:11:27 GMT  
		Size: 1.4 MB (1449992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130dddc1476195e7e0977d2b5625d4904c73bdc63da5b56532136b598baefc8a`  
		Last Modified: Wed, 02 Jul 2025 04:15:17 GMT  
		Size: 135.8 MB (135784787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:eef124806535710dddad9db301376f87c66f0ad791ef4766cfa0169d562756cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24907a5e7483c764122fbfbe3d2a2543f99c0f4c94f546db0af432cd61c9b7b5`

```dockerfile
```

-	Layers:
	-	`sha256:2b7641176a6570be84361accd02e2966a726b640f8c5220fcad66315690bc6eb`  
		Last Modified: Wed, 02 Jul 2025 06:21:13 GMT  
		Size: 2.2 MB (2173508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:062d8aeef74cef1afdc2ed8a0e529914dd991433fb30cf78384896f6e054d7e3`  
		Last Modified: Wed, 02 Jul 2025 06:21:14 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0dfc49e54b96cab01b2d9f0faa2ac9cb8bdd23a307f8cd404b5361d8803d4bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172607671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa126710509d5aad12f8d37bf40215d1e00cc81ff6e7d8b88ebf45461da61da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f581f4e6d076b9a3a2abd7d2780b110e85ed22e65b4361103dcee628dbec2ac6`  
		Last Modified: Wed, 02 Jul 2025 03:54:24 GMT  
		Size: 136.6 MB (136628814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0490dd8aaa1965e6afcc222939705f3e1ced67fc582f169ed11c978716f95ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2dfc34f191c32be6112f2902d9b2aad5a4b67319cb0efebf9ed18a1dacac18`

```dockerfile
```

-	Layers:
	-	`sha256:7f59357e19d60da8dd7a215ac4eef83e815c18200f5322df6251115c864980b7`  
		Last Modified: Wed, 02 Jul 2025 05:01:25 GMT  
		Size: 2.2 MB (2176798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b9ee117cfb64fc03034ecce80400b9922d3c7ac1397bd1dd4b4c9ab95407e1`  
		Last Modified: Wed, 02 Jul 2025 05:01:26 GMT  
		Size: 13.8 KB (13816 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:1af138803ecd97e0d501856dc41f0ab5633080c719cc534ca6d0f4e1c61e2dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162269765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d18314c5e9da7d3fe2e0716583cd8fb02dc271fda569b95a41b74e5066302a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f78588c4bb31985140e15e675b5832054fdf1cef60bb357597ede86a9b3e5`  
		Last Modified: Wed, 02 Jul 2025 04:47:58 GMT  
		Size: 1.5 MB (1455774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd2845940d068d370a18433dcc4e1790d21632c2fbf5aeff078aa7d12b163f6`  
		Last Modified: Wed, 02 Jul 2025 04:47:51 GMT  
		Size: 132.8 MB (132811816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:1a2562601300f9c79b2848e046c0028aa547d6229a0f3fa92d2c66daa76d8f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e934f104fe176504006a48df57848170b0eb7ac3217276138fb5532b4839fcef`

```dockerfile
```

-	Layers:
	-	`sha256:72d93b03b9be0e8f8bcaecda460b1ce76172f9d3b7c869516e56c4dbb384ece2`  
		Last Modified: Wed, 02 Jul 2025 08:01:25 GMT  
		Size: 2.2 MB (2173469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57480cf5c841c8ce1dc982cff99617eebf2c8c8b6c9cc7c9012f85e2065284d`  
		Last Modified: Wed, 02 Jul 2025 08:01:26 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:d7345ef59019c2086bc939386f4798cd6ad97a3f1c9904c84361b97d05486899
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
$ docker pull ibmjava@sha256:e6dc6d758b9e48640eb15800d8cce961ef194c7d5bcf137ca494bc01d63f26ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204168263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bbd844b9770b0c10e0b19adc84bd2f3049fc746f46de543c98198f0701f29e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f678ce4d9a60d6c998236f3e466663b67491d0de867f033ff45f466b1f53d30`  
		Last Modified: Wed, 02 Jul 2025 04:28:31 GMT  
		Size: 1.5 MB (1450007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dbef6e2a79b4a6f488821b533bbd58fc3e82c469e70b2a60b56adcdbb580e6`  
		Last Modified: Wed, 02 Jul 2025 05:05:05 GMT  
		Size: 173.2 MB (173182570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:59c2b50fdae01850d6a93ced94af2e3cac3610cf37f615ad08d156ce0d8e15ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd56d969318b3354dfcd60143885e906e6d50cd5ed5d500b2ae90ecffd5958c`

```dockerfile
```

-	Layers:
	-	`sha256:0f64110ce3adc02b2bec90987e68411cb8d6fff6b69394cab42711c1f547c4b4`  
		Last Modified: Wed, 02 Jul 2025 05:01:28 GMT  
		Size: 3.1 MB (3083828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be2a38af5c85fc51e9f3fe5aab1a30668a6461231a8e0bcd4710a88f31645f1`  
		Last Modified: Wed, 02 Jul 2025 05:01:29 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:e3365e40c4a63ab47e7997d00689a8750cead278ee316dadf0f1a3f7ee38b477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210217391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267afb8e32ffd3ef9ae2bccf716ee830296bbb97029f8e64dd766634e787329e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba99977cd9d6077fd4b307c3357787311ced4b3a091deff606c2244499c52dca`  
		Last Modified: Wed, 02 Jul 2025 05:05:40 GMT  
		Size: 174.2 MB (174238534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8e2cbe645208295d6ce8a67be9f3e35eafc43040b80a6af6c62fb6d25f4fdf7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420f9f75bab2dc52eea96bea822bf74dfdf79c4aeafc5e692c1c907b130ce32d`

```dockerfile
```

-	Layers:
	-	`sha256:2a580b888b091e828d99907782b577e4929fb7af8b70034b3c2f8704a7fccda0`  
		Last Modified: Wed, 02 Jul 2025 05:01:33 GMT  
		Size: 3.1 MB (3069777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:945afa5218986909835c1422d2582bc61260d20f147ee8cd3e743bf8e1842c55`  
		Last Modified: Wed, 02 Jul 2025 05:01:34 GMT  
		Size: 13.2 KB (13212 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:7f02b67a00b34780e004ad1e78bd99304d662f6961f3bbd5ecfa1b64dcb0cc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192755099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ceb09439d1de354bc4115aa7483a7bd74a8fe0de5f5192575a71b52c927bbc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f78588c4bb31985140e15e675b5832054fdf1cef60bb357597ede86a9b3e5`  
		Last Modified: Wed, 02 Jul 2025 04:47:58 GMT  
		Size: 1.5 MB (1455774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acdd11fc7679c3f39efc75001dc136ca312cb4002cb5acb77acf1231f881ccd`  
		Last Modified: Wed, 02 Jul 2025 04:50:56 GMT  
		Size: 163.3 MB (163297150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:59c530bf151bcb2f1aea19a399683b6d8d9bdfdb4ed5c2d470c6af6223a41728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2770322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bd5f21650a301443a601f375c144eecd5dd40d4db9bade4d1c1e53a4e61c1d`

```dockerfile
```

-	Layers:
	-	`sha256:3b8c7cbabb232064664a92fee4de9a58d84976894a8a2429388dad1cffdb8bde`  
		Last Modified: Wed, 02 Jul 2025 08:01:32 GMT  
		Size: 2.8 MB (2757144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce641c03a91d67932096d85ca668f0415aeb757da7821bfe7477b547c91194b`  
		Last Modified: Wed, 02 Jul 2025 08:01:33 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:e041d15f6abe07a37d6defdcb81c3aa56b5b66bde34591763420ed01a3e29fbc
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
$ docker pull ibmjava@sha256:f65bd073daedb49ed96802b60a76f60119b31e755431165c909ccf2d0dbba269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101481307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2eee2c497b4bcd0e07509983c88e6dee908c0234575ca514ac4392d3a2e696`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d6a70c8cfbaff37e547ebecf7b3ad0758bfb5289727983c56aa59c351a0026`  
		Last Modified: Wed, 02 Jul 2025 03:11:21 GMT  
		Size: 1.5 MB (1450016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0edd65963a4164de0d591d28a7fa637d8a55f8059bf8909fc2eb308395c09be`  
		Last Modified: Wed, 02 Jul 2025 03:11:26 GMT  
		Size: 70.5 MB (70495605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5a88e7f28b4a1d36de3580b70b1332e328c78e543bc84f4d65e581ee74812303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47467b5a1d6ef284a8136d436a11f46fb18d8e688f7ee3fb1021c1b54409594`

```dockerfile
```

-	Layers:
	-	`sha256:02f800dfa9063efbc4c3a838a283f891bb91d9751eb26d90d530e95c57ce42f2`  
		Last Modified: Wed, 02 Jul 2025 08:01:32 GMT  
		Size: 2.2 MB (2155939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1775d7d9d6cba9c0132d826a03a9cd2d7acb92cd1ec6ebe326ba6fcff1ffc800`  
		Last Modified: Wed, 02 Jul 2025 08:01:32 GMT  
		Size: 13.2 KB (13180 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:f79d9191c2cfd63a96e6104b819c0a7e5fcaa6935ef4ae9e712668f0c03f94d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107307499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c70aece4bce65f968965847dc6fa280d3cfd62a5160edbf632c9d9b15729da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b508e78ad839eb5804b4140d689c487ab1a9a5ee9bf667cf9d4f054b0f8aa3c`  
		Last Modified: Wed, 02 Jul 2025 03:55:31 GMT  
		Size: 71.3 MB (71328642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3d952bf4ba0008d0443b61c87f05520f6967a47d4dadf989491a93cec747473c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9310ab59c178144de5d53c77bfe20c325f5f00e0f4293e4b036a8aa4558b4`

```dockerfile
```

-	Layers:
	-	`sha256:5d99fc4ae86321e2a3eb17e319204cf5633501cf2c3fe9242c24a88a74f84451`  
		Last Modified: Wed, 02 Jul 2025 05:01:39 GMT  
		Size: 2.2 MB (2160440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cb3a42bca34bb15e981eeb6605c067349398490bf65c4b242538754665e3fc`  
		Last Modified: Wed, 02 Jul 2025 05:01:39 GMT  
		Size: 13.2 KB (13215 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:b61fcc1e3394922624f0fdb0fc3b2347aba3a05bb3358635e4f62babbc240ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100549501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b655ffbc6779da83e76f5aa0d8f03cd71161a0141acb526da3ca8ad54e88122`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f78588c4bb31985140e15e675b5832054fdf1cef60bb357597ede86a9b3e5`  
		Last Modified: Wed, 02 Jul 2025 04:47:58 GMT  
		Size: 1.5 MB (1455774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bdb28d67633587c8dee48a18d043dd21029b1a1d5da6d4773f8fce9a5fdda9`  
		Last Modified: Wed, 02 Jul 2025 04:49:58 GMT  
		Size: 71.1 MB (71091552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9816e5997f5b5c386169983e8580805733c89dd4b5962060b78879bd2ff259ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fddbb029316ccf02e292a218584f912b16df652872954b7a3a1cef655e123ea5`

```dockerfile
```

-	Layers:
	-	`sha256:d7df4a294962a55647be2bf3df71e1fddbdfbdc8ef889c7875f15ef3df5c6cc4`  
		Last Modified: Wed, 02 Jul 2025 08:01:39 GMT  
		Size: 2.2 MB (2159561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3011ea50a23a02def12b297ef9343fcb0dc50380c23bf76bc8372c6e06a1326`  
		Last Modified: Wed, 02 Jul 2025 08:01:40 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:0ed49f9fde4a936e3666a3a3c988a0861269213055753bb572fbf064cbef142b
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
$ docker pull ibmjava@sha256:25b999f62b9f2e511af20c8eb5f1267e53712fa5ce9dbe92016cd2f8ad705de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166770465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e467561527b8887a76d4b9bbe553c4c0d945dd580923c4982720c816a13657`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c754e0c069b23f513303e7a7174dfb0bbda6dc9b2182a442c041aeaab3061`  
		Last Modified: Wed, 02 Jul 2025 03:11:27 GMT  
		Size: 1.4 MB (1449992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130dddc1476195e7e0977d2b5625d4904c73bdc63da5b56532136b598baefc8a`  
		Last Modified: Wed, 02 Jul 2025 04:15:17 GMT  
		Size: 135.8 MB (135784787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:eef124806535710dddad9db301376f87c66f0ad791ef4766cfa0169d562756cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24907a5e7483c764122fbfbe3d2a2543f99c0f4c94f546db0af432cd61c9b7b5`

```dockerfile
```

-	Layers:
	-	`sha256:2b7641176a6570be84361accd02e2966a726b640f8c5220fcad66315690bc6eb`  
		Last Modified: Wed, 02 Jul 2025 06:21:13 GMT  
		Size: 2.2 MB (2173508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:062d8aeef74cef1afdc2ed8a0e529914dd991433fb30cf78384896f6e054d7e3`  
		Last Modified: Wed, 02 Jul 2025 06:21:14 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0dfc49e54b96cab01b2d9f0faa2ac9cb8bdd23a307f8cd404b5361d8803d4bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172607671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa126710509d5aad12f8d37bf40215d1e00cc81ff6e7d8b88ebf45461da61da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f581f4e6d076b9a3a2abd7d2780b110e85ed22e65b4361103dcee628dbec2ac6`  
		Last Modified: Wed, 02 Jul 2025 03:54:24 GMT  
		Size: 136.6 MB (136628814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0490dd8aaa1965e6afcc222939705f3e1ced67fc582f169ed11c978716f95ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2dfc34f191c32be6112f2902d9b2aad5a4b67319cb0efebf9ed18a1dacac18`

```dockerfile
```

-	Layers:
	-	`sha256:7f59357e19d60da8dd7a215ac4eef83e815c18200f5322df6251115c864980b7`  
		Last Modified: Wed, 02 Jul 2025 05:01:25 GMT  
		Size: 2.2 MB (2176798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b9ee117cfb64fc03034ecce80400b9922d3c7ac1397bd1dd4b4c9ab95407e1`  
		Last Modified: Wed, 02 Jul 2025 05:01:26 GMT  
		Size: 13.8 KB (13816 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:1af138803ecd97e0d501856dc41f0ab5633080c719cc534ca6d0f4e1c61e2dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162269765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d18314c5e9da7d3fe2e0716583cd8fb02dc271fda569b95a41b74e5066302a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f78588c4bb31985140e15e675b5832054fdf1cef60bb357597ede86a9b3e5`  
		Last Modified: Wed, 02 Jul 2025 04:47:58 GMT  
		Size: 1.5 MB (1455774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd2845940d068d370a18433dcc4e1790d21632c2fbf5aeff078aa7d12b163f6`  
		Last Modified: Wed, 02 Jul 2025 04:47:51 GMT  
		Size: 132.8 MB (132811816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:1a2562601300f9c79b2848e046c0028aa547d6229a0f3fa92d2c66daa76d8f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e934f104fe176504006a48df57848170b0eb7ac3217276138fb5532b4839fcef`

```dockerfile
```

-	Layers:
	-	`sha256:72d93b03b9be0e8f8bcaecda460b1ce76172f9d3b7c869516e56c4dbb384ece2`  
		Last Modified: Wed, 02 Jul 2025 08:01:25 GMT  
		Size: 2.2 MB (2173469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57480cf5c841c8ce1dc982cff99617eebf2c8c8b6c9cc7c9012f85e2065284d`  
		Last Modified: Wed, 02 Jul 2025 08:01:26 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:0ed49f9fde4a936e3666a3a3c988a0861269213055753bb572fbf064cbef142b
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
$ docker pull ibmjava@sha256:25b999f62b9f2e511af20c8eb5f1267e53712fa5ce9dbe92016cd2f8ad705de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166770465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e467561527b8887a76d4b9bbe553c4c0d945dd580923c4982720c816a13657`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c754e0c069b23f513303e7a7174dfb0bbda6dc9b2182a442c041aeaab3061`  
		Last Modified: Wed, 02 Jul 2025 03:11:27 GMT  
		Size: 1.4 MB (1449992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130dddc1476195e7e0977d2b5625d4904c73bdc63da5b56532136b598baefc8a`  
		Last Modified: Wed, 02 Jul 2025 04:15:17 GMT  
		Size: 135.8 MB (135784787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:eef124806535710dddad9db301376f87c66f0ad791ef4766cfa0169d562756cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24907a5e7483c764122fbfbe3d2a2543f99c0f4c94f546db0af432cd61c9b7b5`

```dockerfile
```

-	Layers:
	-	`sha256:2b7641176a6570be84361accd02e2966a726b640f8c5220fcad66315690bc6eb`  
		Last Modified: Wed, 02 Jul 2025 06:21:13 GMT  
		Size: 2.2 MB (2173508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:062d8aeef74cef1afdc2ed8a0e529914dd991433fb30cf78384896f6e054d7e3`  
		Last Modified: Wed, 02 Jul 2025 06:21:14 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0dfc49e54b96cab01b2d9f0faa2ac9cb8bdd23a307f8cd404b5361d8803d4bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172607671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa126710509d5aad12f8d37bf40215d1e00cc81ff6e7d8b88ebf45461da61da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f581f4e6d076b9a3a2abd7d2780b110e85ed22e65b4361103dcee628dbec2ac6`  
		Last Modified: Wed, 02 Jul 2025 03:54:24 GMT  
		Size: 136.6 MB (136628814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0490dd8aaa1965e6afcc222939705f3e1ced67fc582f169ed11c978716f95ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2dfc34f191c32be6112f2902d9b2aad5a4b67319cb0efebf9ed18a1dacac18`

```dockerfile
```

-	Layers:
	-	`sha256:7f59357e19d60da8dd7a215ac4eef83e815c18200f5322df6251115c864980b7`  
		Last Modified: Wed, 02 Jul 2025 05:01:25 GMT  
		Size: 2.2 MB (2176798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b9ee117cfb64fc03034ecce80400b9922d3c7ac1397bd1dd4b4c9ab95407e1`  
		Last Modified: Wed, 02 Jul 2025 05:01:26 GMT  
		Size: 13.8 KB (13816 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:1af138803ecd97e0d501856dc41f0ab5633080c719cc534ca6d0f4e1c61e2dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162269765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d18314c5e9da7d3fe2e0716583cd8fb02dc271fda569b95a41b74e5066302a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f78588c4bb31985140e15e675b5832054fdf1cef60bb357597ede86a9b3e5`  
		Last Modified: Wed, 02 Jul 2025 04:47:58 GMT  
		Size: 1.5 MB (1455774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd2845940d068d370a18433dcc4e1790d21632c2fbf5aeff078aa7d12b163f6`  
		Last Modified: Wed, 02 Jul 2025 04:47:51 GMT  
		Size: 132.8 MB (132811816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:1a2562601300f9c79b2848e046c0028aa547d6229a0f3fa92d2c66daa76d8f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e934f104fe176504006a48df57848170b0eb7ac3217276138fb5532b4839fcef`

```dockerfile
```

-	Layers:
	-	`sha256:72d93b03b9be0e8f8bcaecda460b1ce76172f9d3b7c869516e56c4dbb384ece2`  
		Last Modified: Wed, 02 Jul 2025 08:01:25 GMT  
		Size: 2.2 MB (2173469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57480cf5c841c8ce1dc982cff99617eebf2c8c8b6c9cc7c9012f85e2065284d`  
		Last Modified: Wed, 02 Jul 2025 08:01:26 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:d7345ef59019c2086bc939386f4798cd6ad97a3f1c9904c84361b97d05486899
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
$ docker pull ibmjava@sha256:e6dc6d758b9e48640eb15800d8cce961ef194c7d5bcf137ca494bc01d63f26ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204168263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bbd844b9770b0c10e0b19adc84bd2f3049fc746f46de543c98198f0701f29e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f678ce4d9a60d6c998236f3e466663b67491d0de867f033ff45f466b1f53d30`  
		Last Modified: Wed, 02 Jul 2025 04:28:31 GMT  
		Size: 1.5 MB (1450007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dbef6e2a79b4a6f488821b533bbd58fc3e82c469e70b2a60b56adcdbb580e6`  
		Last Modified: Wed, 02 Jul 2025 05:05:05 GMT  
		Size: 173.2 MB (173182570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:59c2b50fdae01850d6a93ced94af2e3cac3610cf37f615ad08d156ce0d8e15ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd56d969318b3354dfcd60143885e906e6d50cd5ed5d500b2ae90ecffd5958c`

```dockerfile
```

-	Layers:
	-	`sha256:0f64110ce3adc02b2bec90987e68411cb8d6fff6b69394cab42711c1f547c4b4`  
		Last Modified: Wed, 02 Jul 2025 05:01:28 GMT  
		Size: 3.1 MB (3083828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be2a38af5c85fc51e9f3fe5aab1a30668a6461231a8e0bcd4710a88f31645f1`  
		Last Modified: Wed, 02 Jul 2025 05:01:29 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:e3365e40c4a63ab47e7997d00689a8750cead278ee316dadf0f1a3f7ee38b477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210217391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267afb8e32ffd3ef9ae2bccf716ee830296bbb97029f8e64dd766634e787329e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba99977cd9d6077fd4b307c3357787311ced4b3a091deff606c2244499c52dca`  
		Last Modified: Wed, 02 Jul 2025 05:05:40 GMT  
		Size: 174.2 MB (174238534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8e2cbe645208295d6ce8a67be9f3e35eafc43040b80a6af6c62fb6d25f4fdf7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420f9f75bab2dc52eea96bea822bf74dfdf79c4aeafc5e692c1c907b130ce32d`

```dockerfile
```

-	Layers:
	-	`sha256:2a580b888b091e828d99907782b577e4929fb7af8b70034b3c2f8704a7fccda0`  
		Last Modified: Wed, 02 Jul 2025 05:01:33 GMT  
		Size: 3.1 MB (3069777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:945afa5218986909835c1422d2582bc61260d20f147ee8cd3e743bf8e1842c55`  
		Last Modified: Wed, 02 Jul 2025 05:01:34 GMT  
		Size: 13.2 KB (13212 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:7f02b67a00b34780e004ad1e78bd99304d662f6961f3bbd5ecfa1b64dcb0cc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192755099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ceb09439d1de354bc4115aa7483a7bd74a8fe0de5f5192575a71b52c927bbc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76942795a2ee0718be559c1dabc23764b0c7d2a6f217c758c085db217df1d0b4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a53dc2a93d95396abf46deb7daaa98b5b275b7f20316eb11e864fa6f432f2344';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='60268b6e0a10391b7be735622fb7dccfd3a2164b9fb0d2b31b811f8a0d3f1969';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='1c22096bff67c7d066f3534e5e820ceb7f5dbd16050bbf2d4c575771ebc62160';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f78588c4bb31985140e15e675b5832054fdf1cef60bb357597ede86a9b3e5`  
		Last Modified: Wed, 02 Jul 2025 04:47:58 GMT  
		Size: 1.5 MB (1455774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acdd11fc7679c3f39efc75001dc136ca312cb4002cb5acb77acf1231f881ccd`  
		Last Modified: Wed, 02 Jul 2025 04:50:56 GMT  
		Size: 163.3 MB (163297150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:59c530bf151bcb2f1aea19a399683b6d8d9bdfdb4ed5c2d470c6af6223a41728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2770322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bd5f21650a301443a601f375c144eecd5dd40d4db9bade4d1c1e53a4e61c1d`

```dockerfile
```

-	Layers:
	-	`sha256:3b8c7cbabb232064664a92fee4de9a58d84976894a8a2429388dad1cffdb8bde`  
		Last Modified: Wed, 02 Jul 2025 08:01:32 GMT  
		Size: 2.8 MB (2757144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce641c03a91d67932096d85ca668f0415aeb757da7821bfe7477b547c91194b`  
		Last Modified: Wed, 02 Jul 2025 08:01:33 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:e041d15f6abe07a37d6defdcb81c3aa56b5b66bde34591763420ed01a3e29fbc
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
$ docker pull ibmjava@sha256:f65bd073daedb49ed96802b60a76f60119b31e755431165c909ccf2d0dbba269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101481307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2eee2c497b4bcd0e07509983c88e6dee908c0234575ca514ac4392d3a2e696`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d6a70c8cfbaff37e547ebecf7b3ad0758bfb5289727983c56aa59c351a0026`  
		Last Modified: Wed, 02 Jul 2025 03:11:21 GMT  
		Size: 1.5 MB (1450016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0edd65963a4164de0d591d28a7fa637d8a55f8059bf8909fc2eb308395c09be`  
		Last Modified: Wed, 02 Jul 2025 03:11:26 GMT  
		Size: 70.5 MB (70495605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5a88e7f28b4a1d36de3580b70b1332e328c78e543bc84f4d65e581ee74812303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47467b5a1d6ef284a8136d436a11f46fb18d8e688f7ee3fb1021c1b54409594`

```dockerfile
```

-	Layers:
	-	`sha256:02f800dfa9063efbc4c3a838a283f891bb91d9751eb26d90d530e95c57ce42f2`  
		Last Modified: Wed, 02 Jul 2025 08:01:32 GMT  
		Size: 2.2 MB (2155939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1775d7d9d6cba9c0132d826a03a9cd2d7acb92cd1ec6ebe326ba6fcff1ffc800`  
		Last Modified: Wed, 02 Jul 2025 08:01:32 GMT  
		Size: 13.2 KB (13180 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:f79d9191c2cfd63a96e6104b819c0a7e5fcaa6935ef4ae9e712668f0c03f94d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107307499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c70aece4bce65f968965847dc6fa280d3cfd62a5160edbf632c9d9b15729da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adae4e5e966fdb60721d1f6006c2226f172b1ae6a4af6df07a882f4566c21aa`  
		Last Modified: Wed, 02 Jul 2025 03:54:31 GMT  
		Size: 1.5 MB (1536236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b508e78ad839eb5804b4140d689c487ab1a9a5ee9bf667cf9d4f054b0f8aa3c`  
		Last Modified: Wed, 02 Jul 2025 03:55:31 GMT  
		Size: 71.3 MB (71328642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3d952bf4ba0008d0443b61c87f05520f6967a47d4dadf989491a93cec747473c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9310ab59c178144de5d53c77bfe20c325f5f00e0f4293e4b036a8aa4558b4`

```dockerfile
```

-	Layers:
	-	`sha256:5d99fc4ae86321e2a3eb17e319204cf5633501cf2c3fe9242c24a88a74f84451`  
		Last Modified: Wed, 02 Jul 2025 05:01:39 GMT  
		Size: 2.2 MB (2160440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cb3a42bca34bb15e981eeb6605c067349398490bf65c4b242538754665e3fc`  
		Last Modified: Wed, 02 Jul 2025 05:01:39 GMT  
		Size: 13.2 KB (13215 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:b61fcc1e3394922624f0fdb0fc3b2347aba3a05bb3358635e4f62babbc240ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100549501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b655ffbc6779da83e76f5aa0d8f03cd71161a0141acb526da3ca8ad54e88122`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='239ef4f6f8cff3697f6e5bb9b5404a9d8d7f7e5d9987c4d74729862b6e9de06f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='fc256d39206fbfc963c3c2c54a4d1ed02388c9bcc0179bf2bc1a1d608366ee05';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='309de530a77619b79d3f12252dcbe4dffa64dfc5b3a53b6b53b25e1bdbcc71e4';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='b6ff95ae9ce9fa95cd8a83bff079e9150d0f015a1053a4b429cab0ec21a3aa06';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f78588c4bb31985140e15e675b5832054fdf1cef60bb357597ede86a9b3e5`  
		Last Modified: Wed, 02 Jul 2025 04:47:58 GMT  
		Size: 1.5 MB (1455774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bdb28d67633587c8dee48a18d043dd21029b1a1d5da6d4773f8fce9a5fdda9`  
		Last Modified: Wed, 02 Jul 2025 04:49:58 GMT  
		Size: 71.1 MB (71091552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9816e5997f5b5c386169983e8580805733c89dd4b5962060b78879bd2ff259ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fddbb029316ccf02e292a218584f912b16df652872954b7a3a1cef655e123ea5`

```dockerfile
```

-	Layers:
	-	`sha256:d7df4a294962a55647be2bf3df71e1fddbdfbdc8ef889c7875f15ef3df5c6cc4`  
		Last Modified: Wed, 02 Jul 2025 08:01:39 GMT  
		Size: 2.2 MB (2159561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3011ea50a23a02def12b297ef9343fcb0dc50380c23bf76bc8372c6e06a1326`  
		Last Modified: Wed, 02 Jul 2025 08:01:40 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json
