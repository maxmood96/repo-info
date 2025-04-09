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
