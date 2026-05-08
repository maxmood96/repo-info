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
$ docker pull liquibase@sha256:ea0a5d5914f8526e5a0d49c3b7be480ea0d4d48c546b4fdfb8c2ce2059e82a2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0` - linux; amd64

```console
$ docker pull liquibase@sha256:c8cf85eafe11714eebb0ce4eb530fa4edcd37c6a16ff98b03cf9c6dc751b3b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111450676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4594c5be7feda4877740b1bbcc96712352436ae597674a5068bd6c2ae0f99012`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:39 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:16:01 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 08 May 2026 00:16:01 GMT
WORKDIR /liquibase
# Fri, 08 May 2026 00:16:02 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 08 May 2026 00:16:02 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 08 May 2026 00:16:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 08 May 2026 00:16:02 GMT
ARG LPM_VERSION=0.2.14
# Fri, 08 May 2026 00:16:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 08 May 2026 00:16:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 08 May 2026 00:16:08 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 08 May 2026 00:16:08 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 08 May 2026 00:16:08 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 08 May 2026 00:16:08 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 08 May 2026 00:16:09 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 08 May 2026 00:16:09 GMT
USER liquibase:liquibase
# Fri, 08 May 2026 00:16:09 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 08 May 2026 00:16:09 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f3bb8db2f4dc74d10969086150cb5462adac4d48009d71e48fe1ddf091dbea`  
		Last Modified: Fri, 08 May 2026 00:00:55 GMT  
		Size: 16.2 MB (16152648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0b62ebdf15bee16664fcacbb1c997bab64334377b27819ebe34754a9612343`  
		Last Modified: Fri, 08 May 2026 00:00:56 GMT  
		Size: 53.1 MB (53122853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95479e5f9bc5335e52cd4c9ef213b49a792113e34700e87b77feede68b30d8`  
		Last Modified: Fri, 08 May 2026 00:00:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c913227527c934bbe224166757603d424752d6eaae314b0141b34f9d843b431f`  
		Last Modified: Fri, 08 May 2026 00:00:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337956894102248449362abf51c0c81ca53147049154281664592f42e33000f4`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bfea534fc9680f54e296a39f8dd00fd002463feca8e6c8b2d05e3a9266a6e6`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 8.7 MB (8665800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6c9575fd54901bfff0784d808e3da4ad2dfb6f9b95cb9453d744357989336f`  
		Last Modified: Fri, 08 May 2026 00:16:18 GMT  
		Size: 3.8 MB (3764496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080e64a73cd350bd2b42efbfb003a597c5f1463ea19f5827e3fdf426bd0288a5`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7197048795b6c6afeef9c47dd4b6a137c09caf02759258903734f570c60aa6b`  
		Last Modified: Fri, 08 May 2026 00:16:18 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:b88f9df964b4d4f26b4044c01d08e5c805e67b4c50ef4010dc7365f368233786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167fa86e36ceaabb302800ee5b3389b73d07a697e8297020bb522632f16f14b4`

```dockerfile
```

-	Layers:
	-	`sha256:2a7c7f115162ec03602cb83c5b79db63dff22fa800d50150183495768c025a87`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 3.9 MB (3898374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c53bb8992f4ee5c00c18bdcb7dd218537341c9f8c0bdd466fe28c4ab9c2ffe3`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 24.3 KB (24326 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:7dcbb0c94b489adbd7689f5dec11e3cbccf6857f9d5ca873c77c99a21b97f219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108113224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2641e7feaa77c230db1bfda73a063c689a93a49c76faac2ca118d7209778ef`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:04 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:18:18 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 08 May 2026 00:18:18 GMT
WORKDIR /liquibase
# Fri, 08 May 2026 00:18:19 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 08 May 2026 00:18:19 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 08 May 2026 00:18:19 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 08 May 2026 00:18:19 GMT
ARG LPM_VERSION=0.2.14
# Fri, 08 May 2026 00:18:19 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 08 May 2026 00:18:19 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 08 May 2026 00:18:28 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 08 May 2026 00:18:28 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 08 May 2026 00:18:28 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 08 May 2026 00:18:28 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 08 May 2026 00:18:28 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 08 May 2026 00:18:28 GMT
USER liquibase:liquibase
# Fri, 08 May 2026 00:18:28 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 08 May 2026 00:18:28 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544d22e194278e44be8a69ea7eb1ae3c241a250596adb5ef0785760214ebbddc`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 16.1 MB (16076301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b207660b0f3fb6077de423783c55a3f8e3878d3e29341e2317c5d164f769bbf`  
		Last Modified: Fri, 08 May 2026 00:00:24 GMT  
		Size: 52.3 MB (52314951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9519bf6f9e2bb2bc542725464302c037e9c0c4a1a7a166696c1f95af55c60a99`  
		Last Modified: Fri, 08 May 2026 00:00:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a14ff53ff544f36049ac528a1743609b508d2b29507213a536e2191570dcab0`  
		Last Modified: Fri, 08 May 2026 00:00:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586786e0c705112eab0c01dd9f84af134a01ddeaf80c9ff5b281a1156794bb5f`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dda736a8158ff2fff6271b8757bf17aef48f2500940a99a753ee30a5f1c3769`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 8.7 MB (8665802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75373fcf51c8772e125c08402cf45741b61f12ce95c6b5c96fffc46a68d5a81`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 3.4 MB (3441238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d74abc7d1c1d4bae3e428da2121d24e5ee566ae9680c5d83a649690f3f50f7`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d4e7ee955eb4e18331621739c50c7fd2ab68a56fd4504776078eeb1bdcb1c5`  
		Last Modified: Fri, 08 May 2026 00:18:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:a8adb59546f1b9172f4a76c75f3796fcfdb5522dd18b33d8ad754b69da740eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf886df064cf0ee7d8bf6910b67a5ef295a4e14e4800a0cc6090339aeb04978`

```dockerfile
```

-	Layers:
	-	`sha256:8e51f5590e2ed306bc4b44dcda7c508e1523e957b2038b946e0a0a379c6bf012`  
		Last Modified: Fri, 08 May 2026 00:18:37 GMT  
		Size: 3.9 MB (3898042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f744c614b2c1b223f23f08687a22ef52a198e1be51bdbbcb423463edcdbe9693`  
		Last Modified: Fri, 08 May 2026 00:18:35 GMT  
		Size: 24.4 KB (24448 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0-alpine`

```console
$ docker pull liquibase@sha256:b131a24527add4d4eadc3300aa5cca684aa60abcd734b8d14d4a5c33b169b48b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:ac3e7f22a1f63434bec4e9ac9a459c3d14ff5fbf5b4cf23c41aaa15c8646c35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84056139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735cc69d2a472f1a3213f884cf38c27e7f07f9e006723d24b254987a2fc4c687`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:11 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:30:15 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:30:16 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:30:16 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:16 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c968b03a929ffeffc74e342fa376b3edf03837491ffc31b33bf6355c7e7a7`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b8a26d38c62ddc3835ccdd169cdda87af0f6fc420b7a65a9ddd9f3321ca1a2`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 67.9 MB (67873148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f7f520ce551a37b7e676a5e609d9729695d8ce07c806c1e101c9f205fecf03`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 8.7 MB (8688923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eea34866b5479ef311e6f9062d31c5e6c8a3e9a51dbaf8a25c64f65f673223`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 3.7 MB (3683310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa91b0bcf56568c9049861b5321c46085544a6631527bdefdb84c18a6623fae`  
		Last Modified: Fri, 17 Apr 2026 00:30:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c03822eba8e0cf95dce574baa878c2167415ad48eef1ccbae83246ea874b9ed`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:d088b7b55f51985159b6fe32611b0b4ebc925d08146919b22dc42fa7cd35dfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2dd6a4bb49d474fcadd1abd2f52dc79ca67b31b11a96c5a34f239b5f7893db`

```dockerfile
```

-	Layers:
	-	`sha256:f2156f2fcd7c800b311863e493b109f04e64f083639871cd2b5efce1f17640f3`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 358.0 KB (357987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f79eec151e7ce7c7347244c9c8bfd7431205e45e6b30fa7e98e27e95e0f10e`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:02764df374a1709ff23d3a5dcdc44587ce282ec941977e0ca367393400d4dcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83068134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e817e3c8378838c704e6f2db9767c81860a27f181249cb9e44be5299293faf43`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:31:15 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:31:17 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:31:18 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:31:19 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:31:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:31:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:31:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831166d40df22727a0f749606435ab6a4409084cb7202d34b8b35ccd2fd53ea3`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca45e9539c13dc3120e4487c5eb9306e5662fa360caef114c284f51f1f4f719`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 66.9 MB (66875198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a208d911ef09d8f8a6d13581c531ccc60d996bc210563f23f78e5861586d2`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 8.7 MB (8688840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b5ab7263f6d6b43a369410afbf518ea077ad4e76614e0b52ce51e89eaa9cb7`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 3.4 MB (3359632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be70c70dd84b0d04d247753d188bb7b592163f4fa2eca01b98d762f8d41963b5`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec2acdb9ae64468ca511183e0e8d93e60650516f7ea7bb68d7593fa5a610c9b`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:e3b85712d2657fcb95286ea159735ef6569569f9ddf0c378609ca2a5a9b461a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 KB (379029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab59b0f660b749ad5d77d3e747d5e622c3a40f4a290033d443b1cde84a3b8075`

```dockerfile
```

-	Layers:
	-	`sha256:2d73bc84012845f7b7fc5b6f5675adbae3ba5b0e44ba23b940acbcf56b91f5c2`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 357.2 KB (357234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd48a19d885fdd36c300257a8e06f61a3d7d772787a3409329468d2924df5deb`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.1`

```console
$ docker pull liquibase@sha256:ea0a5d5914f8526e5a0d49c3b7be480ea0d4d48c546b4fdfb8c2ce2059e82a2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1` - linux; amd64

```console
$ docker pull liquibase@sha256:c8cf85eafe11714eebb0ce4eb530fa4edcd37c6a16ff98b03cf9c6dc751b3b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111450676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4594c5be7feda4877740b1bbcc96712352436ae597674a5068bd6c2ae0f99012`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:39 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:16:01 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 08 May 2026 00:16:01 GMT
WORKDIR /liquibase
# Fri, 08 May 2026 00:16:02 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 08 May 2026 00:16:02 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 08 May 2026 00:16:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 08 May 2026 00:16:02 GMT
ARG LPM_VERSION=0.2.14
# Fri, 08 May 2026 00:16:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 08 May 2026 00:16:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 08 May 2026 00:16:08 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 08 May 2026 00:16:08 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 08 May 2026 00:16:08 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 08 May 2026 00:16:08 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 08 May 2026 00:16:09 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 08 May 2026 00:16:09 GMT
USER liquibase:liquibase
# Fri, 08 May 2026 00:16:09 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 08 May 2026 00:16:09 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f3bb8db2f4dc74d10969086150cb5462adac4d48009d71e48fe1ddf091dbea`  
		Last Modified: Fri, 08 May 2026 00:00:55 GMT  
		Size: 16.2 MB (16152648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0b62ebdf15bee16664fcacbb1c997bab64334377b27819ebe34754a9612343`  
		Last Modified: Fri, 08 May 2026 00:00:56 GMT  
		Size: 53.1 MB (53122853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95479e5f9bc5335e52cd4c9ef213b49a792113e34700e87b77feede68b30d8`  
		Last Modified: Fri, 08 May 2026 00:00:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c913227527c934bbe224166757603d424752d6eaae314b0141b34f9d843b431f`  
		Last Modified: Fri, 08 May 2026 00:00:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337956894102248449362abf51c0c81ca53147049154281664592f42e33000f4`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bfea534fc9680f54e296a39f8dd00fd002463feca8e6c8b2d05e3a9266a6e6`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 8.7 MB (8665800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6c9575fd54901bfff0784d808e3da4ad2dfb6f9b95cb9453d744357989336f`  
		Last Modified: Fri, 08 May 2026 00:16:18 GMT  
		Size: 3.8 MB (3764496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080e64a73cd350bd2b42efbfb003a597c5f1463ea19f5827e3fdf426bd0288a5`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7197048795b6c6afeef9c47dd4b6a137c09caf02759258903734f570c60aa6b`  
		Last Modified: Fri, 08 May 2026 00:16:18 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:b88f9df964b4d4f26b4044c01d08e5c805e67b4c50ef4010dc7365f368233786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167fa86e36ceaabb302800ee5b3389b73d07a697e8297020bb522632f16f14b4`

```dockerfile
```

-	Layers:
	-	`sha256:2a7c7f115162ec03602cb83c5b79db63dff22fa800d50150183495768c025a87`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 3.9 MB (3898374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c53bb8992f4ee5c00c18bdcb7dd218537341c9f8c0bdd466fe28c4ab9c2ffe3`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 24.3 KB (24326 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:7dcbb0c94b489adbd7689f5dec11e3cbccf6857f9d5ca873c77c99a21b97f219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108113224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2641e7feaa77c230db1bfda73a063c689a93a49c76faac2ca118d7209778ef`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:04 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:18:18 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 08 May 2026 00:18:18 GMT
WORKDIR /liquibase
# Fri, 08 May 2026 00:18:19 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 08 May 2026 00:18:19 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 08 May 2026 00:18:19 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 08 May 2026 00:18:19 GMT
ARG LPM_VERSION=0.2.14
# Fri, 08 May 2026 00:18:19 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 08 May 2026 00:18:19 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 08 May 2026 00:18:28 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 08 May 2026 00:18:28 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 08 May 2026 00:18:28 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 08 May 2026 00:18:28 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 08 May 2026 00:18:28 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 08 May 2026 00:18:28 GMT
USER liquibase:liquibase
# Fri, 08 May 2026 00:18:28 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 08 May 2026 00:18:28 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544d22e194278e44be8a69ea7eb1ae3c241a250596adb5ef0785760214ebbddc`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 16.1 MB (16076301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b207660b0f3fb6077de423783c55a3f8e3878d3e29341e2317c5d164f769bbf`  
		Last Modified: Fri, 08 May 2026 00:00:24 GMT  
		Size: 52.3 MB (52314951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9519bf6f9e2bb2bc542725464302c037e9c0c4a1a7a166696c1f95af55c60a99`  
		Last Modified: Fri, 08 May 2026 00:00:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a14ff53ff544f36049ac528a1743609b508d2b29507213a536e2191570dcab0`  
		Last Modified: Fri, 08 May 2026 00:00:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586786e0c705112eab0c01dd9f84af134a01ddeaf80c9ff5b281a1156794bb5f`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dda736a8158ff2fff6271b8757bf17aef48f2500940a99a753ee30a5f1c3769`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 8.7 MB (8665802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75373fcf51c8772e125c08402cf45741b61f12ce95c6b5c96fffc46a68d5a81`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 3.4 MB (3441238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d74abc7d1c1d4bae3e428da2121d24e5ee566ae9680c5d83a649690f3f50f7`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d4e7ee955eb4e18331621739c50c7fd2ab68a56fd4504776078eeb1bdcb1c5`  
		Last Modified: Fri, 08 May 2026 00:18:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:a8adb59546f1b9172f4a76c75f3796fcfdb5522dd18b33d8ad754b69da740eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf886df064cf0ee7d8bf6910b67a5ef295a4e14e4800a0cc6090339aeb04978`

```dockerfile
```

-	Layers:
	-	`sha256:8e51f5590e2ed306bc4b44dcda7c508e1523e957b2038b946e0a0a379c6bf012`  
		Last Modified: Fri, 08 May 2026 00:18:37 GMT  
		Size: 3.9 MB (3898042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f744c614b2c1b223f23f08687a22ef52a198e1be51bdbbcb423463edcdbe9693`  
		Last Modified: Fri, 08 May 2026 00:18:35 GMT  
		Size: 24.4 KB (24448 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:5.0.1-alpine`

```console
$ docker pull liquibase@sha256:b131a24527add4d4eadc3300aa5cca684aa60abcd734b8d14d4a5c33b169b48b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:ac3e7f22a1f63434bec4e9ac9a459c3d14ff5fbf5b4cf23c41aaa15c8646c35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84056139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735cc69d2a472f1a3213f884cf38c27e7f07f9e006723d24b254987a2fc4c687`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:11 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:30:15 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:30:16 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:30:16 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:16 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c968b03a929ffeffc74e342fa376b3edf03837491ffc31b33bf6355c7e7a7`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b8a26d38c62ddc3835ccdd169cdda87af0f6fc420b7a65a9ddd9f3321ca1a2`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 67.9 MB (67873148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f7f520ce551a37b7e676a5e609d9729695d8ce07c806c1e101c9f205fecf03`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 8.7 MB (8688923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eea34866b5479ef311e6f9062d31c5e6c8a3e9a51dbaf8a25c64f65f673223`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 3.7 MB (3683310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa91b0bcf56568c9049861b5321c46085544a6631527bdefdb84c18a6623fae`  
		Last Modified: Fri, 17 Apr 2026 00:30:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c03822eba8e0cf95dce574baa878c2167415ad48eef1ccbae83246ea874b9ed`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:d088b7b55f51985159b6fe32611b0b4ebc925d08146919b22dc42fa7cd35dfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2dd6a4bb49d474fcadd1abd2f52dc79ca67b31b11a96c5a34f239b5f7893db`

```dockerfile
```

-	Layers:
	-	`sha256:f2156f2fcd7c800b311863e493b109f04e64f083639871cd2b5efce1f17640f3`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 358.0 KB (357987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f79eec151e7ce7c7347244c9c8bfd7431205e45e6b30fa7e98e27e95e0f10e`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:02764df374a1709ff23d3a5dcdc44587ce282ec941977e0ca367393400d4dcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83068134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e817e3c8378838c704e6f2db9767c81860a27f181249cb9e44be5299293faf43`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:31:15 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:31:17 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:31:18 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:31:19 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:31:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:31:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:31:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831166d40df22727a0f749606435ab6a4409084cb7202d34b8b35ccd2fd53ea3`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca45e9539c13dc3120e4487c5eb9306e5662fa360caef114c284f51f1f4f719`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 66.9 MB (66875198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a208d911ef09d8f8a6d13581c531ccc60d996bc210563f23f78e5861586d2`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 8.7 MB (8688840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b5ab7263f6d6b43a369410afbf518ea077ad4e76614e0b52ce51e89eaa9cb7`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 3.4 MB (3359632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be70c70dd84b0d04d247753d188bb7b592163f4fa2eca01b98d762f8d41963b5`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec2acdb9ae64468ca511183e0e8d93e60650516f7ea7bb68d7593fa5a610c9b`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:e3b85712d2657fcb95286ea159735ef6569569f9ddf0c378609ca2a5a9b461a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 KB (379029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab59b0f660b749ad5d77d3e747d5e622c3a40f4a290033d443b1cde84a3b8075`

```dockerfile
```

-	Layers:
	-	`sha256:2d73bc84012845f7b7fc5b6f5675adbae3ba5b0e44ba23b940acbcf56b91f5c2`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 357.2 KB (357234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd48a19d885fdd36c300257a8e06f61a3d7d772787a3409329468d2924df5deb`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:b131a24527add4d4eadc3300aa5cca684aa60abcd734b8d14d4a5c33b169b48b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:ac3e7f22a1f63434bec4e9ac9a459c3d14ff5fbf5b4cf23c41aaa15c8646c35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84056139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735cc69d2a472f1a3213f884cf38c27e7f07f9e006723d24b254987a2fc4c687`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:11 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:30:13 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:30:15 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:30:15 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:30:15 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:30:16 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:30:16 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:30:16 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:30:16 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:16 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c968b03a929ffeffc74e342fa376b3edf03837491ffc31b33bf6355c7e7a7`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b8a26d38c62ddc3835ccdd169cdda87af0f6fc420b7a65a9ddd9f3321ca1a2`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 67.9 MB (67873148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f7f520ce551a37b7e676a5e609d9729695d8ce07c806c1e101c9f205fecf03`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 8.7 MB (8688923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eea34866b5479ef311e6f9062d31c5e6c8a3e9a51dbaf8a25c64f65f673223`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 3.7 MB (3683310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa91b0bcf56568c9049861b5321c46085544a6631527bdefdb84c18a6623fae`  
		Last Modified: Fri, 17 Apr 2026 00:30:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c03822eba8e0cf95dce574baa878c2167415ad48eef1ccbae83246ea874b9ed`  
		Last Modified: Fri, 17 Apr 2026 00:30:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:d088b7b55f51985159b6fe32611b0b4ebc925d08146919b22dc42fa7cd35dfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2dd6a4bb49d474fcadd1abd2f52dc79ca67b31b11a96c5a34f239b5f7893db`

```dockerfile
```

-	Layers:
	-	`sha256:f2156f2fcd7c800b311863e493b109f04e64f083639871cd2b5efce1f17640f3`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 358.0 KB (357987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f79eec151e7ce7c7347244c9c8bfd7431205e45e6b30fa7e98e27e95e0f10e`  
		Last Modified: Fri, 17 Apr 2026 00:30:28 GMT  
		Size: 21.7 KB (21658 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:02764df374a1709ff23d3a5dcdc44587ce282ec941977e0ca367393400d4dcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83068134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e817e3c8378838c704e6f2db9767c81860a27f181249cb9e44be5299293faf43`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:31:15 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 17 Apr 2026 00:31:17 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 17 Apr 2026 00:31:18 GMT
WORKDIR /liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 17 Apr 2026 00:31:19 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_VERSION=0.2.14
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 17 Apr 2026 00:31:19 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 17 Apr 2026 00:31:19 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 17 Apr 2026 00:31:21 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 17 Apr 2026 00:31:21 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 17 Apr 2026 00:31:21 GMT
USER liquibase:liquibase
# Fri, 17 Apr 2026 00:31:21 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:31:21 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831166d40df22727a0f749606435ab6a4409084cb7202d34b8b35ccd2fd53ea3`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca45e9539c13dc3120e4487c5eb9306e5662fa360caef114c284f51f1f4f719`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 66.9 MB (66875198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a208d911ef09d8f8a6d13581c531ccc60d996bc210563f23f78e5861586d2`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 8.7 MB (8688840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b5ab7263f6d6b43a369410afbf518ea077ad4e76614e0b52ce51e89eaa9cb7`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 3.4 MB (3359632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be70c70dd84b0d04d247753d188bb7b592163f4fa2eca01b98d762f8d41963b5`  
		Last Modified: Fri, 17 Apr 2026 00:31:33 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec2acdb9ae64468ca511183e0e8d93e60650516f7ea7bb68d7593fa5a610c9b`  
		Last Modified: Fri, 17 Apr 2026 00:31:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:e3b85712d2657fcb95286ea159735ef6569569f9ddf0c378609ca2a5a9b461a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 KB (379029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab59b0f660b749ad5d77d3e747d5e622c3a40f4a290033d443b1cde84a3b8075`

```dockerfile
```

-	Layers:
	-	`sha256:2d73bc84012845f7b7fc5b6f5675adbae3ba5b0e44ba23b940acbcf56b91f5c2`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 357.2 KB (357234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd48a19d885fdd36c300257a8e06f61a3d7d772787a3409329468d2924df5deb`  
		Last Modified: Fri, 17 Apr 2026 00:31:32 GMT  
		Size: 21.8 KB (21795 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:ea0a5d5914f8526e5a0d49c3b7be480ea0d4d48c546b4fdfb8c2ce2059e82a2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:c8cf85eafe11714eebb0ce4eb530fa4edcd37c6a16ff98b03cf9c6dc751b3b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111450676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4594c5be7feda4877740b1bbcc96712352436ae597674a5068bd6c2ae0f99012`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:39 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:16:01 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 08 May 2026 00:16:01 GMT
WORKDIR /liquibase
# Fri, 08 May 2026 00:16:02 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 08 May 2026 00:16:02 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 08 May 2026 00:16:02 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 08 May 2026 00:16:02 GMT
ARG LPM_VERSION=0.2.14
# Fri, 08 May 2026 00:16:02 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 08 May 2026 00:16:02 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 08 May 2026 00:16:02 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 08 May 2026 00:16:08 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 08 May 2026 00:16:08 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 08 May 2026 00:16:08 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 08 May 2026 00:16:08 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 08 May 2026 00:16:09 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 08 May 2026 00:16:09 GMT
USER liquibase:liquibase
# Fri, 08 May 2026 00:16:09 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 08 May 2026 00:16:09 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f3bb8db2f4dc74d10969086150cb5462adac4d48009d71e48fe1ddf091dbea`  
		Last Modified: Fri, 08 May 2026 00:00:55 GMT  
		Size: 16.2 MB (16152648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0b62ebdf15bee16664fcacbb1c997bab64334377b27819ebe34754a9612343`  
		Last Modified: Fri, 08 May 2026 00:00:56 GMT  
		Size: 53.1 MB (53122853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95479e5f9bc5335e52cd4c9ef213b49a792113e34700e87b77feede68b30d8`  
		Last Modified: Fri, 08 May 2026 00:00:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c913227527c934bbe224166757603d424752d6eaae314b0141b34f9d843b431f`  
		Last Modified: Fri, 08 May 2026 00:00:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337956894102248449362abf51c0c81ca53147049154281664592f42e33000f4`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bfea534fc9680f54e296a39f8dd00fd002463feca8e6c8b2d05e3a9266a6e6`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 8.7 MB (8665800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6c9575fd54901bfff0784d808e3da4ad2dfb6f9b95cb9453d744357989336f`  
		Last Modified: Fri, 08 May 2026 00:16:18 GMT  
		Size: 3.8 MB (3764496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080e64a73cd350bd2b42efbfb003a597c5f1463ea19f5827e3fdf426bd0288a5`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7197048795b6c6afeef9c47dd4b6a137c09caf02759258903734f570c60aa6b`  
		Last Modified: Fri, 08 May 2026 00:16:18 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:b88f9df964b4d4f26b4044c01d08e5c805e67b4c50ef4010dc7365f368233786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167fa86e36ceaabb302800ee5b3389b73d07a697e8297020bb522632f16f14b4`

```dockerfile
```

-	Layers:
	-	`sha256:2a7c7f115162ec03602cb83c5b79db63dff22fa800d50150183495768c025a87`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 3.9 MB (3898374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c53bb8992f4ee5c00c18bdcb7dd218537341c9f8c0bdd466fe28c4ab9c2ffe3`  
		Last Modified: Fri, 08 May 2026 00:16:17 GMT  
		Size: 24.3 KB (24326 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:7dcbb0c94b489adbd7689f5dec11e3cbccf6857f9d5ca873c77c99a21b97f219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108113224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2641e7feaa77c230db1bfda73a063c689a93a49c76faac2ca118d7209778ef`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:04 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:18:18 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 08 May 2026 00:18:18 GMT
WORKDIR /liquibase
# Fri, 08 May 2026 00:18:19 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 08 May 2026 00:18:19 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 08 May 2026 00:18:19 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 08 May 2026 00:18:19 GMT
ARG LPM_VERSION=0.2.14
# Fri, 08 May 2026 00:18:19 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 08 May 2026 00:18:19 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 08 May 2026 00:18:19 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 08 May 2026 00:18:28 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 08 May 2026 00:18:28 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 08 May 2026 00:18:28 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 08 May 2026 00:18:28 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 08 May 2026 00:18:28 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 08 May 2026 00:18:28 GMT
USER liquibase:liquibase
# Fri, 08 May 2026 00:18:28 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 08 May 2026 00:18:28 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544d22e194278e44be8a69ea7eb1ae3c241a250596adb5ef0785760214ebbddc`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 16.1 MB (16076301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b207660b0f3fb6077de423783c55a3f8e3878d3e29341e2317c5d164f769bbf`  
		Last Modified: Fri, 08 May 2026 00:00:24 GMT  
		Size: 52.3 MB (52314951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9519bf6f9e2bb2bc542725464302c037e9c0c4a1a7a166696c1f95af55c60a99`  
		Last Modified: Fri, 08 May 2026 00:00:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a14ff53ff544f36049ac528a1743609b508d2b29507213a536e2191570dcab0`  
		Last Modified: Fri, 08 May 2026 00:00:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586786e0c705112eab0c01dd9f84af134a01ddeaf80c9ff5b281a1156794bb5f`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dda736a8158ff2fff6271b8757bf17aef48f2500940a99a753ee30a5f1c3769`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 8.7 MB (8665802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75373fcf51c8772e125c08402cf45741b61f12ce95c6b5c96fffc46a68d5a81`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 3.4 MB (3441238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d74abc7d1c1d4bae3e428da2121d24e5ee566ae9680c5d83a649690f3f50f7`  
		Last Modified: Fri, 08 May 2026 00:18:36 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d4e7ee955eb4e18331621739c50c7fd2ab68a56fd4504776078eeb1bdcb1c5`  
		Last Modified: Fri, 08 May 2026 00:18:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:a8adb59546f1b9172f4a76c75f3796fcfdb5522dd18b33d8ad754b69da740eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf886df064cf0ee7d8bf6910b67a5ef295a4e14e4800a0cc6090339aeb04978`

```dockerfile
```

-	Layers:
	-	`sha256:8e51f5590e2ed306bc4b44dcda7c508e1523e957b2038b946e0a0a379c6bf012`  
		Last Modified: Fri, 08 May 2026 00:18:37 GMT  
		Size: 3.9 MB (3898042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f744c614b2c1b223f23f08687a22ef52a198e1be51bdbbcb423463edcdbe9693`  
		Last Modified: Fri, 08 May 2026 00:18:35 GMT  
		Size: 24.4 KB (24448 bytes)  
		MIME: application/vnd.in-toto+json
