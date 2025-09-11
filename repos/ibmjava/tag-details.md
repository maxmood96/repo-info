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
$ docker pull ibmjava@sha256:d239621a96b6bde3217cd455138d83b608e888b13c2441931500d96804940382
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
$ docker pull ibmjava@sha256:1b0a82f76e52d1c6f56d181125ef43476c205f783efe3c76dd1de0c8240a3356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166404491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a65d4cfb107cdf9bc5ce7a3022ddf7f125b04d51db34d7e375d27cd7981ea82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f065c842f2da0845216d333a640514a645a84dd427fccdccb3df9f40b51c79ad`  
		Last Modified: Thu, 11 Sep 2025 16:51:47 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d65874fb3a9b70af7e5e07c3590d8eff39eb32d2abf17167c95e2e2d1407c6`  
		Last Modified: Thu, 11 Sep 2025 16:51:56 GMT  
		Size: 135.4 MB (135417488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9188900a0ee53649aa2c6b470d33f1a8df0c36419199a4fa3b9a8ab996876dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166ab4f1e810df91f7f8a51a91b49e53334c47aae2ea722d27fe385e1b315153`

```dockerfile
```

-	Layers:
	-	`sha256:c4d69b9119265863742b61e0a8a7622e1fab18492f44f8d571ef7106048f65e5`  
		Last Modified: Thu, 11 Sep 2025 17:01:28 GMT  
		Size: 2.2 MB (2173542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44e6790e199eb8d1906ca55a4693385be8f849b664086e990d04cffd631b3c7`  
		Last Modified: Thu, 11 Sep 2025 17:01:28 GMT  
		Size: 13.2 KB (13234 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:f61c0cae7db779aae08e6fc26e104a32d491548689f63043eb24b435af6ed5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172342564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dc03516ec3c4536a1b3609e67d10baf2054cc617b639284dd0c9db5602bce3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4572befc841349373b827c193ac673418ba5463306814c6d4c89cbdc534a3`  
		Last Modified: Thu, 11 Sep 2025 16:55:18 GMT  
		Size: 136.4 MB (136363125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4841b6900a2cdbc0387276356b9f70352556b5734bf3de3e6c1be6ddd48417b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84c88a8f00973496cd1a731c7b4bbc5d7e175db1c0ae733da6ab89a8324b51f`

```dockerfile
```

-	Layers:
	-	`sha256:dfb0586ae56992dd71717c8f0a7350ebb6e5a29cdbed2f8b6898f74884abd35f`  
		Last Modified: Thu, 11 Sep 2025 17:01:32 GMT  
		Size: 2.2 MB (2176832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d64290be2c9bb02e8b692ba3805d90e57aca9a40388943df5dce7bde4976fb`  
		Last Modified: Thu, 11 Sep 2025 17:01:33 GMT  
		Size: 13.3 KB (13279 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:91d5ce03126fc2cfd448fc5b66cb46e24cfe5295cfd3b6e092d7ad61dbdd6f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161748197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9913d20af3119ab7786d40a93fc16122e9cb5d0b07844491b0e9ab7a1d20bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:41 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:42 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 19 Aug 2025 17:21:42 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20c245bb91f7038c8e7666e50e3b477d3bb0faf772b531b6ddcd81ed6b348c`  
		Last Modified: Thu, 11 Sep 2025 16:54:02 GMT  
		Size: 1.5 MB (1455758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76030c75f4142a5689b96eca6cde0a943134234ff6c9d87d03a9329e795eec55`  
		Last Modified: Thu, 11 Sep 2025 16:54:15 GMT  
		Size: 132.3 MB (132288771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:151425a168e86dfb502122878fadd03e0cb693a485fc23b75b261bb32a4d1403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6c3b4ff7ad2d77a75245faa78673e79ee49078659c2c80a15eed04e21d79db`

```dockerfile
```

-	Layers:
	-	`sha256:20a9c4836bb69c0d31098a1bb635b557fd80fb2d19a91d436fc6539892df9bac`  
		Last Modified: Thu, 11 Sep 2025 17:01:37 GMT  
		Size: 2.2 MB (2173503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf945ea1a8caaea9ac34de09891ba9c69351602ed9041dbf0c51024f7dfdbc1f`  
		Last Modified: Thu, 11 Sep 2025 17:01:37 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:d239621a96b6bde3217cd455138d83b608e888b13c2441931500d96804940382
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
$ docker pull ibmjava@sha256:1b0a82f76e52d1c6f56d181125ef43476c205f783efe3c76dd1de0c8240a3356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166404491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a65d4cfb107cdf9bc5ce7a3022ddf7f125b04d51db34d7e375d27cd7981ea82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f065c842f2da0845216d333a640514a645a84dd427fccdccb3df9f40b51c79ad`  
		Last Modified: Thu, 11 Sep 2025 16:51:47 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d65874fb3a9b70af7e5e07c3590d8eff39eb32d2abf17167c95e2e2d1407c6`  
		Last Modified: Thu, 11 Sep 2025 16:51:56 GMT  
		Size: 135.4 MB (135417488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9188900a0ee53649aa2c6b470d33f1a8df0c36419199a4fa3b9a8ab996876dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166ab4f1e810df91f7f8a51a91b49e53334c47aae2ea722d27fe385e1b315153`

```dockerfile
```

-	Layers:
	-	`sha256:c4d69b9119265863742b61e0a8a7622e1fab18492f44f8d571ef7106048f65e5`  
		Last Modified: Thu, 11 Sep 2025 17:01:28 GMT  
		Size: 2.2 MB (2173542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44e6790e199eb8d1906ca55a4693385be8f849b664086e990d04cffd631b3c7`  
		Last Modified: Thu, 11 Sep 2025 17:01:28 GMT  
		Size: 13.2 KB (13234 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:f61c0cae7db779aae08e6fc26e104a32d491548689f63043eb24b435af6ed5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172342564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dc03516ec3c4536a1b3609e67d10baf2054cc617b639284dd0c9db5602bce3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4572befc841349373b827c193ac673418ba5463306814c6d4c89cbdc534a3`  
		Last Modified: Thu, 11 Sep 2025 16:55:18 GMT  
		Size: 136.4 MB (136363125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4841b6900a2cdbc0387276356b9f70352556b5734bf3de3e6c1be6ddd48417b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84c88a8f00973496cd1a731c7b4bbc5d7e175db1c0ae733da6ab89a8324b51f`

```dockerfile
```

-	Layers:
	-	`sha256:dfb0586ae56992dd71717c8f0a7350ebb6e5a29cdbed2f8b6898f74884abd35f`  
		Last Modified: Thu, 11 Sep 2025 17:01:32 GMT  
		Size: 2.2 MB (2176832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d64290be2c9bb02e8b692ba3805d90e57aca9a40388943df5dce7bde4976fb`  
		Last Modified: Thu, 11 Sep 2025 17:01:33 GMT  
		Size: 13.3 KB (13279 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:91d5ce03126fc2cfd448fc5b66cb46e24cfe5295cfd3b6e092d7ad61dbdd6f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161748197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9913d20af3119ab7786d40a93fc16122e9cb5d0b07844491b0e9ab7a1d20bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:41 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:42 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 19 Aug 2025 17:21:42 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20c245bb91f7038c8e7666e50e3b477d3bb0faf772b531b6ddcd81ed6b348c`  
		Last Modified: Thu, 11 Sep 2025 16:54:02 GMT  
		Size: 1.5 MB (1455758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76030c75f4142a5689b96eca6cde0a943134234ff6c9d87d03a9329e795eec55`  
		Last Modified: Thu, 11 Sep 2025 16:54:15 GMT  
		Size: 132.3 MB (132288771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:151425a168e86dfb502122878fadd03e0cb693a485fc23b75b261bb32a4d1403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6c3b4ff7ad2d77a75245faa78673e79ee49078659c2c80a15eed04e21d79db`

```dockerfile
```

-	Layers:
	-	`sha256:20a9c4836bb69c0d31098a1bb635b557fd80fb2d19a91d436fc6539892df9bac`  
		Last Modified: Thu, 11 Sep 2025 17:01:37 GMT  
		Size: 2.2 MB (2173503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf945ea1a8caaea9ac34de09891ba9c69351602ed9041dbf0c51024f7dfdbc1f`  
		Last Modified: Thu, 11 Sep 2025 17:01:37 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:74d3bda6f6d4f2baab5a774fcbe3a261d1c3b39ba4291de93bff21a22b4618a5
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
$ docker pull ibmjava@sha256:a4e86e7e963bb140193bce61999ab60873b194920e6f3f2677c4dd1ff1897114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203651617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c825252fdd90bc45d8d5a8136d843d8abc925f293d6358d0b36d8d119a9521c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6501625c0bd93c3a9e7bdafec2b1df8d65ee819572e7bb6e337314ab31718ce`  
		Last Modified: Thu, 11 Sep 2025 16:55:12 GMT  
		Size: 1.5 MB (1450049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cd794a5e418d61cd9f0391f9aa128310c0ef64a7a804c3fddc9453c8e60e54`  
		Last Modified: Thu, 11 Sep 2025 16:55:28 GMT  
		Size: 172.7 MB (172664633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8d8ed0552d583b4c47cd794b3b7fe65d04cb032ef7a0c5023219eb6e2848b14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0764f247578177811c8299f3f381aaf4c9a6d66ed8078a57a6bb4ca8f99276a`

```dockerfile
```

-	Layers:
	-	`sha256:bc327b38491b257672e0a4502977afe6cc3e8c379e51835b07374cda9a672a22`  
		Last Modified: Thu, 11 Sep 2025 17:01:37 GMT  
		Size: 3.1 MB (3083862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d93adadbac258a4a779929cc35c438bac6094a62a49528fa32beab5441051d`  
		Last Modified: Thu, 11 Sep 2025 17:01:38 GMT  
		Size: 12.6 KB (12640 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:08a8566ccfe4418a3fb255c8bf80d75d075ff4fa57edf1dcd626344367ee0db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209792835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7105fecb952660c84a56ed6369e637166001c98b86c9d5729c71d12bfd168518`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a9f118ca1f1cbf4058ca82bc7edc4791643f5aab1e787697cb7e9c745ab8b`  
		Last Modified: Thu, 11 Sep 2025 19:08:09 GMT  
		Size: 173.8 MB (173813396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2ad0c9a971f6f7cffe9535a8e552aa37f93e4d387a83315e750340fba77c10e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d7b10107d12da4e11d5eccc49ed51187b4c08568a23257eb81c836508a31bb`

```dockerfile
```

-	Layers:
	-	`sha256:d73775d92e2134667c0aff4df85c2160daebc74a5b80c55cd05bc824438657de`  
		Last Modified: Thu, 11 Sep 2025 17:01:43 GMT  
		Size: 3.1 MB (3069811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d985f7e2e6540354f101f0ac3e9c767e6d383caa0f8d32a8c2befb77f6af1dfb`  
		Last Modified: Thu, 11 Sep 2025 17:01:43 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:df015a580d51c21d085a256fdbbca654ebed500e98dcb9f4d4b50fcb086578a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192092404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1171e56899eedb16c53b5d5ea649d0cc709f30f2d14c6e33dd508dcb16598aa6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:41 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:42 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 19 Aug 2025 17:21:42 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20c245bb91f7038c8e7666e50e3b477d3bb0faf772b531b6ddcd81ed6b348c`  
		Last Modified: Thu, 11 Sep 2025 16:54:02 GMT  
		Size: 1.5 MB (1455758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b95b4dad0cf791eac4470394de71d0a10e6de0edfef58b1a82a54a4246b113`  
		Last Modified: Thu, 11 Sep 2025 18:09:36 GMT  
		Size: 162.6 MB (162632978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9a29e52165ffe924b8a4b096073fcc93b18c0267fba859fa8365bc05561df20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2769819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84372ba8dabbe00c434d3759fa6b1f69738b55448e441e7e3a9ce34ce98afb`

```dockerfile
```

-	Layers:
	-	`sha256:f15d35e9681977cabbff2d13b7143d3711edb2591c8307bec77e60decaeaf5aa`  
		Last Modified: Thu, 11 Sep 2025 17:01:48 GMT  
		Size: 2.8 MB (2757178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8212a42d609e6b91efa2b219c2f30e17ed3e3f8f08b9a1f1fc74f297a8e502`  
		Last Modified: Thu, 11 Sep 2025 17:01:49 GMT  
		Size: 12.6 KB (12641 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:018aecce38d94f2bbc3126f8be5af4565e028b22b7f76763f74e7c500daca712
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
$ docker pull ibmjava@sha256:941e76a10c609cdcea7af1a31f64ad460e64a3f2f9858560f03216e94ba604b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101767001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070b5ad024e6926782d4baf3ddbedc89b6ddb7d26592362674608939874add0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5cc1fe4a2152a92f4eb29e17d29c0b87571724d32c79d01c02ff8e1e39162cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='41ad5b9cf2a6b78925bbf89b087358a409c949a7dd21318213faa84edc0f4f6c';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='7761751660e6eef25e16627dd18850eb978eb71757cfbc443d142a0ff24d3019';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97eae39341901ed480b5ffc400b148e3b064ada449dc8356f9021c40d769d763`  
		Last Modified: Thu, 11 Sep 2025 16:58:08 GMT  
		Size: 1.5 MB (1450049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9d58ee16499cb31d15b1881d0cd69484a43df16edc4a6c762d48c2091fe081`  
		Last Modified: Thu, 11 Sep 2025 18:41:35 GMT  
		Size: 70.8 MB (70780017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:647a745cf51a3fd39fbe1cf74bfa7fb56fc30f1647eb1379f8ac8b1388c4bfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314a5292256067f7a4ea967d792da6a62ac807be18b4a3dce19d029df97be455`

```dockerfile
```

-	Layers:
	-	`sha256:3dc43fabb8171065ad60f29eeae2021758f6f635ef87512cf8f5cc13e0f4b051`  
		Last Modified: Thu, 11 Sep 2025 17:01:47 GMT  
		Size: 2.2 MB (2155973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c087eccb9855f5f4f2359b762b7c72ea12fbbaa8487452d58584386498538a1`  
		Last Modified: Thu, 11 Sep 2025 17:01:48 GMT  
		Size: 12.6 KB (12644 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5768283f79683d9c81df8fd439ec1ed2a458a719746e8b035e812503ed71ae7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107697908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6478380cf4949310efe126271609ef891f633ddcac714dad3686c2ef2eb06a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5cc1fe4a2152a92f4eb29e17d29c0b87571724d32c79d01c02ff8e1e39162cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='41ad5b9cf2a6b78925bbf89b087358a409c949a7dd21318213faa84edc0f4f6c';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='7761751660e6eef25e16627dd18850eb978eb71757cfbc443d142a0ff24d3019';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab09ea0d3d5e01e0b96c1ebf6b9caf0a0fd955b2c058934d2cb9b4ab1f1ac1b`  
		Last Modified: Thu, 11 Sep 2025 16:53:07 GMT  
		Size: 71.7 MB (71718469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:013384a5471e14701278511c0d132232484a81251b108ed71affdb1c222ed9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca43401ee7bd05ecdeb6169e3eacad13067cc5ea5d2e8138c56fe25fab5adf80`

```dockerfile
```

-	Layers:
	-	`sha256:4dd21f81db1db48491285445529c24768cb51e5ca63e6a9375b3bcb734d36aa1`  
		Last Modified: Thu, 11 Sep 2025 17:01:51 GMT  
		Size: 2.2 MB (2160474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c065c78a0812bf04e0aeaafb4db82abe6b9da9d59035a828fa505e2c4de8454e`  
		Last Modified: Thu, 11 Sep 2025 17:01:52 GMT  
		Size: 12.7 KB (12678 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:94bba6f5a41cf3bede697e716082d74f37828ea469ed01a41774666fc8ec19f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100737882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ac625bb30e72b6a1b5746089757f75a7c5a0402bc308b39705267a4f6367b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:41 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:42 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 19 Aug 2025 17:21:42 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5cc1fe4a2152a92f4eb29e17d29c0b87571724d32c79d01c02ff8e1e39162cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='41ad5b9cf2a6b78925bbf89b087358a409c949a7dd21318213faa84edc0f4f6c';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='7761751660e6eef25e16627dd18850eb978eb71757cfbc443d142a0ff24d3019';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20c245bb91f7038c8e7666e50e3b477d3bb0faf772b531b6ddcd81ed6b348c`  
		Last Modified: Thu, 11 Sep 2025 16:54:02 GMT  
		Size: 1.5 MB (1455758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f28446ca487e1c75570676d0e415743f6de5e3073a38970ac2e06ba2471a75e`  
		Last Modified: Thu, 11 Sep 2025 19:17:56 GMT  
		Size: 71.3 MB (71278456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6a59aa51a5e4d3a5a8c73b15da2127a8e87052c49641dd954c5c5bd8b12f4b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee240008aa5798377083f90b412066a6bfd3f58b7409e538f2f70f4192e9dd3b`

```dockerfile
```

-	Layers:
	-	`sha256:c7f7b1c827cb525b75438ae3b265c98ace44074050563ca080c6edd2bc4f1b29`  
		Last Modified: Thu, 11 Sep 2025 17:01:59 GMT  
		Size: 2.2 MB (2159595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80c7eb053dbc48034e7fc48d4ddaeba07f67af6734bc30d2198c772143327336`  
		Last Modified: Thu, 11 Sep 2025 17:01:59 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:d239621a96b6bde3217cd455138d83b608e888b13c2441931500d96804940382
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
$ docker pull ibmjava@sha256:1b0a82f76e52d1c6f56d181125ef43476c205f783efe3c76dd1de0c8240a3356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166404491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a65d4cfb107cdf9bc5ce7a3022ddf7f125b04d51db34d7e375d27cd7981ea82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f065c842f2da0845216d333a640514a645a84dd427fccdccb3df9f40b51c79ad`  
		Last Modified: Thu, 11 Sep 2025 16:51:47 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d65874fb3a9b70af7e5e07c3590d8eff39eb32d2abf17167c95e2e2d1407c6`  
		Last Modified: Thu, 11 Sep 2025 16:51:56 GMT  
		Size: 135.4 MB (135417488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9188900a0ee53649aa2c6b470d33f1a8df0c36419199a4fa3b9a8ab996876dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166ab4f1e810df91f7f8a51a91b49e53334c47aae2ea722d27fe385e1b315153`

```dockerfile
```

-	Layers:
	-	`sha256:c4d69b9119265863742b61e0a8a7622e1fab18492f44f8d571ef7106048f65e5`  
		Last Modified: Thu, 11 Sep 2025 17:01:28 GMT  
		Size: 2.2 MB (2173542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44e6790e199eb8d1906ca55a4693385be8f849b664086e990d04cffd631b3c7`  
		Last Modified: Thu, 11 Sep 2025 17:01:28 GMT  
		Size: 13.2 KB (13234 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:f61c0cae7db779aae08e6fc26e104a32d491548689f63043eb24b435af6ed5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172342564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dc03516ec3c4536a1b3609e67d10baf2054cc617b639284dd0c9db5602bce3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4572befc841349373b827c193ac673418ba5463306814c6d4c89cbdc534a3`  
		Last Modified: Thu, 11 Sep 2025 16:55:18 GMT  
		Size: 136.4 MB (136363125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4841b6900a2cdbc0387276356b9f70352556b5734bf3de3e6c1be6ddd48417b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84c88a8f00973496cd1a731c7b4bbc5d7e175db1c0ae733da6ab89a8324b51f`

```dockerfile
```

-	Layers:
	-	`sha256:dfb0586ae56992dd71717c8f0a7350ebb6e5a29cdbed2f8b6898f74884abd35f`  
		Last Modified: Thu, 11 Sep 2025 17:01:32 GMT  
		Size: 2.2 MB (2176832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d64290be2c9bb02e8b692ba3805d90e57aca9a40388943df5dce7bde4976fb`  
		Last Modified: Thu, 11 Sep 2025 17:01:33 GMT  
		Size: 13.3 KB (13279 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:91d5ce03126fc2cfd448fc5b66cb46e24cfe5295cfd3b6e092d7ad61dbdd6f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161748197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9913d20af3119ab7786d40a93fc16122e9cb5d0b07844491b0e9ab7a1d20bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:41 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:42 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 19 Aug 2025 17:21:42 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20c245bb91f7038c8e7666e50e3b477d3bb0faf772b531b6ddcd81ed6b348c`  
		Last Modified: Thu, 11 Sep 2025 16:54:02 GMT  
		Size: 1.5 MB (1455758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76030c75f4142a5689b96eca6cde0a943134234ff6c9d87d03a9329e795eec55`  
		Last Modified: Thu, 11 Sep 2025 16:54:15 GMT  
		Size: 132.3 MB (132288771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:151425a168e86dfb502122878fadd03e0cb693a485fc23b75b261bb32a4d1403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6c3b4ff7ad2d77a75245faa78673e79ee49078659c2c80a15eed04e21d79db`

```dockerfile
```

-	Layers:
	-	`sha256:20a9c4836bb69c0d31098a1bb635b557fd80fb2d19a91d436fc6539892df9bac`  
		Last Modified: Thu, 11 Sep 2025 17:01:37 GMT  
		Size: 2.2 MB (2173503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf945ea1a8caaea9ac34de09891ba9c69351602ed9041dbf0c51024f7dfdbc1f`  
		Last Modified: Thu, 11 Sep 2025 17:01:37 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:d239621a96b6bde3217cd455138d83b608e888b13c2441931500d96804940382
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
$ docker pull ibmjava@sha256:1b0a82f76e52d1c6f56d181125ef43476c205f783efe3c76dd1de0c8240a3356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166404491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a65d4cfb107cdf9bc5ce7a3022ddf7f125b04d51db34d7e375d27cd7981ea82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f065c842f2da0845216d333a640514a645a84dd427fccdccb3df9f40b51c79ad`  
		Last Modified: Thu, 11 Sep 2025 16:51:47 GMT  
		Size: 1.5 MB (1450068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d65874fb3a9b70af7e5e07c3590d8eff39eb32d2abf17167c95e2e2d1407c6`  
		Last Modified: Thu, 11 Sep 2025 16:51:56 GMT  
		Size: 135.4 MB (135417488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9188900a0ee53649aa2c6b470d33f1a8df0c36419199a4fa3b9a8ab996876dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166ab4f1e810df91f7f8a51a91b49e53334c47aae2ea722d27fe385e1b315153`

```dockerfile
```

-	Layers:
	-	`sha256:c4d69b9119265863742b61e0a8a7622e1fab18492f44f8d571ef7106048f65e5`  
		Last Modified: Thu, 11 Sep 2025 17:01:28 GMT  
		Size: 2.2 MB (2173542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44e6790e199eb8d1906ca55a4693385be8f849b664086e990d04cffd631b3c7`  
		Last Modified: Thu, 11 Sep 2025 17:01:28 GMT  
		Size: 13.2 KB (13234 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:f61c0cae7db779aae08e6fc26e104a32d491548689f63043eb24b435af6ed5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172342564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dc03516ec3c4536a1b3609e67d10baf2054cc617b639284dd0c9db5602bce3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a4572befc841349373b827c193ac673418ba5463306814c6d4c89cbdc534a3`  
		Last Modified: Thu, 11 Sep 2025 16:55:18 GMT  
		Size: 136.4 MB (136363125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4841b6900a2cdbc0387276356b9f70352556b5734bf3de3e6c1be6ddd48417b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84c88a8f00973496cd1a731c7b4bbc5d7e175db1c0ae733da6ab89a8324b51f`

```dockerfile
```

-	Layers:
	-	`sha256:dfb0586ae56992dd71717c8f0a7350ebb6e5a29cdbed2f8b6898f74884abd35f`  
		Last Modified: Thu, 11 Sep 2025 17:01:32 GMT  
		Size: 2.2 MB (2176832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d64290be2c9bb02e8b692ba3805d90e57aca9a40388943df5dce7bde4976fb`  
		Last Modified: Thu, 11 Sep 2025 17:01:33 GMT  
		Size: 13.3 KB (13279 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:91d5ce03126fc2cfd448fc5b66cb46e24cfe5295cfd3b6e092d7ad61dbdd6f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161748197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9913d20af3119ab7786d40a93fc16122e9cb5d0b07844491b0e9ab7a1d20bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:41 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:42 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 19 Aug 2025 17:21:42 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f60e0d5d6ccfd8485f946e32a47aa2f27c8c3ffea4f8be3da44fd485e769296b';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='3570bdc9bc6171ca97900a592ca0958630abf445980054cf196a565369b31dd8';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='a2e8c1dc63e33ac0b62072ea27c8ab7aa0e77f16214079fd0d4e4e3ab00770db';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20c245bb91f7038c8e7666e50e3b477d3bb0faf772b531b6ddcd81ed6b348c`  
		Last Modified: Thu, 11 Sep 2025 16:54:02 GMT  
		Size: 1.5 MB (1455758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76030c75f4142a5689b96eca6cde0a943134234ff6c9d87d03a9329e795eec55`  
		Last Modified: Thu, 11 Sep 2025 16:54:15 GMT  
		Size: 132.3 MB (132288771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:151425a168e86dfb502122878fadd03e0cb693a485fc23b75b261bb32a4d1403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6c3b4ff7ad2d77a75245faa78673e79ee49078659c2c80a15eed04e21d79db`

```dockerfile
```

-	Layers:
	-	`sha256:20a9c4836bb69c0d31098a1bb635b557fd80fb2d19a91d436fc6539892df9bac`  
		Last Modified: Thu, 11 Sep 2025 17:01:37 GMT  
		Size: 2.2 MB (2173503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf945ea1a8caaea9ac34de09891ba9c69351602ed9041dbf0c51024f7dfdbc1f`  
		Last Modified: Thu, 11 Sep 2025 17:01:37 GMT  
		Size: 13.2 KB (13235 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:74d3bda6f6d4f2baab5a774fcbe3a261d1c3b39ba4291de93bff21a22b4618a5
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
$ docker pull ibmjava@sha256:a4e86e7e963bb140193bce61999ab60873b194920e6f3f2677c4dd1ff1897114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203651617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c825252fdd90bc45d8d5a8136d843d8abc925f293d6358d0b36d8d119a9521c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6501625c0bd93c3a9e7bdafec2b1df8d65ee819572e7bb6e337314ab31718ce`  
		Last Modified: Thu, 11 Sep 2025 16:55:12 GMT  
		Size: 1.5 MB (1450049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cd794a5e418d61cd9f0391f9aa128310c0ef64a7a804c3fddc9453c8e60e54`  
		Last Modified: Thu, 11 Sep 2025 16:55:28 GMT  
		Size: 172.7 MB (172664633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8d8ed0552d583b4c47cd794b3b7fe65d04cb032ef7a0c5023219eb6e2848b14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0764f247578177811c8299f3f381aaf4c9a6d66ed8078a57a6bb4ca8f99276a`

```dockerfile
```

-	Layers:
	-	`sha256:bc327b38491b257672e0a4502977afe6cc3e8c379e51835b07374cda9a672a22`  
		Last Modified: Thu, 11 Sep 2025 17:01:37 GMT  
		Size: 3.1 MB (3083862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d93adadbac258a4a779929cc35c438bac6094a62a49528fa32beab5441051d`  
		Last Modified: Thu, 11 Sep 2025 17:01:38 GMT  
		Size: 12.6 KB (12640 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:08a8566ccfe4418a3fb255c8bf80d75d075ff4fa57edf1dcd626344367ee0db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209792835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7105fecb952660c84a56ed6369e637166001c98b86c9d5729c71d12bfd168518`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a9f118ca1f1cbf4058ca82bc7edc4791643f5aab1e787697cb7e9c745ab8b`  
		Last Modified: Thu, 11 Sep 2025 19:08:09 GMT  
		Size: 173.8 MB (173813396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2ad0c9a971f6f7cffe9535a8e552aa37f93e4d387a83315e750340fba77c10e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d7b10107d12da4e11d5eccc49ed51187b4c08568a23257eb81c836508a31bb`

```dockerfile
```

-	Layers:
	-	`sha256:d73775d92e2134667c0aff4df85c2160daebc74a5b80c55cd05bc824438657de`  
		Last Modified: Thu, 11 Sep 2025 17:01:43 GMT  
		Size: 3.1 MB (3069811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d985f7e2e6540354f101f0ac3e9c767e6d383caa0f8d32a8c2befb77f6af1dfb`  
		Last Modified: Thu, 11 Sep 2025 17:01:43 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:df015a580d51c21d085a256fdbbca654ebed500e98dcb9f4d4b50fcb086578a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192092404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1171e56899eedb16c53b5d5ea649d0cc709f30f2d14c6e33dd508dcb16598aa6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:41 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:42 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 19 Aug 2025 17:21:42 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20c245bb91f7038c8e7666e50e3b477d3bb0faf772b531b6ddcd81ed6b348c`  
		Last Modified: Thu, 11 Sep 2025 16:54:02 GMT  
		Size: 1.5 MB (1455758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b95b4dad0cf791eac4470394de71d0a10e6de0edfef58b1a82a54a4246b113`  
		Last Modified: Thu, 11 Sep 2025 18:09:36 GMT  
		Size: 162.6 MB (162632978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9a29e52165ffe924b8a4b096073fcc93b18c0267fba859fa8365bc05561df20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2769819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84372ba8dabbe00c434d3759fa6b1f69738b55448e441e7e3a9ce34ce98afb`

```dockerfile
```

-	Layers:
	-	`sha256:f15d35e9681977cabbff2d13b7143d3711edb2591c8307bec77e60decaeaf5aa`  
		Last Modified: Thu, 11 Sep 2025 17:01:48 GMT  
		Size: 2.8 MB (2757178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8212a42d609e6b91efa2b219c2f30e17ed3e3f8f08b9a1f1fc74f297a8e502`  
		Last Modified: Thu, 11 Sep 2025 17:01:49 GMT  
		Size: 12.6 KB (12641 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:018aecce38d94f2bbc3126f8be5af4565e028b22b7f76763f74e7c500daca712
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
$ docker pull ibmjava@sha256:941e76a10c609cdcea7af1a31f64ad460e64a3f2f9858560f03216e94ba604b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101767001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070b5ad024e6926782d4baf3ddbedc89b6ddb7d26592362674608939874add0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5cc1fe4a2152a92f4eb29e17d29c0b87571724d32c79d01c02ff8e1e39162cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='41ad5b9cf2a6b78925bbf89b087358a409c949a7dd21318213faa84edc0f4f6c';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='7761751660e6eef25e16627dd18850eb978eb71757cfbc443d142a0ff24d3019';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97eae39341901ed480b5ffc400b148e3b064ada449dc8356f9021c40d769d763`  
		Last Modified: Thu, 11 Sep 2025 16:58:08 GMT  
		Size: 1.5 MB (1450049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9d58ee16499cb31d15b1881d0cd69484a43df16edc4a6c762d48c2091fe081`  
		Last Modified: Thu, 11 Sep 2025 18:41:35 GMT  
		Size: 70.8 MB (70780017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:647a745cf51a3fd39fbe1cf74bfa7fb56fc30f1647eb1379f8ac8b1388c4bfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2168617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314a5292256067f7a4ea967d792da6a62ac807be18b4a3dce19d029df97be455`

```dockerfile
```

-	Layers:
	-	`sha256:3dc43fabb8171065ad60f29eeae2021758f6f635ef87512cf8f5cc13e0f4b051`  
		Last Modified: Thu, 11 Sep 2025 17:01:47 GMT  
		Size: 2.2 MB (2155973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c087eccb9855f5f4f2359b762b7c72ea12fbbaa8487452d58584386498538a1`  
		Last Modified: Thu, 11 Sep 2025 17:01:48 GMT  
		Size: 12.6 KB (12644 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5768283f79683d9c81df8fd439ec1ed2a458a719746e8b035e812503ed71ae7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107697908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6478380cf4949310efe126271609ef891f633ddcac714dad3686c2ef2eb06a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5cc1fe4a2152a92f4eb29e17d29c0b87571724d32c79d01c02ff8e1e39162cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='41ad5b9cf2a6b78925bbf89b087358a409c949a7dd21318213faa84edc0f4f6c';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='7761751660e6eef25e16627dd18850eb978eb71757cfbc443d142a0ff24d3019';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab09ea0d3d5e01e0b96c1ebf6b9caf0a0fd955b2c058934d2cb9b4ab1f1ac1b`  
		Last Modified: Thu, 11 Sep 2025 16:53:07 GMT  
		Size: 71.7 MB (71718469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:013384a5471e14701278511c0d132232484a81251b108ed71affdb1c222ed9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca43401ee7bd05ecdeb6169e3eacad13067cc5ea5d2e8138c56fe25fab5adf80`

```dockerfile
```

-	Layers:
	-	`sha256:4dd21f81db1db48491285445529c24768cb51e5ca63e6a9375b3bcb734d36aa1`  
		Last Modified: Thu, 11 Sep 2025 17:01:51 GMT  
		Size: 2.2 MB (2160474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c065c78a0812bf04e0aeaafb4db82abe6b9da9d59035a828fa505e2c4de8454e`  
		Last Modified: Thu, 11 Sep 2025 17:01:52 GMT  
		Size: 12.7 KB (12678 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:94bba6f5a41cf3bede697e716082d74f37828ea469ed01a41774666fc8ec19f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100737882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ac625bb30e72b6a1b5746089757f75a7c5a0402bc308b39705267a4f6367b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:41 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:42 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 19 Aug 2025 17:21:42 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b5cc1fe4a2152a92f4eb29e17d29c0b87571724d32c79d01c02ff8e1e39162cb';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='41ad5b9cf2a6b78925bbf89b087358a409c949a7dd21318213faa84edc0f4f6c';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='7761751660e6eef25e16627dd18850eb978eb71757cfbc443d142a0ff24d3019';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20c245bb91f7038c8e7666e50e3b477d3bb0faf772b531b6ddcd81ed6b348c`  
		Last Modified: Thu, 11 Sep 2025 16:54:02 GMT  
		Size: 1.5 MB (1455758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f28446ca487e1c75570676d0e415743f6de5e3073a38970ac2e06ba2471a75e`  
		Last Modified: Thu, 11 Sep 2025 19:17:56 GMT  
		Size: 71.3 MB (71278456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6a59aa51a5e4d3a5a8c73b15da2127a8e87052c49641dd954c5c5bd8b12f4b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee240008aa5798377083f90b412066a6bfd3f58b7409e538f2f70f4192e9dd3b`

```dockerfile
```

-	Layers:
	-	`sha256:c7f7b1c827cb525b75438ae3b265c98ace44074050563ca080c6edd2bc4f1b29`  
		Last Modified: Thu, 11 Sep 2025 17:01:59 GMT  
		Size: 2.2 MB (2159595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80c7eb053dbc48034e7fc48d4ddaeba07f67af6734bc30d2198c772143327336`  
		Last Modified: Thu, 11 Sep 2025 17:01:59 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.in-toto+json
