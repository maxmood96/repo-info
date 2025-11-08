<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:5.0`](#liquibase50)
-	[`liquibase:5.0-alpine`](#liquibase50-alpine)
-	[`liquibase:5.0.1`](#liquibase501)
-	[`liquibase:5.0.1-alpine`](#liquibase501-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:5.0`

```console
$ docker pull liquibase@sha256:d131290a9ce0dbca8afd0ca7eccb3f6a9b0ae888b264502d476dc14614041e55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0` - linux; amd64

```console
$ docker pull liquibase@sha256:f6738e86b0ed9b830d3852034d68fc8e5ed28c19302676e9c4aade93876655ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111104282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c9334313caee17b0e8cb97a04a8370975d1bea689bac69ca4199ec34526d43`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:57 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:00:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:24 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Sat, 08 Nov 2025 18:31:24 GMT
WORKDIR /liquibase
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Sat, 08 Nov 2025 18:31:25 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LPM_VERSION=0.2.14
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.version=5.0.1
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Sat, 08 Nov 2025 18:31:33 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Sat, 08 Nov 2025 18:31:33 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 08 Nov 2025 18:31:33 GMT
ENV DOCKER_LIQUIBASE=true
# Sat, 08 Nov 2025 18:31:33 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Sat, 08 Nov 2025 18:31:33 GMT
COPY liquibase.docker.properties ./ # buildkit
# Sat, 08 Nov 2025 18:31:33 GMT
USER liquibase:liquibase
# Sat, 08 Nov 2025 18:31:33 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:33 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2efaf4f7327a471e1b969eaddc7e44e5ccae0df783fcaa48bf94864d07a0d`  
		Last Modified: Sat, 08 Nov 2025 18:00:21 GMT  
		Size: 16.2 MB (16150304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c0a6ab39aeac3774dd534c27427e0d533f07a637624ab254c6849bda796f16`  
		Last Modified: Sat, 08 Nov 2025 18:00:28 GMT  
		Size: 53.0 MB (52978483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f2a033ca8df84c1a3081f8ef917342b430ebdc1587bedf05eb381e45383ac`  
		Last Modified: Sat, 08 Nov 2025 18:00:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc3096c0eb2bbc9ac33b0cdb8552433f874659010096eb476cdd53f1aae60a3`  
		Last Modified: Sat, 08 Nov 2025 18:00:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ec9c66d679a5a359a749f0019dff70984dc88faf65d5a62a927fe6f5e6632b`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcde102a212eaaaa788081a690006cf06f20c71c03bfdc3758a1ac1a16f4070`  
		Last Modified: Sat, 08 Nov 2025 18:32:38 GMT  
		Size: 8.7 MB (8665799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab43f7991a91feea6744f920d4b991aaee1d5396fa65af6555c8ba54ac50822`  
		Last Modified: Sat, 08 Nov 2025 18:32:38 GMT  
		Size: 3.8 MB (3764497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9d9601a6c3c98ffe832710ca4908f8d1ce3abaaf8deaa9fbb00b64e816b8f0`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ef95f64c6859559af596f690f1df538381454b3abd54699bc22a754475eb3`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:8e1bb903070264aad87f5b99c58b3aa799700437f3fd80ffebf94fe31e4914d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211024646a67fcc63118663481f874d9e34eee6de3810701a6bb3fa344ca0d15`

```dockerfile
```

-	Layers:
	-	`sha256:a140fa9a97d37ef0ad5cbc391c7d29879e82a2033167838f00a90cde951dc6f7`  
		Last Modified: Sat, 08 Nov 2025 22:39:19 GMT  
		Size: 3.9 MB (3897733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ec2236c99a4fff57d018bc4a6f076dd332ed48b2a542ca474e15e1b22c9c90`  
		Last Modified: Sat, 08 Nov 2025 22:39:20 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:e64bcd0c6e92d848f680b661ae907d19ef2beccfa76dc790c8e0c1aed9e1448a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107713379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71373e531f1b834bfb621d16b8b53bc15994e8aa3ebc5d489b7dd89103379235`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:13 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:29:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Sat, 08 Nov 2025 18:29:56 GMT
WORKDIR /liquibase
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Sat, 08 Nov 2025 18:29:57 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LPM_VERSION=0.2.14
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.version=5.0.1
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Sat, 08 Nov 2025 18:30:06 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Sat, 08 Nov 2025 18:30:06 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 08 Nov 2025 18:30:06 GMT
ENV DOCKER_LIQUIBASE=true
# Sat, 08 Nov 2025 18:30:06 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Sat, 08 Nov 2025 18:30:06 GMT
COPY liquibase.docker.properties ./ # buildkit
# Sat, 08 Nov 2025 18:30:06 GMT
USER liquibase:liquibase
# Sat, 08 Nov 2025 18:30:06 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:06 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028993be8a76c7119b0d8ee582ec1146a4a9da89a2876287461de42112766642`  
		Last Modified: Sat, 08 Nov 2025 17:59:53 GMT  
		Size: 16.1 MB (16066196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf12991e52872631db4f5866423e61c9aa264b18e7b99735b58d5e9b7424ea`  
		Last Modified: Sat, 08 Nov 2025 17:59:52 GMT  
		Size: 52.1 MB (52148599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e39452ec2196b4a744bd1ec7029e928fad324f4e0aa146be26945045f2e628`  
		Last Modified: Sat, 08 Nov 2025 17:59:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c83d3140bc0663488b5277b96f30f09c76765775b653007c9573825d31d1e`  
		Last Modified: Sat, 08 Nov 2025 17:59:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b4c3c196182560757b22a9520cf0c88ea94e74859adcabb58de774fce32236`  
		Last Modified: Sat, 08 Nov 2025 18:30:56 GMT  
		Size: 4.3 KB (4329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90e20f94cb6a51e16b46807a43756804ae607659399e661ac07fb980474f4c0`  
		Last Modified: Sat, 08 Nov 2025 18:30:57 GMT  
		Size: 8.7 MB (8665799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cad52fc40c4fce263a8bad4f57afb1c45b0f151d6d925adf26787dd2195d21`  
		Last Modified: Sat, 08 Nov 2025 18:30:57 GMT  
		Size: 3.4 MB (3441276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12be07884b37532cb0a2c5076044f6ca7864584bbeda21ec5d847d7689702dcf`  
		Last Modified: Sat, 08 Nov 2025 18:30:56 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da02e982d759f0862a5a9db768b3c8afc70b9ccae7635034f8f703b69fbd55e`  
		Last Modified: Sat, 08 Nov 2025 18:30:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:448c5410dbbc733b552caf49f0c73ed72688ea61b680ab7a873e4d9611e9ddf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1541f58caec390696f2dd1cf9c1400fa04ff1af219b357d560d602624439d272`

```dockerfile
```

-	Layers:
	-	`sha256:6d9d6ab9f909b5eb6cf21a13cafd18b3c682487740ad261c726dd4c7027b95e5`  
		Last Modified: Sat, 08 Nov 2025 19:39:24 GMT  
		Size: 3.9 MB (3897401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8bb732e22e95ac82f737307760e992437650e16d2a35beb31d32ace08a5205`  
		Last Modified: Sat, 08 Nov 2025 19:39:25 GMT  
		Size: 24.4 KB (24445 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0-alpine`

```console
$ docker pull liquibase@sha256:79faac547231dabb16dc7826dc2f1ba4c38340a64394a25e5c5fc47a3fdf8be4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:ddecc191930f8c219e7fdc31b70fdcf86420668b3fcb93eec00058723077776c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84029488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c540f45126bf802bed524848c3d098a9447df9f28eeb7493959ae47b5cce83`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 03 Oct 2025 18:38:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
WORKDIR /liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_VERSION=0.2.14
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 03 Oct 2025 18:38:32 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
USER liquibase:liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f67999293a8197024f11dbd624adc758381fbf4e996e6169d105b063ebfd31`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb205342480783f5bb1e06318bdaf69160f8dcb2cc985b28fc592db0da1e4d08`  
		Last Modified: Wed, 08 Oct 2025 23:11:12 GMT  
		Size: 67.9 MB (67852201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f233e00b95593d29f2e838cabc639cda38604134af51290577d01ea67bfc3f1f`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 8.7 MB (8688917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f991eef8b65308b0fe2f26e732900a06ea4000eb2deba2e7145f73ba938206`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 3.7 MB (3683351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc85122cd37a70766ba8cc4c8a75b626366c8394102b12927b357587790b633`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5362889dcfde1a1a5fc3853e8c16e58b593bdf96b9e39ce9e23decdb3a30bb8e`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:38312fdc074a63166254eeb8e0de5ab3b287fcb4397179c585330e2228483303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.4 KB (380369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a985c65a2461f599f7f0b8cd21710929ed8392b7d65e47d546322d7a392ddb0d`

```dockerfile
```

-	Layers:
	-	`sha256:a00a34b34001a3ba504d727b96bd7dec360a2a1298408cd846357a5b90f4e9b6`  
		Last Modified: Thu, 09 Oct 2025 00:39:21 GMT  
		Size: 358.7 KB (358668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edd144ccfa0ca865ff206366cdf6aa5c7e585c08a3f3cd5219c71dcd6022aea`  
		Last Modified: Thu, 09 Oct 2025 00:39:22 GMT  
		Size: 21.7 KB (21701 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:560aef75635ecb97933699b33fab77b1d6d37c78ea3e562cc7659e33d670601e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83040049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce0d0a46acaba0bda4738c33737c69fedf98dc6a4420b187fe533d3f2d2c225`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 03 Oct 2025 18:38:32 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
WORKDIR /liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_VERSION=0.2.14
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 03 Oct 2025 18:38:32 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
USER liquibase:liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a978978408660ba16ead2899c0e6f793d970de050dd419acdfec7e851993a1`  
		Last Modified: Wed, 08 Oct 2025 21:56:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f7ade868c96a1721ec2bd136fa8c8ca96903d953f2a47023d5e76c7e00939`  
		Last Modified: Wed, 08 Oct 2025 21:56:07 GMT  
		Size: 66.9 MB (66850853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59db1d4966e87df96fcd3be3db735f9bdd9fc2be1f23bb49a979957e195f8697`  
		Last Modified: Wed, 08 Oct 2025 21:56:05 GMT  
		Size: 8.7 MB (8688887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251e462f64902eae401948526149fb901280d878908bd61622306a97cd3c9067`  
		Last Modified: Wed, 08 Oct 2025 21:56:05 GMT  
		Size: 3.4 MB (3359674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9636ebc80885e4a78c48b8831830c0532a46924df556443d935cd20f6612c9`  
		Last Modified: Wed, 08 Oct 2025 21:56:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9bf3dcc1ddad0806e66e3d58fc44ee595f2c3104c548514c4245811172c682`  
		Last Modified: Wed, 08 Oct 2025 21:56:04 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:84736d7937ec99f5394a54387fe6d9192ce279fdf54b24f85687b6f4332917e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 KB (379753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82b6981cd20307d498c47a2121551182286bc457bc404b74bd4eb53c9f6ec95`

```dockerfile
```

-	Layers:
	-	`sha256:2954d4e0f21fc3328d6f73de8c516257b530294742f27353b80f99e6c7ac7ee1`  
		Last Modified: Thu, 09 Oct 2025 00:39:25 GMT  
		Size: 357.9 KB (357915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486135ddc79373a646134e9069e76fb309dbb74e12fbc96a05718e91b8178c79`  
		Last Modified: Thu, 09 Oct 2025 00:39:26 GMT  
		Size: 21.8 KB (21838 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.1`

```console
$ docker pull liquibase@sha256:d131290a9ce0dbca8afd0ca7eccb3f6a9b0ae888b264502d476dc14614041e55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1` - linux; amd64

```console
$ docker pull liquibase@sha256:f6738e86b0ed9b830d3852034d68fc8e5ed28c19302676e9c4aade93876655ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111104282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c9334313caee17b0e8cb97a04a8370975d1bea689bac69ca4199ec34526d43`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:57 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:00:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:24 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Sat, 08 Nov 2025 18:31:24 GMT
WORKDIR /liquibase
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Sat, 08 Nov 2025 18:31:25 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LPM_VERSION=0.2.14
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.version=5.0.1
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Sat, 08 Nov 2025 18:31:33 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Sat, 08 Nov 2025 18:31:33 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 08 Nov 2025 18:31:33 GMT
ENV DOCKER_LIQUIBASE=true
# Sat, 08 Nov 2025 18:31:33 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Sat, 08 Nov 2025 18:31:33 GMT
COPY liquibase.docker.properties ./ # buildkit
# Sat, 08 Nov 2025 18:31:33 GMT
USER liquibase:liquibase
# Sat, 08 Nov 2025 18:31:33 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:33 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2efaf4f7327a471e1b969eaddc7e44e5ccae0df783fcaa48bf94864d07a0d`  
		Last Modified: Sat, 08 Nov 2025 18:00:21 GMT  
		Size: 16.2 MB (16150304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c0a6ab39aeac3774dd534c27427e0d533f07a637624ab254c6849bda796f16`  
		Last Modified: Sat, 08 Nov 2025 18:00:28 GMT  
		Size: 53.0 MB (52978483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f2a033ca8df84c1a3081f8ef917342b430ebdc1587bedf05eb381e45383ac`  
		Last Modified: Sat, 08 Nov 2025 18:00:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc3096c0eb2bbc9ac33b0cdb8552433f874659010096eb476cdd53f1aae60a3`  
		Last Modified: Sat, 08 Nov 2025 18:00:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ec9c66d679a5a359a749f0019dff70984dc88faf65d5a62a927fe6f5e6632b`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcde102a212eaaaa788081a690006cf06f20c71c03bfdc3758a1ac1a16f4070`  
		Last Modified: Sat, 08 Nov 2025 18:32:38 GMT  
		Size: 8.7 MB (8665799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab43f7991a91feea6744f920d4b991aaee1d5396fa65af6555c8ba54ac50822`  
		Last Modified: Sat, 08 Nov 2025 18:32:38 GMT  
		Size: 3.8 MB (3764497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9d9601a6c3c98ffe832710ca4908f8d1ce3abaaf8deaa9fbb00b64e816b8f0`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ef95f64c6859559af596f690f1df538381454b3abd54699bc22a754475eb3`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:8e1bb903070264aad87f5b99c58b3aa799700437f3fd80ffebf94fe31e4914d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211024646a67fcc63118663481f874d9e34eee6de3810701a6bb3fa344ca0d15`

```dockerfile
```

-	Layers:
	-	`sha256:a140fa9a97d37ef0ad5cbc391c7d29879e82a2033167838f00a90cde951dc6f7`  
		Last Modified: Sat, 08 Nov 2025 22:39:19 GMT  
		Size: 3.9 MB (3897733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ec2236c99a4fff57d018bc4a6f076dd332ed48b2a542ca474e15e1b22c9c90`  
		Last Modified: Sat, 08 Nov 2025 22:39:20 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:e64bcd0c6e92d848f680b661ae907d19ef2beccfa76dc790c8e0c1aed9e1448a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107713379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71373e531f1b834bfb621d16b8b53bc15994e8aa3ebc5d489b7dd89103379235`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:13 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:29:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Sat, 08 Nov 2025 18:29:56 GMT
WORKDIR /liquibase
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Sat, 08 Nov 2025 18:29:57 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LPM_VERSION=0.2.14
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.version=5.0.1
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Sat, 08 Nov 2025 18:30:06 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Sat, 08 Nov 2025 18:30:06 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 08 Nov 2025 18:30:06 GMT
ENV DOCKER_LIQUIBASE=true
# Sat, 08 Nov 2025 18:30:06 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Sat, 08 Nov 2025 18:30:06 GMT
COPY liquibase.docker.properties ./ # buildkit
# Sat, 08 Nov 2025 18:30:06 GMT
USER liquibase:liquibase
# Sat, 08 Nov 2025 18:30:06 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:06 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028993be8a76c7119b0d8ee582ec1146a4a9da89a2876287461de42112766642`  
		Last Modified: Sat, 08 Nov 2025 17:59:53 GMT  
		Size: 16.1 MB (16066196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf12991e52872631db4f5866423e61c9aa264b18e7b99735b58d5e9b7424ea`  
		Last Modified: Sat, 08 Nov 2025 17:59:52 GMT  
		Size: 52.1 MB (52148599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e39452ec2196b4a744bd1ec7029e928fad324f4e0aa146be26945045f2e628`  
		Last Modified: Sat, 08 Nov 2025 17:59:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c83d3140bc0663488b5277b96f30f09c76765775b653007c9573825d31d1e`  
		Last Modified: Sat, 08 Nov 2025 17:59:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b4c3c196182560757b22a9520cf0c88ea94e74859adcabb58de774fce32236`  
		Last Modified: Sat, 08 Nov 2025 18:30:56 GMT  
		Size: 4.3 KB (4329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90e20f94cb6a51e16b46807a43756804ae607659399e661ac07fb980474f4c0`  
		Last Modified: Sat, 08 Nov 2025 18:30:57 GMT  
		Size: 8.7 MB (8665799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cad52fc40c4fce263a8bad4f57afb1c45b0f151d6d925adf26787dd2195d21`  
		Last Modified: Sat, 08 Nov 2025 18:30:57 GMT  
		Size: 3.4 MB (3441276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12be07884b37532cb0a2c5076044f6ca7864584bbeda21ec5d847d7689702dcf`  
		Last Modified: Sat, 08 Nov 2025 18:30:56 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da02e982d759f0862a5a9db768b3c8afc70b9ccae7635034f8f703b69fbd55e`  
		Last Modified: Sat, 08 Nov 2025 18:30:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:448c5410dbbc733b552caf49f0c73ed72688ea61b680ab7a873e4d9611e9ddf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1541f58caec390696f2dd1cf9c1400fa04ff1af219b357d560d602624439d272`

```dockerfile
```

-	Layers:
	-	`sha256:6d9d6ab9f909b5eb6cf21a13cafd18b3c682487740ad261c726dd4c7027b95e5`  
		Last Modified: Sat, 08 Nov 2025 19:39:24 GMT  
		Size: 3.9 MB (3897401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8bb732e22e95ac82f737307760e992437650e16d2a35beb31d32ace08a5205`  
		Last Modified: Sat, 08 Nov 2025 19:39:25 GMT  
		Size: 24.4 KB (24445 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.1-alpine`

```console
$ docker pull liquibase@sha256:79faac547231dabb16dc7826dc2f1ba4c38340a64394a25e5c5fc47a3fdf8be4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:ddecc191930f8c219e7fdc31b70fdcf86420668b3fcb93eec00058723077776c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84029488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c540f45126bf802bed524848c3d098a9447df9f28eeb7493959ae47b5cce83`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 03 Oct 2025 18:38:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
WORKDIR /liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_VERSION=0.2.14
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 03 Oct 2025 18:38:32 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
USER liquibase:liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f67999293a8197024f11dbd624adc758381fbf4e996e6169d105b063ebfd31`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb205342480783f5bb1e06318bdaf69160f8dcb2cc985b28fc592db0da1e4d08`  
		Last Modified: Wed, 08 Oct 2025 23:11:12 GMT  
		Size: 67.9 MB (67852201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f233e00b95593d29f2e838cabc639cda38604134af51290577d01ea67bfc3f1f`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 8.7 MB (8688917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f991eef8b65308b0fe2f26e732900a06ea4000eb2deba2e7145f73ba938206`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 3.7 MB (3683351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc85122cd37a70766ba8cc4c8a75b626366c8394102b12927b357587790b633`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5362889dcfde1a1a5fc3853e8c16e58b593bdf96b9e39ce9e23decdb3a30bb8e`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:38312fdc074a63166254eeb8e0de5ab3b287fcb4397179c585330e2228483303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.4 KB (380369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a985c65a2461f599f7f0b8cd21710929ed8392b7d65e47d546322d7a392ddb0d`

```dockerfile
```

-	Layers:
	-	`sha256:a00a34b34001a3ba504d727b96bd7dec360a2a1298408cd846357a5b90f4e9b6`  
		Last Modified: Thu, 09 Oct 2025 00:39:21 GMT  
		Size: 358.7 KB (358668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edd144ccfa0ca865ff206366cdf6aa5c7e585c08a3f3cd5219c71dcd6022aea`  
		Last Modified: Thu, 09 Oct 2025 00:39:22 GMT  
		Size: 21.7 KB (21701 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:560aef75635ecb97933699b33fab77b1d6d37c78ea3e562cc7659e33d670601e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83040049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce0d0a46acaba0bda4738c33737c69fedf98dc6a4420b187fe533d3f2d2c225`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 03 Oct 2025 18:38:32 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
WORKDIR /liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_VERSION=0.2.14
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 03 Oct 2025 18:38:32 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
USER liquibase:liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a978978408660ba16ead2899c0e6f793d970de050dd419acdfec7e851993a1`  
		Last Modified: Wed, 08 Oct 2025 21:56:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f7ade868c96a1721ec2bd136fa8c8ca96903d953f2a47023d5e76c7e00939`  
		Last Modified: Wed, 08 Oct 2025 21:56:07 GMT  
		Size: 66.9 MB (66850853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59db1d4966e87df96fcd3be3db735f9bdd9fc2be1f23bb49a979957e195f8697`  
		Last Modified: Wed, 08 Oct 2025 21:56:05 GMT  
		Size: 8.7 MB (8688887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251e462f64902eae401948526149fb901280d878908bd61622306a97cd3c9067`  
		Last Modified: Wed, 08 Oct 2025 21:56:05 GMT  
		Size: 3.4 MB (3359674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9636ebc80885e4a78c48b8831830c0532a46924df556443d935cd20f6612c9`  
		Last Modified: Wed, 08 Oct 2025 21:56:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9bf3dcc1ddad0806e66e3d58fc44ee595f2c3104c548514c4245811172c682`  
		Last Modified: Wed, 08 Oct 2025 21:56:04 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:84736d7937ec99f5394a54387fe6d9192ce279fdf54b24f85687b6f4332917e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 KB (379753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82b6981cd20307d498c47a2121551182286bc457bc404b74bd4eb53c9f6ec95`

```dockerfile
```

-	Layers:
	-	`sha256:2954d4e0f21fc3328d6f73de8c516257b530294742f27353b80f99e6c7ac7ee1`  
		Last Modified: Thu, 09 Oct 2025 00:39:25 GMT  
		Size: 357.9 KB (357915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486135ddc79373a646134e9069e76fb309dbb74e12fbc96a05718e91b8178c79`  
		Last Modified: Thu, 09 Oct 2025 00:39:26 GMT  
		Size: 21.8 KB (21838 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:79faac547231dabb16dc7826dc2f1ba4c38340a64394a25e5c5fc47a3fdf8be4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:ddecc191930f8c219e7fdc31b70fdcf86420668b3fcb93eec00058723077776c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84029488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c540f45126bf802bed524848c3d098a9447df9f28eeb7493959ae47b5cce83`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 03 Oct 2025 18:38:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
WORKDIR /liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_VERSION=0.2.14
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 03 Oct 2025 18:38:32 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
USER liquibase:liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f67999293a8197024f11dbd624adc758381fbf4e996e6169d105b063ebfd31`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb205342480783f5bb1e06318bdaf69160f8dcb2cc985b28fc592db0da1e4d08`  
		Last Modified: Wed, 08 Oct 2025 23:11:12 GMT  
		Size: 67.9 MB (67852201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f233e00b95593d29f2e838cabc639cda38604134af51290577d01ea67bfc3f1f`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 8.7 MB (8688917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f991eef8b65308b0fe2f26e732900a06ea4000eb2deba2e7145f73ba938206`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 3.7 MB (3683351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc85122cd37a70766ba8cc4c8a75b626366c8394102b12927b357587790b633`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5362889dcfde1a1a5fc3853e8c16e58b593bdf96b9e39ce9e23decdb3a30bb8e`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:38312fdc074a63166254eeb8e0de5ab3b287fcb4397179c585330e2228483303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.4 KB (380369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a985c65a2461f599f7f0b8cd21710929ed8392b7d65e47d546322d7a392ddb0d`

```dockerfile
```

-	Layers:
	-	`sha256:a00a34b34001a3ba504d727b96bd7dec360a2a1298408cd846357a5b90f4e9b6`  
		Last Modified: Thu, 09 Oct 2025 00:39:21 GMT  
		Size: 358.7 KB (358668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edd144ccfa0ca865ff206366cdf6aa5c7e585c08a3f3cd5219c71dcd6022aea`  
		Last Modified: Thu, 09 Oct 2025 00:39:22 GMT  
		Size: 21.7 KB (21701 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:560aef75635ecb97933699b33fab77b1d6d37c78ea3e562cc7659e33d670601e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83040049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce0d0a46acaba0bda4738c33737c69fedf98dc6a4420b187fe533d3f2d2c225`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 03 Oct 2025 18:38:32 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
WORKDIR /liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_VERSION=0.2.14
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 03 Oct 2025 18:38:32 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 03 Oct 2025 18:38:32 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 03 Oct 2025 18:38:32 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 03 Oct 2025 18:38:32 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 03 Oct 2025 18:38:32 GMT
USER liquibase:liquibase
# Fri, 03 Oct 2025 18:38:32 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 03 Oct 2025 18:38:32 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a978978408660ba16ead2899c0e6f793d970de050dd419acdfec7e851993a1`  
		Last Modified: Wed, 08 Oct 2025 21:56:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f7ade868c96a1721ec2bd136fa8c8ca96903d953f2a47023d5e76c7e00939`  
		Last Modified: Wed, 08 Oct 2025 21:56:07 GMT  
		Size: 66.9 MB (66850853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59db1d4966e87df96fcd3be3db735f9bdd9fc2be1f23bb49a979957e195f8697`  
		Last Modified: Wed, 08 Oct 2025 21:56:05 GMT  
		Size: 8.7 MB (8688887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251e462f64902eae401948526149fb901280d878908bd61622306a97cd3c9067`  
		Last Modified: Wed, 08 Oct 2025 21:56:05 GMT  
		Size: 3.4 MB (3359674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9636ebc80885e4a78c48b8831830c0532a46924df556443d935cd20f6612c9`  
		Last Modified: Wed, 08 Oct 2025 21:56:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9bf3dcc1ddad0806e66e3d58fc44ee595f2c3104c548514c4245811172c682`  
		Last Modified: Wed, 08 Oct 2025 21:56:04 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:84736d7937ec99f5394a54387fe6d9192ce279fdf54b24f85687b6f4332917e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 KB (379753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82b6981cd20307d498c47a2121551182286bc457bc404b74bd4eb53c9f6ec95`

```dockerfile
```

-	Layers:
	-	`sha256:2954d4e0f21fc3328d6f73de8c516257b530294742f27353b80f99e6c7ac7ee1`  
		Last Modified: Thu, 09 Oct 2025 00:39:25 GMT  
		Size: 357.9 KB (357915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486135ddc79373a646134e9069e76fb309dbb74e12fbc96a05718e91b8178c79`  
		Last Modified: Thu, 09 Oct 2025 00:39:26 GMT  
		Size: 21.8 KB (21838 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:d131290a9ce0dbca8afd0ca7eccb3f6a9b0ae888b264502d476dc14614041e55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:f6738e86b0ed9b830d3852034d68fc8e5ed28c19302676e9c4aade93876655ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111104282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c9334313caee17b0e8cb97a04a8370975d1bea689bac69ca4199ec34526d43`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:57 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:00:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:24 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Sat, 08 Nov 2025 18:31:24 GMT
WORKDIR /liquibase
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Sat, 08 Nov 2025 18:31:25 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LPM_VERSION=0.2.14
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Sat, 08 Nov 2025 18:31:25 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.version=5.0.1
# Sat, 08 Nov 2025 18:31:25 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Sat, 08 Nov 2025 18:31:33 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Sat, 08 Nov 2025 18:31:33 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 08 Nov 2025 18:31:33 GMT
ENV DOCKER_LIQUIBASE=true
# Sat, 08 Nov 2025 18:31:33 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Sat, 08 Nov 2025 18:31:33 GMT
COPY liquibase.docker.properties ./ # buildkit
# Sat, 08 Nov 2025 18:31:33 GMT
USER liquibase:liquibase
# Sat, 08 Nov 2025 18:31:33 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:33 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2efaf4f7327a471e1b969eaddc7e44e5ccae0df783fcaa48bf94864d07a0d`  
		Last Modified: Sat, 08 Nov 2025 18:00:21 GMT  
		Size: 16.2 MB (16150304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c0a6ab39aeac3774dd534c27427e0d533f07a637624ab254c6849bda796f16`  
		Last Modified: Sat, 08 Nov 2025 18:00:28 GMT  
		Size: 53.0 MB (52978483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f2a033ca8df84c1a3081f8ef917342b430ebdc1587bedf05eb381e45383ac`  
		Last Modified: Sat, 08 Nov 2025 18:00:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc3096c0eb2bbc9ac33b0cdb8552433f874659010096eb476cdd53f1aae60a3`  
		Last Modified: Sat, 08 Nov 2025 18:00:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ec9c66d679a5a359a749f0019dff70984dc88faf65d5a62a927fe6f5e6632b`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcde102a212eaaaa788081a690006cf06f20c71c03bfdc3758a1ac1a16f4070`  
		Last Modified: Sat, 08 Nov 2025 18:32:38 GMT  
		Size: 8.7 MB (8665799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab43f7991a91feea6744f920d4b991aaee1d5396fa65af6555c8ba54ac50822`  
		Last Modified: Sat, 08 Nov 2025 18:32:38 GMT  
		Size: 3.8 MB (3764497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9d9601a6c3c98ffe832710ca4908f8d1ce3abaaf8deaa9fbb00b64e816b8f0`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ef95f64c6859559af596f690f1df538381454b3abd54699bc22a754475eb3`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:8e1bb903070264aad87f5b99c58b3aa799700437f3fd80ffebf94fe31e4914d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211024646a67fcc63118663481f874d9e34eee6de3810701a6bb3fa344ca0d15`

```dockerfile
```

-	Layers:
	-	`sha256:a140fa9a97d37ef0ad5cbc391c7d29879e82a2033167838f00a90cde951dc6f7`  
		Last Modified: Sat, 08 Nov 2025 22:39:19 GMT  
		Size: 3.9 MB (3897733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ec2236c99a4fff57d018bc4a6f076dd332ed48b2a542ca474e15e1b22c9c90`  
		Last Modified: Sat, 08 Nov 2025 22:39:20 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:e64bcd0c6e92d848f680b661ae907d19ef2beccfa76dc790c8e0c1aed9e1448a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107713379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71373e531f1b834bfb621d16b8b53bc15994e8aa3ebc5d489b7dd89103379235`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:13 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:29:56 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Sat, 08 Nov 2025 18:29:56 GMT
WORKDIR /liquibase
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Sat, 08 Nov 2025 18:29:57 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LPM_VERSION=0.2.14
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Sat, 08 Nov 2025 18:29:57 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.version=5.0.1
# Sat, 08 Nov 2025 18:29:57 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Sat, 08 Nov 2025 18:30:06 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Sat, 08 Nov 2025 18:30:06 GMT
ENV LIQUIBASE_HOME=/liquibase
# Sat, 08 Nov 2025 18:30:06 GMT
ENV DOCKER_LIQUIBASE=true
# Sat, 08 Nov 2025 18:30:06 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Sat, 08 Nov 2025 18:30:06 GMT
COPY liquibase.docker.properties ./ # buildkit
# Sat, 08 Nov 2025 18:30:06 GMT
USER liquibase:liquibase
# Sat, 08 Nov 2025 18:30:06 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:06 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028993be8a76c7119b0d8ee582ec1146a4a9da89a2876287461de42112766642`  
		Last Modified: Sat, 08 Nov 2025 17:59:53 GMT  
		Size: 16.1 MB (16066196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf12991e52872631db4f5866423e61c9aa264b18e7b99735b58d5e9b7424ea`  
		Last Modified: Sat, 08 Nov 2025 17:59:52 GMT  
		Size: 52.1 MB (52148599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e39452ec2196b4a744bd1ec7029e928fad324f4e0aa146be26945045f2e628`  
		Last Modified: Sat, 08 Nov 2025 17:59:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c83d3140bc0663488b5277b96f30f09c76765775b653007c9573825d31d1e`  
		Last Modified: Sat, 08 Nov 2025 17:59:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b4c3c196182560757b22a9520cf0c88ea94e74859adcabb58de774fce32236`  
		Last Modified: Sat, 08 Nov 2025 18:30:56 GMT  
		Size: 4.3 KB (4329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90e20f94cb6a51e16b46807a43756804ae607659399e661ac07fb980474f4c0`  
		Last Modified: Sat, 08 Nov 2025 18:30:57 GMT  
		Size: 8.7 MB (8665799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cad52fc40c4fce263a8bad4f57afb1c45b0f151d6d925adf26787dd2195d21`  
		Last Modified: Sat, 08 Nov 2025 18:30:57 GMT  
		Size: 3.4 MB (3441276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12be07884b37532cb0a2c5076044f6ca7864584bbeda21ec5d847d7689702dcf`  
		Last Modified: Sat, 08 Nov 2025 18:30:56 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da02e982d759f0862a5a9db768b3c8afc70b9ccae7635034f8f703b69fbd55e`  
		Last Modified: Sat, 08 Nov 2025 18:30:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:448c5410dbbc733b552caf49f0c73ed72688ea61b680ab7a873e4d9611e9ddf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1541f58caec390696f2dd1cf9c1400fa04ff1af219b357d560d602624439d272`

```dockerfile
```

-	Layers:
	-	`sha256:6d9d6ab9f909b5eb6cf21a13cafd18b3c682487740ad261c726dd4c7027b95e5`  
		Last Modified: Sat, 08 Nov 2025 19:39:24 GMT  
		Size: 3.9 MB (3897401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8bb732e22e95ac82f737307760e992437650e16d2a35beb31d32ace08a5205`  
		Last Modified: Sat, 08 Nov 2025 19:39:25 GMT  
		Size: 24.4 KB (24445 bytes)  
		MIME: application/vnd.in-toto+json
