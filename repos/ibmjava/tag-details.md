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
$ docker pull ibmjava@sha256:8ca47a39b839fd6c1f4d8d48ce78ef58020a08feed9df894be8b019651a4134c
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
$ docker pull ibmjava@sha256:7245fde91c1be7da7a50557896acdf9229b49a08959ba06b35d1b49087ef0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166767680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069ac94cfd8c83384048e40b5593f987f9a84bcdefb22f0c57e944e5b36b9d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8803db35073b2740da6f9573de7c61691c99ce2638f0e6818c242609f4f3417e`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 1.5 MB (1450255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa120ccd89f04004bf22720a697c7c4a886668c5f0b4bf862447e6a0849572e`  
		Last Modified: Wed, 14 May 2025 19:35:24 GMT  
		Size: 135.8 MB (135784811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:003c5b38b46e7699d817326b40d7d64b9162ba797e82ebfe35ab8d470f6fda56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279184ce7d75118cf6dce892168413cbf9fa99eabb48b61a16c68fa5bc822bf`

```dockerfile
```

-	Layers:
	-	`sha256:729b3ff94df155855b23bf5b281b6da76989fff0bf2271fc08116331c2d86938`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 2.1 MB (2051990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384ce414ff4f341cc543f84db1f5a5fd6af0420b3cab8b20754d964ed93c46b5`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:9514a8f8a3e54d798c90be72d94c6a184fb051ebd1aa03c7d46ec43d9d67312f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172608317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625a932b3b2b3d38c553d7ed0788d6687cb8bcae1dc3437b18cea3c096ac382a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce266802d90bd81a35f2bfa06dda920a30ccaf77bd70a0f972e5ac85814cd8a`  
		Last Modified: Mon, 05 May 2025 17:22:29 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd2353677fff4d204b05c3ede75419526f90b6d0c20311ab2f6f641cbb7a658`  
		Last Modified: Wed, 14 May 2025 19:36:05 GMT  
		Size: 136.6 MB (136628899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:b8cbc09dc421df6788947501a8f6b073b1abb0ef7bb583e6678fd3da78b12267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b99c1077e3552a66f448bb32915e4b9d21376d9d84a9bc30df621d338e760e`

```dockerfile
```

-	Layers:
	-	`sha256:873d16fe61f9a666c1006cdfaa39fe4172973f61f462ab276bef4b3bf91a2fd9`  
		Last Modified: Wed, 14 May 2025 19:35:56 GMT  
		Size: 2.1 MB (2055166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c742d86a84fa17e49d269ac36c17b143747079ee0ee6f799e4f634f1e7cd168a`  
		Last Modified: Wed, 14 May 2025 19:35:56 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:62c5f305404d3a321e75e30a674edd7b759731cef575037d2d9539337cbf556b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162267526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9d6362791bc2dca0a49f74b2c9417294c1e7229ac63b4c65ac0205772aaf5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
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
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a80e8992168178f43fd2602a23cc2b2a1380dcba5882f3fbf1da5fe7f83ac5`  
		Last Modified: Fri, 09 May 2025 12:35:37 GMT  
		Size: 1.5 MB (1455700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2e97bf327de9faf2ba1006ffe91356f4a07ad8ca28c996b313b77ffabe65ed`  
		Last Modified: Wed, 14 May 2025 19:37:01 GMT  
		Size: 132.8 MB (132811842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2de4112e0e7cb468da7b2de7729f23471c90be919a2f8fbee7205db321abf7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511c43160567facffa91e8f2052b8adc602d9daf8ee77d6b9f0a3a8d4863094b`

```dockerfile
```

-	Layers:
	-	`sha256:efa81eaf47fe4d6b627689354089aa90e455bd0c3cca6897925cafa1ac3aa1f0`  
		Last Modified: Wed, 14 May 2025 19:36:58 GMT  
		Size: 2.1 MB (2051951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa96ce8bfb479a11efb17ba449805d9d2d159974d6a093f893725a01503ae8cf`  
		Last Modified: Wed, 14 May 2025 19:36:58 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:8ca47a39b839fd6c1f4d8d48ce78ef58020a08feed9df894be8b019651a4134c
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
$ docker pull ibmjava@sha256:7245fde91c1be7da7a50557896acdf9229b49a08959ba06b35d1b49087ef0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166767680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069ac94cfd8c83384048e40b5593f987f9a84bcdefb22f0c57e944e5b36b9d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8803db35073b2740da6f9573de7c61691c99ce2638f0e6818c242609f4f3417e`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 1.5 MB (1450255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa120ccd89f04004bf22720a697c7c4a886668c5f0b4bf862447e6a0849572e`  
		Last Modified: Wed, 14 May 2025 19:35:24 GMT  
		Size: 135.8 MB (135784811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:003c5b38b46e7699d817326b40d7d64b9162ba797e82ebfe35ab8d470f6fda56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279184ce7d75118cf6dce892168413cbf9fa99eabb48b61a16c68fa5bc822bf`

```dockerfile
```

-	Layers:
	-	`sha256:729b3ff94df155855b23bf5b281b6da76989fff0bf2271fc08116331c2d86938`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 2.1 MB (2051990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384ce414ff4f341cc543f84db1f5a5fd6af0420b3cab8b20754d964ed93c46b5`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:9514a8f8a3e54d798c90be72d94c6a184fb051ebd1aa03c7d46ec43d9d67312f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172608317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625a932b3b2b3d38c553d7ed0788d6687cb8bcae1dc3437b18cea3c096ac382a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce266802d90bd81a35f2bfa06dda920a30ccaf77bd70a0f972e5ac85814cd8a`  
		Last Modified: Mon, 05 May 2025 17:22:29 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd2353677fff4d204b05c3ede75419526f90b6d0c20311ab2f6f641cbb7a658`  
		Last Modified: Wed, 14 May 2025 19:36:05 GMT  
		Size: 136.6 MB (136628899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:b8cbc09dc421df6788947501a8f6b073b1abb0ef7bb583e6678fd3da78b12267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b99c1077e3552a66f448bb32915e4b9d21376d9d84a9bc30df621d338e760e`

```dockerfile
```

-	Layers:
	-	`sha256:873d16fe61f9a666c1006cdfaa39fe4172973f61f462ab276bef4b3bf91a2fd9`  
		Last Modified: Wed, 14 May 2025 19:35:56 GMT  
		Size: 2.1 MB (2055166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c742d86a84fa17e49d269ac36c17b143747079ee0ee6f799e4f634f1e7cd168a`  
		Last Modified: Wed, 14 May 2025 19:35:56 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:62c5f305404d3a321e75e30a674edd7b759731cef575037d2d9539337cbf556b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162267526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9d6362791bc2dca0a49f74b2c9417294c1e7229ac63b4c65ac0205772aaf5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
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
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a80e8992168178f43fd2602a23cc2b2a1380dcba5882f3fbf1da5fe7f83ac5`  
		Last Modified: Fri, 09 May 2025 12:35:37 GMT  
		Size: 1.5 MB (1455700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2e97bf327de9faf2ba1006ffe91356f4a07ad8ca28c996b313b77ffabe65ed`  
		Last Modified: Wed, 14 May 2025 19:37:01 GMT  
		Size: 132.8 MB (132811842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2de4112e0e7cb468da7b2de7729f23471c90be919a2f8fbee7205db321abf7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511c43160567facffa91e8f2052b8adc602d9daf8ee77d6b9f0a3a8d4863094b`

```dockerfile
```

-	Layers:
	-	`sha256:efa81eaf47fe4d6b627689354089aa90e455bd0c3cca6897925cafa1ac3aa1f0`  
		Last Modified: Wed, 14 May 2025 19:36:58 GMT  
		Size: 2.1 MB (2051951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa96ce8bfb479a11efb17ba449805d9d2d159974d6a093f893725a01503ae8cf`  
		Last Modified: Wed, 14 May 2025 19:36:58 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:abf1a59f4f7b3497575d8cff863856b7e2a465ca4218f89be1a5dd07b3deeb34
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
$ docker pull ibmjava@sha256:ffd157a6665eb5e83e985ea447912ec82f4ecf6844fbfefde7f25871de39c943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204165422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bde78b368af83bb67156f81f125751d8e2b8d3ed0c66630231772985d72550`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6962f96344b6c493e1b942768423a56f71b8f635c2e25c7676e355c88c53279d`  
		Last Modified: Wed, 14 May 2025 19:35:40 GMT  
		Size: 1.5 MB (1450231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5c70074815bbfb3fd09210499005273d14afe16346373a337df8725cfff53c`  
		Last Modified: Wed, 14 May 2025 19:35:45 GMT  
		Size: 173.2 MB (173182577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a7744df62e6edf2045242978fe8f35017c2c6be1bb03e3e46a6a276718db8e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b568ef9c73ec7ab732e64cbdc3fa1e19ee5e8baad563738148147ff6f838376`

```dockerfile
```

-	Layers:
	-	`sha256:3c916191bc79472793a7b5029980f5ab5a2525a426a4ae3bb3faef06528b3dd8`  
		Last Modified: Wed, 14 May 2025 19:35:40 GMT  
		Size: 3.0 MB (2959908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44773bb2d5124cdd99590404bd05ebf0eb197d053f839d73d66ab137ef5c5819`  
		Last Modified: Wed, 14 May 2025 19:35:40 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:6be5cb8faf4b43a00757d4c1bfcb66ae7c4852f351acbdabb56e1be4d42e4bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210217915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250f2d89a83619e3dcf97e47a7636bf4dfa30eb4d35a5908cdeddd3fa952925d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce266802d90bd81a35f2bfa06dda920a30ccaf77bd70a0f972e5ac85814cd8a`  
		Last Modified: Mon, 05 May 2025 17:22:29 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e629021b53c2cb70e253b5068fd4f2a2f722c6dcb7d4700becae336978296877`  
		Last Modified: Wed, 14 May 2025 19:39:43 GMT  
		Size: 174.2 MB (174238497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:01391054089a0eac32950e67842132d29da66c84a1d940999c5b02498662c0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478839d2dc6147877f81a400487b68097c96c7b7df949f6815d8a3c77766a0ec`

```dockerfile
```

-	Layers:
	-	`sha256:62482704c0a3ad0b0fbc4a2e987c389c0aae331599049f4eca17ef7f5ed0bf09`  
		Last Modified: Wed, 14 May 2025 19:39:39 GMT  
		Size: 2.9 MB (2945743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade8702e2fc4f692aa6658a04b0272df6114f9e8027807dfc134fc97183bc44e`  
		Last Modified: Wed, 14 May 2025 19:39:38 GMT  
		Size: 13.2 KB (13211 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:01848844bc0c00a2473148366442ae366305fdb0df310df7915cbb7e19fe6679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192752835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac94fdfd03ceb9550ad5f515d620d6de74fb7a138ad5ea55ef4341dda88c0fd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
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
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a80e8992168178f43fd2602a23cc2b2a1380dcba5882f3fbf1da5fe7f83ac5`  
		Last Modified: Fri, 09 May 2025 12:35:37 GMT  
		Size: 1.5 MB (1455700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297889e368b4824543ea7f53c5a3dc986923a3bce09df6bc01b2c18d6b86a999`  
		Last Modified: Wed, 14 May 2025 19:41:35 GMT  
		Size: 163.3 MB (163297151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:77fc2696317934f5b7b32dc1568f6b17e9d18c1031bae0bb6d092cbefbbb3b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2648804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a41b39131ab1fc4f0b1c32b57e621f14f3078763400acc81876b8e8e6ffa4c`

```dockerfile
```

-	Layers:
	-	`sha256:dbb5f741f97de049c10f99fd3567ee0debf5e39819bb8dc6607841092e0eb2b1`  
		Last Modified: Wed, 14 May 2025 19:41:32 GMT  
		Size: 2.6 MB (2635626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b945928497c851cc0dee42318e178c726ff1ed9bf47347994e234e9435c7896`  
		Last Modified: Wed, 14 May 2025 19:41:32 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:2601ddddac50dbc7c317da1811e3356c3441394726b91f9da448c24b746af4f2
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
$ docker pull ibmjava@sha256:6c2a688d5855cfc3d1845bc16ce4516f5a0add138597c4f791caf15b6a11bfb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101478466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c752f48f13b64d48c37527671bc44e19033f974b349d5ded31e01d653ae5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fce7ad64d8e7a6e537f46ad89e4578bc2bc7219954201134354c28360bed14`  
		Last Modified: Wed, 14 May 2025 19:35:01 GMT  
		Size: 1.5 MB (1450208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e28bd27d016252f68af84939c9ba6b1f15eb24d79800b7d9280b56ee614c89`  
		Last Modified: Wed, 14 May 2025 19:35:02 GMT  
		Size: 70.5 MB (70495644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e0339fd7b8ed0e3a9d21c87855ec6e2536f9bf46a83b263798e5342bf3ebad6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2047602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15481a73c6c9e0a8f31316aae1884c90dcd66c4c112084ad7ed40cda32f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:0c959c03c4030fdf817351c18fcabd8805c23dbfaaba9738f53f28b55c4b32fe`  
		Last Modified: Wed, 14 May 2025 19:35:01 GMT  
		Size: 2.0 MB (2034421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed15e5715112fd5a2cd433c56de13c9ed2a9c5504a635005f194cfba87e84b0`  
		Last Modified: Wed, 14 May 2025 19:35:00 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:b9d8cf73ed1812770b2c08ee06171ff8c84364664038f42b90c1db3667cf2fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107308043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fb0a1e978c2f1ea1aebea5f79764cbacf6822948c37c3638d2b4f961241989`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce266802d90bd81a35f2bfa06dda920a30ccaf77bd70a0f972e5ac85814cd8a`  
		Last Modified: Mon, 05 May 2025 17:22:29 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4c6905e04c9184247640579fafa52e096976ddf445a8fb4f7068b37a97f105`  
		Last Modified: Wed, 14 May 2025 19:37:48 GMT  
		Size: 71.3 MB (71328625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:da12c3265d566874701cd5ff713424d6dd77b3e2abc1e5a08d420c8037dea192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2052021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29958454ad666049460ed204953cf7a937a999b6ecc4d65e6a34df5c727c2d1b`

```dockerfile
```

-	Layers:
	-	`sha256:c307d7361520511a758951b1750cdddb3824b83d49ccfa3d498028ee84900e88`  
		Last Modified: Wed, 14 May 2025 19:37:45 GMT  
		Size: 2.0 MB (2038808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243397b71c2380bde1bca649bad6b23ebd5fe7a4254a4cf5c24767d2e27f5d7c`  
		Last Modified: Wed, 14 May 2025 19:37:44 GMT  
		Size: 13.2 KB (13213 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:9a50cb7c83b39903272c273d4112b50e33c2b5934f7943c9b58c440ce505f472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100547274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cfc583b4b8cc4f57bc672be46f1bf7acdb7f8c250e5500bdfac0f279ad32bb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
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
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a80e8992168178f43fd2602a23cc2b2a1380dcba5882f3fbf1da5fe7f83ac5`  
		Last Modified: Fri, 09 May 2025 12:35:37 GMT  
		Size: 1.5 MB (1455700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a0f1fd0bd2f7bbc2ffdbb416daf60034b798141f7efecc1effec1fcb92d49c`  
		Last Modified: Wed, 14 May 2025 19:39:02 GMT  
		Size: 71.1 MB (71091590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f702c3bc00c05601fff77baa83b0b1f97d46d51e260664c369cdffa715cbe53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373c74f4df4e7141bcc97e62e380873f99d0d1dda2fe1938b3d91df69a795ea`

```dockerfile
```

-	Layers:
	-	`sha256:985fd38328266389a298f2d419903f609e0b18739c8936725e16bc4bce455e01`  
		Last Modified: Wed, 14 May 2025 19:39:00 GMT  
		Size: 2.0 MB (2038043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a2b33f3e43440c3414fe7bf75a0a04cbe26ac913cd20d207203c9f5b9906e8f`  
		Last Modified: Wed, 14 May 2025 19:39:00 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:8ca47a39b839fd6c1f4d8d48ce78ef58020a08feed9df894be8b019651a4134c
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
$ docker pull ibmjava@sha256:7245fde91c1be7da7a50557896acdf9229b49a08959ba06b35d1b49087ef0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166767680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069ac94cfd8c83384048e40b5593f987f9a84bcdefb22f0c57e944e5b36b9d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8803db35073b2740da6f9573de7c61691c99ce2638f0e6818c242609f4f3417e`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 1.5 MB (1450255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa120ccd89f04004bf22720a697c7c4a886668c5f0b4bf862447e6a0849572e`  
		Last Modified: Wed, 14 May 2025 19:35:24 GMT  
		Size: 135.8 MB (135784811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:003c5b38b46e7699d817326b40d7d64b9162ba797e82ebfe35ab8d470f6fda56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279184ce7d75118cf6dce892168413cbf9fa99eabb48b61a16c68fa5bc822bf`

```dockerfile
```

-	Layers:
	-	`sha256:729b3ff94df155855b23bf5b281b6da76989fff0bf2271fc08116331c2d86938`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 2.1 MB (2051990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384ce414ff4f341cc543f84db1f5a5fd6af0420b3cab8b20754d964ed93c46b5`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:9514a8f8a3e54d798c90be72d94c6a184fb051ebd1aa03c7d46ec43d9d67312f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172608317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625a932b3b2b3d38c553d7ed0788d6687cb8bcae1dc3437b18cea3c096ac382a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce266802d90bd81a35f2bfa06dda920a30ccaf77bd70a0f972e5ac85814cd8a`  
		Last Modified: Mon, 05 May 2025 17:22:29 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd2353677fff4d204b05c3ede75419526f90b6d0c20311ab2f6f641cbb7a658`  
		Last Modified: Wed, 14 May 2025 19:36:05 GMT  
		Size: 136.6 MB (136628899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:b8cbc09dc421df6788947501a8f6b073b1abb0ef7bb583e6678fd3da78b12267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b99c1077e3552a66f448bb32915e4b9d21376d9d84a9bc30df621d338e760e`

```dockerfile
```

-	Layers:
	-	`sha256:873d16fe61f9a666c1006cdfaa39fe4172973f61f462ab276bef4b3bf91a2fd9`  
		Last Modified: Wed, 14 May 2025 19:35:56 GMT  
		Size: 2.1 MB (2055166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c742d86a84fa17e49d269ac36c17b143747079ee0ee6f799e4f634f1e7cd168a`  
		Last Modified: Wed, 14 May 2025 19:35:56 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:62c5f305404d3a321e75e30a674edd7b759731cef575037d2d9539337cbf556b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162267526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9d6362791bc2dca0a49f74b2c9417294c1e7229ac63b4c65ac0205772aaf5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
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
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a80e8992168178f43fd2602a23cc2b2a1380dcba5882f3fbf1da5fe7f83ac5`  
		Last Modified: Fri, 09 May 2025 12:35:37 GMT  
		Size: 1.5 MB (1455700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2e97bf327de9faf2ba1006ffe91356f4a07ad8ca28c996b313b77ffabe65ed`  
		Last Modified: Wed, 14 May 2025 19:37:01 GMT  
		Size: 132.8 MB (132811842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2de4112e0e7cb468da7b2de7729f23471c90be919a2f8fbee7205db321abf7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511c43160567facffa91e8f2052b8adc602d9daf8ee77d6b9f0a3a8d4863094b`

```dockerfile
```

-	Layers:
	-	`sha256:efa81eaf47fe4d6b627689354089aa90e455bd0c3cca6897925cafa1ac3aa1f0`  
		Last Modified: Wed, 14 May 2025 19:36:58 GMT  
		Size: 2.1 MB (2051951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa96ce8bfb479a11efb17ba449805d9d2d159974d6a093f893725a01503ae8cf`  
		Last Modified: Wed, 14 May 2025 19:36:58 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:8ca47a39b839fd6c1f4d8d48ce78ef58020a08feed9df894be8b019651a4134c
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
$ docker pull ibmjava@sha256:7245fde91c1be7da7a50557896acdf9229b49a08959ba06b35d1b49087ef0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166767680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069ac94cfd8c83384048e40b5593f987f9a84bcdefb22f0c57e944e5b36b9d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8803db35073b2740da6f9573de7c61691c99ce2638f0e6818c242609f4f3417e`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 1.5 MB (1450255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa120ccd89f04004bf22720a697c7c4a886668c5f0b4bf862447e6a0849572e`  
		Last Modified: Wed, 14 May 2025 19:35:24 GMT  
		Size: 135.8 MB (135784811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:003c5b38b46e7699d817326b40d7d64b9162ba797e82ebfe35ab8d470f6fda56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5279184ce7d75118cf6dce892168413cbf9fa99eabb48b61a16c68fa5bc822bf`

```dockerfile
```

-	Layers:
	-	`sha256:729b3ff94df155855b23bf5b281b6da76989fff0bf2271fc08116331c2d86938`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 2.1 MB (2051990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384ce414ff4f341cc543f84db1f5a5fd6af0420b3cab8b20754d964ed93c46b5`  
		Last Modified: Wed, 14 May 2025 19:35:21 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:9514a8f8a3e54d798c90be72d94c6a184fb051ebd1aa03c7d46ec43d9d67312f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172608317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625a932b3b2b3d38c553d7ed0788d6687cb8bcae1dc3437b18cea3c096ac382a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce266802d90bd81a35f2bfa06dda920a30ccaf77bd70a0f972e5ac85814cd8a`  
		Last Modified: Mon, 05 May 2025 17:22:29 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd2353677fff4d204b05c3ede75419526f90b6d0c20311ab2f6f641cbb7a658`  
		Last Modified: Wed, 14 May 2025 19:36:05 GMT  
		Size: 136.6 MB (136628899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:b8cbc09dc421df6788947501a8f6b073b1abb0ef7bb583e6678fd3da78b12267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b99c1077e3552a66f448bb32915e4b9d21376d9d84a9bc30df621d338e760e`

```dockerfile
```

-	Layers:
	-	`sha256:873d16fe61f9a666c1006cdfaa39fe4172973f61f462ab276bef4b3bf91a2fd9`  
		Last Modified: Wed, 14 May 2025 19:35:56 GMT  
		Size: 2.1 MB (2055166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c742d86a84fa17e49d269ac36c17b143747079ee0ee6f799e4f634f1e7cd168a`  
		Last Modified: Wed, 14 May 2025 19:35:56 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:62c5f305404d3a321e75e30a674edd7b759731cef575037d2d9539337cbf556b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162267526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9d6362791bc2dca0a49f74b2c9417294c1e7229ac63b4c65ac0205772aaf5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
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
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a80e8992168178f43fd2602a23cc2b2a1380dcba5882f3fbf1da5fe7f83ac5`  
		Last Modified: Fri, 09 May 2025 12:35:37 GMT  
		Size: 1.5 MB (1455700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2e97bf327de9faf2ba1006ffe91356f4a07ad8ca28c996b313b77ffabe65ed`  
		Last Modified: Wed, 14 May 2025 19:37:01 GMT  
		Size: 132.8 MB (132811842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2de4112e0e7cb468da7b2de7729f23471c90be919a2f8fbee7205db321abf7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511c43160567facffa91e8f2052b8adc602d9daf8ee77d6b9f0a3a8d4863094b`

```dockerfile
```

-	Layers:
	-	`sha256:efa81eaf47fe4d6b627689354089aa90e455bd0c3cca6897925cafa1ac3aa1f0`  
		Last Modified: Wed, 14 May 2025 19:36:58 GMT  
		Size: 2.1 MB (2051951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa96ce8bfb479a11efb17ba449805d9d2d159974d6a093f893725a01503ae8cf`  
		Last Modified: Wed, 14 May 2025 19:36:58 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:abf1a59f4f7b3497575d8cff863856b7e2a465ca4218f89be1a5dd07b3deeb34
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
$ docker pull ibmjava@sha256:ffd157a6665eb5e83e985ea447912ec82f4ecf6844fbfefde7f25871de39c943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204165422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bde78b368af83bb67156f81f125751d8e2b8d3ed0c66630231772985d72550`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6962f96344b6c493e1b942768423a56f71b8f635c2e25c7676e355c88c53279d`  
		Last Modified: Wed, 14 May 2025 19:35:40 GMT  
		Size: 1.5 MB (1450231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5c70074815bbfb3fd09210499005273d14afe16346373a337df8725cfff53c`  
		Last Modified: Wed, 14 May 2025 19:35:45 GMT  
		Size: 173.2 MB (173182577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a7744df62e6edf2045242978fe8f35017c2c6be1bb03e3e46a6a276718db8e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b568ef9c73ec7ab732e64cbdc3fa1e19ee5e8baad563738148147ff6f838376`

```dockerfile
```

-	Layers:
	-	`sha256:3c916191bc79472793a7b5029980f5ab5a2525a426a4ae3bb3faef06528b3dd8`  
		Last Modified: Wed, 14 May 2025 19:35:40 GMT  
		Size: 3.0 MB (2959908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44773bb2d5124cdd99590404bd05ebf0eb197d053f839d73d66ab137ef5c5819`  
		Last Modified: Wed, 14 May 2025 19:35:40 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:6be5cb8faf4b43a00757d4c1bfcb66ae7c4852f351acbdabb56e1be4d42e4bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210217915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250f2d89a83619e3dcf97e47a7636bf4dfa30eb4d35a5908cdeddd3fa952925d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce266802d90bd81a35f2bfa06dda920a30ccaf77bd70a0f972e5ac85814cd8a`  
		Last Modified: Mon, 05 May 2025 17:22:29 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e629021b53c2cb70e253b5068fd4f2a2f722c6dcb7d4700becae336978296877`  
		Last Modified: Wed, 14 May 2025 19:39:43 GMT  
		Size: 174.2 MB (174238497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:01391054089a0eac32950e67842132d29da66c84a1d940999c5b02498662c0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478839d2dc6147877f81a400487b68097c96c7b7df949f6815d8a3c77766a0ec`

```dockerfile
```

-	Layers:
	-	`sha256:62482704c0a3ad0b0fbc4a2e987c389c0aae331599049f4eca17ef7f5ed0bf09`  
		Last Modified: Wed, 14 May 2025 19:39:39 GMT  
		Size: 2.9 MB (2945743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade8702e2fc4f692aa6658a04b0272df6114f9e8027807dfc134fc97183bc44e`  
		Last Modified: Wed, 14 May 2025 19:39:38 GMT  
		Size: 13.2 KB (13211 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:01848844bc0c00a2473148366442ae366305fdb0df310df7915cbb7e19fe6679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192752835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac94fdfd03ceb9550ad5f515d620d6de74fb7a138ad5ea55ef4341dda88c0fd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
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
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a80e8992168178f43fd2602a23cc2b2a1380dcba5882f3fbf1da5fe7f83ac5`  
		Last Modified: Fri, 09 May 2025 12:35:37 GMT  
		Size: 1.5 MB (1455700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297889e368b4824543ea7f53c5a3dc986923a3bce09df6bc01b2c18d6b86a999`  
		Last Modified: Wed, 14 May 2025 19:41:35 GMT  
		Size: 163.3 MB (163297151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:77fc2696317934f5b7b32dc1568f6b17e9d18c1031bae0bb6d092cbefbbb3b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2648804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a41b39131ab1fc4f0b1c32b57e621f14f3078763400acc81876b8e8e6ffa4c`

```dockerfile
```

-	Layers:
	-	`sha256:dbb5f741f97de049c10f99fd3567ee0debf5e39819bb8dc6607841092e0eb2b1`  
		Last Modified: Wed, 14 May 2025 19:41:32 GMT  
		Size: 2.6 MB (2635626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b945928497c851cc0dee42318e178c726ff1ed9bf47347994e234e9435c7896`  
		Last Modified: Wed, 14 May 2025 19:41:32 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:2601ddddac50dbc7c317da1811e3356c3441394726b91f9da448c24b746af4f2
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
$ docker pull ibmjava@sha256:6c2a688d5855cfc3d1845bc16ce4516f5a0add138597c4f791caf15b6a11bfb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101478466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c752f48f13b64d48c37527671bc44e19033f974b349d5ded31e01d653ae5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fce7ad64d8e7a6e537f46ad89e4578bc2bc7219954201134354c28360bed14`  
		Last Modified: Wed, 14 May 2025 19:35:01 GMT  
		Size: 1.5 MB (1450208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e28bd27d016252f68af84939c9ba6b1f15eb24d79800b7d9280b56ee614c89`  
		Last Modified: Wed, 14 May 2025 19:35:02 GMT  
		Size: 70.5 MB (70495644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e0339fd7b8ed0e3a9d21c87855ec6e2536f9bf46a83b263798e5342bf3ebad6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2047602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb15481a73c6c9e0a8f31316aae1884c90dcd66c4c112084ad7ed40cda32f9a1`

```dockerfile
```

-	Layers:
	-	`sha256:0c959c03c4030fdf817351c18fcabd8805c23dbfaaba9738f53f28b55c4b32fe`  
		Last Modified: Wed, 14 May 2025 19:35:01 GMT  
		Size: 2.0 MB (2034421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed15e5715112fd5a2cd433c56de13c9ed2a9c5504a635005f194cfba87e84b0`  
		Last Modified: Wed, 14 May 2025 19:35:00 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:b9d8cf73ed1812770b2c08ee06171ff8c84364664038f42b90c1db3667cf2fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107308043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fb0a1e978c2f1ea1aebea5f79764cbacf6822948c37c3638d2b4f961241989`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce266802d90bd81a35f2bfa06dda920a30ccaf77bd70a0f972e5ac85814cd8a`  
		Last Modified: Mon, 05 May 2025 17:22:29 GMT  
		Size: 1.5 MB (1536203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4c6905e04c9184247640579fafa52e096976ddf445a8fb4f7068b37a97f105`  
		Last Modified: Wed, 14 May 2025 19:37:48 GMT  
		Size: 71.3 MB (71328625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:da12c3265d566874701cd5ff713424d6dd77b3e2abc1e5a08d420c8037dea192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2052021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29958454ad666049460ed204953cf7a937a999b6ecc4d65e6a34df5c727c2d1b`

```dockerfile
```

-	Layers:
	-	`sha256:c307d7361520511a758951b1750cdddb3824b83d49ccfa3d498028ee84900e88`  
		Last Modified: Wed, 14 May 2025 19:37:45 GMT  
		Size: 2.0 MB (2038808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243397b71c2380bde1bca649bad6b23ebd5fe7a4254a4cf5c24767d2e27f5d7c`  
		Last Modified: Wed, 14 May 2025 19:37:44 GMT  
		Size: 13.2 KB (13213 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:9a50cb7c83b39903272c273d4112b50e33c2b5934f7943c9b58c440ce505f472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100547274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cfc583b4b8cc4f57bc672be46f1bf7acdb7f8c250e5500bdfac0f279ad32bb2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
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
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a80e8992168178f43fd2602a23cc2b2a1380dcba5882f3fbf1da5fe7f83ac5`  
		Last Modified: Fri, 09 May 2025 12:35:37 GMT  
		Size: 1.5 MB (1455700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a0f1fd0bd2f7bbc2ffdbb416daf60034b798141f7efecc1effec1fcb92d49c`  
		Last Modified: Wed, 14 May 2025 19:39:02 GMT  
		Size: 71.1 MB (71091590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f702c3bc00c05601fff77baa83b0b1f97d46d51e260664c369cdffa715cbe53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373c74f4df4e7141bcc97e62e380873f99d0d1dda2fe1938b3d91df69a795ea`

```dockerfile
```

-	Layers:
	-	`sha256:985fd38328266389a298f2d419903f609e0b18739c8936725e16bc4bce455e01`  
		Last Modified: Wed, 14 May 2025 19:39:00 GMT  
		Size: 2.0 MB (2038043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a2b33f3e43440c3414fe7bf75a0a04cbe26ac913cd20d207203c9f5b9906e8f`  
		Last Modified: Wed, 14 May 2025 19:39:00 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json
