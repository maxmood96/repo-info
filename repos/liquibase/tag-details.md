<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.30`](#liquibase430)
-	[`liquibase:4.30-alpine`](#liquibase430-alpine)
-	[`liquibase:4.30.0`](#liquibase4300)
-	[`liquibase:4.30.0-alpine`](#liquibase4300-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.30`

```console
$ docker pull liquibase@sha256:2f1c3a747c413e24c0416166b7e5b465a347d0fa0925eb747a6794fa7123182e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.30` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:d1b0a14cdc02d70f60fc17f86050f1347c37c01ecfd8de86dddd408ee5b77a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253366358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab604bcc37cdb37e2e3dc377d0a86760adb8f46b92c6a512e7e551a42970034`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
WORKDIR /liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LIQUIBASE_VERSION=4.30.0
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_VERSION=0.2.8
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 07 Nov 2024 14:28:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
USER liquibase:liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Last Modified: Thu, 24 Oct 2024 00:58:15 GMT  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c88cd8dd8835e47c7a890ad7abd2ca59cf691145582518cf5843edbd6d6bfa0`  
		Last Modified: Thu, 24 Oct 2024 01:12:30 GMT  
		Size: 46.4 MB (46430856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c3c08b455337af9ba6b5fe522389a1d0a2b621fe437f3832a54289cac03397`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26811a6e12de121df2970871f9027eb19d2c672b0045944972cf63a39c74aa15`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442f72222307f30935fbff788dac6d016c6946f8a65bcb838128b74973c0f35a`  
		Last Modified: Thu, 07 Nov 2024 17:58:12 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324b752e40711c198465c2ee31038c60a24496494a292ba0c9dff1c632f14d63`  
		Last Modified: Thu, 07 Nov 2024 17:58:16 GMT  
		Size: 160.4 MB (160436970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607b1321566c31f38d6db97f6fe463c21c31254838c259c27180e2800e75714`  
		Last Modified: Thu, 07 Nov 2024 17:58:13 GMT  
		Size: 3.1 MB (3073119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089c50d4666afd32c4952210420f1e1de7eb3f56dac670cac1060e861dea5a98`  
		Last Modified: Thu, 07 Nov 2024 17:58:12 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aad88c5dd4dfb476fc17ed7ecdba4c5ab7d90ddcf7153bc3b58db21bad6128`  
		Last Modified: Thu, 07 Nov 2024 17:58:13 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.30` - unknown; unknown

```console
$ docker pull liquibase@sha256:216e520563953450ed67707563f8567c77922e6d006f3d406a1f772ecaced335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3779638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abde6873e56a8b39fa847f9c764c72b58b992317ce3cc4986e2f65e0f3348e48`

```dockerfile
```

-	Layers:
	-	`sha256:335d60c271f354c1f2a9d1ae25e0a395bbe4f3e541f1224c4be5758e51d8a890`  
		Last Modified: Thu, 07 Nov 2024 17:58:13 GMT  
		Size: 3.8 MB (3755332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb1471a79e7351c797d3817fe11b04db472905f60774c633864addb6d034495`  
		Last Modified: Thu, 07 Nov 2024 17:58:12 GMT  
		Size: 24.3 KB (24306 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.30-alpine`

```console
$ docker pull liquibase@sha256:29a957d09fa43439b44abdd4c490ce9a4587a6e868452901fa8d38e460f5957d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.30-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:270ec5290acf31e89e16c6fb27cc1958b0daf17a700b8a37592bd73f4a1d0698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229859775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e84fa4d09e44048b50989485c4df918c5e7819d81320f53a7b3261f9b8d571c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
WORKDIR /liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LIQUIBASE_VERSION=4.30.0
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_VERSION=0.2.8
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 07 Nov 2024 14:28:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
USER liquibase:liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e6ac71992bf291867c2507881911c4061b04c54a93f7e2beaec48bea06f829`  
		Last Modified: Thu, 07 Nov 2024 17:59:01 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1499c3188073e498b692507679e7a5cab359218af5fd77b2241df66e4ab44f5`  
		Last Modified: Thu, 07 Nov 2024 17:59:04 GMT  
		Size: 62.3 MB (62319669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bf49cf4b1f4fe1d7c997ad35fb720f6288671f6bc545711bba1a32de9ccde2`  
		Last Modified: Thu, 07 Nov 2024 17:59:06 GMT  
		Size: 160.5 MB (160458979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c1f922cd3d04a175abb3a69638c70aab74fe2c66c0e42c0900206e63ea0bd`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 3.0 MB (2991813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660abfac3b136d4c9e15ff7338387bc7b642288b30e632988a4d43c6c4f15ac6`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d329f5d539eaede4ab7921e3931739a26a88ace1c9aa8e2ad3078179d2bf26`  
		Last Modified: Thu, 07 Nov 2024 17:59:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.30-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:17bbf4e21a4672aed94dec05405f0ea98d08b0f524dc29bcb50172d2b5ecc33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 KB (398720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36a72c74fce5f785ba0eb5310a8889dfe0f1166b25413b35c73460a88183297`

```dockerfile
```

-	Layers:
	-	`sha256:5bdc276e1c686d0511f1fc13b6bfbe2a72a1bff61a1b0b47e6de1e680a5a06db`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 377.5 KB (377500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bc74e2eed68cb1aed11378697ffd08b7ba27bd914e5d89955d6b66e45c2c21`  
		Last Modified: Thu, 07 Nov 2024 17:59:01 GMT  
		Size: 21.2 KB (21220 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.30.0`

```console
$ docker pull liquibase@sha256:2f1c3a747c413e24c0416166b7e5b465a347d0fa0925eb747a6794fa7123182e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.30.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:d1b0a14cdc02d70f60fc17f86050f1347c37c01ecfd8de86dddd408ee5b77a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253366358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab604bcc37cdb37e2e3dc377d0a86760adb8f46b92c6a512e7e551a42970034`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
WORKDIR /liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LIQUIBASE_VERSION=4.30.0
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_VERSION=0.2.8
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 07 Nov 2024 14:28:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
USER liquibase:liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Last Modified: Thu, 24 Oct 2024 00:58:15 GMT  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c88cd8dd8835e47c7a890ad7abd2ca59cf691145582518cf5843edbd6d6bfa0`  
		Last Modified: Thu, 24 Oct 2024 01:12:30 GMT  
		Size: 46.4 MB (46430856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c3c08b455337af9ba6b5fe522389a1d0a2b621fe437f3832a54289cac03397`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26811a6e12de121df2970871f9027eb19d2c672b0045944972cf63a39c74aa15`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442f72222307f30935fbff788dac6d016c6946f8a65bcb838128b74973c0f35a`  
		Last Modified: Thu, 07 Nov 2024 17:58:12 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324b752e40711c198465c2ee31038c60a24496494a292ba0c9dff1c632f14d63`  
		Last Modified: Thu, 07 Nov 2024 17:58:16 GMT  
		Size: 160.4 MB (160436970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607b1321566c31f38d6db97f6fe463c21c31254838c259c27180e2800e75714`  
		Last Modified: Thu, 07 Nov 2024 17:58:13 GMT  
		Size: 3.1 MB (3073119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089c50d4666afd32c4952210420f1e1de7eb3f56dac670cac1060e861dea5a98`  
		Last Modified: Thu, 07 Nov 2024 17:58:12 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aad88c5dd4dfb476fc17ed7ecdba4c5ab7d90ddcf7153bc3b58db21bad6128`  
		Last Modified: Thu, 07 Nov 2024 17:58:13 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.30.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:216e520563953450ed67707563f8567c77922e6d006f3d406a1f772ecaced335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3779638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abde6873e56a8b39fa847f9c764c72b58b992317ce3cc4986e2f65e0f3348e48`

```dockerfile
```

-	Layers:
	-	`sha256:335d60c271f354c1f2a9d1ae25e0a395bbe4f3e541f1224c4be5758e51d8a890`  
		Last Modified: Thu, 07 Nov 2024 17:58:13 GMT  
		Size: 3.8 MB (3755332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb1471a79e7351c797d3817fe11b04db472905f60774c633864addb6d034495`  
		Last Modified: Thu, 07 Nov 2024 17:58:12 GMT  
		Size: 24.3 KB (24306 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.30.0-alpine`

```console
$ docker pull liquibase@sha256:29a957d09fa43439b44abdd4c490ce9a4587a6e868452901fa8d38e460f5957d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.30.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:270ec5290acf31e89e16c6fb27cc1958b0daf17a700b8a37592bd73f4a1d0698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229859775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e84fa4d09e44048b50989485c4df918c5e7819d81320f53a7b3261f9b8d571c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
WORKDIR /liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LIQUIBASE_VERSION=4.30.0
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_VERSION=0.2.8
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 07 Nov 2024 14:28:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
USER liquibase:liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e6ac71992bf291867c2507881911c4061b04c54a93f7e2beaec48bea06f829`  
		Last Modified: Thu, 07 Nov 2024 17:59:01 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1499c3188073e498b692507679e7a5cab359218af5fd77b2241df66e4ab44f5`  
		Last Modified: Thu, 07 Nov 2024 17:59:04 GMT  
		Size: 62.3 MB (62319669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bf49cf4b1f4fe1d7c997ad35fb720f6288671f6bc545711bba1a32de9ccde2`  
		Last Modified: Thu, 07 Nov 2024 17:59:06 GMT  
		Size: 160.5 MB (160458979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c1f922cd3d04a175abb3a69638c70aab74fe2c66c0e42c0900206e63ea0bd`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 3.0 MB (2991813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660abfac3b136d4c9e15ff7338387bc7b642288b30e632988a4d43c6c4f15ac6`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d329f5d539eaede4ab7921e3931739a26a88ace1c9aa8e2ad3078179d2bf26`  
		Last Modified: Thu, 07 Nov 2024 17:59:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.30.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:17bbf4e21a4672aed94dec05405f0ea98d08b0f524dc29bcb50172d2b5ecc33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 KB (398720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36a72c74fce5f785ba0eb5310a8889dfe0f1166b25413b35c73460a88183297`

```dockerfile
```

-	Layers:
	-	`sha256:5bdc276e1c686d0511f1fc13b6bfbe2a72a1bff61a1b0b47e6de1e680a5a06db`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 377.5 KB (377500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bc74e2eed68cb1aed11378697ffd08b7ba27bd914e5d89955d6b66e45c2c21`  
		Last Modified: Thu, 07 Nov 2024 17:59:01 GMT  
		Size: 21.2 KB (21220 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:2163ad05fa622348b68026cda4a96991e3ce9342345566a0ac514b8b8c9eed57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:fbfebab6b53ebbec5f81fdfd4cbfaf586dd409ba823bd6a43a11697c6c6a3c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228895340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f0c74c1b66f84f0fc6211dce3c9400b67cc842a8fa8952f92cdeacd86a2147`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 13 Sep 2024 07:37:36 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
WORKDIR /liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LIQUIBASE_VERSION=4.29.2
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9
# Fri, 13 Sep 2024 07:37:36 GMT
# ARGS: LIQUIBASE_VERSION=4.29.2 LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_VERSION=0.2.8
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 13 Sep 2024 07:37:36 GMT
# ARGS: LIQUIBASE_VERSION=4.29.2 LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9 LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
USER liquibase:liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 13 Sep 2024 07:37:36 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5968dad0c5cd11a1dee26f10ff16e5b41d50d6f3d9f206ef6f6cad5d30d1e44a`  
		Last Modified: Sat, 19 Oct 2024 01:00:16 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41864b028bfc744d8c900562c033aba6ab8bc1159e3c20e5b8308843096c44e4`  
		Last Modified: Sat, 19 Oct 2024 01:00:17 GMT  
		Size: 62.6 MB (62569517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03669f15c7771ef019bf7c4adad4e61009471faa0896dc92ee695c518eae4c71`  
		Last Modified: Sat, 19 Oct 2024 01:00:18 GMT  
		Size: 159.5 MB (159459672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547696384ce3bb9b391a1773f5050f6f77273f6a26cdd20fd63963cac5eac930`  
		Last Modified: Sat, 19 Oct 2024 01:00:16 GMT  
		Size: 3.2 MB (3240676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b07e40482a3e324ae7dcf0ff483dce5337b0179fd2d18bdb75d18ab92ef11a3`  
		Last Modified: Sat, 19 Oct 2024 01:00:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e6d3b220e0ede1553c4aff874c35c91bce9cd15fc58f1fb0e5de0b8530a185`  
		Last Modified: Sat, 19 Oct 2024 01:00:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:cf4a97ff56096437023cd86d5266aa8b45d7cbf098c0e24c8d67d3f8b598d9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.3 KB (398270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b10bc2c76a6f66d4fb806b977fb05df61858d51c2e9305032685c38a712d8ff`

```dockerfile
```

-	Layers:
	-	`sha256:d0a96d1d867d8f3ec45647ab8f6be33de323cac9247495e2bb3bf5aa83245f05`  
		Last Modified: Sat, 19 Oct 2024 01:00:16 GMT  
		Size: 377.3 KB (377297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556cc695717e6c5fc4fa965e1fbca86a74506567416ef8a836ea49e2f42a67d5`  
		Last Modified: Sat, 19 Oct 2024 01:00:16 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:270ec5290acf31e89e16c6fb27cc1958b0daf17a700b8a37592bd73f4a1d0698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229859775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e84fa4d09e44048b50989485c4df918c5e7819d81320f53a7b3261f9b8d571c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
WORKDIR /liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LIQUIBASE_VERSION=4.30.0
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_VERSION=0.2.8
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 07 Nov 2024 14:28:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
USER liquibase:liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e6ac71992bf291867c2507881911c4061b04c54a93f7e2beaec48bea06f829`  
		Last Modified: Thu, 07 Nov 2024 17:59:01 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1499c3188073e498b692507679e7a5cab359218af5fd77b2241df66e4ab44f5`  
		Last Modified: Thu, 07 Nov 2024 17:59:04 GMT  
		Size: 62.3 MB (62319669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bf49cf4b1f4fe1d7c997ad35fb720f6288671f6bc545711bba1a32de9ccde2`  
		Last Modified: Thu, 07 Nov 2024 17:59:06 GMT  
		Size: 160.5 MB (160458979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c1f922cd3d04a175abb3a69638c70aab74fe2c66c0e42c0900206e63ea0bd`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 3.0 MB (2991813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660abfac3b136d4c9e15ff7338387bc7b642288b30e632988a4d43c6c4f15ac6`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d329f5d539eaede4ab7921e3931739a26a88ace1c9aa8e2ad3078179d2bf26`  
		Last Modified: Thu, 07 Nov 2024 17:59:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:17bbf4e21a4672aed94dec05405f0ea98d08b0f524dc29bcb50172d2b5ecc33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 KB (398720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36a72c74fce5f785ba0eb5310a8889dfe0f1166b25413b35c73460a88183297`

```dockerfile
```

-	Layers:
	-	`sha256:5bdc276e1c686d0511f1fc13b6bfbe2a72a1bff61a1b0b47e6de1e680a5a06db`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 377.5 KB (377500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bc74e2eed68cb1aed11378697ffd08b7ba27bd914e5d89955d6b66e45c2c21`  
		Last Modified: Thu, 07 Nov 2024 17:59:01 GMT  
		Size: 21.2 KB (21220 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:d1c4f0e32cefe3bdc7d963846b20846ad08c90ed16fcdad016aad1010923a5ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:aee45b45de2a265416faf2f269760acbf76072c4f1e60872b2ea30d8598c853a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255380761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04732b3e9480c54c38f08b988556acb0348d86a6ecdfc408d4f974608cc2faaf`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Fri, 13 Sep 2024 07:37:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Sep 2024 07:37:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Sep 2024 07:37:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 13 Sep 2024 07:37:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Fri, 13 Sep 2024 07:37:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 13 Sep 2024 07:37:36 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
WORKDIR /liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LIQUIBASE_VERSION=4.29.2
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9
# Fri, 13 Sep 2024 07:37:36 GMT
# ARGS: LIQUIBASE_VERSION=4.29.2 LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_VERSION=0.2.8
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 13 Sep 2024 07:37:36 GMT
# ARGS: LIQUIBASE_VERSION=4.29.2 LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9 LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
USER liquibase:liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 13 Sep 2024 07:37:36 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f91d5e2834cdc3ece6895ee8e98d38d4ea2bfa40495dd2c3980bfc346c752`  
		Last Modified: Thu, 24 Oct 2024 01:58:24 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227882e2eb085fc8ca36693d175daa277d0d59ad2b5e6d63320ba39e88daf630`  
		Last Modified: Thu, 24 Oct 2024 01:58:28 GMT  
		Size: 159.4 MB (159436912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b78539e04b92df5f0304ff72bd8dd7649cf235e33427567398f62e2ff71e5a9`  
		Last Modified: Thu, 24 Oct 2024 01:58:25 GMT  
		Size: 3.3 MB (3318509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b600acee49d888f47eb0b34592303b021e0061c07722ac13b6f4e83aff03afc9`  
		Last Modified: Thu, 24 Oct 2024 01:58:24 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a3a4f6c609e5cbaac25b13a80a9474f54c14ed245da9a17cfa56b31ce1a8d2`  
		Last Modified: Thu, 24 Oct 2024 01:58:25 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:65079f894a5d214ff5aab47995554d4a27d9f30a1e62262e323d1b4d06df6a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3779590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf1525ca32c43126381468b4a9cf934faa4f942076deb7c7efd0881dc48f511`

```dockerfile
```

-	Layers:
	-	`sha256:4febf014d843c498cd6e955f58ceae73813560c76ad9a08806f198e8705cafc9`  
		Last Modified: Thu, 24 Oct 2024 01:58:24 GMT  
		Size: 3.8 MB (3755526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd960294bd24b7f1faef35880b72a5ecf4c24f4168b2df32d1270c8761962c15`  
		Last Modified: Thu, 24 Oct 2024 01:58:24 GMT  
		Size: 24.1 KB (24064 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:d1b0a14cdc02d70f60fc17f86050f1347c37c01ecfd8de86dddd408ee5b77a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253366358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab604bcc37cdb37e2e3dc377d0a86760adb8f46b92c6a512e7e551a42970034`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
WORKDIR /liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LIQUIBASE_VERSION=4.30.0
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_VERSION=0.2.8
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 07 Nov 2024 14:28:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
USER liquibase:liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Last Modified: Thu, 24 Oct 2024 00:58:15 GMT  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c88cd8dd8835e47c7a890ad7abd2ca59cf691145582518cf5843edbd6d6bfa0`  
		Last Modified: Thu, 24 Oct 2024 01:12:30 GMT  
		Size: 46.4 MB (46430856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c3c08b455337af9ba6b5fe522389a1d0a2b621fe437f3832a54289cac03397`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26811a6e12de121df2970871f9027eb19d2c672b0045944972cf63a39c74aa15`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442f72222307f30935fbff788dac6d016c6946f8a65bcb838128b74973c0f35a`  
		Last Modified: Thu, 07 Nov 2024 17:58:12 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324b752e40711c198465c2ee31038c60a24496494a292ba0c9dff1c632f14d63`  
		Last Modified: Thu, 07 Nov 2024 17:58:16 GMT  
		Size: 160.4 MB (160436970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607b1321566c31f38d6db97f6fe463c21c31254838c259c27180e2800e75714`  
		Last Modified: Thu, 07 Nov 2024 17:58:13 GMT  
		Size: 3.1 MB (3073119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089c50d4666afd32c4952210420f1e1de7eb3f56dac670cac1060e861dea5a98`  
		Last Modified: Thu, 07 Nov 2024 17:58:12 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aad88c5dd4dfb476fc17ed7ecdba4c5ab7d90ddcf7153bc3b58db21bad6128`  
		Last Modified: Thu, 07 Nov 2024 17:58:13 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:216e520563953450ed67707563f8567c77922e6d006f3d406a1f772ecaced335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3779638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abde6873e56a8b39fa847f9c764c72b58b992317ce3cc4986e2f65e0f3348e48`

```dockerfile
```

-	Layers:
	-	`sha256:335d60c271f354c1f2a9d1ae25e0a395bbe4f3e541f1224c4be5758e51d8a890`  
		Last Modified: Thu, 07 Nov 2024 17:58:13 GMT  
		Size: 3.8 MB (3755332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb1471a79e7351c797d3817fe11b04db472905f60774c633864addb6d034495`  
		Last Modified: Thu, 07 Nov 2024 17:58:12 GMT  
		Size: 24.3 KB (24306 bytes)  
		MIME: application/vnd.in-toto+json
