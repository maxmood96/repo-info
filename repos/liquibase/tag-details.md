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
$ docker pull liquibase@sha256:4db403b96dd9790c6239e94e583ffa4cdce444eb0153f190b74a5eb7789e6e2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0` - linux; amd64

```console
$ docker pull liquibase@sha256:df5e13fe1995365a2c3bf4c0ebdcb23d1072fafc039053c129d3337d000a81eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111104487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f7fbffdd75eb6e9195a60f90858ffc61a94cafe5040bdc07c5ecd02411c65b`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:00 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:29:51 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 14 Nov 2025 00:29:51 GMT
WORKDIR /liquibase
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 14 Nov 2025 00:29:52 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LPM_VERSION=0.2.14
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 14 Nov 2025 00:29:58 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 14 Nov 2025 00:29:58 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 14 Nov 2025 00:29:58 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 14 Nov 2025 00:29:58 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 14 Nov 2025 00:29:58 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 14 Nov 2025 00:29:58 GMT
USER liquibase:liquibase
# Fri, 14 Nov 2025 00:29:58 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:29:58 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10875650961bf4063d5186970a8c79ef61cf11ca22d49b715b9d59712e0869b`  
		Last Modified: Thu, 13 Nov 2025 23:21:30 GMT  
		Size: 16.2 MB (16150480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be944c6b743dbf21ecbe2d28355dc9f0e5ceadd25ba4c33e09883ea3fb27acc`  
		Last Modified: Thu, 13 Nov 2025 23:21:56 GMT  
		Size: 53.0 MB (52978531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f0f6707dd14f4b50b2fcf046afafdd21c569b1c8c0d05eed070ceaa196fdf0`  
		Last Modified: Thu, 13 Nov 2025 23:21:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55135a7213f6021c2f7be62142583bd9d4eef722869235128decb808bad7d3cd`  
		Last Modified: Thu, 13 Nov 2025 23:21:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646dc22b1b228b5280c7a22d2e48e933c4ee2ad60c15207e2530c614430c2ae`  
		Last Modified: Fri, 14 Nov 2025 00:30:14 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d102f0c3c9b9b13fb321d8826c5729ea91606769560f118dc4961a2ec8053c0`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 8.7 MB (8665785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec7321b9c80fcc2f5bece23eb102671281f63577490090bc16cceb817aa114d`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 3.8 MB (3764507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edd43d6ff9ad1ab776bb92116bf92a1dcf283c8d8a150b13d1714373d917c37`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c313b17dccb4f5357fe4c9848d3d66ede5447be2a0cc3e7acf19d86b803c10`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:06d72e7697718e19facccf4e8a417f658bf4fb1746762f16b5e9fbe95be6104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b5797602b4cf49b265132a059af432d958dcedb7984ac3781bd17b917361fe`

```dockerfile
```

-	Layers:
	-	`sha256:ea992b1fe3b40411a87bae59bed08fc37ce2a5871a24caf38ca97f56c08354f6`  
		Last Modified: Fri, 14 Nov 2025 01:39:47 GMT  
		Size: 3.9 MB (3897733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c42140375498b2deaefc70e0250cf7443d8fe0870d1348c4fd081034493b624a`  
		Last Modified: Fri, 14 Nov 2025 01:39:48 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:7ff2798e6e8ee00f79bc2321725f93b40783e9c293aa54b02ec09bed15bf362e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107714162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aff88730e9557518bf43139cedc0887d65808390e35fe3414e3a8350c588946`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:29:59 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 14 Nov 2025 00:29:59 GMT
WORKDIR /liquibase
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 14 Nov 2025 00:30:00 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LPM_VERSION=0.2.14
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 14 Nov 2025 00:30:09 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 14 Nov 2025 00:30:09 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 14 Nov 2025 00:30:09 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 14 Nov 2025 00:30:09 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 14 Nov 2025 00:30:09 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 14 Nov 2025 00:30:09 GMT
USER liquibase:liquibase
# Fri, 14 Nov 2025 00:30:09 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:30:09 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44e93e2f17680350eef250800f885c5ec5b1dfc6fb7c43cf8e92ea04d5a6f0b`  
		Last Modified: Thu, 13 Nov 2025 23:21:06 GMT  
		Size: 16.1 MB (16066283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc40a6001ee01be38cea704e5d4e64e6b569c37c42227eabc9d308b26755e806`  
		Last Modified: Thu, 13 Nov 2025 23:21:46 GMT  
		Size: 52.1 MB (52148587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fed4c697cbdb704ffa20faeed81c4eb8b16824faa140cce1fd03b6eff14fb7`  
		Last Modified: Thu, 13 Nov 2025 23:21:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Thu, 13 Nov 2025 23:21:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047ec8bdc60d151ac458159439620a95f57b3a8b98e633f57de0fd830cff220a`  
		Last Modified: Fri, 14 Nov 2025 00:30:26 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360f3c0e6bcb0eb19251b7b4cd6a81f58f9921c4b55c50b76a3ac70e22201256`  
		Last Modified: Fri, 14 Nov 2025 00:30:28 GMT  
		Size: 8.7 MB (8665787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2bc033cf2c0c3faa97d699477dafc3e51deb66041970d9b9497062df915b4`  
		Last Modified: Fri, 14 Nov 2025 00:30:27 GMT  
		Size: 3.4 MB (3441244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc8319e6136f9b84269f70241f62a4c28f1c581603ec0a8be540ff9e00d48d8`  
		Last Modified: Fri, 14 Nov 2025 00:30:27 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd34b3b601f870cb1fbfe2e006a537f9b49ca4c3def9463e7bc48c6c1c21b0`  
		Last Modified: Fri, 14 Nov 2025 00:30:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:b9dec2343f4afd65087ef44800bfea84b1b6d0c70e938a45ace3e733819b9462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f780190558e512d48cf00b6b8ece6fb185a709c92e9ee6df5a2a689b5c37e0`

```dockerfile
```

-	Layers:
	-	`sha256:c92fad7af6ac29b35b12f8d3e560379d6dd16177d8877230ca7f8de68be4b10d`  
		Last Modified: Fri, 14 Nov 2025 01:39:52 GMT  
		Size: 3.9 MB (3897401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe87d269a824d8b33e0305d82299906cec78ffafbbe68705db662eb200cb5d0d`  
		Last Modified: Fri, 14 Nov 2025 01:39:53 GMT  
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
$ docker pull liquibase@sha256:4db403b96dd9790c6239e94e583ffa4cdce444eb0153f190b74a5eb7789e6e2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:5.0.1` - linux; amd64

```console
$ docker pull liquibase@sha256:df5e13fe1995365a2c3bf4c0ebdcb23d1072fafc039053c129d3337d000a81eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111104487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f7fbffdd75eb6e9195a60f90858ffc61a94cafe5040bdc07c5ecd02411c65b`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:00 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:29:51 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 14 Nov 2025 00:29:51 GMT
WORKDIR /liquibase
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 14 Nov 2025 00:29:52 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LPM_VERSION=0.2.14
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 14 Nov 2025 00:29:58 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 14 Nov 2025 00:29:58 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 14 Nov 2025 00:29:58 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 14 Nov 2025 00:29:58 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 14 Nov 2025 00:29:58 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 14 Nov 2025 00:29:58 GMT
USER liquibase:liquibase
# Fri, 14 Nov 2025 00:29:58 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:29:58 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10875650961bf4063d5186970a8c79ef61cf11ca22d49b715b9d59712e0869b`  
		Last Modified: Thu, 13 Nov 2025 23:21:30 GMT  
		Size: 16.2 MB (16150480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be944c6b743dbf21ecbe2d28355dc9f0e5ceadd25ba4c33e09883ea3fb27acc`  
		Last Modified: Thu, 13 Nov 2025 23:21:56 GMT  
		Size: 53.0 MB (52978531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f0f6707dd14f4b50b2fcf046afafdd21c569b1c8c0d05eed070ceaa196fdf0`  
		Last Modified: Thu, 13 Nov 2025 23:21:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55135a7213f6021c2f7be62142583bd9d4eef722869235128decb808bad7d3cd`  
		Last Modified: Thu, 13 Nov 2025 23:21:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646dc22b1b228b5280c7a22d2e48e933c4ee2ad60c15207e2530c614430c2ae`  
		Last Modified: Fri, 14 Nov 2025 00:30:14 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d102f0c3c9b9b13fb321d8826c5729ea91606769560f118dc4961a2ec8053c0`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 8.7 MB (8665785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec7321b9c80fcc2f5bece23eb102671281f63577490090bc16cceb817aa114d`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 3.8 MB (3764507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edd43d6ff9ad1ab776bb92116bf92a1dcf283c8d8a150b13d1714373d917c37`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c313b17dccb4f5357fe4c9848d3d66ede5447be2a0cc3e7acf19d86b803c10`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:06d72e7697718e19facccf4e8a417f658bf4fb1746762f16b5e9fbe95be6104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b5797602b4cf49b265132a059af432d958dcedb7984ac3781bd17b917361fe`

```dockerfile
```

-	Layers:
	-	`sha256:ea992b1fe3b40411a87bae59bed08fc37ce2a5871a24caf38ca97f56c08354f6`  
		Last Modified: Fri, 14 Nov 2025 01:39:47 GMT  
		Size: 3.9 MB (3897733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c42140375498b2deaefc70e0250cf7443d8fe0870d1348c4fd081034493b624a`  
		Last Modified: Fri, 14 Nov 2025 01:39:48 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:5.0.1` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:7ff2798e6e8ee00f79bc2321725f93b40783e9c293aa54b02ec09bed15bf362e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107714162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aff88730e9557518bf43139cedc0887d65808390e35fe3414e3a8350c588946`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:29:59 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 14 Nov 2025 00:29:59 GMT
WORKDIR /liquibase
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 14 Nov 2025 00:30:00 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LPM_VERSION=0.2.14
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 14 Nov 2025 00:30:09 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 14 Nov 2025 00:30:09 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 14 Nov 2025 00:30:09 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 14 Nov 2025 00:30:09 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 14 Nov 2025 00:30:09 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 14 Nov 2025 00:30:09 GMT
USER liquibase:liquibase
# Fri, 14 Nov 2025 00:30:09 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:30:09 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44e93e2f17680350eef250800f885c5ec5b1dfc6fb7c43cf8e92ea04d5a6f0b`  
		Last Modified: Thu, 13 Nov 2025 23:21:06 GMT  
		Size: 16.1 MB (16066283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc40a6001ee01be38cea704e5d4e64e6b569c37c42227eabc9d308b26755e806`  
		Last Modified: Thu, 13 Nov 2025 23:21:46 GMT  
		Size: 52.1 MB (52148587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fed4c697cbdb704ffa20faeed81c4eb8b16824faa140cce1fd03b6eff14fb7`  
		Last Modified: Thu, 13 Nov 2025 23:21:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Thu, 13 Nov 2025 23:21:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047ec8bdc60d151ac458159439620a95f57b3a8b98e633f57de0fd830cff220a`  
		Last Modified: Fri, 14 Nov 2025 00:30:26 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360f3c0e6bcb0eb19251b7b4cd6a81f58f9921c4b55c50b76a3ac70e22201256`  
		Last Modified: Fri, 14 Nov 2025 00:30:28 GMT  
		Size: 8.7 MB (8665787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2bc033cf2c0c3faa97d699477dafc3e51deb66041970d9b9497062df915b4`  
		Last Modified: Fri, 14 Nov 2025 00:30:27 GMT  
		Size: 3.4 MB (3441244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc8319e6136f9b84269f70241f62a4c28f1c581603ec0a8be540ff9e00d48d8`  
		Last Modified: Fri, 14 Nov 2025 00:30:27 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd34b3b601f870cb1fbfe2e006a537f9b49ca4c3def9463e7bc48c6c1c21b0`  
		Last Modified: Fri, 14 Nov 2025 00:30:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:5.0.1` - unknown; unknown

```console
$ docker pull liquibase@sha256:b9dec2343f4afd65087ef44800bfea84b1b6d0c70e938a45ace3e733819b9462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f780190558e512d48cf00b6b8ece6fb185a709c92e9ee6df5a2a689b5c37e0`

```dockerfile
```

-	Layers:
	-	`sha256:c92fad7af6ac29b35b12f8d3e560379d6dd16177d8877230ca7f8de68be4b10d`  
		Last Modified: Fri, 14 Nov 2025 01:39:52 GMT  
		Size: 3.9 MB (3897401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe87d269a824d8b33e0305d82299906cec78ffafbbe68705db662eb200cb5d0d`  
		Last Modified: Fri, 14 Nov 2025 01:39:53 GMT  
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
$ docker pull liquibase@sha256:4db403b96dd9790c6239e94e583ffa4cdce444eb0153f190b74a5eb7789e6e2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:df5e13fe1995365a2c3bf4c0ebdcb23d1072fafc039053c129d3337d000a81eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111104487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f7fbffdd75eb6e9195a60f90858ffc61a94cafe5040bdc07c5ecd02411c65b`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:00 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:29:51 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 14 Nov 2025 00:29:51 GMT
WORKDIR /liquibase
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 14 Nov 2025 00:29:52 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LPM_VERSION=0.2.14
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 14 Nov 2025 00:29:52 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 14 Nov 2025 00:29:52 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 14 Nov 2025 00:29:58 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 14 Nov 2025 00:29:58 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 14 Nov 2025 00:29:58 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 14 Nov 2025 00:29:58 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 14 Nov 2025 00:29:58 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 14 Nov 2025 00:29:58 GMT
USER liquibase:liquibase
# Fri, 14 Nov 2025 00:29:58 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:29:58 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10875650961bf4063d5186970a8c79ef61cf11ca22d49b715b9d59712e0869b`  
		Last Modified: Thu, 13 Nov 2025 23:21:30 GMT  
		Size: 16.2 MB (16150480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be944c6b743dbf21ecbe2d28355dc9f0e5ceadd25ba4c33e09883ea3fb27acc`  
		Last Modified: Thu, 13 Nov 2025 23:21:56 GMT  
		Size: 53.0 MB (52978531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f0f6707dd14f4b50b2fcf046afafdd21c569b1c8c0d05eed070ceaa196fdf0`  
		Last Modified: Thu, 13 Nov 2025 23:21:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55135a7213f6021c2f7be62142583bd9d4eef722869235128decb808bad7d3cd`  
		Last Modified: Thu, 13 Nov 2025 23:21:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646dc22b1b228b5280c7a22d2e48e933c4ee2ad60c15207e2530c614430c2ae`  
		Last Modified: Fri, 14 Nov 2025 00:30:14 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d102f0c3c9b9b13fb321d8826c5729ea91606769560f118dc4961a2ec8053c0`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 8.7 MB (8665785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec7321b9c80fcc2f5bece23eb102671281f63577490090bc16cceb817aa114d`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 3.8 MB (3764507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edd43d6ff9ad1ab776bb92116bf92a1dcf283c8d8a150b13d1714373d917c37`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c313b17dccb4f5357fe4c9848d3d66ede5447be2a0cc3e7acf19d86b803c10`  
		Last Modified: Fri, 14 Nov 2025 00:30:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:06d72e7697718e19facccf4e8a417f658bf4fb1746762f16b5e9fbe95be6104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b5797602b4cf49b265132a059af432d958dcedb7984ac3781bd17b917361fe`

```dockerfile
```

-	Layers:
	-	`sha256:ea992b1fe3b40411a87bae59bed08fc37ce2a5871a24caf38ca97f56c08354f6`  
		Last Modified: Fri, 14 Nov 2025 01:39:47 GMT  
		Size: 3.9 MB (3897733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c42140375498b2deaefc70e0250cf7443d8fe0870d1348c4fd081034493b624a`  
		Last Modified: Fri, 14 Nov 2025 01:39:48 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:7ff2798e6e8ee00f79bc2321725f93b40783e9c293aa54b02ec09bed15bf362e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107714162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aff88730e9557518bf43139cedc0887d65808390e35fe3414e3a8350c588946`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:29:59 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 14 Nov 2025 00:29:59 GMT
WORKDIR /liquibase
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LIQUIBASE_VERSION=5.0.1
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
# Fri, 14 Nov 2025 00:30:00 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://package.liquibase.com/downloads/dockerhub/official/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LPM_VERSION=0.2.14
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e
# Fri, 14 Nov 2025 00:30:00 GMT
ARG LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.licenses=FSL-1.1-ALv2
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.version=5.0.1
# Fri, 14 Nov 2025 00:30:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 14 Nov 2025 00:30:09 GMT
# ARGS: LIQUIBASE_VERSION=5.0.1 LB_SHA256=3ae11ccdcd4c080e421e5fd043bdbd624d56fcfc9b294d5d9d898cb8b074e449 LPM_VERSION=0.2.14 LPM_SHA256=28750d84bf76d32ba3a2d51674a1b4e14205523c87e4655b2cd8de68b916758e LPM_SHA256_ARM=541a220aa3c3227cc0fb40b15976b11011568a06a6499af090258bf604f45cc0
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 14 Nov 2025 00:30:09 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 14 Nov 2025 00:30:09 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 14 Nov 2025 00:30:09 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 14 Nov 2025 00:30:09 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 14 Nov 2025 00:30:09 GMT
USER liquibase:liquibase
# Fri, 14 Nov 2025 00:30:09 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:30:09 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44e93e2f17680350eef250800f885c5ec5b1dfc6fb7c43cf8e92ea04d5a6f0b`  
		Last Modified: Thu, 13 Nov 2025 23:21:06 GMT  
		Size: 16.1 MB (16066283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc40a6001ee01be38cea704e5d4e64e6b569c37c42227eabc9d308b26755e806`  
		Last Modified: Thu, 13 Nov 2025 23:21:46 GMT  
		Size: 52.1 MB (52148587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fed4c697cbdb704ffa20faeed81c4eb8b16824faa140cce1fd03b6eff14fb7`  
		Last Modified: Thu, 13 Nov 2025 23:21:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Thu, 13 Nov 2025 23:21:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047ec8bdc60d151ac458159439620a95f57b3a8b98e633f57de0fd830cff220a`  
		Last Modified: Fri, 14 Nov 2025 00:30:26 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360f3c0e6bcb0eb19251b7b4cd6a81f58f9921c4b55c50b76a3ac70e22201256`  
		Last Modified: Fri, 14 Nov 2025 00:30:28 GMT  
		Size: 8.7 MB (8665787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2bc033cf2c0c3faa97d699477dafc3e51deb66041970d9b9497062df915b4`  
		Last Modified: Fri, 14 Nov 2025 00:30:27 GMT  
		Size: 3.4 MB (3441244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc8319e6136f9b84269f70241f62a4c28f1c581603ec0a8be540ff9e00d48d8`  
		Last Modified: Fri, 14 Nov 2025 00:30:27 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd34b3b601f870cb1fbfe2e006a537f9b49ca4c3def9463e7bc48c6c1c21b0`  
		Last Modified: Fri, 14 Nov 2025 00:30:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:b9dec2343f4afd65087ef44800bfea84b1b6d0c70e938a45ace3e733819b9462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f780190558e512d48cf00b6b8ece6fb185a709c92e9ee6df5a2a689b5c37e0`

```dockerfile
```

-	Layers:
	-	`sha256:c92fad7af6ac29b35b12f8d3e560379d6dd16177d8877230ca7f8de68be4b10d`  
		Last Modified: Fri, 14 Nov 2025 01:39:52 GMT  
		Size: 3.9 MB (3897401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe87d269a824d8b33e0305d82299906cec78ffafbbe68705db662eb200cb5d0d`  
		Last Modified: Fri, 14 Nov 2025 01:39:53 GMT  
		Size: 24.4 KB (24445 bytes)  
		MIME: application/vnd.in-toto+json
