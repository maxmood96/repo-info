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
$ docker pull liquibase@sha256:e3049d29622fa418eb2642c7d93e87aaedab62791cd8b62f96cfe5b8d33f172c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0` - linux; amd64

```console
$ docker pull liquibase@sha256:e5ea908f9bec1c44423e19610c1f5ad41f789ba74aa46867e855808f3eda1c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111310042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae7d12aeb5480ea81e2e85198c405763b855b208fc045e2aa6f95fb675fa8d`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:03 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:10:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:41 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 01 Apr 2026 21:09:41 GMT
WORKDIR /liquibase
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 01 Apr 2026 21:09:42 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LPM_VERSION=0.2.14
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 01 Apr 2026 21:09:49 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 01 Apr 2026 21:09:49 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 01 Apr 2026 21:09:49 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 01 Apr 2026 21:09:49 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 01 Apr 2026 21:09:49 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 01 Apr 2026 21:09:49 GMT
USER liquibase:liquibase
# Wed, 01 Apr 2026 21:09:49 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:49 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedbe7a7f974cd5e22a8bfde6806ab9362ef702fffc0f695deb267c3d5559917`  
		Last Modified: Wed, 01 Apr 2026 20:10:19 GMT  
		Size: 16.1 MB (16149364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3804ba6bff73469147f6fae7c7fe225f067d6300d746c73b601d11ec86aadc95`  
		Last Modified: Wed, 01 Apr 2026 20:10:43 GMT  
		Size: 53.0 MB (52985551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37362c6be30a6b98c5fb295f72f8dc6d7e244f517ac8cdedbfd8ddbfc35f483d`  
		Last Modified: Wed, 01 Apr 2026 20:10:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4344daae9c653e41df744ff6dc2031ac59062111661991fff8856f0791bdea`  
		Last Modified: Wed, 01 Apr 2026 20:10:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d8e2252cdd5a7d0fb4bb876b5caa69b9f8664c1817125a784a0762ac2d4b64`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd321b0130d5beb905d1f43e8e0197aa7919cd4af2b85943efa2c97d4a83b44`  
		Last Modified: Wed, 01 Apr 2026 21:09:58 GMT  
		Size: 8.7 MB (8665798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17374b8fa4064aebcb05b5d3437278d57c3d9634da809dd1918246a07d0db419`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 3.8 MB (3764531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66de9fc499567375af872927ae1990dc395cac4e61cdb615c9ec1538b3f4e171`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12171062160e3149d8a9f43626f2f62ae985a7d11796584132e291d9bb6dc62c`  
		Last Modified: Wed, 01 Apr 2026 21:09:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:94dd11b356793be0761bd28d975649f8225a65baac92971eb48d8735ac93e4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fe285af99d2da68120c5aeb58c6cf698e76ac15407cd074ac85d6c8e90aaee`

```dockerfile
```

-	Layers:
	-	`sha256:d564fc6462936a96774efd15f144dc258f5bd2456894a177036ff8ac9a68853e`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 3.9 MB (3897747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13dee93addf4da8345eef94988ea759a6546c75b8198e2d10702444f78c14a00`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:0b0f326ba0cdf4b828e50cdde8163a91614e599c4c7ecb175e07a96412b06990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107951457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc313e27cbb17fcf2e3f116313d43dbbead18063cf462b5b565f15ba9be27b8c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:48 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:10:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:40 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 01 Apr 2026 21:09:40 GMT
WORKDIR /liquibase
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 01 Apr 2026 21:09:41 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LPM_VERSION=0.2.14
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 01 Apr 2026 21:09:51 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 01 Apr 2026 21:09:51 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 01 Apr 2026 21:09:51 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 01 Apr 2026 21:09:51 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 01 Apr 2026 21:09:51 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 01 Apr 2026 21:09:51 GMT
USER liquibase:liquibase
# Wed, 01 Apr 2026 21:09:51 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:51 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963beb3bb70b2cebe7d47d994eafcdb017e7b54e6384c981571029519a38ea81`  
		Last Modified: Wed, 01 Apr 2026 20:11:06 GMT  
		Size: 16.1 MB (16073461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd019c3adabdec1621320404cbcbf8000084b66cd60b8f5838a2d1e6f42702f`  
		Last Modified: Wed, 01 Apr 2026 20:11:09 GMT  
		Size: 52.2 MB (52155647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aa479ab8defbc52e300a4fedcb30c0e90cd6c53ff7f31a0855de60e65ffb7d`  
		Last Modified: Wed, 01 Apr 2026 20:11:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d407e998bf208d5b7a1aeb7f7ee16ecc1d4a6dd5b119948e88ef59763bcc83d1`  
		Last Modified: Wed, 01 Apr 2026 20:11:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853f9e3350bbe659d68111ed34ceb27cdb2202a55301af9eff9ef3a54ad334b7`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee158e567883bf3f83da4ff78fed593ca5243277dfd4f2ef795862b4c2c324e6`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 8.7 MB (8665802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917a03aa81c36409b5b6db68afb914809615c9473cef43aeb934e9a8460527b2`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 3.4 MB (3441218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17663e2374dea500562e4773ecb0d295cd0619d6c9010e7c850f7f9f29096d7e`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65a45e4e0db49b8ff56377c6030b193beb5cc5181b2ecf4b18936c161539148`  
		Last Modified: Wed, 01 Apr 2026 21:10:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:d522a7ff05811c7e0e6419753d7e00597d78458718f1f8f971e633f9a20a786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28239c7a57566a02523f6ccc8c0fe929a84df36491f3e12cb40691987f040b4`

```dockerfile
```

-	Layers:
	-	`sha256:3d54db257709c364b934d444229ea0481b0a6f3969f25e50cab96d6f680e5674`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 3.9 MB (3897415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f5698d84b23cbf60737808bcb26b69dcc65c0a81f5e406e60087eaea9e0544`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 24.4 KB (24444 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0-alpine`

```console
$ docker pull liquibase@sha256:55e874d6009083f80ed330d7df32a10191f24c5b701761c7f14a6ab79e18e089
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:1651b75ef5be4a46e94ec6f80812f83cf07047abcb332eec98f86aa9d404212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84052800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f02f0f58f9fc7177762cb87d9c44e9dabb0952443add6bb4794341e6201ddff`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:28:16 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:28:18 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:28:19 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:28:20 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:28:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:28:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:28:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a517c94efd15ae4380810eb3ef0c6bbc1cbe4f6a169b4c3b262c3e2ecb0597d4`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ba6c13ed2b369098495155588f501358969c8078880c90eac391faa8cd`  
		Last Modified: Wed, 28 Jan 2026 03:28:36 GMT  
		Size: 67.9 MB (67873060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb37bb887be4af24ea7f347024732b5ea81f7ee300b6e58e534927820447afd`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 8.7 MB (8688932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56a9f2195435c4b4e6ed9d8ce9c116f0b376fd272964557424bd2d4142e40a`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 3.7 MB (3683370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8dac592986c035ba295c431c9f5e7e2ddd59db473eb3abe92647071024c83`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7c304a5473a660a9f08bf95fd628809c3d8cc5b12990b3d8b8e454e452fbcf`  
		Last Modified: Wed, 28 Jan 2026 03:28:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:48c09dded8cd9e167bead9b170c733d1c723d54d9b92af760d01650b42a0f7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 KB (380330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4131dac041c8c2a8ddc01f403267f72ce6cb45d2984fe8c35e6454e14314fa1`

```dockerfile
```

-	Layers:
	-	`sha256:bf36103b79098cd70f39bb2215e8ae56168008ab33d8bf62d0934d71ddf95882`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 358.7 KB (358672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8eee20485eb91c9d97fde6d2c11fdcb7df7b8856cc0f37e1fef9ab75eda0ddd`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:0a601fa9413305912b4bb989be606c93985f4cc0053ffa6cdf282857bfad39bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83061766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bf042758b6e54ce231f76afecbb51959dad218a3c6f102a136d5330acd4401`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:44 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:15:49 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:15:50 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:15:50 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:50 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e305c1df01b60cf83f099c190ced97031f3ffd5df0a427176d17d785594c2ed`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2f425aad41d745ff2356f728973d218620e3fc17765fd4860b11351d502880`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 66.9 MB (66871125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c00c7bdafc89ac06f31b791ee9164b9c4422c2eb65358dbdcd21c4874f81b`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 8.7 MB (8688881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11bcc129589226fcbe9cb6f0501bb9609640700da044edecbeaf01da1b1ab29`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 3.4 MB (3359669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd913dbb84c3cecaaad1148b7a3cef53b9a46c5566f8e2bcd32c2995f6131f50`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a315e3d5ef6dbe812f97f820051b1cb54ae61c4f58918fc4949299ea1a7212a`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:ce8477b08b0b8be7c82f3a41b5ea7c109a305f9070925d944cb09ff42c5dcc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 KB (379714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb7a885191f6817558260cc1fbf52e9a2beb1c7e1409d9fe9ac3e590e11c326`

```dockerfile
```

-	Layers:
	-	`sha256:48678c606e0933835ea00ac8f084324dd20f5094cc0057f0049c6907650a995e`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 357.9 KB (357919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15029936ae049086763018e19c62ee4a2816adec5b6c262f9ded2ffdf9bd14d7`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.1`

```console
$ docker pull liquibase@sha256:e3049d29622fa418eb2642c7d93e87aaedab62791cd8b62f96cfe5b8d33f172c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1` - linux; amd64

```console
$ docker pull liquibase@sha256:e5ea908f9bec1c44423e19610c1f5ad41f789ba74aa46867e855808f3eda1c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111310042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae7d12aeb5480ea81e2e85198c405763b855b208fc045e2aa6f95fb675fa8d`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:03 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:10:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:41 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 01 Apr 2026 21:09:41 GMT
WORKDIR /liquibase
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 01 Apr 2026 21:09:42 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LPM_VERSION=0.2.14
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 01 Apr 2026 21:09:49 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 01 Apr 2026 21:09:49 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 01 Apr 2026 21:09:49 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 01 Apr 2026 21:09:49 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 01 Apr 2026 21:09:49 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 01 Apr 2026 21:09:49 GMT
USER liquibase:liquibase
# Wed, 01 Apr 2026 21:09:49 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:49 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedbe7a7f974cd5e22a8bfde6806ab9362ef702fffc0f695deb267c3d5559917`  
		Last Modified: Wed, 01 Apr 2026 20:10:19 GMT  
		Size: 16.1 MB (16149364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3804ba6bff73469147f6fae7c7fe225f067d6300d746c73b601d11ec86aadc95`  
		Last Modified: Wed, 01 Apr 2026 20:10:43 GMT  
		Size: 53.0 MB (52985551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37362c6be30a6b98c5fb295f72f8dc6d7e244f517ac8cdedbfd8ddbfc35f483d`  
		Last Modified: Wed, 01 Apr 2026 20:10:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4344daae9c653e41df744ff6dc2031ac59062111661991fff8856f0791bdea`  
		Last Modified: Wed, 01 Apr 2026 20:10:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d8e2252cdd5a7d0fb4bb876b5caa69b9f8664c1817125a784a0762ac2d4b64`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd321b0130d5beb905d1f43e8e0197aa7919cd4af2b85943efa2c97d4a83b44`  
		Last Modified: Wed, 01 Apr 2026 21:09:58 GMT  
		Size: 8.7 MB (8665798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17374b8fa4064aebcb05b5d3437278d57c3d9634da809dd1918246a07d0db419`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 3.8 MB (3764531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66de9fc499567375af872927ae1990dc395cac4e61cdb615c9ec1538b3f4e171`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12171062160e3149d8a9f43626f2f62ae985a7d11796584132e291d9bb6dc62c`  
		Last Modified: Wed, 01 Apr 2026 21:09:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:94dd11b356793be0761bd28d975649f8225a65baac92971eb48d8735ac93e4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fe285af99d2da68120c5aeb58c6cf698e76ac15407cd074ac85d6c8e90aaee`

```dockerfile
```

-	Layers:
	-	`sha256:d564fc6462936a96774efd15f144dc258f5bd2456894a177036ff8ac9a68853e`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 3.9 MB (3897747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13dee93addf4da8345eef94988ea759a6546c75b8198e2d10702444f78c14a00`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:0b0f326ba0cdf4b828e50cdde8163a91614e599c4c7ecb175e07a96412b06990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107951457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc313e27cbb17fcf2e3f116313d43dbbead18063cf462b5b565f15ba9be27b8c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:48 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:10:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:40 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 01 Apr 2026 21:09:40 GMT
WORKDIR /liquibase
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 01 Apr 2026 21:09:41 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LPM_VERSION=0.2.14
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 01 Apr 2026 21:09:51 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 01 Apr 2026 21:09:51 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 01 Apr 2026 21:09:51 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 01 Apr 2026 21:09:51 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 01 Apr 2026 21:09:51 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 01 Apr 2026 21:09:51 GMT
USER liquibase:liquibase
# Wed, 01 Apr 2026 21:09:51 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:51 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963beb3bb70b2cebe7d47d994eafcdb017e7b54e6384c981571029519a38ea81`  
		Last Modified: Wed, 01 Apr 2026 20:11:06 GMT  
		Size: 16.1 MB (16073461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd019c3adabdec1621320404cbcbf8000084b66cd60b8f5838a2d1e6f42702f`  
		Last Modified: Wed, 01 Apr 2026 20:11:09 GMT  
		Size: 52.2 MB (52155647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aa479ab8defbc52e300a4fedcb30c0e90cd6c53ff7f31a0855de60e65ffb7d`  
		Last Modified: Wed, 01 Apr 2026 20:11:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d407e998bf208d5b7a1aeb7f7ee16ecc1d4a6dd5b119948e88ef59763bcc83d1`  
		Last Modified: Wed, 01 Apr 2026 20:11:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853f9e3350bbe659d68111ed34ceb27cdb2202a55301af9eff9ef3a54ad334b7`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee158e567883bf3f83da4ff78fed593ca5243277dfd4f2ef795862b4c2c324e6`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 8.7 MB (8665802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917a03aa81c36409b5b6db68afb914809615c9473cef43aeb934e9a8460527b2`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 3.4 MB (3441218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17663e2374dea500562e4773ecb0d295cd0619d6c9010e7c850f7f9f29096d7e`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65a45e4e0db49b8ff56377c6030b193beb5cc5181b2ecf4b18936c161539148`  
		Last Modified: Wed, 01 Apr 2026 21:10:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:d522a7ff05811c7e0e6419753d7e00597d78458718f1f8f971e633f9a20a786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28239c7a57566a02523f6ccc8c0fe929a84df36491f3e12cb40691987f040b4`

```dockerfile
```

-	Layers:
	-	`sha256:3d54db257709c364b934d444229ea0481b0a6f3969f25e50cab96d6f680e5674`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 3.9 MB (3897415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f5698d84b23cbf60737808bcb26b69dcc65c0a81f5e406e60087eaea9e0544`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 24.4 KB (24444 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.1-alpine`

```console
$ docker pull liquibase@sha256:55e874d6009083f80ed330d7df32a10191f24c5b701761c7f14a6ab79e18e089
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:1651b75ef5be4a46e94ec6f80812f83cf07047abcb332eec98f86aa9d404212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84052800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f02f0f58f9fc7177762cb87d9c44e9dabb0952443add6bb4794341e6201ddff`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:28:16 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:28:18 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:28:19 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:28:20 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:28:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:28:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:28:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a517c94efd15ae4380810eb3ef0c6bbc1cbe4f6a169b4c3b262c3e2ecb0597d4`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ba6c13ed2b369098495155588f501358969c8078880c90eac391faa8cd`  
		Last Modified: Wed, 28 Jan 2026 03:28:36 GMT  
		Size: 67.9 MB (67873060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb37bb887be4af24ea7f347024732b5ea81f7ee300b6e58e534927820447afd`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 8.7 MB (8688932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56a9f2195435c4b4e6ed9d8ce9c116f0b376fd272964557424bd2d4142e40a`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 3.7 MB (3683370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8dac592986c035ba295c431c9f5e7e2ddd59db473eb3abe92647071024c83`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7c304a5473a660a9f08bf95fd628809c3d8cc5b12990b3d8b8e454e452fbcf`  
		Last Modified: Wed, 28 Jan 2026 03:28:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:48c09dded8cd9e167bead9b170c733d1c723d54d9b92af760d01650b42a0f7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 KB (380330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4131dac041c8c2a8ddc01f403267f72ce6cb45d2984fe8c35e6454e14314fa1`

```dockerfile
```

-	Layers:
	-	`sha256:bf36103b79098cd70f39bb2215e8ae56168008ab33d8bf62d0934d71ddf95882`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 358.7 KB (358672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8eee20485eb91c9d97fde6d2c11fdcb7df7b8856cc0f37e1fef9ab75eda0ddd`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:0a601fa9413305912b4bb989be606c93985f4cc0053ffa6cdf282857bfad39bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83061766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bf042758b6e54ce231f76afecbb51959dad218a3c6f102a136d5330acd4401`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:44 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:15:49 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:15:50 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:15:50 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:50 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e305c1df01b60cf83f099c190ced97031f3ffd5df0a427176d17d785594c2ed`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2f425aad41d745ff2356f728973d218620e3fc17765fd4860b11351d502880`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 66.9 MB (66871125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c00c7bdafc89ac06f31b791ee9164b9c4422c2eb65358dbdcd21c4874f81b`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 8.7 MB (8688881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11bcc129589226fcbe9cb6f0501bb9609640700da044edecbeaf01da1b1ab29`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 3.4 MB (3359669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd913dbb84c3cecaaad1148b7a3cef53b9a46c5566f8e2bcd32c2995f6131f50`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a315e3d5ef6dbe812f97f820051b1cb54ae61c4f58918fc4949299ea1a7212a`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:ce8477b08b0b8be7c82f3a41b5ea7c109a305f9070925d944cb09ff42c5dcc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 KB (379714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb7a885191f6817558260cc1fbf52e9a2beb1c7e1409d9fe9ac3e590e11c326`

```dockerfile
```

-	Layers:
	-	`sha256:48678c606e0933835ea00ac8f084324dd20f5094cc0057f0049c6907650a995e`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 357.9 KB (357919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15029936ae049086763018e19c62ee4a2816adec5b6c262f9ded2ffdf9bd14d7`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:55e874d6009083f80ed330d7df32a10191f24c5b701761c7f14a6ab79e18e089
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:1651b75ef5be4a46e94ec6f80812f83cf07047abcb332eec98f86aa9d404212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84052800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f02f0f58f9fc7177762cb87d9c44e9dabb0952443add6bb4794341e6201ddff`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:28:16 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:28:18 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:28:19 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:28:20 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:28:20 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:28:20 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:28:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:28:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:28:21 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:28:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:28:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a517c94efd15ae4380810eb3ef0c6bbc1cbe4f6a169b4c3b262c3e2ecb0597d4`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfff5ba6c13ed2b369098495155588f501358969c8078880c90eac391faa8cd`  
		Last Modified: Wed, 28 Jan 2026 03:28:36 GMT  
		Size: 67.9 MB (67873060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb37bb887be4af24ea7f347024732b5ea81f7ee300b6e58e534927820447afd`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 8.7 MB (8688932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56a9f2195435c4b4e6ed9d8ce9c116f0b376fd272964557424bd2d4142e40a`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 3.7 MB (3683370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8dac592986c035ba295c431c9f5e7e2ddd59db473eb3abe92647071024c83`  
		Last Modified: Wed, 28 Jan 2026 03:28:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7c304a5473a660a9f08bf95fd628809c3d8cc5b12990b3d8b8e454e452fbcf`  
		Last Modified: Wed, 28 Jan 2026 03:28:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:48c09dded8cd9e167bead9b170c733d1c723d54d9b92af760d01650b42a0f7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 KB (380330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4131dac041c8c2a8ddc01f403267f72ce6cb45d2984fe8c35e6454e14314fa1`

```dockerfile
```

-	Layers:
	-	`sha256:bf36103b79098cd70f39bb2215e8ae56168008ab33d8bf62d0934d71ddf95882`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 358.7 KB (358672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8eee20485eb91c9d97fde6d2c11fdcb7df7b8856cc0f37e1fef9ab75eda0ddd`  
		Last Modified: Wed, 28 Jan 2026 03:28:33 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:0a601fa9413305912b4bb989be606c93985f4cc0053ffa6cdf282857bfad39bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83061766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bf042758b6e54ce231f76afecbb51959dad218a3c6f102a136d5330acd4401`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:44 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Wed, 28 Jan 2026 03:15:47 GMT
WORKDIR /liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 28 Jan 2026 03:15:49 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_VERSION=0.2.14
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 28 Jan 2026 03:15:49 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 28 Jan 2026 03:15:49 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 28 Jan 2026 03:15:50 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 28 Jan 2026 03:15:50 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 28 Jan 2026 03:15:50 GMT
USER liquibase:liquibase
# Wed, 28 Jan 2026 03:15:50 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:50 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e305c1df01b60cf83f099c190ced97031f3ffd5df0a427176d17d785594c2ed`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2f425aad41d745ff2356f728973d218620e3fc17765fd4860b11351d502880`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 66.9 MB (66871125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c00c7bdafc89ac06f31b791ee9164b9c4422c2eb65358dbdcd21c4874f81b`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 8.7 MB (8688881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11bcc129589226fcbe9cb6f0501bb9609640700da044edecbeaf01da1b1ab29`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 3.4 MB (3359669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd913dbb84c3cecaaad1148b7a3cef53b9a46c5566f8e2bcd32c2995f6131f50`  
		Last Modified: Wed, 28 Jan 2026 03:16:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a315e3d5ef6dbe812f97f820051b1cb54ae61c4f58918fc4949299ea1a7212a`  
		Last Modified: Wed, 28 Jan 2026 03:16:04 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:ce8477b08b0b8be7c82f3a41b5ea7c109a305f9070925d944cb09ff42c5dcc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 KB (379714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb7a885191f6817558260cc1fbf52e9a2beb1c7e1409d9fe9ac3e590e11c326`

```dockerfile
```

-	Layers:
	-	`sha256:48678c606e0933835ea00ac8f084324dd20f5094cc0057f0049c6907650a995e`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 357.9 KB (357919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15029936ae049086763018e19c62ee4a2816adec5b6c262f9ded2ffdf9bd14d7`  
		Last Modified: Wed, 28 Jan 2026 03:16:02 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:e3049d29622fa418eb2642c7d93e87aaedab62791cd8b62f96cfe5b8d33f172c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:e5ea908f9bec1c44423e19610c1f5ad41f789ba74aa46867e855808f3eda1c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111310042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ae7d12aeb5480ea81e2e85198c405763b855b208fc045e2aa6f95fb675fa8d`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:03 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:10:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:41 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 01 Apr 2026 21:09:41 GMT
WORKDIR /liquibase
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 01 Apr 2026 21:09:42 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LPM_VERSION=0.2.14
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 01 Apr 2026 21:09:42 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 01 Apr 2026 21:09:42 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 01 Apr 2026 21:09:49 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 01 Apr 2026 21:09:49 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 01 Apr 2026 21:09:49 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 01 Apr 2026 21:09:49 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 01 Apr 2026 21:09:49 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 01 Apr 2026 21:09:49 GMT
USER liquibase:liquibase
# Wed, 01 Apr 2026 21:09:49 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:49 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedbe7a7f974cd5e22a8bfde6806ab9362ef702fffc0f695deb267c3d5559917`  
		Last Modified: Wed, 01 Apr 2026 20:10:19 GMT  
		Size: 16.1 MB (16149364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3804ba6bff73469147f6fae7c7fe225f067d6300d746c73b601d11ec86aadc95`  
		Last Modified: Wed, 01 Apr 2026 20:10:43 GMT  
		Size: 53.0 MB (52985551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37362c6be30a6b98c5fb295f72f8dc6d7e244f517ac8cdedbfd8ddbfc35f483d`  
		Last Modified: Wed, 01 Apr 2026 20:10:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4344daae9c653e41df744ff6dc2031ac59062111661991fff8856f0791bdea`  
		Last Modified: Wed, 01 Apr 2026 20:10:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d8e2252cdd5a7d0fb4bb876b5caa69b9f8664c1817125a784a0762ac2d4b64`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd321b0130d5beb905d1f43e8e0197aa7919cd4af2b85943efa2c97d4a83b44`  
		Last Modified: Wed, 01 Apr 2026 21:09:58 GMT  
		Size: 8.7 MB (8665798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17374b8fa4064aebcb05b5d3437278d57c3d9634da809dd1918246a07d0db419`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 3.8 MB (3764531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66de9fc499567375af872927ae1990dc395cac4e61cdb615c9ec1538b3f4e171`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12171062160e3149d8a9f43626f2f62ae985a7d11796584132e291d9bb6dc62c`  
		Last Modified: Wed, 01 Apr 2026 21:09:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:94dd11b356793be0761bd28d975649f8225a65baac92971eb48d8735ac93e4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fe285af99d2da68120c5aeb58c6cf698e76ac15407cd074ac85d6c8e90aaee`

```dockerfile
```

-	Layers:
	-	`sha256:d564fc6462936a96774efd15f144dc258f5bd2456894a177036ff8ac9a68853e`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 3.9 MB (3897747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13dee93addf4da8345eef94988ea759a6546c75b8198e2d10702444f78c14a00`  
		Last Modified: Wed, 01 Apr 2026 21:09:57 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:0b0f326ba0cdf4b828e50cdde8163a91614e599c4c7ecb175e07a96412b06990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107951457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc313e27cbb17fcf2e3f116313d43dbbead18063cf462b5b565f15ba9be27b8c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:48 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:10:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:40 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Wed, 01 Apr 2026 21:09:40 GMT
WORKDIR /liquibase
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Wed, 01 Apr 2026 21:09:41 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LPM_VERSION=0.2.14
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Wed, 01 Apr 2026 21:09:41 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.version=5.0.1
# Wed, 01 Apr 2026 21:09:41 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Wed, 01 Apr 2026 21:09:51 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Wed, 01 Apr 2026 21:09:51 GMT
ENV LIQUIBASE_HOME=/liquibase
# Wed, 01 Apr 2026 21:09:51 GMT
ENV DOCKER_LIQUIBASE=true
# Wed, 01 Apr 2026 21:09:51 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Wed, 01 Apr 2026 21:09:51 GMT
COPY liquibase.docker.properties ./ # buildkit
# Wed, 01 Apr 2026 21:09:51 GMT
USER liquibase:liquibase
# Wed, 01 Apr 2026 21:09:51 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:09:51 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963beb3bb70b2cebe7d47d994eafcdb017e7b54e6384c981571029519a38ea81`  
		Last Modified: Wed, 01 Apr 2026 20:11:06 GMT  
		Size: 16.1 MB (16073461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd019c3adabdec1621320404cbcbf8000084b66cd60b8f5838a2d1e6f42702f`  
		Last Modified: Wed, 01 Apr 2026 20:11:09 GMT  
		Size: 52.2 MB (52155647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aa479ab8defbc52e300a4fedcb30c0e90cd6c53ff7f31a0855de60e65ffb7d`  
		Last Modified: Wed, 01 Apr 2026 20:11:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d407e998bf208d5b7a1aeb7f7ee16ecc1d4a6dd5b119948e88ef59763bcc83d1`  
		Last Modified: Wed, 01 Apr 2026 20:11:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853f9e3350bbe659d68111ed34ceb27cdb2202a55301af9eff9ef3a54ad334b7`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee158e567883bf3f83da4ff78fed593ca5243277dfd4f2ef795862b4c2c324e6`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 8.7 MB (8665802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917a03aa81c36409b5b6db68afb914809615c9473cef43aeb934e9a8460527b2`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 3.4 MB (3441218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17663e2374dea500562e4773ecb0d295cd0619d6c9010e7c850f7f9f29096d7e`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65a45e4e0db49b8ff56377c6030b193beb5cc5181b2ecf4b18936c161539148`  
		Last Modified: Wed, 01 Apr 2026 21:10:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:d522a7ff05811c7e0e6419753d7e00597d78458718f1f8f971e633f9a20a786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28239c7a57566a02523f6ccc8c0fe929a84df36491f3e12cb40691987f040b4`

```dockerfile
```

-	Layers:
	-	`sha256:3d54db257709c364b934d444229ea0481b0a6f3969f25e50cab96d6f680e5674`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 3.9 MB (3897415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f5698d84b23cbf60737808bcb26b69dcc65c0a81f5e406e60087eaea9e0544`  
		Last Modified: Wed, 01 Apr 2026 21:10:05 GMT  
		Size: 24.4 KB (24444 bytes)  
		MIME: application/vnd.in-toto+json
