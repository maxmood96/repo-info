<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:2.2`](#orientdb22)
-	[`orientdb:2.2.37`](#orientdb2237)
-	[`orientdb:2.2.37-spatial`](#orientdb2237-spatial)
-	[`orientdb:3.0`](#orientdb30)
-	[`orientdb:3.0-tp3`](#orientdb30-tp3)
-	[`orientdb:3.0.44`](#orientdb3044)
-	[`orientdb:3.0.44-tp3`](#orientdb3044-tp3)
-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.20`](#orientdb3120)
-	[`orientdb:3.1.20-tp3`](#orientdb3120-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.27`](#orientdb3227)
-	[`orientdb:3.2.27-tp3`](#orientdb3227-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:2.2`

```console
$ docker pull orientdb@sha256:7b119612ff889df167026be649e99106cffc8c411e2311ddf378b68ca7211b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2` - linux; amd64

```console
$ docker pull orientdb@sha256:249275ddf7d63b4513c404d6a5fb129894dc1adcaf249ddb416db43018afc52d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193430629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9262d00e0f482af5add08bc9f33f0f79ef70412a77872cb5860f80154d592402`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_VERSION=2.2.37
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Fri, 02 Feb 2024 18:06:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:06:45 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:06:45 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:06:45 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:06:45 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:06:45 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:06:45 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:06:45 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9d0583b05a29400d38001c357a63df793818f8899058e5ad318e48cc7af417`  
		Last Modified: Fri, 02 Feb 2024 18:08:22 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150547b4eb52297656ba3e48b035333b56407db52c36e31e77e06017775a0322`  
		Last Modified: Fri, 02 Feb 2024 18:08:25 GMT  
		Size: 46.5 MB (46473886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37`

```console
$ docker pull orientdb@sha256:7b119612ff889df167026be649e99106cffc8c411e2311ddf378b68ca7211b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37` - linux; amd64

```console
$ docker pull orientdb@sha256:249275ddf7d63b4513c404d6a5fb129894dc1adcaf249ddb416db43018afc52d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193430629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9262d00e0f482af5add08bc9f33f0f79ef70412a77872cb5860f80154d592402`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_VERSION=2.2.37
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Fri, 02 Feb 2024 18:06:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:06:45 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:06:45 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:06:45 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:06:45 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:06:45 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:06:45 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:06:45 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9d0583b05a29400d38001c357a63df793818f8899058e5ad318e48cc7af417`  
		Last Modified: Fri, 02 Feb 2024 18:08:22 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150547b4eb52297656ba3e48b035333b56407db52c36e31e77e06017775a0322`  
		Last Modified: Fri, 02 Feb 2024 18:08:25 GMT  
		Size: 46.5 MB (46473886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37-spatial`

```console
$ docker pull orientdb@sha256:4c77e51820732af3b2196f34db29f32aa522b8358e32d6972356e8ccfeb8c359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37-spatial` - linux; amd64

```console
$ docker pull orientdb@sha256:e935a2986f9d6ab3d03ade2e88f7de1e09d3e66d7a54f833e12ca3871d97ad02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194633220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbc6d67ed6bc0a5ddb7f0c860aab0205dbe474f9ba5360eb74f43915f8cb26e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_VERSION=2.2.37
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Fri, 02 Feb 2024 18:06:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Fri, 02 Feb 2024 18:06:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:06:45 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:06:45 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:06:45 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:06:45 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:06:45 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:06:45 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:06:45 GMT
CMD ["server.sh"]
# Fri, 02 Feb 2024 18:06:49 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_MD5=9f64ab5e959f5d9ad9ea5195d6d621d2
# Fri, 02 Feb 2024 18:06:49 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_SHA1=1748c9779ea7a8cb8fc068fcabf960e1778e8a19
# Fri, 02 Feb 2024 18:06:49 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-spatial/2.2.37/orientdb-spatial-2.2.37-dist.jar
# Fri, 02 Feb 2024 18:06:50 GMT
RUN wget $ORIENTDB_DOWNLOAD_SPATIAL_URL     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_MD5 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | md5sum -c -     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_SHA1 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | sha1sum -c -     && mv orientdb-spatial-*-dist.jar /orientdb/lib/
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9d0583b05a29400d38001c357a63df793818f8899058e5ad318e48cc7af417`  
		Last Modified: Fri, 02 Feb 2024 18:08:22 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150547b4eb52297656ba3e48b035333b56407db52c36e31e77e06017775a0322`  
		Last Modified: Fri, 02 Feb 2024 18:08:25 GMT  
		Size: 46.5 MB (46473886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1482defa402fa316fb57a71d4220268f3e404b25b4e432ea5406bbb62e88d710`  
		Last Modified: Fri, 02 Feb 2024 18:08:36 GMT  
		Size: 1.2 MB (1202591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0`

```console
$ docker pull orientdb@sha256:a11a50f943e4f6f235fabcb23c4aaf2384aa205f97ad40ebe051aa1bdff87949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0` - linux; amd64

```console
$ docker pull orientdb@sha256:87b7c7da80dfa71b512632b5438583cb5024cc2f09860d86b13ec854735fe671
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.0 MB (184021542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7e4f1001d3b953b7841cfce2475e4eba515a3086751e51aa4882eb77bba576`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:06:13 GMT
ENV ORIENTDB_VERSION=3.0.44
# Fri, 02 Feb 2024 18:06:13 GMT
ENV ORIENTDB_DOWNLOAD_MD5=1bdcdb4d9c54fc78a1b56b8375ca990d
# Fri, 02 Feb 2024 18:06:13 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6462dacd0df0725f10f85bee9666a0f6979187a6
# Fri, 02 Feb 2024 18:06:13 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.44/orientdb-community-3.0.44.tar.gz
# Fri, 02 Feb 2024 18:06:18 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:06:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:06:20 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:06:20 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:06:21 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:06:21 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:06:21 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:06:21 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4305c7594fb281e715f001b4a09107dd406a281185a04aef610567da471895b`  
		Last Modified: Fri, 02 Feb 2024 18:07:59 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9e41c82fb9eb808b7a687047046b9221922fb9ae7d58640e21b92e48dde982`  
		Last Modified: Fri, 02 Feb 2024 18:08:02 GMT  
		Size: 37.1 MB (37064801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0-tp3`

```console
$ docker pull orientdb@sha256:9ffb42e8b8d5bcf6219ab63fdcb22cf00b736f3ece4c0680c1d4350aa04cd8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:978dd6a4ad831a0571082a400734a926311b5e6b9de65dfbcaf490a5504f14b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211041877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7386935c86295438b3f5ccf5750be1308566309e7263268f6622e5ea2cef6909`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:06:13 GMT
ENV ORIENTDB_VERSION=3.0.44
# Fri, 02 Feb 2024 18:06:24 GMT
ENV ORIENTDB_DOWNLOAD_MD5=44f8c96f57f75a4b9e2a3996a3b17512
# Fri, 02 Feb 2024 18:06:24 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c49067782368e13082648d48bf6685969a5ed550
# Fri, 02 Feb 2024 18:06:24 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.44/orientdb-tp3-3.0.44.tar.gz
# Fri, 02 Feb 2024 18:06:28 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:06:33 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:06:33 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Fri, 02 Feb 2024 18:06:33 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:06:33 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:06:33 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:06:33 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:06:33 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:06:34 GMT
EXPOSE 8182
# Fri, 02 Feb 2024 18:06:34 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1e4a0fcc7e3436b405455727e48c037b88fc3c1a46522ec7084ef3f07b588d`  
		Last Modified: Fri, 02 Feb 2024 18:08:10 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4752d270d4f4f38d90b095c39d83b6b9ae0b17e26317221a1d2d01d4ecdbeb`  
		Last Modified: Fri, 02 Feb 2024 18:08:14 GMT  
		Size: 64.1 MB (64083756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e6d42eaa89d474186f209646c26a1de71755e3514e92a9ceaaf702e5ca94cf`  
		Last Modified: Fri, 02 Feb 2024 18:08:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.44`

```console
$ docker pull orientdb@sha256:a11a50f943e4f6f235fabcb23c4aaf2384aa205f97ad40ebe051aa1bdff87949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.44` - linux; amd64

```console
$ docker pull orientdb@sha256:87b7c7da80dfa71b512632b5438583cb5024cc2f09860d86b13ec854735fe671
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.0 MB (184021542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7e4f1001d3b953b7841cfce2475e4eba515a3086751e51aa4882eb77bba576`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:06:13 GMT
ENV ORIENTDB_VERSION=3.0.44
# Fri, 02 Feb 2024 18:06:13 GMT
ENV ORIENTDB_DOWNLOAD_MD5=1bdcdb4d9c54fc78a1b56b8375ca990d
# Fri, 02 Feb 2024 18:06:13 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6462dacd0df0725f10f85bee9666a0f6979187a6
# Fri, 02 Feb 2024 18:06:13 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.44/orientdb-community-3.0.44.tar.gz
# Fri, 02 Feb 2024 18:06:18 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:06:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:06:20 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:06:20 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:06:21 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:06:21 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:06:21 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:06:21 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4305c7594fb281e715f001b4a09107dd406a281185a04aef610567da471895b`  
		Last Modified: Fri, 02 Feb 2024 18:07:59 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9e41c82fb9eb808b7a687047046b9221922fb9ae7d58640e21b92e48dde982`  
		Last Modified: Fri, 02 Feb 2024 18:08:02 GMT  
		Size: 37.1 MB (37064801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.44-tp3`

```console
$ docker pull orientdb@sha256:9ffb42e8b8d5bcf6219ab63fdcb22cf00b736f3ece4c0680c1d4350aa04cd8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.44-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:978dd6a4ad831a0571082a400734a926311b5e6b9de65dfbcaf490a5504f14b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211041877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7386935c86295438b3f5ccf5750be1308566309e7263268f6622e5ea2cef6909`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:06:13 GMT
ENV ORIENTDB_VERSION=3.0.44
# Fri, 02 Feb 2024 18:06:24 GMT
ENV ORIENTDB_DOWNLOAD_MD5=44f8c96f57f75a4b9e2a3996a3b17512
# Fri, 02 Feb 2024 18:06:24 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c49067782368e13082648d48bf6685969a5ed550
# Fri, 02 Feb 2024 18:06:24 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.44/orientdb-tp3-3.0.44.tar.gz
# Fri, 02 Feb 2024 18:06:28 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:06:33 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:06:33 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Fri, 02 Feb 2024 18:06:33 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:06:33 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:06:33 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:06:33 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:06:33 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:06:34 GMT
EXPOSE 8182
# Fri, 02 Feb 2024 18:06:34 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1e4a0fcc7e3436b405455727e48c037b88fc3c1a46522ec7084ef3f07b588d`  
		Last Modified: Fri, 02 Feb 2024 18:08:10 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4752d270d4f4f38d90b095c39d83b6b9ae0b17e26317221a1d2d01d4ecdbeb`  
		Last Modified: Fri, 02 Feb 2024 18:08:14 GMT  
		Size: 64.1 MB (64083756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e6d42eaa89d474186f209646c26a1de71755e3514e92a9ceaaf702e5ca94cf`  
		Last Modified: Fri, 02 Feb 2024 18:08:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:98590addbb6213314ea79202c2e840f3681ae19a815c72386bed38cdbbfd7d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:115f5807cc90d9790ae6931c3ca3674b968a95bb36ebe12cc13afcf380f96b63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (200037961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b38b0e981f2927c10d6a55d950afc1757cf6383230dee0daf3040544af1828e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:05:40 GMT
ENV ORIENTDB_VERSION=3.1.20
# Fri, 02 Feb 2024 18:05:40 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Fri, 02 Feb 2024 18:05:40 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Fri, 02 Feb 2024 18:05:40 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Fri, 02 Feb 2024 18:05:45 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:05:48 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:05:48 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:05:48 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:05:48 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:05:48 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:05:49 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:05:49 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9da062d4caf4d33d100c878e06d316a711ecb254f82b805010c340a6f22d51c`  
		Last Modified: Fri, 02 Feb 2024 18:07:36 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97050339ddb63aae60f146a01d60d278b8fc91b3177d61316ca491105d024c29`  
		Last Modified: Fri, 02 Feb 2024 18:07:39 GMT  
		Size: 53.1 MB (53081222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:10d686932760ee6994b99ea6835ce6a59621f575c119b11ec540c83d79eb14d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:61a1cd2abfe49d9ecd80dd37a737c78833febb2618836225c23fcfb5a31bab59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223044981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe501dac42a623b323bcb2648e5734efc54ca4603f25c557598dea0c708e460`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:05:40 GMT
ENV ORIENTDB_VERSION=3.1.20
# Fri, 02 Feb 2024 18:05:53 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Fri, 02 Feb 2024 18:05:53 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Fri, 02 Feb 2024 18:05:53 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Fri, 02 Feb 2024 18:05:57 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:06:08 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:06:08 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Fri, 02 Feb 2024 18:06:08 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:06:08 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:06:08 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:06:08 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:06:08 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:06:08 GMT
EXPOSE 8182
# Fri, 02 Feb 2024 18:06:09 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705bd9565a9191dd62bb1c116b69924037522547013e1ae3d94efb41e289ccc8`  
		Last Modified: Fri, 02 Feb 2024 18:07:47 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e833b645d63405c954d9d353961315cf830ebc81fdc1cfd046644b01d05294`  
		Last Modified: Fri, 02 Feb 2024 18:07:51 GMT  
		Size: 76.1 MB (76086862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff705f6bbdc251d458accc3e6ea41da552af15dbba83ebe014f63a6d9ce1af17`  
		Last Modified: Fri, 02 Feb 2024 18:07:47 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:98590addbb6213314ea79202c2e840f3681ae19a815c72386bed38cdbbfd7d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:115f5807cc90d9790ae6931c3ca3674b968a95bb36ebe12cc13afcf380f96b63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (200037961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b38b0e981f2927c10d6a55d950afc1757cf6383230dee0daf3040544af1828e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:05:40 GMT
ENV ORIENTDB_VERSION=3.1.20
# Fri, 02 Feb 2024 18:05:40 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Fri, 02 Feb 2024 18:05:40 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Fri, 02 Feb 2024 18:05:40 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Fri, 02 Feb 2024 18:05:45 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:05:48 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:05:48 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:05:48 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:05:48 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:05:48 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:05:49 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:05:49 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9da062d4caf4d33d100c878e06d316a711ecb254f82b805010c340a6f22d51c`  
		Last Modified: Fri, 02 Feb 2024 18:07:36 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97050339ddb63aae60f146a01d60d278b8fc91b3177d61316ca491105d024c29`  
		Last Modified: Fri, 02 Feb 2024 18:07:39 GMT  
		Size: 53.1 MB (53081222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:10d686932760ee6994b99ea6835ce6a59621f575c119b11ec540c83d79eb14d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:61a1cd2abfe49d9ecd80dd37a737c78833febb2618836225c23fcfb5a31bab59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223044981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe501dac42a623b323bcb2648e5734efc54ca4603f25c557598dea0c708e460`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:05:40 GMT
ENV ORIENTDB_VERSION=3.1.20
# Fri, 02 Feb 2024 18:05:53 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Fri, 02 Feb 2024 18:05:53 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Fri, 02 Feb 2024 18:05:53 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Fri, 02 Feb 2024 18:05:57 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:06:08 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:06:08 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Fri, 02 Feb 2024 18:06:08 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:06:08 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:06:08 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:06:08 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:06:08 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:06:08 GMT
EXPOSE 8182
# Fri, 02 Feb 2024 18:06:09 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705bd9565a9191dd62bb1c116b69924037522547013e1ae3d94efb41e289ccc8`  
		Last Modified: Fri, 02 Feb 2024 18:07:47 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e833b645d63405c954d9d353961315cf830ebc81fdc1cfd046644b01d05294`  
		Last Modified: Fri, 02 Feb 2024 18:07:51 GMT  
		Size: 76.1 MB (76086862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff705f6bbdc251d458accc3e6ea41da552af15dbba83ebe014f63a6d9ce1af17`  
		Last Modified: Fri, 02 Feb 2024 18:07:47 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:d2b6c5d838821a36a5070d948feddd2526ac142502303baeca0c597c2f567f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2` - linux; amd64

```console
$ docker pull orientdb@sha256:72ace32766c923d890bed1c56e2f774c0f5772b15133b091fb1a4736a0e3f257
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210960851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bc8d7bae2eabfa5996ce3ceea6047a8547d5cbd73daac5694c2b02c89ea47f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:05:15 GMT
ENV ORIENTDB_VERSION=3.2.26
# Fri, 02 Feb 2024 18:05:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b90008923e8b228d62d9181499015cf9
# Fri, 02 Feb 2024 18:05:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=e18a190249dca50b9cdeebdd1687037af0349b21
# Fri, 02 Feb 2024 18:05:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.26/orientdb-community-3.2.26.tar.gz
# Fri, 02 Feb 2024 18:05:20 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:05:23 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:05:24 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:05:24 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:05:24 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:05:24 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:05:24 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:05:24 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94dc12f2a331ba1c98de6e05d4195fa2d8648e7e0b92a0c14b48e50a842cb8e`  
		Last Modified: Fri, 02 Feb 2024 18:07:07 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f5d34b4ed6ef3ccc8538dd9183cb2413cfaf0aff6d3dd05ebd2a2ea5e019bb`  
		Last Modified: Fri, 02 Feb 2024 18:07:11 GMT  
		Size: 64.0 MB (64004110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:9750912fcf40ed846d7e4c4ce6ff5e65e3eab14e0027c2994ca18babfad382da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203255461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639ec99ac884db1c2d30e900c0f0f3427493dcf843387a32f5d05fea4af13561`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:40:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 23:40:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 23:40:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 23:41:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:41:24 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 01 Feb 2024 23:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Feb 2024 23:41:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 01 Feb 2024 23:41:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 01 Feb 2024 23:41:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 01:19:49 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 01:19:49 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 01:19:50 GMT
ENV ORIENTDB_VERSION=3.2.26
# Fri, 02 Feb 2024 01:19:50 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b90008923e8b228d62d9181499015cf9
# Fri, 02 Feb 2024 01:19:50 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=e18a190249dca50b9cdeebdd1687037af0349b21
# Fri, 02 Feb 2024 01:19:51 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.26/orientdb-community-3.2.26.tar.gz
# Fri, 02 Feb 2024 01:19:57 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:20:06 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 01:20:07 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 01:20:07 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 01:20:08 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 01:20:08 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 01:20:08 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 01:20:08 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:708d435a5d58f83439fc15ec09677faf51737e48d41a910750f0f6e9ef7285fe`  
		Last Modified: Fri, 26 Jan 2024 09:13:01 GMT  
		Size: 27.5 MB (27526382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5fe67a29e28e299e1f69ba69453fcb55293e3c5137cc797c4b2099c524988f`  
		Last Modified: Thu, 01 Feb 2024 23:45:28 GMT  
		Size: 12.5 MB (12494090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76e8958a60be0d867bdd6836110ce7a6921682d3feddb1a335ceb4a6b158ff2`  
		Last Modified: Thu, 01 Feb 2024 23:45:39 GMT  
		Size: 99.2 MB (99229619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e7a84ed0b2e9dd2d83a10e5ee76d508e41bdf1bb4582e1ca975e9f08c3626e`  
		Last Modified: Thu, 01 Feb 2024 23:45:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175b3a789f678dfb0171341ad9085d2714c04014935c3d5cb0549e1811b74ab`  
		Last Modified: Thu, 01 Feb 2024 23:45:26 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f993e9655fb9f0c35b805af0b44a655f114c42d680adf263dec5797a834681`  
		Last Modified: Fri, 02 Feb 2024 01:20:41 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b42d38598d0494cdce91344fe2e9f4eff58799739139f8e1f661b7ec0cb7fe`  
		Last Modified: Fri, 02 Feb 2024 01:20:48 GMT  
		Size: 64.0 MB (64004126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:79f9c5971fabd125290694b45b04fdc55b623e05152ac9c39f2f787590c7ab93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207960514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdca6c16673b631a86bdb96e8731ed73089026e7bc498fc88e345e19a7ec350`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:10:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 02:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 02:10:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:10:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:10:13 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 02:10:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 02:10:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 02:10:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 09:24:31 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 09:24:31 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 09:24:31 GMT
ENV ORIENTDB_VERSION=3.2.26
# Fri, 02 Feb 2024 09:24:31 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b90008923e8b228d62d9181499015cf9
# Fri, 02 Feb 2024 09:24:31 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=e18a190249dca50b9cdeebdd1687037af0349b21
# Fri, 02 Feb 2024 09:24:32 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.26/orientdb-community-3.2.26.tar.gz
# Fri, 02 Feb 2024 09:24:36 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 09:24:39 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 09:24:40 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 09:24:40 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 09:24:40 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 09:24:40 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 09:24:40 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 09:24:40 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d95dd031b6947986c4e6ec03480d6cf870d0799e7c4aedb94072112e09bf46`  
		Last Modified: Fri, 02 Feb 2024 02:14:19 GMT  
		Size: 12.8 MB (12849205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbd5edc21c73a50bc2baddacc1de06dda6aa85b57b9c2fdb69d8e134481892c`  
		Last Modified: Fri, 02 Feb 2024 02:14:24 GMT  
		Size: 102.7 MB (102705833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6f3e998208a18db1290d8c87cdb484fc992e985d5853e40592eefe384dd172`  
		Last Modified: Fri, 02 Feb 2024 02:14:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0b92b348457895515e6390ad70809750c9a696861ac0f5fc499392d661e3ae`  
		Last Modified: Fri, 02 Feb 2024 02:14:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd4c26266999b5abf77af685de0a9593fd04f7086ba73da9a402d5647dab23`  
		Last Modified: Fri, 02 Feb 2024 09:25:02 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ef201e534fc13fcf84554f8567dbc761027977d4acfccccbbf1f1c78e5bb1e`  
		Last Modified: Fri, 02 Feb 2024 09:25:06 GMT  
		Size: 64.0 MB (64004126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:bdc5812edc4e66fa23eb7500bc1501bf884f7dc413a703da15cb2fda7ed80117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:5c65df387512f25e083fd7f790298824748d282705d12a8a558b2667fcef5003
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238934797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4091705b47cefbb219e39e274c7f129da452f438aac12bdada787099c8d7e494`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:05:15 GMT
ENV ORIENTDB_VERSION=3.2.26
# Fri, 02 Feb 2024 18:05:28 GMT
ENV ORIENTDB_DOWNLOAD_MD5=54d2f92a8042de7f1de3458ca884aa91
# Fri, 02 Feb 2024 18:05:28 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a03de96e3b904bbccc48c59eee618f9584e6609e
# Fri, 02 Feb 2024 18:05:28 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.26/orientdb-tp3-3.2.26.tar.gz
# Fri, 02 Feb 2024 18:05:32 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:05:36 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:05:36 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Fri, 02 Feb 2024 18:05:37 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:05:37 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:05:37 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:05:37 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:05:37 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:05:37 GMT
EXPOSE 8182
# Fri, 02 Feb 2024 18:05:37 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd501fdf3105367d728f6630c882445816645c4227c68217a93a04abe53b4a8`  
		Last Modified: Fri, 02 Feb 2024 18:07:22 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d051440f6ab710204ddae2c79663341af5dd7f2614aaccc2faaf86c48dbc44`  
		Last Modified: Fri, 02 Feb 2024 18:07:27 GMT  
		Size: 92.0 MB (91976680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea586816d3c0f8a6ce3f75e3ebf88efc523957d105e0f7c12e80ce13f5eac0c`  
		Last Modified: Fri, 02 Feb 2024 18:07:22 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:62fe4b508f74d9b14cd7bbcd2bd53cb4093fee7a3a1fc10d0ff0b967e35e322d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231229367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9fd58d4349d044de249a0b19798cadf91dfc617e33026b131f823479190b2a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:40:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 23:40:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 23:40:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 23:41:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:41:24 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 01 Feb 2024 23:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Feb 2024 23:41:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 01 Feb 2024 23:41:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 01 Feb 2024 23:41:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 01:19:49 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 01:19:49 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 01:19:50 GMT
ENV ORIENTDB_VERSION=3.2.26
# Fri, 02 Feb 2024 01:20:13 GMT
ENV ORIENTDB_DOWNLOAD_MD5=54d2f92a8042de7f1de3458ca884aa91
# Fri, 02 Feb 2024 01:20:13 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a03de96e3b904bbccc48c59eee618f9584e6609e
# Fri, 02 Feb 2024 01:20:13 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.26/orientdb-tp3-3.2.26.tar.gz
# Fri, 02 Feb 2024 01:20:19 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:20:28 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 01:20:29 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Fri, 02 Feb 2024 01:20:29 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 01:20:29 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 01:20:29 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 01:20:29 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 01:20:30 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 01:20:30 GMT
EXPOSE 8182
# Fri, 02 Feb 2024 01:20:30 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:708d435a5d58f83439fc15ec09677faf51737e48d41a910750f0f6e9ef7285fe`  
		Last Modified: Fri, 26 Jan 2024 09:13:01 GMT  
		Size: 27.5 MB (27526382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5fe67a29e28e299e1f69ba69453fcb55293e3c5137cc797c4b2099c524988f`  
		Last Modified: Thu, 01 Feb 2024 23:45:28 GMT  
		Size: 12.5 MB (12494090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76e8958a60be0d867bdd6836110ce7a6921682d3feddb1a335ceb4a6b158ff2`  
		Last Modified: Thu, 01 Feb 2024 23:45:39 GMT  
		Size: 99.2 MB (99229619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e7a84ed0b2e9dd2d83a10e5ee76d508e41bdf1bb4582e1ca975e9f08c3626e`  
		Last Modified: Thu, 01 Feb 2024 23:45:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175b3a789f678dfb0171341ad9085d2714c04014935c3d5cb0549e1811b74ab`  
		Last Modified: Thu, 01 Feb 2024 23:45:26 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c088738b0c16783c2085a4955b2ad7850412acd14f8bcd499aca50adea9db5`  
		Last Modified: Fri, 02 Feb 2024 01:21:00 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8afc5489bf1ca8d966d6bf58fc4105d549dc41b5c25d4eac2e96a2b1cb7772`  
		Last Modified: Fri, 02 Feb 2024 01:21:10 GMT  
		Size: 92.0 MB (91976656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1734cf4a04f9e02a0736098e6fdd9e03c21d0a41bb83bc893d51cc7b747929d`  
		Last Modified: Fri, 02 Feb 2024 01:21:00 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:ee7449b21bb929030e0f1cab6c745b1c29b5a96aa91824988a1dee29da32b319
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235934446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5664e5c9c5442cff9ba6006b1690a4538f164d669f171388faefa6ef7ed2283b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:10:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 02:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 02:10:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:10:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:10:13 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 02:10:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 02:10:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 02:10:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 09:24:31 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 09:24:31 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 09:24:31 GMT
ENV ORIENTDB_VERSION=3.2.26
# Fri, 02 Feb 2024 09:24:43 GMT
ENV ORIENTDB_DOWNLOAD_MD5=54d2f92a8042de7f1de3458ca884aa91
# Fri, 02 Feb 2024 09:24:43 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a03de96e3b904bbccc48c59eee618f9584e6609e
# Fri, 02 Feb 2024 09:24:43 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.26/orientdb-tp3-3.2.26.tar.gz
# Fri, 02 Feb 2024 09:24:46 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 09:24:50 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 09:24:50 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Fri, 02 Feb 2024 09:24:50 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 09:24:51 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 09:24:51 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 09:24:51 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 09:24:51 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 09:24:51 GMT
EXPOSE 8182
# Fri, 02 Feb 2024 09:24:51 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d95dd031b6947986c4e6ec03480d6cf870d0799e7c4aedb94072112e09bf46`  
		Last Modified: Fri, 02 Feb 2024 02:14:19 GMT  
		Size: 12.8 MB (12849205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbd5edc21c73a50bc2baddacc1de06dda6aa85b57b9c2fdb69d8e134481892c`  
		Last Modified: Fri, 02 Feb 2024 02:14:24 GMT  
		Size: 102.7 MB (102705833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6f3e998208a18db1290d8c87cdb484fc992e985d5853e40592eefe384dd172`  
		Last Modified: Fri, 02 Feb 2024 02:14:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0b92b348457895515e6390ad70809750c9a696861ac0f5fc499392d661e3ae`  
		Last Modified: Fri, 02 Feb 2024 02:14:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3228f128cd071e05645c13a074f57cae0655f852243159b792d1f50f7e8f3d`  
		Last Modified: Fri, 02 Feb 2024 09:25:16 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7271f5cc15cb1467f0b1dce87573653569d4cffee5e3476dfce01784cf7fda11`  
		Last Modified: Fri, 02 Feb 2024 09:25:25 GMT  
		Size: 92.0 MB (91976684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75d4497bed284380ace5d88aac1e697a1a7a20dd07908aef28c2b2300847fbb`  
		Last Modified: Fri, 02 Feb 2024 09:25:16 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.27`

```console
$ docker pull orientdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `orientdb:3.2.27-tp3`

```console
$ docker pull orientdb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:d2b6c5d838821a36a5070d948feddd2526ac142502303baeca0c597c2f567f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:72ace32766c923d890bed1c56e2f774c0f5772b15133b091fb1a4736a0e3f257
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210960851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bc8d7bae2eabfa5996ce3ceea6047a8547d5cbd73daac5694c2b02c89ea47f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:42:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:37 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 18:05:15 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 18:05:15 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 18:05:15 GMT
ENV ORIENTDB_VERSION=3.2.26
# Fri, 02 Feb 2024 18:05:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b90008923e8b228d62d9181499015cf9
# Fri, 02 Feb 2024 18:05:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=e18a190249dca50b9cdeebdd1687037af0349b21
# Fri, 02 Feb 2024 18:05:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.26/orientdb-community-3.2.26.tar.gz
# Fri, 02 Feb 2024 18:05:20 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 18:05:23 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 18:05:24 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 18:05:24 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 18:05:24 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 18:05:24 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 18:05:24 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 18:05:24 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b311b806c85db4346e8b1835111a4685f302d3b9df8c823b84513d5a390fa9`  
		Last Modified: Fri, 02 Feb 2024 07:47:37 GMT  
		Size: 12.9 MB (12906315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca6a207a8e7a80be1d2a50f72153f172df979e0303a07bebcf4d227f52008c`  
		Last Modified: Fri, 02 Feb 2024 07:47:43 GMT  
		Size: 103.6 MB (103601294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826877f016d85e74d96235667bffee85ae6367c4a6557ebb624fa4763b8c5700`  
		Last Modified: Fri, 02 Feb 2024 07:47:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77c5b1038cba6c10d34b66fbe72283aae2bc733387e95b98ea685ba9643ab1c`  
		Last Modified: Fri, 02 Feb 2024 07:47:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94dc12f2a331ba1c98de6e05d4195fa2d8648e7e0b92a0c14b48e50a842cb8e`  
		Last Modified: Fri, 02 Feb 2024 18:07:07 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f5d34b4ed6ef3ccc8538dd9183cb2413cfaf0aff6d3dd05ebd2a2ea5e019bb`  
		Last Modified: Fri, 02 Feb 2024 18:07:11 GMT  
		Size: 64.0 MB (64004110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:9750912fcf40ed846d7e4c4ce6ff5e65e3eab14e0027c2994ca18babfad382da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203255461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639ec99ac884db1c2d30e900c0f0f3427493dcf843387a32f5d05fea4af13561`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:40:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 23:40:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 23:40:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 23:41:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:41:24 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 01 Feb 2024 23:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Feb 2024 23:41:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 01 Feb 2024 23:41:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 01 Feb 2024 23:41:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 01:19:49 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 01:19:49 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 01:19:50 GMT
ENV ORIENTDB_VERSION=3.2.26
# Fri, 02 Feb 2024 01:19:50 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b90008923e8b228d62d9181499015cf9
# Fri, 02 Feb 2024 01:19:50 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=e18a190249dca50b9cdeebdd1687037af0349b21
# Fri, 02 Feb 2024 01:19:51 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.26/orientdb-community-3.2.26.tar.gz
# Fri, 02 Feb 2024 01:19:57 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:20:06 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 01:20:07 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 01:20:07 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 01:20:08 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 01:20:08 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 01:20:08 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 01:20:08 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:708d435a5d58f83439fc15ec09677faf51737e48d41a910750f0f6e9ef7285fe`  
		Last Modified: Fri, 26 Jan 2024 09:13:01 GMT  
		Size: 27.5 MB (27526382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5fe67a29e28e299e1f69ba69453fcb55293e3c5137cc797c4b2099c524988f`  
		Last Modified: Thu, 01 Feb 2024 23:45:28 GMT  
		Size: 12.5 MB (12494090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76e8958a60be0d867bdd6836110ce7a6921682d3feddb1a335ceb4a6b158ff2`  
		Last Modified: Thu, 01 Feb 2024 23:45:39 GMT  
		Size: 99.2 MB (99229619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e7a84ed0b2e9dd2d83a10e5ee76d508e41bdf1bb4582e1ca975e9f08c3626e`  
		Last Modified: Thu, 01 Feb 2024 23:45:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175b3a789f678dfb0171341ad9085d2714c04014935c3d5cb0549e1811b74ab`  
		Last Modified: Thu, 01 Feb 2024 23:45:26 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f993e9655fb9f0c35b805af0b44a655f114c42d680adf263dec5797a834681`  
		Last Modified: Fri, 02 Feb 2024 01:20:41 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b42d38598d0494cdce91344fe2e9f4eff58799739139f8e1f661b7ec0cb7fe`  
		Last Modified: Fri, 02 Feb 2024 01:20:48 GMT  
		Size: 64.0 MB (64004126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:79f9c5971fabd125290694b45b04fdc55b623e05152ac9c39f2f787590c7ab93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207960514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdca6c16673b631a86bdb96e8731ed73089026e7bc498fc88e345e19a7ec350`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:10:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 02:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 02:10:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:10:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:10:13 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 02:10:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 02:10:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 02:10:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 09:24:31 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Feb 2024 09:24:31 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Feb 2024 09:24:31 GMT
ENV ORIENTDB_VERSION=3.2.26
# Fri, 02 Feb 2024 09:24:31 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b90008923e8b228d62d9181499015cf9
# Fri, 02 Feb 2024 09:24:31 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=e18a190249dca50b9cdeebdd1687037af0349b21
# Fri, 02 Feb 2024 09:24:32 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.26/orientdb-community-3.2.26.tar.gz
# Fri, 02 Feb 2024 09:24:36 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 09:24:39 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Feb 2024 09:24:40 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 09:24:40 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Feb 2024 09:24:40 GMT
WORKDIR /orientdb
# Fri, 02 Feb 2024 09:24:40 GMT
EXPOSE 2424
# Fri, 02 Feb 2024 09:24:40 GMT
EXPOSE 2480
# Fri, 02 Feb 2024 09:24:40 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d95dd031b6947986c4e6ec03480d6cf870d0799e7c4aedb94072112e09bf46`  
		Last Modified: Fri, 02 Feb 2024 02:14:19 GMT  
		Size: 12.8 MB (12849205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbd5edc21c73a50bc2baddacc1de06dda6aa85b57b9c2fdb69d8e134481892c`  
		Last Modified: Fri, 02 Feb 2024 02:14:24 GMT  
		Size: 102.7 MB (102705833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6f3e998208a18db1290d8c87cdb484fc992e985d5853e40592eefe384dd172`  
		Last Modified: Fri, 02 Feb 2024 02:14:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0b92b348457895515e6390ad70809750c9a696861ac0f5fc499392d661e3ae`  
		Last Modified: Fri, 02 Feb 2024 02:14:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd4c26266999b5abf77af685de0a9593fd04f7086ba73da9a402d5647dab23`  
		Last Modified: Fri, 02 Feb 2024 09:25:02 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ef201e534fc13fcf84554f8567dbc761027977d4acfccccbbf1f1c78e5bb1e`  
		Last Modified: Fri, 02 Feb 2024 09:25:06 GMT  
		Size: 64.0 MB (64004126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
