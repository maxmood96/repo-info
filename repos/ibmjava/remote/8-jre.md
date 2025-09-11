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
