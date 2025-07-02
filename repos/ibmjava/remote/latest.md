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
