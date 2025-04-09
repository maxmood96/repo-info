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
$ docker pull ibmjava@sha256:f7a858a768b1975fa2f67fb7a9df25b53ca8b8af0cf783c7e25941d03638015b
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
$ docker pull ibmjava@sha256:fa66d3ffd6d446f4b7858a6db9468c233fa92b051bdb23952adc207a1698ae14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166504912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e25eb75a6e22a7f0c45c2f7aef2dae1eb5023e54010d888f2e1f7cf11ef23e`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db27cdfb76d083e85aa00bbe22cd27db8f26db49351cade3f1f1b94273a1da76`  
		Last Modified: Wed, 09 Apr 2025 01:18:32 GMT  
		Size: 1.5 MB (1450041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e999e5f4f81077186816d9ba8ce0d947fae85e4a5c0bac65f34bd23e065130`  
		Last Modified: Wed, 09 Apr 2025 01:18:35 GMT  
		Size: 135.5 MB (135522506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:bccc2d46c8b1939c71bc18f9c3be972421d179917812414d1687951908ecfb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456adc6ec54ad9c4056d307c39fda6724e7ccb5e0980085f49e87770364a95ba`

```dockerfile
```

-	Layers:
	-	`sha256:71dcaadab602430665323c5ccbe9b5b0c0f7992a9ecc4903375fc8006bcd3311`  
		Last Modified: Wed, 09 Apr 2025 01:18:33 GMT  
		Size: 2.1 MB (2051990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a78f5b5dcfb992cb1cdf54870844f424b32b56f799ad8003faf14d134360e2f`  
		Last Modified: Wed, 09 Apr 2025 01:18:32 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:274270747b5abea21a960f42061f464b3ce49b22a30cec37dfe0508d38b55031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172333065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b26e41a656c9a0420f2113876e9119ec2be0e302b0603f32e468e55b1c80a8`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:f6e20e03e21013c0c4063080549d0a6eeb04f87b108b83647341cd63ff74c591`  
		Last Modified: Wed, 09 Apr 2025 05:42:41 GMT  
		Size: 136.4 MB (136354215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:881d77f73bc488d26516a6a3a533f178e623b8ff67dc2562e9b0b59e32b841b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919cf8b458ff02d5ce49d4499665bf9490a7fc6209c16087ef4189bbddf69eda`

```dockerfile
```

-	Layers:
	-	`sha256:98fdee18d002d796d9680efcc7f18b9fd65cfec3bdb30a37bcd59a4ed953f6dc`  
		Last Modified: Wed, 09 Apr 2025 05:42:37 GMT  
		Size: 2.1 MB (2055166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428dadb91c413ba99bd94f5e4fdba3ce40af984476999bf152cbbdf4aa9ad138`  
		Last Modified: Wed, 09 Apr 2025 05:42:36 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:598bab09312b3707322b2a7b19e154a36793adddf50c045c2eda84cc554ee644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161995411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3d773cf6b524aff5660720beddcad47cf49f041f780e2f32c9fc39f16fad1`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:2a96f83eeef125d13c15be0fe185813042737a1ad8d8b818317b0b11146c6488`  
		Last Modified: Wed, 09 Apr 2025 05:08:28 GMT  
		Size: 132.5 MB (132539569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c87c4f16e43d3231108e6c4acb27d943d0398cdf703b5c59db0e64127014c63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c63aa6fb40a036e4be21c1d343fe4811cb8b303593c30f94b0d89fe40c63fe`

```dockerfile
```

-	Layers:
	-	`sha256:4918f6b620b6b98ec9b961693c2967a74d902df2f9b91df36d7d492a47a57654`  
		Last Modified: Wed, 09 Apr 2025 05:08:26 GMT  
		Size: 2.1 MB (2051951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b53a31dc11ac2921f5b5c4caaf9fec772cdfb5b8c996997be205f18245832f07`  
		Last Modified: Wed, 09 Apr 2025 05:08:26 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:f7a858a768b1975fa2f67fb7a9df25b53ca8b8af0cf783c7e25941d03638015b
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
$ docker pull ibmjava@sha256:fa66d3ffd6d446f4b7858a6db9468c233fa92b051bdb23952adc207a1698ae14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166504912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e25eb75a6e22a7f0c45c2f7aef2dae1eb5023e54010d888f2e1f7cf11ef23e`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db27cdfb76d083e85aa00bbe22cd27db8f26db49351cade3f1f1b94273a1da76`  
		Last Modified: Wed, 09 Apr 2025 01:18:32 GMT  
		Size: 1.5 MB (1450041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e999e5f4f81077186816d9ba8ce0d947fae85e4a5c0bac65f34bd23e065130`  
		Last Modified: Wed, 09 Apr 2025 01:18:35 GMT  
		Size: 135.5 MB (135522506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:bccc2d46c8b1939c71bc18f9c3be972421d179917812414d1687951908ecfb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456adc6ec54ad9c4056d307c39fda6724e7ccb5e0980085f49e87770364a95ba`

```dockerfile
```

-	Layers:
	-	`sha256:71dcaadab602430665323c5ccbe9b5b0c0f7992a9ecc4903375fc8006bcd3311`  
		Last Modified: Wed, 09 Apr 2025 01:18:33 GMT  
		Size: 2.1 MB (2051990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a78f5b5dcfb992cb1cdf54870844f424b32b56f799ad8003faf14d134360e2f`  
		Last Modified: Wed, 09 Apr 2025 01:18:32 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:274270747b5abea21a960f42061f464b3ce49b22a30cec37dfe0508d38b55031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172333065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b26e41a656c9a0420f2113876e9119ec2be0e302b0603f32e468e55b1c80a8`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:f6e20e03e21013c0c4063080549d0a6eeb04f87b108b83647341cd63ff74c591`  
		Last Modified: Wed, 09 Apr 2025 05:42:41 GMT  
		Size: 136.4 MB (136354215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:881d77f73bc488d26516a6a3a533f178e623b8ff67dc2562e9b0b59e32b841b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919cf8b458ff02d5ce49d4499665bf9490a7fc6209c16087ef4189bbddf69eda`

```dockerfile
```

-	Layers:
	-	`sha256:98fdee18d002d796d9680efcc7f18b9fd65cfec3bdb30a37bcd59a4ed953f6dc`  
		Last Modified: Wed, 09 Apr 2025 05:42:37 GMT  
		Size: 2.1 MB (2055166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428dadb91c413ba99bd94f5e4fdba3ce40af984476999bf152cbbdf4aa9ad138`  
		Last Modified: Wed, 09 Apr 2025 05:42:36 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:598bab09312b3707322b2a7b19e154a36793adddf50c045c2eda84cc554ee644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161995411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3d773cf6b524aff5660720beddcad47cf49f041f780e2f32c9fc39f16fad1`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:2a96f83eeef125d13c15be0fe185813042737a1ad8d8b818317b0b11146c6488`  
		Last Modified: Wed, 09 Apr 2025 05:08:28 GMT  
		Size: 132.5 MB (132539569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c87c4f16e43d3231108e6c4acb27d943d0398cdf703b5c59db0e64127014c63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c63aa6fb40a036e4be21c1d343fe4811cb8b303593c30f94b0d89fe40c63fe`

```dockerfile
```

-	Layers:
	-	`sha256:4918f6b620b6b98ec9b961693c2967a74d902df2f9b91df36d7d492a47a57654`  
		Last Modified: Wed, 09 Apr 2025 05:08:26 GMT  
		Size: 2.1 MB (2051951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b53a31dc11ac2921f5b5c4caaf9fec772cdfb5b8c996997be205f18245832f07`  
		Last Modified: Wed, 09 Apr 2025 05:08:26 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:19e09864e3ec5c5b4710216274a89e1a7d4942df9a6c8a2ee782b531f73aabae
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
$ docker pull ibmjava@sha256:d6a7265a5c1dddceb25a6ae417fa0c8555506d1669e2f468b2410c03867178e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203889890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ce5a0f7586a8bf116f8960f585c666af55405a55ee8f405b1f44dc737409fb`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e160359d8ef9f6b95400b0f6946e1ad5590c998300f10ac80576e68a624f5ee`  
		Last Modified: Wed, 09 Apr 2025 01:18:51 GMT  
		Size: 1.5 MB (1450037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03d8575c7c900c1ac40fc6b6d512946ce651e0fb3883564d887013f164d0186`  
		Last Modified: Wed, 09 Apr 2025 01:18:55 GMT  
		Size: 172.9 MB (172907488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:422ad9740ca1f51d146a57c52f7bcda727b4a30b255371ad1b49979cc39a39fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d264201ed5c558a7f17952d06e543a75450e0695ffc3af936214b28b3d9f1289`

```dockerfile
```

-	Layers:
	-	`sha256:359202f8bd9abfc2584827afb339f435559012e613bd8592974f37de610d6ea2`  
		Last Modified: Wed, 09 Apr 2025 01:18:51 GMT  
		Size: 3.0 MB (2959908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc8c6287d8981938b613ac5acb7739f90c763dc38c337365c6ab7b1d7bdd102`  
		Last Modified: Wed, 09 Apr 2025 01:18:51 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:8c02f261e17e774ef6b2592404977ed53365082ddea6bd369f15b61cc39f4a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209920489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696ba1a2214faa0b81dcdb3e54ecf593f71c835b2fea333c7ad1984a2b7cefe8`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:94a486f14c82490d7022fce81becc9831b167271c5d80e92e44d831d55dfbd10`  
		Last Modified: Wed, 09 Apr 2025 05:45:19 GMT  
		Size: 173.9 MB (173941639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:cb4b91fb2c9c9f2f4701d0ace000423092d3a0d589830e3ab05df0d025051184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3626e0958e7b6cb9cd325c53a9f055bbf150edcaef8d842843d1c9653cac7f`

```dockerfile
```

-	Layers:
	-	`sha256:78eb1d10af6ab42f4af54f4ff54475443060d36a3b070f3a1b590a904f63fb9f`  
		Last Modified: Wed, 09 Apr 2025 05:45:14 GMT  
		Size: 2.9 MB (2945743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54e5a823c1208b307b7551d76b0590ee18e3e97b8d997e2054fb92f395bf9b2`  
		Last Modified: Wed, 09 Apr 2025 05:45:13 GMT  
		Size: 13.2 KB (13212 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:b8e17beabe21f7ebaf1b8061ba88908a7e78f1ecff1c817369cdf0e7d0ca510f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192505552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded2a8728cde5788b371a54de5fb3830b1767a8962a5d999b1603f817553978f`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:9775d5de41669e8a25add8ba3d9865f1d82d1d3297bdde2813194a937393ad4a`  
		Last Modified: Wed, 09 Apr 2025 05:11:01 GMT  
		Size: 163.0 MB (163049710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ed0ea94062e1787480b1f2958a35b3e02df386cb1acf42fab014781ce6abf5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2648804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103b6b50efb62c54bd910c3bfb3c6afc5cce8c4b184b0e092e7c3c42f18a7ca`

```dockerfile
```

-	Layers:
	-	`sha256:11426236ad15329b9281051e4e0de11b91ac4a252e40149a2254bf71ded55da4`  
		Last Modified: Wed, 09 Apr 2025 05:10:57 GMT  
		Size: 2.6 MB (2635626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3699f70236e444819ff6cc4b818c7edf604176198bc6561ce9a6d1d70c61a0`  
		Last Modified: Wed, 09 Apr 2025 05:10:56 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

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

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:f7a858a768b1975fa2f67fb7a9df25b53ca8b8af0cf783c7e25941d03638015b
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
$ docker pull ibmjava@sha256:fa66d3ffd6d446f4b7858a6db9468c233fa92b051bdb23952adc207a1698ae14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166504912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e25eb75a6e22a7f0c45c2f7aef2dae1eb5023e54010d888f2e1f7cf11ef23e`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db27cdfb76d083e85aa00bbe22cd27db8f26db49351cade3f1f1b94273a1da76`  
		Last Modified: Wed, 09 Apr 2025 01:18:32 GMT  
		Size: 1.5 MB (1450041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e999e5f4f81077186816d9ba8ce0d947fae85e4a5c0bac65f34bd23e065130`  
		Last Modified: Wed, 09 Apr 2025 01:18:35 GMT  
		Size: 135.5 MB (135522506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:bccc2d46c8b1939c71bc18f9c3be972421d179917812414d1687951908ecfb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456adc6ec54ad9c4056d307c39fda6724e7ccb5e0980085f49e87770364a95ba`

```dockerfile
```

-	Layers:
	-	`sha256:71dcaadab602430665323c5ccbe9b5b0c0f7992a9ecc4903375fc8006bcd3311`  
		Last Modified: Wed, 09 Apr 2025 01:18:33 GMT  
		Size: 2.1 MB (2051990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a78f5b5dcfb992cb1cdf54870844f424b32b56f799ad8003faf14d134360e2f`  
		Last Modified: Wed, 09 Apr 2025 01:18:32 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:274270747b5abea21a960f42061f464b3ce49b22a30cec37dfe0508d38b55031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172333065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b26e41a656c9a0420f2113876e9119ec2be0e302b0603f32e468e55b1c80a8`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:f6e20e03e21013c0c4063080549d0a6eeb04f87b108b83647341cd63ff74c591`  
		Last Modified: Wed, 09 Apr 2025 05:42:41 GMT  
		Size: 136.4 MB (136354215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:881d77f73bc488d26516a6a3a533f178e623b8ff67dc2562e9b0b59e32b841b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919cf8b458ff02d5ce49d4499665bf9490a7fc6209c16087ef4189bbddf69eda`

```dockerfile
```

-	Layers:
	-	`sha256:98fdee18d002d796d9680efcc7f18b9fd65cfec3bdb30a37bcd59a4ed953f6dc`  
		Last Modified: Wed, 09 Apr 2025 05:42:37 GMT  
		Size: 2.1 MB (2055166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428dadb91c413ba99bd94f5e4fdba3ce40af984476999bf152cbbdf4aa9ad138`  
		Last Modified: Wed, 09 Apr 2025 05:42:36 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:598bab09312b3707322b2a7b19e154a36793adddf50c045c2eda84cc554ee644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161995411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3d773cf6b524aff5660720beddcad47cf49f041f780e2f32c9fc39f16fad1`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:2a96f83eeef125d13c15be0fe185813042737a1ad8d8b818317b0b11146c6488`  
		Last Modified: Wed, 09 Apr 2025 05:08:28 GMT  
		Size: 132.5 MB (132539569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c87c4f16e43d3231108e6c4acb27d943d0398cdf703b5c59db0e64127014c63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c63aa6fb40a036e4be21c1d343fe4811cb8b303593c30f94b0d89fe40c63fe`

```dockerfile
```

-	Layers:
	-	`sha256:4918f6b620b6b98ec9b961693c2967a74d902df2f9b91df36d7d492a47a57654`  
		Last Modified: Wed, 09 Apr 2025 05:08:26 GMT  
		Size: 2.1 MB (2051951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b53a31dc11ac2921f5b5c4caaf9fec772cdfb5b8c996997be205f18245832f07`  
		Last Modified: Wed, 09 Apr 2025 05:08:26 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:f7a858a768b1975fa2f67fb7a9df25b53ca8b8af0cf783c7e25941d03638015b
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
$ docker pull ibmjava@sha256:fa66d3ffd6d446f4b7858a6db9468c233fa92b051bdb23952adc207a1698ae14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166504912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e25eb75a6e22a7f0c45c2f7aef2dae1eb5023e54010d888f2e1f7cf11ef23e`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db27cdfb76d083e85aa00bbe22cd27db8f26db49351cade3f1f1b94273a1da76`  
		Last Modified: Wed, 09 Apr 2025 01:18:32 GMT  
		Size: 1.5 MB (1450041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e999e5f4f81077186816d9ba8ce0d947fae85e4a5c0bac65f34bd23e065130`  
		Last Modified: Wed, 09 Apr 2025 01:18:35 GMT  
		Size: 135.5 MB (135522506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:bccc2d46c8b1939c71bc18f9c3be972421d179917812414d1687951908ecfb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456adc6ec54ad9c4056d307c39fda6724e7ccb5e0980085f49e87770364a95ba`

```dockerfile
```

-	Layers:
	-	`sha256:71dcaadab602430665323c5ccbe9b5b0c0f7992a9ecc4903375fc8006bcd3311`  
		Last Modified: Wed, 09 Apr 2025 01:18:33 GMT  
		Size: 2.1 MB (2051990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a78f5b5dcfb992cb1cdf54870844f424b32b56f799ad8003faf14d134360e2f`  
		Last Modified: Wed, 09 Apr 2025 01:18:32 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:274270747b5abea21a960f42061f464b3ce49b22a30cec37dfe0508d38b55031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172333065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b26e41a656c9a0420f2113876e9119ec2be0e302b0603f32e468e55b1c80a8`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:f6e20e03e21013c0c4063080549d0a6eeb04f87b108b83647341cd63ff74c591`  
		Last Modified: Wed, 09 Apr 2025 05:42:41 GMT  
		Size: 136.4 MB (136354215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:881d77f73bc488d26516a6a3a533f178e623b8ff67dc2562e9b0b59e32b841b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919cf8b458ff02d5ce49d4499665bf9490a7fc6209c16087ef4189bbddf69eda`

```dockerfile
```

-	Layers:
	-	`sha256:98fdee18d002d796d9680efcc7f18b9fd65cfec3bdb30a37bcd59a4ed953f6dc`  
		Last Modified: Wed, 09 Apr 2025 05:42:37 GMT  
		Size: 2.1 MB (2055166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428dadb91c413ba99bd94f5e4fdba3ce40af984476999bf152cbbdf4aa9ad138`  
		Last Modified: Wed, 09 Apr 2025 05:42:36 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:598bab09312b3707322b2a7b19e154a36793adddf50c045c2eda84cc554ee644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161995411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3d773cf6b524aff5660720beddcad47cf49f041f780e2f32c9fc39f16fad1`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='20797bfcc79f9a5db0b83469f9d2dc90179ca8ef69d300d1a9f461f2e0ad49e2';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cd5b5435261af9a88e900b7780b79da4faf4b5b5dc573b3eb1106eec11a5f741';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1c112c7be92f201b0ec010d23d6b590744c3435b0b0f5398e7db1a23119fd590';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='6583c6e0bb859988ac10a2135c4700aaf069181d98b0a6d80414a17a6810e6e1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:2a96f83eeef125d13c15be0fe185813042737a1ad8d8b818317b0b11146c6488`  
		Last Modified: Wed, 09 Apr 2025 05:08:28 GMT  
		Size: 132.5 MB (132539569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c87c4f16e43d3231108e6c4acb27d943d0398cdf703b5c59db0e64127014c63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c63aa6fb40a036e4be21c1d343fe4811cb8b303593c30f94b0d89fe40c63fe`

```dockerfile
```

-	Layers:
	-	`sha256:4918f6b620b6b98ec9b961693c2967a74d902df2f9b91df36d7d492a47a57654`  
		Last Modified: Wed, 09 Apr 2025 05:08:26 GMT  
		Size: 2.1 MB (2051951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b53a31dc11ac2921f5b5c4caaf9fec772cdfb5b8c996997be205f18245832f07`  
		Last Modified: Wed, 09 Apr 2025 05:08:26 GMT  
		Size: 13.8 KB (13772 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:19e09864e3ec5c5b4710216274a89e1a7d4942df9a6c8a2ee782b531f73aabae
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
$ docker pull ibmjava@sha256:d6a7265a5c1dddceb25a6ae417fa0c8555506d1669e2f468b2410c03867178e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203889890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ce5a0f7586a8bf116f8960f585c666af55405a55ee8f405b1f44dc737409fb`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e160359d8ef9f6b95400b0f6946e1ad5590c998300f10ac80576e68a624f5ee`  
		Last Modified: Wed, 09 Apr 2025 01:18:51 GMT  
		Size: 1.5 MB (1450037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03d8575c7c900c1ac40fc6b6d512946ce651e0fb3883564d887013f164d0186`  
		Last Modified: Wed, 09 Apr 2025 01:18:55 GMT  
		Size: 172.9 MB (172907488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:422ad9740ca1f51d146a57c52f7bcda727b4a30b255371ad1b49979cc39a39fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d264201ed5c558a7f17952d06e543a75450e0695ffc3af936214b28b3d9f1289`

```dockerfile
```

-	Layers:
	-	`sha256:359202f8bd9abfc2584827afb339f435559012e613bd8592974f37de610d6ea2`  
		Last Modified: Wed, 09 Apr 2025 01:18:51 GMT  
		Size: 3.0 MB (2959908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc8c6287d8981938b613ac5acb7739f90c763dc38c337365c6ab7b1d7bdd102`  
		Last Modified: Wed, 09 Apr 2025 01:18:51 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:8c02f261e17e774ef6b2592404977ed53365082ddea6bd369f15b61cc39f4a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209920489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696ba1a2214faa0b81dcdb3e54ecf593f71c835b2fea333c7ad1984a2b7cefe8`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:94a486f14c82490d7022fce81becc9831b167271c5d80e92e44d831d55dfbd10`  
		Last Modified: Wed, 09 Apr 2025 05:45:19 GMT  
		Size: 173.9 MB (173941639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:cb4b91fb2c9c9f2f4701d0ace000423092d3a0d589830e3ab05df0d025051184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3626e0958e7b6cb9cd325c53a9f055bbf150edcaef8d842843d1c9653cac7f`

```dockerfile
```

-	Layers:
	-	`sha256:78eb1d10af6ab42f4af54f4ff54475443060d36a3b070f3a1b590a904f63fb9f`  
		Last Modified: Wed, 09 Apr 2025 05:45:14 GMT  
		Size: 2.9 MB (2945743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54e5a823c1208b307b7551d76b0590ee18e3e97b8d997e2054fb92f395bf9b2`  
		Last Modified: Wed, 09 Apr 2025 05:45:13 GMT  
		Size: 13.2 KB (13212 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:b8e17beabe21f7ebaf1b8061ba88908a7e78f1ecff1c817369cdf0e7d0ca510f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192505552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded2a8728cde5788b371a54de5fb3830b1767a8962a5d999b1603f817553978f`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 14 Feb 2025 09:27:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:9775d5de41669e8a25add8ba3d9865f1d82d1d3297bdde2813194a937393ad4a`  
		Last Modified: Wed, 09 Apr 2025 05:11:01 GMT  
		Size: 163.0 MB (163049710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:ed0ea94062e1787480b1f2958a35b3e02df386cb1acf42fab014781ce6abf5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2648804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103b6b50efb62c54bd910c3bfb3c6afc5cce8c4b184b0e092e7c3c42f18a7ca`

```dockerfile
```

-	Layers:
	-	`sha256:11426236ad15329b9281051e4e0de11b91ac4a252e40149a2254bf71ded55da4`  
		Last Modified: Wed, 09 Apr 2025 05:10:57 GMT  
		Size: 2.6 MB (2635626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3699f70236e444819ff6cc4b818c7edf604176198bc6561ce9a6d1d70c61a0`  
		Last Modified: Wed, 09 Apr 2025 05:10:56 GMT  
		Size: 13.2 KB (13178 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

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

### `ibmjava:sfj` - linux; amd64

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

### `ibmjava:sfj` - unknown; unknown

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

### `ibmjava:sfj` - linux; ppc64le

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

### `ibmjava:sfj` - unknown; unknown

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

### `ibmjava:sfj` - linux; s390x

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

### `ibmjava:sfj` - unknown; unknown

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
