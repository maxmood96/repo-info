## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:3ee99d793e46399ebffcfb18c1dbf36890af8e256546f53067e9339e18406871
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
$ docker pull ibmjava@sha256:951c6bd5644caa1536ef38c2c7c82566c9dff3196388273117f9e81e5a499bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101273959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ef70bf37086dcfe4e01599736306eb8490db24a1c00750e2adce9a7a2113b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Feb 2025 09:27:08 GMT
ARG RELEASE
# Fri, 14 Feb 2025 09:27:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Feb 2025 09:27:08 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Fri, 14 Feb 2025 09:27:08 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='eed8efe1f3df198a66d24595f35433608aaed346916463353f64f664609df1a3';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d90bbeb03ba463c18d363088f606fdfe04905f52d6d79b53ff797ef5e3537f35';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f2c9a80832c6b631422fb72e18c269fb32d771e690bb9a821c8fa086ae685301';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='2e21e291682130e60d2d1a45a5f218a91f3d836061b7e3f6128ebd9a1f50a1d2';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ff3cf418f6876c1a11d9c9fb5d1f93abf4c920199ab3de83e0168de8828bdb`  
		Last Modified: Wed, 09 Apr 2025 01:18:23 GMT  
		Size: 1.5 MB (1450025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c547594127ae8a44e8ec0bf7ef633ad8236e8eea1d02441ed00f81c88d15f1`  
		Last Modified: Wed, 09 Apr 2025 01:18:25 GMT  
		Size: 70.3 MB (70291569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:7a9a9d8aa74fbd4182cddbcf464c97885a104815a1665c835b7fdacd67e845f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2047601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5539dbb5c89d71908bb49996a73e44024f750c760c216de1e4bb277f0935eac8`

```dockerfile
```

-	Layers:
	-	`sha256:119f9d26b05a6e694f9653bf8874e8418acc98a857184b900d1a02e0e47f3701`  
		Last Modified: Wed, 09 Apr 2025 01:18:24 GMT  
		Size: 2.0 MB (2034421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8bd2bff7e0011e2fbab984400a5650eb22fa30d27ab0ee8b9cbfc338fc6f441`  
		Last Modified: Wed, 09 Apr 2025 01:18:23 GMT  
		Size: 13.2 KB (13180 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:dae35417c2e572b4f42d2152464102cde31ba849feec1138bf0158f1fd0ae326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107100216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4698ab6488f4cb647e7aaac489bc32ae68e649f87ef633b87e981d49731643a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Feb 2025 09:27:08 GMT
ARG RELEASE
# Fri, 14 Feb 2025 09:27:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Feb 2025 09:27:08 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Fri, 14 Feb 2025 09:27:08 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='eed8efe1f3df198a66d24595f35433608aaed346916463353f64f664609df1a3';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d90bbeb03ba463c18d363088f606fdfe04905f52d6d79b53ff797ef5e3537f35';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f2c9a80832c6b631422fb72e18c269fb32d771e690bb9a821c8fa086ae685301';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='2e21e291682130e60d2d1a45a5f218a91f3d836061b7e3f6128ebd9a1f50a1d2';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547283e0c0c821c0ccce507ca8c0bf3a722405e0f39eb5af2c012b83f5afb63e`  
		Last Modified: Wed, 09 Apr 2025 05:42:37 GMT  
		Size: 1.5 MB (1536154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7933849feb221240c7c962aa50f30f0b2dc75aa494a1c981248831be216663`  
		Last Modified: Wed, 09 Apr 2025 05:43:37 GMT  
		Size: 71.1 MB (71121366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:79ca1af2455ad87978b9b62cabfb20564f7677e2f7c3b09248cec252e8c8db78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2052022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49eeb0698070db6536efa5a62071eaa28a5e9b84b007de5ac02a15b7f8b0d14c`

```dockerfile
```

-	Layers:
	-	`sha256:336fea574a3e45f5110646be3833d17321bd597d3a9d755ae0da87cc7e20b847`  
		Last Modified: Wed, 09 Apr 2025 05:43:35 GMT  
		Size: 2.0 MB (2038808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ccc7d1edc2adfa3778ef97f975775adac59a2df8ed7ef288f658c227dc9395d`  
		Last Modified: Wed, 09 Apr 2025 05:43:35 GMT  
		Size: 13.2 KB (13214 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:22a9263a46b26097cee95bee6463cb393594148d6de9d0d69de31ab6da12aefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100359675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe75b2584fe38008918adc4ebc8541d1b2da230aaa53d171d18d2cd2e92929b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Feb 2025 09:27:08 GMT
ARG RELEASE
# Fri, 14 Feb 2025 09:27:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 09:27:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Feb 2025 09:27:08 GMT
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Fri, 14 Feb 2025 09:27:08 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 09:27:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 14 Feb 2025 09:27:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_VERSION=8.0.8.40
# Fri, 14 Feb 2025 09:27:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='eed8efe1f3df198a66d24595f35433608aaed346916463353f64f664609df1a3';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d90bbeb03ba463c18d363088f606fdfe04905f52d6d79b53ff797ef5e3537f35';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f2c9a80832c6b631422fb72e18c269fb32d771e690bb9a821c8fa086ae685301';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='2e21e291682130e60d2d1a45a5f218a91f3d836061b7e3f6128ebd9a1f50a1d2';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:25cf79adc8d2979d397edb23d9d8f0127bc0edfd1addfa501b8a0cc74338576b`  
		Last Modified: Mon, 07 Apr 2025 08:26:58 GMT  
		Size: 28.0 MB (28000118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6215c58d34327932bbbf6cbb5a3923233ece2ff56399c106ff3b26c6484ea063`  
		Last Modified: Wed, 09 Apr 2025 05:08:26 GMT  
		Size: 1.5 MB (1455724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6043a4c0dd4123e6545247921c9695ebb8db9106e47b67aee96dd19080904e`  
		Last Modified: Wed, 09 Apr 2025 05:09:24 GMT  
		Size: 70.9 MB (70903833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6eb37ed991889500000c87ead92955cabc03d88e0d63a9e3a3ac639077b09b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad8a8110a9282af440443f1bc111faa69362e8d62e5d301aa972457c64ab20d`

```dockerfile
```

-	Layers:
	-	`sha256:9a70d5b850dc281efb51ebce0e1106d4537956a419ec7e47bdc699e248efa0f1`  
		Last Modified: Wed, 09 Apr 2025 05:09:22 GMT  
		Size: 2.0 MB (2038043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c943c07ea18bbd633001d11096b40fbf0a7517cdf3e07309da7d80705f99d003`  
		Last Modified: Wed, 09 Apr 2025 05:09:22 GMT  
		Size: 13.2 KB (13180 bytes)  
		MIME: application/vnd.in-toto+json
