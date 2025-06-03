## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:4b87b048f696812030c42b25e99753f21685e683fff63f9da1a5b9f102af9d9d
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
$ docker pull ibmjava@sha256:20f9d44884baea081e43815f0c3d9d943b63d058f8283d43c8dd833df5f39825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204165671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f57f05b562f6be51de90aa3bb09397a9ee7c5dea890d78d4eb8be1223c9494`
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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1673ecf1f8cf29c7b6d44154073b2680ebb266fb061c00ce97737116e2f3ae`  
		Last Modified: Tue, 03 Jun 2025 13:40:34 GMT  
		Size: 1.5 MB (1450055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a185752a0304fcd0e6e7695a76b658b3b2519964cbb14da9e9c6023d3a2df39`  
		Last Modified: Tue, 03 Jun 2025 13:40:50 GMT  
		Size: 173.2 MB (173182613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a31d52ad4e81ff9d9bf4474de8008eeb09e626981d03af0303ca4ba335fbab39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2995717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f7f5edc90ce99963a574390b48faf8e194fcc849591142661f7e9274a911c9`

```dockerfile
```

-	Layers:
	-	`sha256:2b0f78e9080b325581210f9ae857d7eefe35ede6580979fc549aa51b4d1cb4ec`  
		Last Modified: Tue, 03 Jun 2025 04:16:30 GMT  
		Size: 3.0 MB (2982539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e749ad81944be5d3dcb8be2766d40da1a1d210a5b9e5176aed053ebfeda35c3`  
		Last Modified: Tue, 03 Jun 2025 04:16:30 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:d570c20f5a19b564cd6ba473e3094fe40f42e91f12d8ac6964894ffa3d51060a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210215096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d43aed8684f9a234fe8b4a9a0b2e23eca37b67a119375b6dde37f0f006db647`
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
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 14 May 2025 06:59:54 GMT
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
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891109dd0128b9f59129f4522b4284aca40ef5ea9f2dc570cb2c0b92efb59fa1`  
		Last Modified: Tue, 03 Jun 2025 04:50:25 GMT  
		Size: 1.5 MB (1536197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b2f15547e085ef3c2dab3cf0b44b8874219e968cbbda093d20abd7c8d74782`  
		Last Modified: Tue, 03 Jun 2025 04:53:16 GMT  
		Size: 174.2 MB (174238542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4d55357fb38c6953f24e09641304a3d961a8c69787ce99c7eab3a1cfc4fc891f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c972396277330bced79b7e419c2b5dcee2f83114f21a0973accc49a01bf45cc`

```dockerfile
```

-	Layers:
	-	`sha256:f31da5dc5ccdd685059bb0b15e8aff4edb6eed9dcd1906e91db89e9939f9d5fe`  
		Last Modified: Tue, 03 Jun 2025 04:53:01 GMT  
		Size: 3.0 MB (2968488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a5ccf50fc6429eab43f8ed24ea73b49a4ff4c8eac053070c55395a6938b398`  
		Last Modified: Tue, 03 Jun 2025 04:53:01 GMT  
		Size: 13.2 KB (13212 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:92c479b9321584afd388a500009071de71605089938119defa89d5a82ee4c74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192753473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd384000d924a2236616fec91fd4af7b135931b63869fe3a1b37fd79591ad5f`
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
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
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
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2d974b5413f042241053a768c76f997e675bc55e8e98836da09fd5211caf69`  
		Last Modified: Tue, 03 Jun 2025 04:39:50 GMT  
		Size: 163.3 MB (163297145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:86bad0987a14f67bfb89db9ee2684dc7c1f50acf6501ae85604317315bff7503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2669033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1348730ceea4c07afd5a1a64d53cbece01a0b205a6108b0fa6b00cb72d5451c`

```dockerfile
```

-	Layers:
	-	`sha256:74df62495bb96ef85a20d09412940687ef4e6fd3074c14dc90b4b4603424503e`  
		Last Modified: Tue, 03 Jun 2025 04:39:47 GMT  
		Size: 2.7 MB (2655855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d83a744ca31a81fdecced1884f246faa6ce3fb50139d3ec01cb389aabf576e`  
		Last Modified: Tue, 03 Jun 2025 04:39:47 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json
