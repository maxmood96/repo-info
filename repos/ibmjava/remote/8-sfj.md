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
