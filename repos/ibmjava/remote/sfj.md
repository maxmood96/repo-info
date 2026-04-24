## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:0dbb057ba5a16072c4c2362b8a473d4a01ebbcaae9db2155934809a114a87203
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
$ docker pull ibmjava@sha256:1678f4ebcdbe99b0c21541643b7986ccdd88e288064ca2392afafe8ecd83775d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102358232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b6bca4b98100a69ef9d612febfa73225e1936f33ada229c8baee7d5a563d95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 17:27:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2026 17:27:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Apr 2026 17:27:55 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:28:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:28:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a0d80514b8219bde29705f38ed9b2738489539c787898f6f7c506254c1a958`  
		Last Modified: Fri, 24 Apr 2026 17:28:34 GMT  
		Size: 1.5 MB (1450085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf1299181d5f5c89288edc76bc3524391830db8eeb6d97afb0e960842e1bb36`  
		Last Modified: Fri, 24 Apr 2026 17:28:38 GMT  
		Size: 71.2 MB (71171649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e43d9e3a487f9af90d640bc304f1e05b6f058c0fa32045ec013db4ca729c589d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f915df40306b5a30c4a12cabbfb4741179c525f583a3573c7ef50ff8ba7c0dd3`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f91ccbdb31be34553b4d3ba5467547f4b51ba453da425dfb2bdf38fd1e5b9`  
		Last Modified: Fri, 24 Apr 2026 17:28:34 GMT  
		Size: 2.2 MB (2156549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3d8752b7ecfb858c84437b30a56ca1ab6d731a0ffe7546e8ad0f72b4e16184`  
		Last Modified: Fri, 24 Apr 2026 17:28:34 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:72b1f13a06250a12ff8eec92056f932358070d8bc51f36eaa02eac2eed527c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108299917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8378fdaebd67b0d5baf6e0108d794f3e98c5ef645019c0ac9eb4581bae769b5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:25:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:25:55 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb02b7620f1c9a312232aae8d2b12e460397a04548ba64d41301281d6ccd3d1`  
		Last Modified: Fri, 24 Apr 2026 17:26:21 GMT  
		Size: 72.1 MB (72115335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0b1c4089116e98b80594155afa0e01110bd351fc166d4a717ce3d90e62a9acbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16b373f284321e73f50454fe1f5859551ce0ea4e4e8beed53047dd06bc2b591`

```dockerfile
```

-	Layers:
	-	`sha256:1f152ea86f4edd743f02e6484c10b34f789a2e4a1d83f66cc5711cc064962d0a`  
		Last Modified: Fri, 24 Apr 2026 17:26:19 GMT  
		Size: 2.2 MB (2161050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f7c70c427b34e9a67b6ec46f9e0848a9facacb75ba0332c9e9ac3a673f8125`  
		Last Modified: Fri, 24 Apr 2026 17:26:19 GMT  
		Size: 12.6 KB (12634 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:016a4fae381bd1666202808d37d16c2168c1ae91e4e2998a5c6451ef05f79a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102890298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ed624af855a75673af5df09a0e59cbb5c909fb41c9616bdb2e301d348987c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:59:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:17 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:26:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:26:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0a94005458eecbf59d36fdcb472759320381954eb3b9e0a8ea9c1e920dc2a0`  
		Last Modified: Wed, 15 Apr 2026 21:00:37 GMT  
		Size: 1.5 MB (1455873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb1befb7a4f3a44bb6b445ca487f754e3d05dcea256b474aef455a0abfc2535`  
		Last Modified: Fri, 24 Apr 2026 17:29:12 GMT  
		Size: 73.2 MB (73232126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:724200d1cf109c31a8f7b3a100827a2d30468a9575c2e6946814797c90c2d246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71ec594cbde2b248bb2eca2da15e95be8b49b6bbc0d3601c072634bad0dbc8d`

```dockerfile
```

-	Layers:
	-	`sha256:4bbb3b6725faf8ef76c5fc348e8fd02a7bf2d8cce61b96c96db55ae9789a36cf`  
		Last Modified: Fri, 24 Apr 2026 17:28:53 GMT  
		Size: 2.2 MB (2160171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ceb848da9744c4e5dab51fd313bc648d16c13086f11010f0791ef38da761810`  
		Last Modified: Fri, 24 Apr 2026 17:28:52 GMT  
		Size: 12.6 KB (12600 bytes)  
		MIME: application/vnd.in-toto+json
