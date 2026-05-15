## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:2d28e5ab81654e259c7d36df5871bb9050b66ed9134544c9c7d6efde999e8e54
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
$ docker pull ibmjava@sha256:904df201f6383cc9ead70e181687b883df0acef801f0bf09a352d8164a489ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102358541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecf05ff280707ac486f26eebfd19d4127324e471eccf78947f35718a31bedaa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:19:05 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:19:05 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:19:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:19:28 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba576c4ef316d68967379dec28bb03028d4a3a95f768d9828ad2ef0ea30fb35`  
		Last Modified: Fri, 15 May 2026 21:19:38 GMT  
		Size: 1.5 MB (1450176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62586f28c7f918a7b3925c573f9d9504f2576f54fddc892f5a487a1de25fd29`  
		Last Modified: Fri, 15 May 2026 21:19:40 GMT  
		Size: 71.2 MB (71171681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:89cff7ba916d446828004a88553f0abcbfe72a7d3c832784a35551fef381bd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eee37ba6c912849820dff6783ad0aeeaca9ac87c258a0fe3c8470ce7a838523`

```dockerfile
```

-	Layers:
	-	`sha256:1b1b02646687b911212436e1ba09c3181569d6a015b9cef86e49a2db45b65312`  
		Last Modified: Fri, 15 May 2026 21:19:38 GMT  
		Size: 2.2 MB (2156553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67e39377de5d3fa77d47d43687b83872fe3324ee72e1f82ac876eaae91117ed0`  
		Last Modified: Fri, 15 May 2026 21:19:38 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:3141383ebe5a2e089e25b39bfdd673e8f1418e8fbf8c20707b7f07a0e49d2b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108298399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1792fcae05d923353cc2f840f4b90eb0a4464ed154f96f7b88e197e2a9717e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:28:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:28:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:28:40 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:29:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:29:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1d9502a29e5927b7c6acfcd4d85b9058b023b826aa21b29033ebc1aa0f839a`  
		Last Modified: Fri, 15 May 2026 21:29:48 GMT  
		Size: 1.5 MB (1536350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42df6d338f8a5ddd310bc564326251cb6eb60ba0e6a0a5d6a2ca9129d84c0cf6`  
		Last Modified: Fri, 15 May 2026 21:30:07 GMT  
		Size: 72.1 MB (72115329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:5344fb527b97ab23aa72e7573a21b62833cc65d8fa3723780d8323063eb04511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eab812fd50352e6b732160aa39576f395f3ffb4bd1eb0bd3e18a05bdfa5258b`

```dockerfile
```

-	Layers:
	-	`sha256:b7499d1c055b6fe9427040b3a1161b5e531308a134f705b4f755ee8a8c7979a5`  
		Last Modified: Fri, 15 May 2026 21:30:05 GMT  
		Size: 2.2 MB (2161054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f1e437aa4a8c2105265c995ae98dd28938ec9bdbf10fc45dbee111c0c32b8c`  
		Last Modified: Fri, 15 May 2026 21:30:05 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:ed614eff26a33fd4c0a754e09c4c94862858ea1419548a93f00472e0a9ea3132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102890366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0622d1544688a6ffa7890ec8fcb955af48cac15a5812ea9d892f22e12bffede6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:25:56 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:25:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:25:56 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:26:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a21f423374e941588c9d22e69cc011821558d044ba6a30c27eeb333535ed30be';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e85af7337f10d424e2660093dc3fc9d04e8c7e018eaa353a49e4dfa6902dd31d';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='bd360b8ccf462c9537dd214c9cc5920b93145b44fe05d3b49e214d01d79cfb5c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:26:21 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db157cb22854d83df151b1cab375b07af965e81376821890ae19bc26409b7219`  
		Last Modified: Fri, 15 May 2026 21:26:47 GMT  
		Size: 1.5 MB (1455969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4c42c019d3a6cf3720c16966fb9c81793db4c39ca129edeefbebad9400df91`  
		Last Modified: Fri, 15 May 2026 21:26:49 GMT  
		Size: 73.2 MB (73232092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:0e46d8dc6c281e1f443487b85919b8ff673a29acc759f8652e1eb216e38e7297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e107e4f2de3d38c6d7679419d2dc09c1dd472b528db1691aa3ef4faa568e7d`

```dockerfile
```

-	Layers:
	-	`sha256:9f4368106e43a0789afab179900d7e5928b4bd9fd83e8770a396cf5ba5523917`  
		Last Modified: Fri, 15 May 2026 21:26:46 GMT  
		Size: 2.2 MB (2160175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9eeaba87ac6805046ec5f6b5e3a40594fed4a08e9e7f6794af5efe0ad35d7f3`  
		Last Modified: Fri, 15 May 2026 21:26:46 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json
