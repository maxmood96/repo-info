## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:79b6e7b5f4f45eb532e4dc42477dc8ac7926208c2336ecd461941d39c29b01f3
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
$ docker pull ibmjava@sha256:94c86ca640ae5046c95125186258feb487169dc14a5db3739149ecc45a30e66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101795904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b299bebb433c40b89c3876eecd6aa8965dfdf6019f033c58f229af13cab68dc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:27:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:27:49 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:27:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f22293aa3dd1339100ae535f17165394ff107c8e3d96405d05f60dbd18f33f`  
		Last Modified: Thu, 13 Nov 2025 23:28:15 GMT  
		Size: 1.5 MB (1450120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d0c814951bc26aff8bff2d03b3ec64752fbafbeaf30e4528abafc99f9fc4f`  
		Last Modified: Thu, 13 Nov 2025 23:28:20 GMT  
		Size: 70.8 MB (70808986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e9344b379d323244df6ad5d78a9f1e6655495a33c20d00de0f8b2223d748a1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae97aa9fb04459eba1b3315f5647068b02997c2f37f5e9e5d99d1bb3490246fc`

```dockerfile
```

-	Layers:
	-	`sha256:d6beec6b486e9d9052486b54ddc3494cf60d82e956cd174864a2eed4cc32639e`  
		Last Modified: Fri, 14 Nov 2025 03:01:57 GMT  
		Size: 2.2 MB (2156553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d0c3e94320d49bb99b87a3b2a6412ba1164c208415e2977b987c85e2742207`  
		Last Modified: Fri, 14 Nov 2025 03:01:58 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:518898ecd353b1044020a3ac61e07f26981f33b798bbf9711c40e45d12ffaa2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107727942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c19e111323729ada63eb5bb62d1a94e18e1f008cb6d02beb26b9505c4908fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:09:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Nov 2025 00:09:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:09:25 GMT
ENV JAVA_VERSION=8.0.8.55
# Fri, 14 Nov 2025 00:10:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Nov 2025 00:10:32 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76270b161ad8aaab04f9d34ed9a759cb51f3badfe1e68d38e0d4b16506a51c2a`  
		Last Modified: Fri, 14 Nov 2025 00:10:18 GMT  
		Size: 1.5 MB (1536370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654c90ad57f1edace0e0837db894bc0f380d9c70a6642765f5625f5c2bd33fbb`  
		Last Modified: Fri, 14 Nov 2025 00:11:27 GMT  
		Size: 71.7 MB (71744850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:15a924c340dee20d80c5050ba5a9b2e3f12a5a1f2b70a7f2dee8c255ca85396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9472854f14764c847815b00a80b4630d2a02746fda6fe8d9bff753849d293f6a`

```dockerfile
```

-	Layers:
	-	`sha256:1f34efeedc9393f0bb43fb3d576570fa7073193d90e34d2aec31a7f0b8ee9daf`  
		Last Modified: Fri, 14 Nov 2025 03:02:02 GMT  
		Size: 2.2 MB (2161054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c5abf748813773a40dd4e7e8ebdd3fedbac5808e4446978ace29f3db51f229`  
		Last Modified: Fri, 14 Nov 2025 03:02:03 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:c754e5d3e4a6ca0dc1d32fbbf5150459e7aa23dabfca2e9babb52e88b32539a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101310498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2d682c11770b03a8d42c13260ad11557d9da23c232225f6ccd303c99c9db94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 13 Nov 2025 23:21:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:34 GMT
ENV JAVA_VERSION=8.0.8.55
# Thu, 13 Nov 2025 23:21:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='71f43874965302abd8905a9db5c8ebc91941cf1d1d742b49f9637136d75c31a2';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75dd366468ffb66fc7a38d9957d9051c39ef5ba06b58f29eb7d3f3a808a0bbfc';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='d19d5cc55f1d038211f23977eeb5ad31bc9227c38ede315dd9e26ecb3e67e03a';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 13 Nov 2025 23:21:58 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f53e2b06c4170f07ebf435fd72ef9ac6ac15a3124bc334c9b384fb2289ba66`  
		Last Modified: Thu, 13 Nov 2025 23:22:20 GMT  
		Size: 1.5 MB (1455744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfc6a31a90c9551e444527c9e1bb0727b7f3199306d593fec65d07940d0a8c5`  
		Last Modified: Thu, 13 Nov 2025 23:22:27 GMT  
		Size: 71.9 MB (71851469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5da19de5508346b8f1487fea4acb01e86f75db8078fad59a63c9372748181d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00225b72fe8bfd0bb9dfa99f09128dc1c66397f42de7a6a034fd4a8e1671a59`

```dockerfile
```

-	Layers:
	-	`sha256:5f989522c73a9337d0f297c998ef0be16b7597c489b888eab913735242270344`  
		Last Modified: Fri, 14 Nov 2025 03:02:08 GMT  
		Size: 2.2 MB (2160175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:937e6097f5a082656133be1b409dfec0d50a9082cb45b3421aabe98123715c36`  
		Last Modified: Fri, 14 Nov 2025 03:02:09 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json
