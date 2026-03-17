## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:08d142fa029f34acb6fc7138b664f2866c17528afa66cdd8e37e8f5c33704c30
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
$ docker pull ibmjava@sha256:40eb55678154cbec43f955b29627c94489bdb980c375e17fd002497177d71b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102032501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f59f5ba1d86d57d8192caeec156e72839f8015e23466e834b4e637c481fe180`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:38:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 01:38:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:38:21 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 01:38:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 01:38:49 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda6992acf7946bb49b19b813307ddce44be037dc956f72cbdefad5c0451011c`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 1.5 MB (1450004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6f4b5a9618d868ebd1368148ccc36913a08be266accd214995e162ae610cff`  
		Last Modified: Tue, 17 Mar 2026 01:39:00 GMT  
		Size: 71.0 MB (71043977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:113c8de52cfed403979b357e017553fb39c87e866902e72c142f3448b9509a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20578745d0e6efe0205ce7690683230fa3ba73b8c96d802b9fde147f212c854a`

```dockerfile
```

-	Layers:
	-	`sha256:39e638f4ad76558e1abc1522f4ee8d20807f100be1cda00c4ed3012e64a7c9c8`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 2.2 MB (2156549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21878a916161ded72eac50ef9bb13140ea347aaeac3a1d096c951e9a48fd088c`  
		Last Modified: Tue, 17 Mar 2026 01:38:58 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:4a226ef900cb19af8d10b761688db8b599e05d4d78fc736f3b7b5bcc9389c851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107973118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69417ff2c11f5f058aeab9921034c20189da4fbc237a0c1f625f495198a56dac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:00:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 09:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:00:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 09:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 09:01:30 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d2f7f8365d8d5d5c83ad30e1c8995b2eaa6b1c50b7e1b1caa14e6ba0d13e1`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 1.5 MB (1536093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2930a63157b00bf9aef8c2f7549bbcf8184530de6350d92d7787b15cf5a48668`  
		Last Modified: Tue, 17 Mar 2026 09:01:51 GMT  
		Size: 72.0 MB (71983577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:49097b98767c4fc1cae0e6c101e7f7b92ec696ddda329142a0a2362cde6eacf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4c235d56166ee198cd6aad97055aa0b2f9e34bc28a8b43ae3a6e087f7937d8`

```dockerfile
```

-	Layers:
	-	`sha256:163a666ec3e5b9e602de3b47db381f48e17dc1ed4a6da72900338601197d6024`  
		Last Modified: Tue, 17 Mar 2026 09:01:49 GMT  
		Size: 2.2 MB (2161050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:047260f196209b742c556aa8395c44856bc18bc1ef92d6919821ff536d3795fc`  
		Last Modified: Tue, 17 Mar 2026 09:01:49 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:848e4a88e781fe55d0159064ede17578f5bcb7d597f1dc39e175f3cac6bc5b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101548222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6b0cb963e9187490f69b2e7dbb3c7794de4f7e5643b36fd364bc1cfbf6415b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:31 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 02:34:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:34:31 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 02:34:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='059b82eb134858fb2b89bc8b23cb08d5b475158df4fc0abe2437103e40afb456';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='39990c2ccf575835d6475faeedf1716b9d9df4d5a7eee33de17ca9c3681aa038';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='45121191aa75d6ae3fdc3e771cff460b40b085430873060a86eccce3613de828';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 02:34:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edcd91a41ee09197ac78b9446645d919d302d4e6bd111070c1d80415e1f6f5a`  
		Last Modified: Tue, 17 Mar 2026 02:35:09 GMT  
		Size: 1.5 MB (1455776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11b08ab3fd61ca7d95eeb83e30dfc381cef5518aff1e320af9178d2d24bd211`  
		Last Modified: Tue, 17 Mar 2026 02:35:11 GMT  
		Size: 72.1 MB (72085344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:44e72ef13cc6e7230ae50a8abe22a98e4d46705a849ffee8b998b5112eb7b81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd08ffb05a271ec84d6e4fecb3916910bf1f071339cf4e6331d9366b58acbf29`

```dockerfile
```

-	Layers:
	-	`sha256:5012b78f94d748a661594abcc798a8c428742b614ec665ee79a8e9a34e365d4a`  
		Last Modified: Tue, 17 Mar 2026 02:35:09 GMT  
		Size: 2.2 MB (2160171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5a06999fafd55e15280321d2ddd19a67729dce56f1a205c83eec31c5d9479e`  
		Last Modified: Tue, 17 Mar 2026 02:35:09 GMT  
		Size: 12.6 KB (12600 bytes)  
		MIME: application/vnd.in-toto+json
