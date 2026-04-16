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
$ docker pull ibmjava@sha256:82a60c33570b4324e1a87d2bafcb4bc21cb6d229b9dbcd2317b9d46baee926a0
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
$ docker pull ibmjava@sha256:3491232ff36bb2d4291d32592fc0d6d04659f82fe7285e78771749cdc0a6d73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166990892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00c0255f01a74b5c7d4029f0c805b8d28551852dc0109d149505673a4dd6a3`
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
# Wed, 15 Apr 2026 20:43:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:43:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:43:03 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 15 Apr 2026 20:43:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 15 Apr 2026 20:43:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e6656aa949bc9120668008f0174df9af3263d89667721ba72b12d09832f84`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 1.5 MB (1450022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3ecc6727718bf42c434efd7c7d1448c5f249d557d296b12929aa8bc485f786`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 135.8 MB (135804372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:994150632679ccaa2542cd8e8f1b568f50c7686a32597bc61e0fa4e8f16a4bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28171f8678bb38436b4c9f63d587c50b3159b1c323d08476ddf6b0553a2fe466`

```dockerfile
```

-	Layers:
	-	`sha256:3fb831c80a7b71bd8d472c6b86cc381c0a8b64ce39af2ac4abe6132e1e73b7b2`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a06b96681d1b808c624c0e496814ef5f0017399e916ce8e20d7c449fab53f59`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:ce65a6f74e61c8dbd4681de82fe4e1b2697ea3d17aaad55d4651f36d4e1328a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172935759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818dba4fac2f3123827f24aa06bf48258286c6cb889cbee6eac029f8e60e6c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:35:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:35:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:35:59 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:36:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:36:41 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46f08eac5722791db689e31db7f3285ed36585185e1d6504498fb2c08160e1`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 1.5 MB (1536273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d34c2a8dc55ce7c2250f94a4a595c8747b9ea52bfdd50e5969292410820bbb4`  
		Last Modified: Wed, 01 Apr 2026 20:37:15 GMT  
		Size: 136.7 MB (136749826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6f0f04c21ec936a32c58347aad18248c57a81f1d00ac69e39f347f2d9cbc3aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6559bb550fcaf84ed2a06d2f50535f5ad09b2b1f03e46fc98b89901a4c87557`

```dockerfile
```

-	Layers:
	-	`sha256:2c1de585674bd458e69cdf53ed7c001703cd146a896c3985ddf383712f8a3dee`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3412fa6ba7ccaf088978f38cda49e613a624d8c23b4f0c79c894f376fa6be13e`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 13.2 KB (13237 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:6877ad0a7acf115d4dd954cb59f02cdc55b6939ae6d7ccc5a53f1a4145af623c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162929286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a05f65b60ea8028df484076509f5f14247129f389292920ae1de006d1b5acc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:20:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:20:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:20:52 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:25:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:25:28 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30411c0701e1daa1284b05687f223b1a2b9f84bbda71434a999c08f0d9847d7`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 1.5 MB (1455847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a3b19b26b60a27ac5874f0fbec061f0b7034006a93de279b6ba92da6268cd`  
		Last Modified: Wed, 01 Apr 2026 20:25:55 GMT  
		Size: 133.3 MB (133270712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f5afdf88bb75b1f54ffe05dcf9d4d64c98fe222b765c5fbb1aedadb85858ab27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6aafb22e0168d4216173d81320646a7e7e83f31d4c6aff13b238bf6733b8c2`

```dockerfile
```

-	Layers:
	-	`sha256:57e43f6a518347a59ba752e76839196061631ea5965e76419ee78d4e37257625`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 2.2 MB (2174077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c23318e44a09c3f19a04bbcd5f49132602dcde09873bcdf5da725e23ec5c20`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:82a60c33570b4324e1a87d2bafcb4bc21cb6d229b9dbcd2317b9d46baee926a0
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
$ docker pull ibmjava@sha256:3491232ff36bb2d4291d32592fc0d6d04659f82fe7285e78771749cdc0a6d73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166990892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00c0255f01a74b5c7d4029f0c805b8d28551852dc0109d149505673a4dd6a3`
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
# Wed, 15 Apr 2026 20:43:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:43:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:43:03 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 15 Apr 2026 20:43:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 15 Apr 2026 20:43:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e6656aa949bc9120668008f0174df9af3263d89667721ba72b12d09832f84`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 1.5 MB (1450022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3ecc6727718bf42c434efd7c7d1448c5f249d557d296b12929aa8bc485f786`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 135.8 MB (135804372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:994150632679ccaa2542cd8e8f1b568f50c7686a32597bc61e0fa4e8f16a4bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28171f8678bb38436b4c9f63d587c50b3159b1c323d08476ddf6b0553a2fe466`

```dockerfile
```

-	Layers:
	-	`sha256:3fb831c80a7b71bd8d472c6b86cc381c0a8b64ce39af2ac4abe6132e1e73b7b2`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a06b96681d1b808c624c0e496814ef5f0017399e916ce8e20d7c449fab53f59`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:ce65a6f74e61c8dbd4681de82fe4e1b2697ea3d17aaad55d4651f36d4e1328a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172935759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818dba4fac2f3123827f24aa06bf48258286c6cb889cbee6eac029f8e60e6c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:35:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:35:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:35:59 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:36:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:36:41 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46f08eac5722791db689e31db7f3285ed36585185e1d6504498fb2c08160e1`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 1.5 MB (1536273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d34c2a8dc55ce7c2250f94a4a595c8747b9ea52bfdd50e5969292410820bbb4`  
		Last Modified: Wed, 01 Apr 2026 20:37:15 GMT  
		Size: 136.7 MB (136749826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6f0f04c21ec936a32c58347aad18248c57a81f1d00ac69e39f347f2d9cbc3aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6559bb550fcaf84ed2a06d2f50535f5ad09b2b1f03e46fc98b89901a4c87557`

```dockerfile
```

-	Layers:
	-	`sha256:2c1de585674bd458e69cdf53ed7c001703cd146a896c3985ddf383712f8a3dee`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3412fa6ba7ccaf088978f38cda49e613a624d8c23b4f0c79c894f376fa6be13e`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 13.2 KB (13237 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:6877ad0a7acf115d4dd954cb59f02cdc55b6939ae6d7ccc5a53f1a4145af623c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162929286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a05f65b60ea8028df484076509f5f14247129f389292920ae1de006d1b5acc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:20:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:20:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:20:52 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:25:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:25:28 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30411c0701e1daa1284b05687f223b1a2b9f84bbda71434a999c08f0d9847d7`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 1.5 MB (1455847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a3b19b26b60a27ac5874f0fbec061f0b7034006a93de279b6ba92da6268cd`  
		Last Modified: Wed, 01 Apr 2026 20:25:55 GMT  
		Size: 133.3 MB (133270712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f5afdf88bb75b1f54ffe05dcf9d4d64c98fe222b765c5fbb1aedadb85858ab27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6aafb22e0168d4216173d81320646a7e7e83f31d4c6aff13b238bf6733b8c2`

```dockerfile
```

-	Layers:
	-	`sha256:57e43f6a518347a59ba752e76839196061631ea5965e76419ee78d4e37257625`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 2.2 MB (2174077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c23318e44a09c3f19a04bbcd5f49132602dcde09873bcdf5da725e23ec5c20`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:f4d0723261e7406ab543b150bde55898a5282a2fce91249c29a693ed2f832951
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
$ docker pull ibmjava@sha256:31485e564e13cec7b80d47b3571ef0ac804e3ae8adc1bb47ae9117d272c89a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204244733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190341d61bb45400a204a184da4774427ed8b1e863c34ab69d2d4d1128356f0d`
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
# Wed, 15 Apr 2026 20:43:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:43:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:43:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 15 Apr 2026 20:44:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 15 Apr 2026 20:44:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de0869c1d8322d2c466905fc89398127e5fa8da14bf6344b72aeaebf3e4b9fa`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 1.5 MB (1450020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3970b600b7b1cd0857ebfeea7cea0eb07dad38ecf3a14c048202c18536742bd7`  
		Last Modified: Wed, 15 Apr 2026 20:44:30 GMT  
		Size: 173.1 MB (173058215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:d84be83ff945e96525d226a74f6081139fe486120f8891c1f3e38d16332330b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4c3ac150eca994a850b2638985fd86e758a7c14e966ea4dce2e2c0175010db`

```dockerfile
```

-	Layers:
	-	`sha256:9ae97ec0cc041c42e95fd19a7e8b8b36cbcf6a1ce1b2276e7f9ae93a68e5afd8`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 3.1 MB (3084436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b85285139e231839d658cf0f7f98484356042e021c3eb3b37e9748ad57f0c12f`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:da4cd35af00a678bc964f706b210ece57db44c3009545aeeef6844252c295dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210398594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eb7b97a4786f07985c288e0fbdcd4ac0911b6292926e65ea666b8199f8e07f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:35:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:35:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:35:59 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:38:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:38:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46f08eac5722791db689e31db7f3285ed36585185e1d6504498fb2c08160e1`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 1.5 MB (1536273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29860e716cdf5ebc33e42e2dfa9ebfc64424bdcb33dd0e665d639d8eccb8aa8a`  
		Last Modified: Wed, 01 Apr 2026 20:38:57 GMT  
		Size: 174.2 MB (174212661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:824ddc6123b9818c1a7c90600348b2d40a1eee5fa7ede6f0cc0c9e05bf15b179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b849d45431a5a49fd351226991c561b22cf597494239fe9eefbc0214ab4da4`

```dockerfile
```

-	Layers:
	-	`sha256:62e2d3ac81361451182cfb82bd6a1d9467a14df00c477efaf289ee10405a3ec3`  
		Last Modified: Wed, 01 Apr 2026 20:38:53 GMT  
		Size: 3.1 MB (3070385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef331800c1c610791ea3e8c313c5e7ab32c9d24b0133324125900c7e1c94336c`  
		Last Modified: Wed, 01 Apr 2026 20:38:53 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:7f7561a6c6f525235f49f5ee91f1086b3ee9d5e716b0d601153f0cf32e889c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193289107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daeb577723fa0c44ef125d8138fcf6fb0f60a59aef81c1a278772c793e4e07b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:21:56 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:21:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:21:56 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:26:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:26:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad3ba51fec85d95bc5946df2275446083583154b2c7efc5456844e0bc64a45`  
		Last Modified: Wed, 01 Apr 2026 20:24:45 GMT  
		Size: 1.5 MB (1455857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6952d6f6d72c8342d9547619945891a7effe935c315d9400506aa5ac9399e286`  
		Last Modified: Wed, 01 Apr 2026 20:27:36 GMT  
		Size: 163.6 MB (163630523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:d4b2732951d6e9dd2e4db69fbc6a34990e971a12265c2035a5cdf0f3b56d9ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2770350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535739bd26c04d5fe9fd73f8dbcffeae233f28bffed8e059f6fb8b4cdcb3093e`

```dockerfile
```

-	Layers:
	-	`sha256:c4afb088eef489e5659cf50a68cb11ea0092988c306eeb13ac79a8fa1bc262e9`  
		Last Modified: Wed, 01 Apr 2026 20:27:29 GMT  
		Size: 2.8 MB (2757752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3584261466822b60939ab7f36bac4f4a03fc405b82dbd15fbfcd1e405e015b07`  
		Last Modified: Wed, 01 Apr 2026 20:27:28 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:cb6d7a596278de121699789801ab8eb0b7def6642a69951cf16ca34b23fb9df1
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
$ docker pull ibmjava@sha256:3a14b5984556e8fc0993827621b8c8b64e419028e41bcadca0ce3f435618b19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102230649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df32196461ef0ec34e6a8cc349dd3816390c9497994e1d72f93c981c8b5d9c0b`
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
# Wed, 15 Apr 2026 20:43:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:43:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:43:00 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 15 Apr 2026 20:43:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 15 Apr 2026 20:43:23 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f7e6e23a459d508a1abf241b2061398a1aec74217c34c26e4045b3c5cc3ec0`  
		Last Modified: Wed, 15 Apr 2026 20:43:32 GMT  
		Size: 1.5 MB (1450156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb58e8b751043787aa29355c95bee810f0392f4b6c024cbe7b101d311447c97c`  
		Last Modified: Wed, 15 Apr 2026 20:43:34 GMT  
		Size: 71.0 MB (71043995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0365b137c2c668acff2947f10cd08f1b746965473c7bfa5dd8cabeb126478d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295f4702c2492e56652fd74ef3155c3fda57ecadb47755168a3cd35f2f68474a`

```dockerfile
```

-	Layers:
	-	`sha256:1e2ca45aeb3b6074c931ad4a0ec0ce534e42ea7575c66b789a66281c27b3937f`  
		Last Modified: Wed, 15 Apr 2026 20:43:33 GMT  
		Size: 2.2 MB (2156549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8fd142bb184816755c48c529b4de22b4d14396281337eb0ec91092b9d814a92`  
		Last Modified: Wed, 15 Apr 2026 20:43:32 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:a5da2612afe2fd369a388208deb7e10c1c8b9faeb9f5ead043600761a8b1db03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108169505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbdff74e65251f931c593a9f4a115e49ccacd5ff9988cc4a143f741b8fcd005`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:35:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:35:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:35:59 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:37:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:37:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46f08eac5722791db689e31db7f3285ed36585185e1d6504498fb2c08160e1`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 1.5 MB (1536273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd694889bf001caff37f11b8e72dafa84e801353564d721038f5fa09d87031`  
		Last Modified: Wed, 01 Apr 2026 20:37:30 GMT  
		Size: 72.0 MB (71983572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:67066ecdb648f23de1d408590d9c1124eebb66507badf17ece8f13e3a00397df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22a4c76c05bfe2ba2876fe07ea9da6cb3114b6ad73bc133604a3903cd587e31`

```dockerfile
```

-	Layers:
	-	`sha256:b9f85b52a6a2940a2fe7f53ea6d23d3db1f183ac1f7d2496188259d6bdb82592`  
		Last Modified: Wed, 01 Apr 2026 20:37:28 GMT  
		Size: 2.2 MB (2161050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8faabe4539b61fbef265dac4f544a92bba01828ffb3d9fd4ea2f2ec623c9423f`  
		Last Modified: Wed, 01 Apr 2026 20:37:27 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:4d072d9413ac4463a815d1ce6897ccf301ebdb2d7d80339d6d3302a27270a544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101743950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1609f3f652195ca934b1cc87286e2bfea4d0ddaca5d132f790f3647bd8e9c038`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:21:56 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:21:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:21:56 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:24:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:24:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad3ba51fec85d95bc5946df2275446083583154b2c7efc5456844e0bc64a45`  
		Last Modified: Wed, 01 Apr 2026 20:24:45 GMT  
		Size: 1.5 MB (1455857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f729be7b49cfec4cd2b235d013ed3581054fa5e8b71feeda1493168cc8c60c`  
		Last Modified: Wed, 01 Apr 2026 20:24:47 GMT  
		Size: 72.1 MB (72085366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9ec577c012d35739d93d78593c621a00c41e638525eefe1ffd40b9d2f3b0aa16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe8db5465e6432d7d69d8dd097d31896481d60f5d01425c196e69c6f3896e73`

```dockerfile
```

-	Layers:
	-	`sha256:ac066dc2bd56d506a69bf1379dc64937b8e7367c67bb31b8eb526fd5a11c9f5a`  
		Last Modified: Wed, 01 Apr 2026 20:24:45 GMT  
		Size: 2.2 MB (2160171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3f860477b481f504c6edadc01f659414897fd4b86b3692d5ff115333d5f3f6`  
		Last Modified: Wed, 01 Apr 2026 20:24:45 GMT  
		Size: 12.6 KB (12600 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:82a60c33570b4324e1a87d2bafcb4bc21cb6d229b9dbcd2317b9d46baee926a0
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
$ docker pull ibmjava@sha256:3491232ff36bb2d4291d32592fc0d6d04659f82fe7285e78771749cdc0a6d73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166990892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00c0255f01a74b5c7d4029f0c805b8d28551852dc0109d149505673a4dd6a3`
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
# Wed, 15 Apr 2026 20:43:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:43:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:43:03 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 15 Apr 2026 20:43:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 15 Apr 2026 20:43:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e6656aa949bc9120668008f0174df9af3263d89667721ba72b12d09832f84`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 1.5 MB (1450022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3ecc6727718bf42c434efd7c7d1448c5f249d557d296b12929aa8bc485f786`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 135.8 MB (135804372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:994150632679ccaa2542cd8e8f1b568f50c7686a32597bc61e0fa4e8f16a4bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28171f8678bb38436b4c9f63d587c50b3159b1c323d08476ddf6b0553a2fe466`

```dockerfile
```

-	Layers:
	-	`sha256:3fb831c80a7b71bd8d472c6b86cc381c0a8b64ce39af2ac4abe6132e1e73b7b2`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a06b96681d1b808c624c0e496814ef5f0017399e916ce8e20d7c449fab53f59`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:ce65a6f74e61c8dbd4681de82fe4e1b2697ea3d17aaad55d4651f36d4e1328a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172935759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818dba4fac2f3123827f24aa06bf48258286c6cb889cbee6eac029f8e60e6c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:35:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:35:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:35:59 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:36:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:36:41 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46f08eac5722791db689e31db7f3285ed36585185e1d6504498fb2c08160e1`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 1.5 MB (1536273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d34c2a8dc55ce7c2250f94a4a595c8747b9ea52bfdd50e5969292410820bbb4`  
		Last Modified: Wed, 01 Apr 2026 20:37:15 GMT  
		Size: 136.7 MB (136749826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6f0f04c21ec936a32c58347aad18248c57a81f1d00ac69e39f347f2d9cbc3aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6559bb550fcaf84ed2a06d2f50535f5ad09b2b1f03e46fc98b89901a4c87557`

```dockerfile
```

-	Layers:
	-	`sha256:2c1de585674bd458e69cdf53ed7c001703cd146a896c3985ddf383712f8a3dee`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3412fa6ba7ccaf088978f38cda49e613a624d8c23b4f0c79c894f376fa6be13e`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 13.2 KB (13237 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:6877ad0a7acf115d4dd954cb59f02cdc55b6939ae6d7ccc5a53f1a4145af623c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162929286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a05f65b60ea8028df484076509f5f14247129f389292920ae1de006d1b5acc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:20:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:20:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:20:52 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:25:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:25:28 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30411c0701e1daa1284b05687f223b1a2b9f84bbda71434a999c08f0d9847d7`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 1.5 MB (1455847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a3b19b26b60a27ac5874f0fbec061f0b7034006a93de279b6ba92da6268cd`  
		Last Modified: Wed, 01 Apr 2026 20:25:55 GMT  
		Size: 133.3 MB (133270712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f5afdf88bb75b1f54ffe05dcf9d4d64c98fe222b765c5fbb1aedadb85858ab27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6aafb22e0168d4216173d81320646a7e7e83f31d4c6aff13b238bf6733b8c2`

```dockerfile
```

-	Layers:
	-	`sha256:57e43f6a518347a59ba752e76839196061631ea5965e76419ee78d4e37257625`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 2.2 MB (2174077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c23318e44a09c3f19a04bbcd5f49132602dcde09873bcdf5da725e23ec5c20`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:82a60c33570b4324e1a87d2bafcb4bc21cb6d229b9dbcd2317b9d46baee926a0
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
$ docker pull ibmjava@sha256:3491232ff36bb2d4291d32592fc0d6d04659f82fe7285e78771749cdc0a6d73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166990892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00c0255f01a74b5c7d4029f0c805b8d28551852dc0109d149505673a4dd6a3`
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
# Wed, 15 Apr 2026 20:43:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:43:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:43:03 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 15 Apr 2026 20:43:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 15 Apr 2026 20:43:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e6656aa949bc9120668008f0174df9af3263d89667721ba72b12d09832f84`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 1.5 MB (1450022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3ecc6727718bf42c434efd7c7d1448c5f249d557d296b12929aa8bc485f786`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 135.8 MB (135804372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:994150632679ccaa2542cd8e8f1b568f50c7686a32597bc61e0fa4e8f16a4bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28171f8678bb38436b4c9f63d587c50b3159b1c323d08476ddf6b0553a2fe466`

```dockerfile
```

-	Layers:
	-	`sha256:3fb831c80a7b71bd8d472c6b86cc381c0a8b64ce39af2ac4abe6132e1e73b7b2`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 2.2 MB (2174116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a06b96681d1b808c624c0e496814ef5f0017399e916ce8e20d7c449fab53f59`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:ce65a6f74e61c8dbd4681de82fe4e1b2697ea3d17aaad55d4651f36d4e1328a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172935759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818dba4fac2f3123827f24aa06bf48258286c6cb889cbee6eac029f8e60e6c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:35:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:35:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:35:59 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:36:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:36:41 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46f08eac5722791db689e31db7f3285ed36585185e1d6504498fb2c08160e1`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 1.5 MB (1536273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d34c2a8dc55ce7c2250f94a4a595c8747b9ea52bfdd50e5969292410820bbb4`  
		Last Modified: Wed, 01 Apr 2026 20:37:15 GMT  
		Size: 136.7 MB (136749826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6f0f04c21ec936a32c58347aad18248c57a81f1d00ac69e39f347f2d9cbc3aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6559bb550fcaf84ed2a06d2f50535f5ad09b2b1f03e46fc98b89901a4c87557`

```dockerfile
```

-	Layers:
	-	`sha256:2c1de585674bd458e69cdf53ed7c001703cd146a896c3985ddf383712f8a3dee`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 2.2 MB (2177406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3412fa6ba7ccaf088978f38cda49e613a624d8c23b4f0c79c894f376fa6be13e`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 13.2 KB (13237 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:6877ad0a7acf115d4dd954cb59f02cdc55b6939ae6d7ccc5a53f1a4145af623c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162929286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a05f65b60ea8028df484076509f5f14247129f389292920ae1de006d1b5acc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:20:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:20:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:20:52 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:25:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0a965c513bb522004ddb195fbb3cda7124559b8c7c082fc8626b2f45b4ce9a94';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ebf5f90f77e524593cba310d9e73d993bc8d3357af0127ec4627b1ce8236f385';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8353fb367a56fd150bd5b1facb595bde690c9f9a1f3db7db3b7fb240399a6ae9';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:25:28 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30411c0701e1daa1284b05687f223b1a2b9f84bbda71434a999c08f0d9847d7`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 1.5 MB (1455847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a3b19b26b60a27ac5874f0fbec061f0b7034006a93de279b6ba92da6268cd`  
		Last Modified: Wed, 01 Apr 2026 20:25:55 GMT  
		Size: 133.3 MB (133270712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f5afdf88bb75b1f54ffe05dcf9d4d64c98fe222b765c5fbb1aedadb85858ab27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6aafb22e0168d4216173d81320646a7e7e83f31d4c6aff13b238bf6733b8c2`

```dockerfile
```

-	Layers:
	-	`sha256:57e43f6a518347a59ba752e76839196061631ea5965e76419ee78d4e37257625`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 2.2 MB (2174077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c23318e44a09c3f19a04bbcd5f49132602dcde09873bcdf5da725e23ec5c20`  
		Last Modified: Wed, 01 Apr 2026 20:25:52 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:f4d0723261e7406ab543b150bde55898a5282a2fce91249c29a693ed2f832951
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
$ docker pull ibmjava@sha256:31485e564e13cec7b80d47b3571ef0ac804e3ae8adc1bb47ae9117d272c89a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204244733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190341d61bb45400a204a184da4774427ed8b1e863c34ab69d2d4d1128356f0d`
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
# Wed, 15 Apr 2026 20:43:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:43:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:43:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 15 Apr 2026 20:44:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 15 Apr 2026 20:44:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de0869c1d8322d2c466905fc89398127e5fa8da14bf6344b72aeaebf3e4b9fa`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 1.5 MB (1450020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3970b600b7b1cd0857ebfeea7cea0eb07dad38ecf3a14c048202c18536742bd7`  
		Last Modified: Wed, 15 Apr 2026 20:44:30 GMT  
		Size: 173.1 MB (173058215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:d84be83ff945e96525d226a74f6081139fe486120f8891c1f3e38d16332330b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4c3ac150eca994a850b2638985fd86e758a7c14e966ea4dce2e2c0175010db`

```dockerfile
```

-	Layers:
	-	`sha256:9ae97ec0cc041c42e95fd19a7e8b8b36cbcf6a1ce1b2276e7f9ae93a68e5afd8`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 3.1 MB (3084436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b85285139e231839d658cf0f7f98484356042e021c3eb3b37e9748ad57f0c12f`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:da4cd35af00a678bc964f706b210ece57db44c3009545aeeef6844252c295dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210398594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eb7b97a4786f07985c288e0fbdcd4ac0911b6292926e65ea666b8199f8e07f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:35:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:35:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:35:59 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:38:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:38:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46f08eac5722791db689e31db7f3285ed36585185e1d6504498fb2c08160e1`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 1.5 MB (1536273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29860e716cdf5ebc33e42e2dfa9ebfc64424bdcb33dd0e665d639d8eccb8aa8a`  
		Last Modified: Wed, 01 Apr 2026 20:38:57 GMT  
		Size: 174.2 MB (174212661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:824ddc6123b9818c1a7c90600348b2d40a1eee5fa7ede6f0cc0c9e05bf15b179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b849d45431a5a49fd351226991c561b22cf597494239fe9eefbc0214ab4da4`

```dockerfile
```

-	Layers:
	-	`sha256:62e2d3ac81361451182cfb82bd6a1d9467a14df00c477efaf289ee10405a3ec3`  
		Last Modified: Wed, 01 Apr 2026 20:38:53 GMT  
		Size: 3.1 MB (3070385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef331800c1c610791ea3e8c313c5e7ab32c9d24b0133324125900c7e1c94336c`  
		Last Modified: Wed, 01 Apr 2026 20:38:53 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:7f7561a6c6f525235f49f5ee91f1086b3ee9d5e716b0d601153f0cf32e889c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193289107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daeb577723fa0c44ef125d8138fcf6fb0f60a59aef81c1a278772c793e4e07b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:21:56 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:21:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:21:56 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:26:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:26:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad3ba51fec85d95bc5946df2275446083583154b2c7efc5456844e0bc64a45`  
		Last Modified: Wed, 01 Apr 2026 20:24:45 GMT  
		Size: 1.5 MB (1455857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6952d6f6d72c8342d9547619945891a7effe935c315d9400506aa5ac9399e286`  
		Last Modified: Wed, 01 Apr 2026 20:27:36 GMT  
		Size: 163.6 MB (163630523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:d4b2732951d6e9dd2e4db69fbc6a34990e971a12265c2035a5cdf0f3b56d9ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2770350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535739bd26c04d5fe9fd73f8dbcffeae233f28bffed8e059f6fb8b4cdcb3093e`

```dockerfile
```

-	Layers:
	-	`sha256:c4afb088eef489e5659cf50a68cb11ea0092988c306eeb13ac79a8fa1bc262e9`  
		Last Modified: Wed, 01 Apr 2026 20:27:29 GMT  
		Size: 2.8 MB (2757752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3584261466822b60939ab7f36bac4f4a03fc405b82dbd15fbfcd1e405e015b07`  
		Last Modified: Wed, 01 Apr 2026 20:27:28 GMT  
		Size: 12.6 KB (12598 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:cb6d7a596278de121699789801ab8eb0b7def6642a69951cf16ca34b23fb9df1
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
$ docker pull ibmjava@sha256:3a14b5984556e8fc0993827621b8c8b64e419028e41bcadca0ce3f435618b19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102230649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df32196461ef0ec34e6a8cc349dd3816390c9497994e1d72f93c981c8b5d9c0b`
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
# Wed, 15 Apr 2026 20:43:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 20:43:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:43:00 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 15 Apr 2026 20:43:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 15 Apr 2026 20:43:23 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f7e6e23a459d508a1abf241b2061398a1aec74217c34c26e4045b3c5cc3ec0`  
		Last Modified: Wed, 15 Apr 2026 20:43:32 GMT  
		Size: 1.5 MB (1450156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb58e8b751043787aa29355c95bee810f0392f4b6c024cbe7b101d311447c97c`  
		Last Modified: Wed, 15 Apr 2026 20:43:34 GMT  
		Size: 71.0 MB (71043995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0365b137c2c668acff2947f10cd08f1b746965473c7bfa5dd8cabeb126478d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295f4702c2492e56652fd74ef3155c3fda57ecadb47755168a3cd35f2f68474a`

```dockerfile
```

-	Layers:
	-	`sha256:1e2ca45aeb3b6074c931ad4a0ec0ce534e42ea7575c66b789a66281c27b3937f`  
		Last Modified: Wed, 15 Apr 2026 20:43:33 GMT  
		Size: 2.2 MB (2156549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8fd142bb184816755c48c529b4de22b4d14396281337eb0ec91092b9d814a92`  
		Last Modified: Wed, 15 Apr 2026 20:43:32 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:a5da2612afe2fd369a388208deb7e10c1c8b9faeb9f5ead043600761a8b1db03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108169505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbdff74e65251f931c593a9f4a115e49ccacd5ff9988cc4a143f741b8fcd005`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:35:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:35:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:35:59 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:37:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:37:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46f08eac5722791db689e31db7f3285ed36585185e1d6504498fb2c08160e1`  
		Last Modified: Wed, 01 Apr 2026 20:37:11 GMT  
		Size: 1.5 MB (1536273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd694889bf001caff37f11b8e72dafa84e801353564d721038f5fa09d87031`  
		Last Modified: Wed, 01 Apr 2026 20:37:30 GMT  
		Size: 72.0 MB (71983572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:67066ecdb648f23de1d408590d9c1124eebb66507badf17ece8f13e3a00397df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22a4c76c05bfe2ba2876fe07ea9da6cb3114b6ad73bc133604a3903cd587e31`

```dockerfile
```

-	Layers:
	-	`sha256:b9f85b52a6a2940a2fe7f53ea6d23d3db1f183ac1f7d2496188259d6bdb82592`  
		Last Modified: Wed, 01 Apr 2026 20:37:28 GMT  
		Size: 2.2 MB (2161050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8faabe4539b61fbef265dac4f544a92bba01828ffb3d9fd4ea2f2ec623c9423f`  
		Last Modified: Wed, 01 Apr 2026 20:37:27 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:4d072d9413ac4463a815d1ce6897ccf301ebdb2d7d80339d6d3302a27270a544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101743950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1609f3f652195ca934b1cc87286e2bfea4d0ddaca5d132f790f3647bd8e9c038`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:21:56 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 01 Apr 2026 20:21:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:21:56 GMT
ENV JAVA_VERSION=8.0.8.60
# Wed, 01 Apr 2026 20:24:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 01 Apr 2026 20:24:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ad3ba51fec85d95bc5946df2275446083583154b2c7efc5456844e0bc64a45`  
		Last Modified: Wed, 01 Apr 2026 20:24:45 GMT  
		Size: 1.5 MB (1455857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f729be7b49cfec4cd2b235d013ed3581054fa5e8b71feeda1493168cc8c60c`  
		Last Modified: Wed, 01 Apr 2026 20:24:47 GMT  
		Size: 72.1 MB (72085366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9ec577c012d35739d93d78593c621a00c41e638525eefe1ffd40b9d2f3b0aa16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe8db5465e6432d7d69d8dd097d31896481d60f5d01425c196e69c6f3896e73`

```dockerfile
```

-	Layers:
	-	`sha256:ac066dc2bd56d506a69bf1379dc64937b8e7367c67bb31b8eb526fd5a11c9f5a`  
		Last Modified: Wed, 01 Apr 2026 20:24:45 GMT  
		Size: 2.2 MB (2160171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3f860477b481f504c6edadc01f659414897fd4b86b3692d5ff115333d5f3f6`  
		Last Modified: Wed, 01 Apr 2026 20:24:45 GMT  
		Size: 12.6 KB (12600 bytes)  
		MIME: application/vnd.in-toto+json
