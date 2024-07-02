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
$ docker pull ibmjava@sha256:d385cbe02259c025cfa615e87cbd4d06a0404dcf3422339026953675c63a69dc
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
$ docker pull ibmjava@sha256:21f377bfda519a154380365455875d75e95902ae2378fada84680996034d2669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165991641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97efc9bdb4c9c22713b9ce88b8aaa53b095610a427f8c191dd35ef78868597c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaded0e53a88b524ef08c280c8b4216fdc6ce0974541ee972a6015deb15334a`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 1.4 MB (1438230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f582295772e343c4cdc5066091ddfe10e5b9d6bf7ab6f3a13385beb33e68c5`  
		Last Modified: Mon, 01 Jul 2024 23:55:21 GMT  
		Size: 135.0 MB (135019657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:de137e57f805ace4005c0c478e1907156219b727b1c61ed5def52bf8ad1fde3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d594c4b45c16366fce57b0240a3eb350884faf4d4cd047e5edd364c1371a37`

```dockerfile
```

-	Layers:
	-	`sha256:95b79fa0268dbecc37a314f92c423754faa7276927d2b826ba1f4832adde14d0`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 2.0 MB (2003200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47d06fa40c3814f96fb059e5b9899a4109097308bffc8d1b79c14f6da923daa`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:feea3e0f32f6a4ca527a95dbac4dbc092beb477bdedf3904f5ed0b691222f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171478023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad2908bb593ed2f32181d25e5c8c99b408d283ff97fe030f2f8bd243423bc84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8ee8490119da3e5abc69ca837e325095d5af37d4bfde5e0a15135ab4d2c77d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 1.5 MB (1523276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fb31235783601bd59538e24e276a9e82866c05187cf11f6d7f103ee2da2a7f`  
		Last Modified: Mon, 01 Jul 2024 23:58:28 GMT  
		Size: 135.5 MB (135494054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:965a639b56106ba77fac71d5b0b2e2f8114a828582516f98cef43a205c3b8ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2019193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d60b0f9f418e28f7812400eee4286a6eab36af7568d7a56f1825867be648fc`

```dockerfile
```

-	Layers:
	-	`sha256:13e00de8f3ffacd80d684cdd1efe9581c3ea60f160e70e62f633bfd2165b0a9d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 2.0 MB (2005635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d0bde9dec7dad702d9174dc7c6f4269c8aba29f158a8a8b5ea457a772046d3f`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:9caddcc5130f064ad583b38d25b35976f8fa1d80f01c3c0e7dfcd9ce63fb6126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161218052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302e9342effe91a3bed89461e74f1f5cf68904a23e3c1a403e5e2030f0237df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1440bcfeaafeae00232629e6e94bea1e1dd64b34196bce4d04421380c2f15`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 1.4 MB (1441963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765dbfcb4c1b46ddc1850a42907c8b085aae31b3a7011bec428c88f2e42058a1`  
		Last Modified: Mon, 01 Jul 2024 23:57:01 GMT  
		Size: 131.8 MB (131775574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4f3474545b0c985f4aabffabb11929af627fcc7bc9984eb5a81f2572054d747f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2015218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0185f46eade1974b889ef4ecafd65120663a10cf324092cdfc0d238d5eddee51`

```dockerfile
```

-	Layers:
	-	`sha256:7ddd66171008f794aa45628f5209edffdaf8b58e16d506534ebfb47b176a71d4`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 2.0 MB (2001700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b51474b2177138891a5eea1e84b78f256d5a57f71d918dfef4e81b36e03a059`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:d385cbe02259c025cfa615e87cbd4d06a0404dcf3422339026953675c63a69dc
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
$ docker pull ibmjava@sha256:21f377bfda519a154380365455875d75e95902ae2378fada84680996034d2669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165991641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97efc9bdb4c9c22713b9ce88b8aaa53b095610a427f8c191dd35ef78868597c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaded0e53a88b524ef08c280c8b4216fdc6ce0974541ee972a6015deb15334a`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 1.4 MB (1438230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f582295772e343c4cdc5066091ddfe10e5b9d6bf7ab6f3a13385beb33e68c5`  
		Last Modified: Mon, 01 Jul 2024 23:55:21 GMT  
		Size: 135.0 MB (135019657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:de137e57f805ace4005c0c478e1907156219b727b1c61ed5def52bf8ad1fde3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d594c4b45c16366fce57b0240a3eb350884faf4d4cd047e5edd364c1371a37`

```dockerfile
```

-	Layers:
	-	`sha256:95b79fa0268dbecc37a314f92c423754faa7276927d2b826ba1f4832adde14d0`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 2.0 MB (2003200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47d06fa40c3814f96fb059e5b9899a4109097308bffc8d1b79c14f6da923daa`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:feea3e0f32f6a4ca527a95dbac4dbc092beb477bdedf3904f5ed0b691222f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171478023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad2908bb593ed2f32181d25e5c8c99b408d283ff97fe030f2f8bd243423bc84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8ee8490119da3e5abc69ca837e325095d5af37d4bfde5e0a15135ab4d2c77d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 1.5 MB (1523276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fb31235783601bd59538e24e276a9e82866c05187cf11f6d7f103ee2da2a7f`  
		Last Modified: Mon, 01 Jul 2024 23:58:28 GMT  
		Size: 135.5 MB (135494054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:965a639b56106ba77fac71d5b0b2e2f8114a828582516f98cef43a205c3b8ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2019193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d60b0f9f418e28f7812400eee4286a6eab36af7568d7a56f1825867be648fc`

```dockerfile
```

-	Layers:
	-	`sha256:13e00de8f3ffacd80d684cdd1efe9581c3ea60f160e70e62f633bfd2165b0a9d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 2.0 MB (2005635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d0bde9dec7dad702d9174dc7c6f4269c8aba29f158a8a8b5ea457a772046d3f`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:9caddcc5130f064ad583b38d25b35976f8fa1d80f01c3c0e7dfcd9ce63fb6126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161218052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302e9342effe91a3bed89461e74f1f5cf68904a23e3c1a403e5e2030f0237df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1440bcfeaafeae00232629e6e94bea1e1dd64b34196bce4d04421380c2f15`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 1.4 MB (1441963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765dbfcb4c1b46ddc1850a42907c8b085aae31b3a7011bec428c88f2e42058a1`  
		Last Modified: Mon, 01 Jul 2024 23:57:01 GMT  
		Size: 131.8 MB (131775574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4f3474545b0c985f4aabffabb11929af627fcc7bc9984eb5a81f2572054d747f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2015218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0185f46eade1974b889ef4ecafd65120663a10cf324092cdfc0d238d5eddee51`

```dockerfile
```

-	Layers:
	-	`sha256:7ddd66171008f794aa45628f5209edffdaf8b58e16d506534ebfb47b176a71d4`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 2.0 MB (2001700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b51474b2177138891a5eea1e84b78f256d5a57f71d918dfef4e81b36e03a059`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:7a13ab3f8db08b892c76692f13d8b011b6585c31d239e6bd6a3185cf2d6c8e34
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
$ docker pull ibmjava@sha256:1fc8862e3d4c97ee79c55a9167391f7068db625f5e0f5c9511b87109cc7b0a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203206456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aa338381ca3b03907d7e0b9a13279faf34eb44c423eb6f1cec60754f89a612`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf754c15c64c10d89ff3d27c6ca5c2ca94ee741ca11a32de9abfb4d9612dbe9`  
		Last Modified: Mon, 01 Jul 2024 23:55:15 GMT  
		Size: 1.4 MB (1438218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd29f8694f9d0ab6629e8cd424eb313fa842ae6f75e989706cb6081ca472480`  
		Last Modified: Mon, 01 Jul 2024 23:55:19 GMT  
		Size: 172.2 MB (172234484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f692323a8b9700a43c9d33cb96d5d105486b8c9249b7ab4496bf171271bb48d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171bf71e460aba61558ab6447bcdebc8583a7606c676357184c4bbeadf626f70`

```dockerfile
```

-	Layers:
	-	`sha256:8c24611d2a8c119ee2e52ddf3fba185eb482f0a1c3e6a069058d087979590eef`  
		Last Modified: Mon, 01 Jul 2024 23:55:15 GMT  
		Size: 2.1 MB (2055787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632d36dfd1f6f47ecbc6f0cf7dab88a397f2bb9fdf7f072f78bb605676af917b`  
		Last Modified: Mon, 01 Jul 2024 23:55:15 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:ef44775393a86e60241d0fe51f663b01a9ccba194b425c50c0d9236134499150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208821538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79e50767a16d00a2a20214ae192ffb7d5784273994083518e35e24168835f95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8ee8490119da3e5abc69ca837e325095d5af37d4bfde5e0a15135ab4d2c77d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 1.5 MB (1523276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569aebd0b75fda90f363ccbe2bae86e91da81747055c3eddcecfc6d56ed07267`  
		Last Modified: Tue, 02 Jul 2024 00:00:16 GMT  
		Size: 172.8 MB (172837569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e159f46dd5b13c27ada43a1c8408f0ad48ed34093ceb7e30e3d072aea562bb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851ce891911c095abdbea831c4e7bb6dd91a74fa1cdb0aee4f7ab4bb67eb504c`

```dockerfile
```

-	Layers:
	-	`sha256:c5c4bb4eacc165c0679a1a5e92f69821b323a793208e1db8c76b23053ed471e9`  
		Last Modified: Tue, 02 Jul 2024 00:00:09 GMT  
		Size: 2.1 MB (2058210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af18f017d064cae41714c2b4a9055d7238153677ce7b908149a8efcf7b55b8c9`  
		Last Modified: Tue, 02 Jul 2024 00:00:09 GMT  
		Size: 13.0 KB (12951 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:92ef9f55133612405254b25b8584103c5141b56514c0ecdc28b591bbb8fe3c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191505988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5286b4c3b5e4bf80d06b549c248cab97b9d640f18e3d4dd97f07018da9b04476`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1440bcfeaafeae00232629e6e94bea1e1dd64b34196bce4d04421380c2f15`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 1.4 MB (1441963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220558a1d6fe452132948c80609a4e29f8f47367b0b46efaf89e63c37bc3da92`  
		Last Modified: Mon, 01 Jul 2024 23:58:32 GMT  
		Size: 162.1 MB (162063510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f947818ad5e0a5e06aa4b1b3c9a09ab623cd9d6123a298232821650afb7b5c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2042436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067b9ddeaaf23dd5efcdd7a276a11da3fe39f12ec9b2f9be1c77833de818098`

```dockerfile
```

-	Layers:
	-	`sha256:61453b70012b462f722109f4405dfb69f712fabcc0c1f6e7b99ac12a2b989f15`  
		Last Modified: Mon, 01 Jul 2024 23:58:30 GMT  
		Size: 2.0 MB (2029513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023ec0453cec5dbd5e180cd4786de3477fdfedc7276cc1247d4a8c4082019e69`  
		Last Modified: Mon, 01 Jul 2024 23:58:30 GMT  
		Size: 12.9 KB (12923 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:c3f37e52e68c249c3bdd56bf9b0d245bed9d2b6ebf77873df8df71662dc769d9
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
$ docker pull ibmjava@sha256:235f4749cfd4a9b11948a781da9e66f390da40d22d12a9e13d87c57bb339674f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100877046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9631de094f5caef24e4cbee09cdef6bb53397e6aaae579eb378f806e99b53ee2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecbfd7b6c160400ea9952aefaa2a5a399e6210ef5d0ab6c65e59c9779f319d1`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 1.4 MB (1438223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29995a467d55c0447a2742539da59d117bd5b2ca72b96d8a4f8d9a62cf664a1d`  
		Last Modified: Mon, 01 Jul 2024 23:55:05 GMT  
		Size: 69.9 MB (69905069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:7751b54473ef6d57b0f7b70c86504c6c9f3c272337553a85ff7889f71cb76e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2002033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2a71faa7ae03aa4b78ba36977170bc3152d1ed35c3ba12cc62ce9ae42fd718`

```dockerfile
```

-	Layers:
	-	`sha256:825ed06a15a3205e38a2f4f99634dafd45719a5b41d9dcdcdb682a6cebdde4d1`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 2.0 MB (1989106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1da54cf03571f3a4c7a06be97eb66617a00b6e9db8e0d6c94746bafb84444e8`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:b2dcb62f57ee446f5b404533ab220303a4a33f5b0f2aa0f23cf1d90a09c6e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106386730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97be7d66e1ecc2d3201b283e69d6b7a61b4b90a80d660569a2d95541a628b459`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8ee8490119da3e5abc69ca837e325095d5af37d4bfde5e0a15135ab4d2c77d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 1.5 MB (1523276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931c5e4dd486c8b6e739d1d63a66784037fbac8a7c6db683ddc9bb274e70188f`  
		Last Modified: Mon, 01 Jul 2024 23:59:09 GMT  
		Size: 70.4 MB (70402761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:d77c1db7362b0a00bfb31e50086d7d3fcc8ece0c2b375ca7ae57ee8ad0418eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be2c20a74fdfda27f7caf6245c17571b4e57ae4a608e63933999da1be4778f4`

```dockerfile
```

-	Layers:
	-	`sha256:452a2cea572a876e34d1756b41eed27b5aa0d809474a6b60ad723e68cb842074`  
		Last Modified: Mon, 01 Jul 2024 23:59:07 GMT  
		Size: 2.0 MB (1992490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12331d57dc50061d1126e4f2ffda4c621d60c42f63d332b0eda7fca81cd3218e`  
		Last Modified: Mon, 01 Jul 2024 23:59:07 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:56918331a479357a9046b00bfa9cac113eb2520de73b55152ac3825cb3bfdbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99820949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b538fc5f45c5b721c9ec7505f035a37ec2fe2499c3a30557ea55c9cf5cab7355`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1440bcfeaafeae00232629e6e94bea1e1dd64b34196bce4d04421380c2f15`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 1.4 MB (1441963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c0ce8c3e76419e27c7140d29d7a13681b1f997591505a180fe442203298be`  
		Last Modified: Mon, 01 Jul 2024 23:57:41 GMT  
		Size: 70.4 MB (70378471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3dec87ba4700cb91f457fef6ea168eb7db55f658cb4b2f1ce1d20dd5063ba8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1493ec3d9d626aaf22d92c5ee30fcd2125a3a3bce808394dbce22ac82b5713f9`

```dockerfile
```

-	Layers:
	-	`sha256:31dc3e5f49697201b3b49326f2e3e31452cc851a83984e925ffe09307db6c2b6`  
		Last Modified: Mon, 01 Jul 2024 23:57:40 GMT  
		Size: 2.0 MB (1990495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbcb45fa29ce20bae53eda2f5ba6f6c85f09148ebcc0dc8c1706cbcc9dbfaeb9`  
		Last Modified: Mon, 01 Jul 2024 23:57:39 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:d385cbe02259c025cfa615e87cbd4d06a0404dcf3422339026953675c63a69dc
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
$ docker pull ibmjava@sha256:21f377bfda519a154380365455875d75e95902ae2378fada84680996034d2669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165991641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97efc9bdb4c9c22713b9ce88b8aaa53b095610a427f8c191dd35ef78868597c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaded0e53a88b524ef08c280c8b4216fdc6ce0974541ee972a6015deb15334a`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 1.4 MB (1438230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f582295772e343c4cdc5066091ddfe10e5b9d6bf7ab6f3a13385beb33e68c5`  
		Last Modified: Mon, 01 Jul 2024 23:55:21 GMT  
		Size: 135.0 MB (135019657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:de137e57f805ace4005c0c478e1907156219b727b1c61ed5def52bf8ad1fde3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d594c4b45c16366fce57b0240a3eb350884faf4d4cd047e5edd364c1371a37`

```dockerfile
```

-	Layers:
	-	`sha256:95b79fa0268dbecc37a314f92c423754faa7276927d2b826ba1f4832adde14d0`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 2.0 MB (2003200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47d06fa40c3814f96fb059e5b9899a4109097308bffc8d1b79c14f6da923daa`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:feea3e0f32f6a4ca527a95dbac4dbc092beb477bdedf3904f5ed0b691222f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171478023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad2908bb593ed2f32181d25e5c8c99b408d283ff97fe030f2f8bd243423bc84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8ee8490119da3e5abc69ca837e325095d5af37d4bfde5e0a15135ab4d2c77d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 1.5 MB (1523276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fb31235783601bd59538e24e276a9e82866c05187cf11f6d7f103ee2da2a7f`  
		Last Modified: Mon, 01 Jul 2024 23:58:28 GMT  
		Size: 135.5 MB (135494054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:965a639b56106ba77fac71d5b0b2e2f8114a828582516f98cef43a205c3b8ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2019193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d60b0f9f418e28f7812400eee4286a6eab36af7568d7a56f1825867be648fc`

```dockerfile
```

-	Layers:
	-	`sha256:13e00de8f3ffacd80d684cdd1efe9581c3ea60f160e70e62f633bfd2165b0a9d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 2.0 MB (2005635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d0bde9dec7dad702d9174dc7c6f4269c8aba29f158a8a8b5ea457a772046d3f`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:9caddcc5130f064ad583b38d25b35976f8fa1d80f01c3c0e7dfcd9ce63fb6126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161218052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302e9342effe91a3bed89461e74f1f5cf68904a23e3c1a403e5e2030f0237df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1440bcfeaafeae00232629e6e94bea1e1dd64b34196bce4d04421380c2f15`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 1.4 MB (1441963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765dbfcb4c1b46ddc1850a42907c8b085aae31b3a7011bec428c88f2e42058a1`  
		Last Modified: Mon, 01 Jul 2024 23:57:01 GMT  
		Size: 131.8 MB (131775574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:jre` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4f3474545b0c985f4aabffabb11929af627fcc7bc9984eb5a81f2572054d747f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2015218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0185f46eade1974b889ef4ecafd65120663a10cf324092cdfc0d238d5eddee51`

```dockerfile
```

-	Layers:
	-	`sha256:7ddd66171008f794aa45628f5209edffdaf8b58e16d506534ebfb47b176a71d4`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 2.0 MB (2001700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b51474b2177138891a5eea1e84b78f256d5a57f71d918dfef4e81b36e03a059`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:d385cbe02259c025cfa615e87cbd4d06a0404dcf3422339026953675c63a69dc
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
$ docker pull ibmjava@sha256:21f377bfda519a154380365455875d75e95902ae2378fada84680996034d2669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165991641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97efc9bdb4c9c22713b9ce88b8aaa53b095610a427f8c191dd35ef78868597c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaded0e53a88b524ef08c280c8b4216fdc6ce0974541ee972a6015deb15334a`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 1.4 MB (1438230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f582295772e343c4cdc5066091ddfe10e5b9d6bf7ab6f3a13385beb33e68c5`  
		Last Modified: Mon, 01 Jul 2024 23:55:21 GMT  
		Size: 135.0 MB (135019657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:de137e57f805ace4005c0c478e1907156219b727b1c61ed5def52bf8ad1fde3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d594c4b45c16366fce57b0240a3eb350884faf4d4cd047e5edd364c1371a37`

```dockerfile
```

-	Layers:
	-	`sha256:95b79fa0268dbecc37a314f92c423754faa7276927d2b826ba1f4832adde14d0`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 2.0 MB (2003200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47d06fa40c3814f96fb059e5b9899a4109097308bffc8d1b79c14f6da923daa`  
		Last Modified: Mon, 01 Jul 2024 23:55:18 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:feea3e0f32f6a4ca527a95dbac4dbc092beb477bdedf3904f5ed0b691222f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171478023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad2908bb593ed2f32181d25e5c8c99b408d283ff97fe030f2f8bd243423bc84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8ee8490119da3e5abc69ca837e325095d5af37d4bfde5e0a15135ab4d2c77d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 1.5 MB (1523276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fb31235783601bd59538e24e276a9e82866c05187cf11f6d7f103ee2da2a7f`  
		Last Modified: Mon, 01 Jul 2024 23:58:28 GMT  
		Size: 135.5 MB (135494054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:965a639b56106ba77fac71d5b0b2e2f8114a828582516f98cef43a205c3b8ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2019193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d60b0f9f418e28f7812400eee4286a6eab36af7568d7a56f1825867be648fc`

```dockerfile
```

-	Layers:
	-	`sha256:13e00de8f3ffacd80d684cdd1efe9581c3ea60f160e70e62f633bfd2165b0a9d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 2.0 MB (2005635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d0bde9dec7dad702d9174dc7c6f4269c8aba29f158a8a8b5ea457a772046d3f`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 13.6 KB (13558 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:9caddcc5130f064ad583b38d25b35976f8fa1d80f01c3c0e7dfcd9ce63fb6126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161218052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302e9342effe91a3bed89461e74f1f5cf68904a23e3c1a403e5e2030f0237df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9184a6a2be733e8fdb8316f6afcd373c88749c0ec154823ffff45103e528bd6d';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='995426328cc8b7d29dbe4611a1876abbae5f345dcbb2ab6126dcfff5c7985098';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='65ba530a8fc6750c928594ac37fdfeb465f2b5f46bbf809d24353e68e82617fe';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='8985c1fd333d8aef810af8c21acb775e12d741dfffc34aacc3fa4f27440b157f';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1440bcfeaafeae00232629e6e94bea1e1dd64b34196bce4d04421380c2f15`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 1.4 MB (1441963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765dbfcb4c1b46ddc1850a42907c8b085aae31b3a7011bec428c88f2e42058a1`  
		Last Modified: Mon, 01 Jul 2024 23:57:01 GMT  
		Size: 131.8 MB (131775574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:latest` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4f3474545b0c985f4aabffabb11929af627fcc7bc9984eb5a81f2572054d747f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2015218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0185f46eade1974b889ef4ecafd65120663a10cf324092cdfc0d238d5eddee51`

```dockerfile
```

-	Layers:
	-	`sha256:7ddd66171008f794aa45628f5209edffdaf8b58e16d506534ebfb47b176a71d4`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 2.0 MB (2001700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b51474b2177138891a5eea1e84b78f256d5a57f71d918dfef4e81b36e03a059`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 13.5 KB (13518 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:7a13ab3f8db08b892c76692f13d8b011b6585c31d239e6bd6a3185cf2d6c8e34
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
$ docker pull ibmjava@sha256:1fc8862e3d4c97ee79c55a9167391f7068db625f5e0f5c9511b87109cc7b0a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203206456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aa338381ca3b03907d7e0b9a13279faf34eb44c423eb6f1cec60754f89a612`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf754c15c64c10d89ff3d27c6ca5c2ca94ee741ca11a32de9abfb4d9612dbe9`  
		Last Modified: Mon, 01 Jul 2024 23:55:15 GMT  
		Size: 1.4 MB (1438218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd29f8694f9d0ab6629e8cd424eb313fa842ae6f75e989706cb6081ca472480`  
		Last Modified: Mon, 01 Jul 2024 23:55:19 GMT  
		Size: 172.2 MB (172234484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f692323a8b9700a43c9d33cb96d5d105486b8c9249b7ab4496bf171271bb48d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171bf71e460aba61558ab6447bcdebc8583a7606c676357184c4bbeadf626f70`

```dockerfile
```

-	Layers:
	-	`sha256:8c24611d2a8c119ee2e52ddf3fba185eb482f0a1c3e6a069058d087979590eef`  
		Last Modified: Mon, 01 Jul 2024 23:55:15 GMT  
		Size: 2.1 MB (2055787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632d36dfd1f6f47ecbc6f0cf7dab88a397f2bb9fdf7f072f78bb605676af917b`  
		Last Modified: Mon, 01 Jul 2024 23:55:15 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:ef44775393a86e60241d0fe51f663b01a9ccba194b425c50c0d9236134499150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208821538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79e50767a16d00a2a20214ae192ffb7d5784273994083518e35e24168835f95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8ee8490119da3e5abc69ca837e325095d5af37d4bfde5e0a15135ab4d2c77d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 1.5 MB (1523276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569aebd0b75fda90f363ccbe2bae86e91da81747055c3eddcecfc6d56ed07267`  
		Last Modified: Tue, 02 Jul 2024 00:00:16 GMT  
		Size: 172.8 MB (172837569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:e159f46dd5b13c27ada43a1c8408f0ad48ed34093ceb7e30e3d072aea562bb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851ce891911c095abdbea831c4e7bb6dd91a74fa1cdb0aee4f7ab4bb67eb504c`

```dockerfile
```

-	Layers:
	-	`sha256:c5c4bb4eacc165c0679a1a5e92f69821b323a793208e1db8c76b23053ed471e9`  
		Last Modified: Tue, 02 Jul 2024 00:00:09 GMT  
		Size: 2.1 MB (2058210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af18f017d064cae41714c2b4a9055d7238153677ce7b908149a8efcf7b55b8c9`  
		Last Modified: Tue, 02 Jul 2024 00:00:09 GMT  
		Size: 13.0 KB (12951 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:92ef9f55133612405254b25b8584103c5141b56514c0ecdc28b591bbb8fe3c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191505988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5286b4c3b5e4bf80d06b549c248cab97b9d640f18e3d4dd97f07018da9b04476`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1440bcfeaafeae00232629e6e94bea1e1dd64b34196bce4d04421380c2f15`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 1.4 MB (1441963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220558a1d6fe452132948c80609a4e29f8f47367b0b46efaf89e63c37bc3da92`  
		Last Modified: Mon, 01 Jul 2024 23:58:32 GMT  
		Size: 162.1 MB (162063510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:f947818ad5e0a5e06aa4b1b3c9a09ab623cd9d6123a298232821650afb7b5c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2042436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067b9ddeaaf23dd5efcdd7a276a11da3fe39f12ec9b2f9be1c77833de818098`

```dockerfile
```

-	Layers:
	-	`sha256:61453b70012b462f722109f4405dfb69f712fabcc0c1f6e7b99ac12a2b989f15`  
		Last Modified: Mon, 01 Jul 2024 23:58:30 GMT  
		Size: 2.0 MB (2029513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023ec0453cec5dbd5e180cd4786de3477fdfedc7276cc1247d4a8c4082019e69`  
		Last Modified: Mon, 01 Jul 2024 23:58:30 GMT  
		Size: 12.9 KB (12923 bytes)  
		MIME: application/vnd.in-toto+json

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:c3f37e52e68c249c3bdd56bf9b0d245bed9d2b6ebf77873df8df71662dc769d9
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
$ docker pull ibmjava@sha256:235f4749cfd4a9b11948a781da9e66f390da40d22d12a9e13d87c57bb339674f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100877046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9631de094f5caef24e4cbee09cdef6bb53397e6aaae579eb378f806e99b53ee2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecbfd7b6c160400ea9952aefaa2a5a399e6210ef5d0ab6c65e59c9779f319d1`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 1.4 MB (1438223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29995a467d55c0447a2742539da59d117bd5b2ca72b96d8a4f8d9a62cf664a1d`  
		Last Modified: Mon, 01 Jul 2024 23:55:05 GMT  
		Size: 69.9 MB (69905069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:7751b54473ef6d57b0f7b70c86504c6c9f3c272337553a85ff7889f71cb76e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2002033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2a71faa7ae03aa4b78ba36977170bc3152d1ed35c3ba12cc62ce9ae42fd718`

```dockerfile
```

-	Layers:
	-	`sha256:825ed06a15a3205e38a2f4f99634dafd45719a5b41d9dcdcdb682a6cebdde4d1`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 2.0 MB (1989106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1da54cf03571f3a4c7a06be97eb66617a00b6e9db8e0d6c94746bafb84444e8`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:b2dcb62f57ee446f5b404533ab220303a4a33f5b0f2aa0f23cf1d90a09c6e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106386730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97be7d66e1ecc2d3201b283e69d6b7a61b4b90a80d660569a2d95541a628b459`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8ee8490119da3e5abc69ca837e325095d5af37d4bfde5e0a15135ab4d2c77d`  
		Last Modified: Mon, 01 Jul 2024 23:58:24 GMT  
		Size: 1.5 MB (1523276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931c5e4dd486c8b6e739d1d63a66784037fbac8a7c6db683ddc9bb274e70188f`  
		Last Modified: Mon, 01 Jul 2024 23:59:09 GMT  
		Size: 70.4 MB (70402761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:d77c1db7362b0a00bfb31e50086d7d3fcc8ece0c2b375ca7ae57ee8ad0418eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be2c20a74fdfda27f7caf6245c17571b4e57ae4a608e63933999da1be4778f4`

```dockerfile
```

-	Layers:
	-	`sha256:452a2cea572a876e34d1756b41eed27b5aa0d809474a6b60ad723e68cb842074`  
		Last Modified: Mon, 01 Jul 2024 23:59:07 GMT  
		Size: 2.0 MB (1992490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12331d57dc50061d1126e4f2ffda4c621d60c42f63d332b0eda7fca81cd3218e`  
		Last Modified: Mon, 01 Jul 2024 23:59:07 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:56918331a479357a9046b00bfa9cac113eb2520de73b55152ac3825cb3bfdbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99820949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b538fc5f45c5b721c9ec7505f035a37ec2fe2499c3a30557ea55c9cf5cab7355`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 12:53:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 28 Jun 2024 12:53:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_VERSION=8.0.8.26
# Fri, 28 Jun 2024 12:53:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='17f545aec349208b9532ebdbae71a40cda31853981db56370dc68046b6a94585';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a8d4a72fbc3ffdb54f75cdab416edeea81274e3e23da88aee60a473d55385231';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='21bf2cfa38c86b9ce8521c853d63d6c43a78fa2d02643309c03775999089f4c9';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='cb8c2da2a8eeddc8338ddc27910105f643c8d3a6f13dbafaa3ae52d41a19be74';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 28 Jun 2024 12:53:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1440bcfeaafeae00232629e6e94bea1e1dd64b34196bce4d04421380c2f15`  
		Last Modified: Mon, 01 Jul 2024 23:56:59 GMT  
		Size: 1.4 MB (1441963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c0ce8c3e76419e27c7140d29d7a13681b1f997591505a180fe442203298be`  
		Last Modified: Mon, 01 Jul 2024 23:57:41 GMT  
		Size: 70.4 MB (70378471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:3dec87ba4700cb91f457fef6ea168eb7db55f658cb4b2f1ce1d20dd5063ba8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1493ec3d9d626aaf22d92c5ee30fcd2125a3a3bce808394dbce22ac82b5713f9`

```dockerfile
```

-	Layers:
	-	`sha256:31dc3e5f49697201b3b49326f2e3e31452cc851a83984e925ffe09307db6c2b6`  
		Last Modified: Mon, 01 Jul 2024 23:57:40 GMT  
		Size: 2.0 MB (1990495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbcb45fa29ce20bae53eda2f5ba6f6c85f09148ebcc0dc8c1706cbcc9dbfaeb9`  
		Last Modified: Mon, 01 Jul 2024 23:57:39 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json
