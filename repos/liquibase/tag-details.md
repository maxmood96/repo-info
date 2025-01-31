<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.31`](#liquibase431)
-	[`liquibase:4.31-alpine`](#liquibase431-alpine)
-	[`liquibase:4.31.0`](#liquibase4310)
-	[`liquibase:4.31.0-alpine`](#liquibase4310-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.31`

```console
$ docker pull liquibase@sha256:2f41c8aee90a91f8578bbe418a91fdad78b2eeeeca621ad9251bdec841c0e578
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31` - linux; amd64

```console
$ docker pull liquibase@sha256:b1288aa761ed85b690a3a515509e6bee01a7d17c26604c1f74c2ef6bc4fb8b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445890856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87322767acd8c8b0421320d0e5f0205de577a6641b0427c3044638df2415801`
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
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eaabae6c1076a4ceb667df821452a382fdff978ad229398104a2694c59f3757`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cd2e59e4508d443adb0b1784789c5da9a30c823b96c62f407082edaf12235`  
		Last Modified: Fri, 31 Jan 2025 02:15:56 GMT  
		Size: 349.9 MB (349941644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b4aec374b722376f2090f4aa874f9199ebed7ff317337d69a906a043b6233b`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 3.3 MB (3318530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a3c1c8b6462013cfd20ef684834e02d65c888bff635e59ee0691f2c3163a1`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d929c09cd2e07de178377e076e1b11dc179476b419925f711bfca26ec6fbbe10`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31` - unknown; unknown

```console
$ docker pull liquibase@sha256:3341f5a6e25c070b0462ca8874e97fc6485d636623baf95972b636838ae8c6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620c4ea8e0d3e2f197c7f418fd4c7cabf8328495668376db51122047812f818`

```dockerfile
```

-	Layers:
	-	`sha256:5365a53a954c7e143ec6fec195be393d663f58c2214fe5a4a709afb6051ef7ae`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 3.8 MB (3751335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d670ec86775e9bd140b0240d8cbcfe3db2ea59fab3ae1d2d36f8986fda8fac`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 24.2 KB (24207 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:dbcf532a56681fd9a90aa3ca799ac4d38a3df0d7855cf0d792242ee9b8d3c564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442906081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144722298992a629771851f5ae8285dcac862c7c86b782ebd097ade2866f376c`
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
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f5544512208bbc55ac60cde702e34a19180f2ece7e91807cf0736fa78a3522`  
		Last Modified: Fri, 31 Jan 2025 03:31:57 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927840b0f99be69514b16d3b430cfe9e0ed4113718960bc7f9674fce8e83400d`  
		Last Modified: Fri, 31 Jan 2025 03:32:08 GMT  
		Size: 349.9 MB (349941655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfaa7419a5a752ea1426e53b2369ab1875fa3430996336e265f198aebfb8844`  
		Last Modified: Fri, 31 Jan 2025 03:31:58 GMT  
		Size: 3.1 MB (3073129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6fec9f232e165cf97d956cbbdbee50a489c2097327370185e5453ae7d9d4ad`  
		Last Modified: Fri, 31 Jan 2025 03:31:57 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9895d30194730d6a2c5f4c747780a788115a7d2f6e5e6501cd185ae40e050eda`  
		Last Modified: Fri, 31 Jan 2025 03:31:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31` - unknown; unknown

```console
$ docker pull liquibase@sha256:81c89085eff13fd543c9a1736d8054635e8d11d55d5bf385bdbf2c2d679e300f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e9cf6bb519284572307609b27cf564ddd69bcf268012d0390ada12565f4794`

```dockerfile
```

-	Layers:
	-	`sha256:c19e47d461c69cc45feb34a9d91a61fa7791f9e518144f7f5f875c8c61d384ea`  
		Last Modified: Fri, 31 Jan 2025 03:31:58 GMT  
		Size: 3.8 MB (3752879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19631acc3dfc19e93261818ed64fb721f28e11f49430a52b8f679af9f8e8ce1`  
		Last Modified: Fri, 31 Jan 2025 03:31:57 GMT  
		Size: 24.3 KB (24328 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31-alpine`

```console
$ docker pull liquibase@sha256:ef20205dc221e41b83efd3290916bf403a9952031cc0bba2ca01219577b6d311
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:0ad90368b45fa70f1787b80afafe63cce8de87af8f911888b251d284498d4775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.6 MB (419617036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a10f91af43a8f969ad3116b0208c942e3a42fae433a1e5479b46089fea10e3`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62d7db0b44e7c655bbcb122f5d99b6c0399954f3e1ac048082bf4b607f374cb`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64808a362dcbd996c28bf0bc68fff938e8c3b54961eca9badac7f20449f9726f`  
		Last Modified: Tue, 28 Jan 2025 01:29:43 GMT  
		Size: 62.8 MB (62768769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee37b4df01ecccbccb28d99b34d85bd5c80579cdca911d1840fdda154298442`  
		Last Modified: Tue, 28 Jan 2025 01:29:47 GMT  
		Size: 350.0 MB (349963648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ad3cb07fa4bab2499399c1f8bf688fb1fff976f3a27d8a7f602bf1d35f105e`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 3.2 MB (3241278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfe462e73a4a04018736008d0bdd405c45654de3de58192b6d80d7dd60b6224`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f02e2cd6e863d8f051e35cf9718a6fa69aefb729591fb70cee5180af6128fc5`  
		Last Modified: Tue, 28 Jan 2025 01:29:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:f7934f76510bb353c33accd4d0eeb1d00cda09f4411a2bc81af91707c63ce9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5f0a1708b7783e306c51c639aef32f4dd7b8763d36428a66b53dd091c7901`

```dockerfile
```

-	Layers:
	-	`sha256:1ec08e29c8ea958d1772c9c0b9ef37bb89da4a90660b3755b03a92e6df54d252`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 385.1 KB (385082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21727b369c00d75a893103c654d82d79991e27bfb864f0b3dbb2bfb388066f8`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 21.2 KB (21247 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:44fc4ac094cf4fad9e0b6d431a6736bdb93125a31108c376198f709ad00a66d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.9 MB (418882041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1cd05ecf3f117138b49197023ecc0013ce9b6a5383006ed70cfe1e499c029a`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230f7fe18e406daf125bd07fd5a46f55a54cb4eae8bae389b007d877e9c987d2`  
		Last Modified: Tue, 28 Jan 2025 02:17:53 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71edc36c036a6afcb77e5b949b1f51a75e8e93f1bb40ece51bc0a08dc5c5aa1`  
		Last Modified: Tue, 28 Jan 2025 02:17:55 GMT  
		Size: 61.9 MB (61932416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1c7bb538dc4f1ea75dfc93b0c7513b532b6ccab17c2521d3a1678c04fca2c4`  
		Last Modified: Tue, 28 Jan 2025 02:18:01 GMT  
		Size: 350.0 MB (349963679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b67ffa8fd49111e4cf49ad96a45c918a4549d3aa8cc4ab5306276c759c4f4a5`  
		Last Modified: Tue, 28 Jan 2025 02:17:54 GMT  
		Size: 3.0 MB (2991961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ab32a5b4dcfcd62713b917aea7630adbfdc1b404b8455d4f7b7098a060022b`  
		Last Modified: Tue, 28 Jan 2025 02:17:54 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39feb5fdeb015f9a72b4811b17fc79e08a626f2b58f0e06e712fc90e179b004`  
		Last Modified: Tue, 28 Jan 2025 02:17:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a53b43742359ddb6d7954f936e03adb996bbc005c15dca77fdf0bc316fdc0ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 KB (405714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b006443f69f208c844f54dfd7ff48d4edf32b4071500a97310299c9842ca7e`

```dockerfile
```

-	Layers:
	-	`sha256:ff5d9ef7c7c0a7a5eed00cbacf06c32da4ebb0f0dcbd01f9c24341877bdb7b00`  
		Last Modified: Tue, 28 Jan 2025 02:17:53 GMT  
		Size: 384.3 KB (384329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08bb1fc94f441a190b36b591f8a6d22fbd1c6f5c2c6558080b420624791cd396`  
		Last Modified: Tue, 28 Jan 2025 02:17:53 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31.0`

```console
$ docker pull liquibase@sha256:2f41c8aee90a91f8578bbe418a91fdad78b2eeeeca621ad9251bdec841c0e578
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31.0` - linux; amd64

```console
$ docker pull liquibase@sha256:b1288aa761ed85b690a3a515509e6bee01a7d17c26604c1f74c2ef6bc4fb8b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445890856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87322767acd8c8b0421320d0e5f0205de577a6641b0427c3044638df2415801`
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
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eaabae6c1076a4ceb667df821452a382fdff978ad229398104a2694c59f3757`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cd2e59e4508d443adb0b1784789c5da9a30c823b96c62f407082edaf12235`  
		Last Modified: Fri, 31 Jan 2025 02:15:56 GMT  
		Size: 349.9 MB (349941644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b4aec374b722376f2090f4aa874f9199ebed7ff317337d69a906a043b6233b`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 3.3 MB (3318530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a3c1c8b6462013cfd20ef684834e02d65c888bff635e59ee0691f2c3163a1`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d929c09cd2e07de178377e076e1b11dc179476b419925f711bfca26ec6fbbe10`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:3341f5a6e25c070b0462ca8874e97fc6485d636623baf95972b636838ae8c6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620c4ea8e0d3e2f197c7f418fd4c7cabf8328495668376db51122047812f818`

```dockerfile
```

-	Layers:
	-	`sha256:5365a53a954c7e143ec6fec195be393d663f58c2214fe5a4a709afb6051ef7ae`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 3.8 MB (3751335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d670ec86775e9bd140b0240d8cbcfe3db2ea59fab3ae1d2d36f8986fda8fac`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 24.2 KB (24207 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:dbcf532a56681fd9a90aa3ca799ac4d38a3df0d7855cf0d792242ee9b8d3c564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442906081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144722298992a629771851f5ae8285dcac862c7c86b782ebd097ade2866f376c`
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
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f5544512208bbc55ac60cde702e34a19180f2ece7e91807cf0736fa78a3522`  
		Last Modified: Fri, 31 Jan 2025 03:31:57 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927840b0f99be69514b16d3b430cfe9e0ed4113718960bc7f9674fce8e83400d`  
		Last Modified: Fri, 31 Jan 2025 03:32:08 GMT  
		Size: 349.9 MB (349941655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfaa7419a5a752ea1426e53b2369ab1875fa3430996336e265f198aebfb8844`  
		Last Modified: Fri, 31 Jan 2025 03:31:58 GMT  
		Size: 3.1 MB (3073129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6fec9f232e165cf97d956cbbdbee50a489c2097327370185e5453ae7d9d4ad`  
		Last Modified: Fri, 31 Jan 2025 03:31:57 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9895d30194730d6a2c5f4c747780a788115a7d2f6e5e6501cd185ae40e050eda`  
		Last Modified: Fri, 31 Jan 2025 03:31:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:81c89085eff13fd543c9a1736d8054635e8d11d55d5bf385bdbf2c2d679e300f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e9cf6bb519284572307609b27cf564ddd69bcf268012d0390ada12565f4794`

```dockerfile
```

-	Layers:
	-	`sha256:c19e47d461c69cc45feb34a9d91a61fa7791f9e518144f7f5f875c8c61d384ea`  
		Last Modified: Fri, 31 Jan 2025 03:31:58 GMT  
		Size: 3.8 MB (3752879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19631acc3dfc19e93261818ed64fb721f28e11f49430a52b8f679af9f8e8ce1`  
		Last Modified: Fri, 31 Jan 2025 03:31:57 GMT  
		Size: 24.3 KB (24328 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31.0-alpine`

```console
$ docker pull liquibase@sha256:ef20205dc221e41b83efd3290916bf403a9952031cc0bba2ca01219577b6d311
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:0ad90368b45fa70f1787b80afafe63cce8de87af8f911888b251d284498d4775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.6 MB (419617036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a10f91af43a8f969ad3116b0208c942e3a42fae433a1e5479b46089fea10e3`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62d7db0b44e7c655bbcb122f5d99b6c0399954f3e1ac048082bf4b607f374cb`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64808a362dcbd996c28bf0bc68fff938e8c3b54961eca9badac7f20449f9726f`  
		Last Modified: Tue, 28 Jan 2025 01:29:43 GMT  
		Size: 62.8 MB (62768769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee37b4df01ecccbccb28d99b34d85bd5c80579cdca911d1840fdda154298442`  
		Last Modified: Tue, 28 Jan 2025 01:29:47 GMT  
		Size: 350.0 MB (349963648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ad3cb07fa4bab2499399c1f8bf688fb1fff976f3a27d8a7f602bf1d35f105e`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 3.2 MB (3241278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfe462e73a4a04018736008d0bdd405c45654de3de58192b6d80d7dd60b6224`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f02e2cd6e863d8f051e35cf9718a6fa69aefb729591fb70cee5180af6128fc5`  
		Last Modified: Tue, 28 Jan 2025 01:29:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:f7934f76510bb353c33accd4d0eeb1d00cda09f4411a2bc81af91707c63ce9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5f0a1708b7783e306c51c639aef32f4dd7b8763d36428a66b53dd091c7901`

```dockerfile
```

-	Layers:
	-	`sha256:1ec08e29c8ea958d1772c9c0b9ef37bb89da4a90660b3755b03a92e6df54d252`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 385.1 KB (385082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21727b369c00d75a893103c654d82d79991e27bfb864f0b3dbb2bfb388066f8`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 21.2 KB (21247 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:44fc4ac094cf4fad9e0b6d431a6736bdb93125a31108c376198f709ad00a66d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.9 MB (418882041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1cd05ecf3f117138b49197023ecc0013ce9b6a5383006ed70cfe1e499c029a`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230f7fe18e406daf125bd07fd5a46f55a54cb4eae8bae389b007d877e9c987d2`  
		Last Modified: Tue, 28 Jan 2025 02:17:53 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71edc36c036a6afcb77e5b949b1f51a75e8e93f1bb40ece51bc0a08dc5c5aa1`  
		Last Modified: Tue, 28 Jan 2025 02:17:55 GMT  
		Size: 61.9 MB (61932416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1c7bb538dc4f1ea75dfc93b0c7513b532b6ccab17c2521d3a1678c04fca2c4`  
		Last Modified: Tue, 28 Jan 2025 02:18:01 GMT  
		Size: 350.0 MB (349963679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b67ffa8fd49111e4cf49ad96a45c918a4549d3aa8cc4ab5306276c759c4f4a5`  
		Last Modified: Tue, 28 Jan 2025 02:17:54 GMT  
		Size: 3.0 MB (2991961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ab32a5b4dcfcd62713b917aea7630adbfdc1b404b8455d4f7b7098a060022b`  
		Last Modified: Tue, 28 Jan 2025 02:17:54 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39feb5fdeb015f9a72b4811b17fc79e08a626f2b58f0e06e712fc90e179b004`  
		Last Modified: Tue, 28 Jan 2025 02:17:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a53b43742359ddb6d7954f936e03adb996bbc005c15dca77fdf0bc316fdc0ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 KB (405714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b006443f69f208c844f54dfd7ff48d4edf32b4071500a97310299c9842ca7e`

```dockerfile
```

-	Layers:
	-	`sha256:ff5d9ef7c7c0a7a5eed00cbacf06c32da4ebb0f0dcbd01f9c24341877bdb7b00`  
		Last Modified: Tue, 28 Jan 2025 02:17:53 GMT  
		Size: 384.3 KB (384329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08bb1fc94f441a190b36b591f8a6d22fbd1c6f5c2c6558080b420624791cd396`  
		Last Modified: Tue, 28 Jan 2025 02:17:53 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:ef20205dc221e41b83efd3290916bf403a9952031cc0bba2ca01219577b6d311
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:0ad90368b45fa70f1787b80afafe63cce8de87af8f911888b251d284498d4775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.6 MB (419617036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a10f91af43a8f969ad3116b0208c942e3a42fae433a1e5479b46089fea10e3`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62d7db0b44e7c655bbcb122f5d99b6c0399954f3e1ac048082bf4b607f374cb`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64808a362dcbd996c28bf0bc68fff938e8c3b54961eca9badac7f20449f9726f`  
		Last Modified: Tue, 28 Jan 2025 01:29:43 GMT  
		Size: 62.8 MB (62768769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee37b4df01ecccbccb28d99b34d85bd5c80579cdca911d1840fdda154298442`  
		Last Modified: Tue, 28 Jan 2025 01:29:47 GMT  
		Size: 350.0 MB (349963648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ad3cb07fa4bab2499399c1f8bf688fb1fff976f3a27d8a7f602bf1d35f105e`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 3.2 MB (3241278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfe462e73a4a04018736008d0bdd405c45654de3de58192b6d80d7dd60b6224`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f02e2cd6e863d8f051e35cf9718a6fa69aefb729591fb70cee5180af6128fc5`  
		Last Modified: Tue, 28 Jan 2025 01:29:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:f7934f76510bb353c33accd4d0eeb1d00cda09f4411a2bc81af91707c63ce9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a5f0a1708b7783e306c51c639aef32f4dd7b8763d36428a66b53dd091c7901`

```dockerfile
```

-	Layers:
	-	`sha256:1ec08e29c8ea958d1772c9c0b9ef37bb89da4a90660b3755b03a92e6df54d252`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 385.1 KB (385082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21727b369c00d75a893103c654d82d79991e27bfb864f0b3dbb2bfb388066f8`  
		Last Modified: Tue, 28 Jan 2025 01:29:42 GMT  
		Size: 21.2 KB (21247 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:44fc4ac094cf4fad9e0b6d431a6736bdb93125a31108c376198f709ad00a66d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.9 MB (418882041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1cd05ecf3f117138b49197023ecc0013ce9b6a5383006ed70cfe1e499c029a`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230f7fe18e406daf125bd07fd5a46f55a54cb4eae8bae389b007d877e9c987d2`  
		Last Modified: Tue, 28 Jan 2025 02:17:53 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71edc36c036a6afcb77e5b949b1f51a75e8e93f1bb40ece51bc0a08dc5c5aa1`  
		Last Modified: Tue, 28 Jan 2025 02:17:55 GMT  
		Size: 61.9 MB (61932416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1c7bb538dc4f1ea75dfc93b0c7513b532b6ccab17c2521d3a1678c04fca2c4`  
		Last Modified: Tue, 28 Jan 2025 02:18:01 GMT  
		Size: 350.0 MB (349963679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b67ffa8fd49111e4cf49ad96a45c918a4549d3aa8cc4ab5306276c759c4f4a5`  
		Last Modified: Tue, 28 Jan 2025 02:17:54 GMT  
		Size: 3.0 MB (2991961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ab32a5b4dcfcd62713b917aea7630adbfdc1b404b8455d4f7b7098a060022b`  
		Last Modified: Tue, 28 Jan 2025 02:17:54 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39feb5fdeb015f9a72b4811b17fc79e08a626f2b58f0e06e712fc90e179b004`  
		Last Modified: Tue, 28 Jan 2025 02:17:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a53b43742359ddb6d7954f936e03adb996bbc005c15dca77fdf0bc316fdc0ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 KB (405714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b006443f69f208c844f54dfd7ff48d4edf32b4071500a97310299c9842ca7e`

```dockerfile
```

-	Layers:
	-	`sha256:ff5d9ef7c7c0a7a5eed00cbacf06c32da4ebb0f0dcbd01f9c24341877bdb7b00`  
		Last Modified: Tue, 28 Jan 2025 02:17:53 GMT  
		Size: 384.3 KB (384329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08bb1fc94f441a190b36b591f8a6d22fbd1c6f5c2c6558080b420624791cd396`  
		Last Modified: Tue, 28 Jan 2025 02:17:53 GMT  
		Size: 21.4 KB (21385 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:2f41c8aee90a91f8578bbe418a91fdad78b2eeeeca621ad9251bdec841c0e578
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:b1288aa761ed85b690a3a515509e6bee01a7d17c26604c1f74c2ef6bc4fb8b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445890856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87322767acd8c8b0421320d0e5f0205de577a6641b0427c3044638df2415801`
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
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eaabae6c1076a4ceb667df821452a382fdff978ad229398104a2694c59f3757`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cd2e59e4508d443adb0b1784789c5da9a30c823b96c62f407082edaf12235`  
		Last Modified: Fri, 31 Jan 2025 02:15:56 GMT  
		Size: 349.9 MB (349941644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b4aec374b722376f2090f4aa874f9199ebed7ff317337d69a906a043b6233b`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 3.3 MB (3318530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a3c1c8b6462013cfd20ef684834e02d65c888bff635e59ee0691f2c3163a1`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d929c09cd2e07de178377e076e1b11dc179476b419925f711bfca26ec6fbbe10`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:3341f5a6e25c070b0462ca8874e97fc6485d636623baf95972b636838ae8c6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0620c4ea8e0d3e2f197c7f418fd4c7cabf8328495668376db51122047812f818`

```dockerfile
```

-	Layers:
	-	`sha256:5365a53a954c7e143ec6fec195be393d663f58c2214fe5a4a709afb6051ef7ae`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 3.8 MB (3751335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d670ec86775e9bd140b0240d8cbcfe3db2ea59fab3ae1d2d36f8986fda8fac`  
		Last Modified: Fri, 31 Jan 2025 02:15:51 GMT  
		Size: 24.2 KB (24207 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:dbcf532a56681fd9a90aa3ca799ac4d38a3df0d7855cf0d792242ee9b8d3c564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442906081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144722298992a629771851f5ae8285dcac862c7c86b782ebd097ade2866f376c`
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
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Jan 2025 17:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
WORKDIR /liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_VERSION=0.2.8
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 24 Jan 2025 17:25:12 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 24 Jan 2025 17:25:12 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 24 Jan 2025 17:25:12 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 24 Jan 2025 17:25:12 GMT
USER liquibase:liquibase
# Fri, 24 Jan 2025 17:25:12 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 24 Jan 2025 17:25:12 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f5544512208bbc55ac60cde702e34a19180f2ece7e91807cf0736fa78a3522`  
		Last Modified: Fri, 31 Jan 2025 03:31:57 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927840b0f99be69514b16d3b430cfe9e0ed4113718960bc7f9674fce8e83400d`  
		Last Modified: Fri, 31 Jan 2025 03:32:08 GMT  
		Size: 349.9 MB (349941655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfaa7419a5a752ea1426e53b2369ab1875fa3430996336e265f198aebfb8844`  
		Last Modified: Fri, 31 Jan 2025 03:31:58 GMT  
		Size: 3.1 MB (3073129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6fec9f232e165cf97d956cbbdbee50a489c2097327370185e5453ae7d9d4ad`  
		Last Modified: Fri, 31 Jan 2025 03:31:57 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9895d30194730d6a2c5f4c747780a788115a7d2f6e5e6501cd185ae40e050eda`  
		Last Modified: Fri, 31 Jan 2025 03:31:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:81c89085eff13fd543c9a1736d8054635e8d11d55d5bf385bdbf2c2d679e300f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e9cf6bb519284572307609b27cf564ddd69bcf268012d0390ada12565f4794`

```dockerfile
```

-	Layers:
	-	`sha256:c19e47d461c69cc45feb34a9d91a61fa7791f9e518144f7f5f875c8c61d384ea`  
		Last Modified: Fri, 31 Jan 2025 03:31:58 GMT  
		Size: 3.8 MB (3752879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19631acc3dfc19e93261818ed64fb721f28e11f49430a52b8f679af9f8e8ce1`  
		Last Modified: Fri, 31 Jan 2025 03:31:57 GMT  
		Size: 24.3 KB (24328 bytes)  
		MIME: application/vnd.in-toto+json
