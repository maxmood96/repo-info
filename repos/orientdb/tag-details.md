<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.20`](#orientdb3120)
-	[`orientdb:3.1.20-tp3`](#orientdb3120-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.28`](#orientdb3228)
-	[`orientdb:3.2.28-tp3`](#orientdb3228-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:8bba0e340d1bc1397d162a7f750038407a353fa4467d421e36b6ec3a462ecef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:f83f55b2fe726168f4360cab01498151099b0d4fa1741917b38137227b1db174
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (200039613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb6f87937571c5e321dde0c0385e719afaafefd842cfded126dba7761a4d4cc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:02:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:02:33 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 06:02:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 06:02:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 06:02:39 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:02:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 14:33:47 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 14:33:47 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 14:34:19 GMT
ENV ORIENTDB_VERSION=3.1.20
# Wed, 06 Mar 2024 14:34:19 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Wed, 06 Mar 2024 14:34:19 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Wed, 06 Mar 2024 14:34:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Wed, 06 Mar 2024 14:34:24 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 14:34:27 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 14:34:27 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:34:27 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 14:34:27 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 14:34:28 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 14:34:28 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 14:34:28 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8069355d5739c7da6dbe5ac9692d576813db815ada8e298f80c69c9624b46e9b`  
		Last Modified: Wed, 06 Mar 2024 06:07:30 GMT  
		Size: 12.9 MB (12904599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0818127cd97b321529b68d069c224d5847d3d40a93d2ac194b85d97e7d06269`  
		Last Modified: Wed, 06 Mar 2024 06:07:36 GMT  
		Size: 103.6 MB (103601240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db15aff3aedb36071e783b4c821f5244536c6bb5d8d6a4af69a143ebe525c0e3`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8727e407d8afb0bc127215ae7755d265a18fae32a798b36e72e1aa732ade25`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0e9bd8a2f2584987d4219e12b4e6c72c3f505569bd0a92e86c601f00957843`  
		Last Modified: Wed, 06 Mar 2024 14:35:26 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e874744ce85db46bfb4199a1ce0e0756201b0f87636c475bf8d431b9571904f9`  
		Last Modified: Wed, 06 Mar 2024 14:35:29 GMT  
		Size: 53.1 MB (53081228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:70c09e66d37fc201cdce7a9474bf1a17f0a6a7b502a85b36444e2a2cd6ae1467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:e5677bac5e9c288a0d8b16c0b24b1d5656aa2eed28348e69b0796daabf83182d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223046649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c657426e4cb6ce23fa1516ce44cbfe6dfb726fd4f4894f1bbc57c15bef66728`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:02:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:02:33 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 06:02:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 06:02:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 06:02:39 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:02:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 14:33:47 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 14:33:47 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 14:34:19 GMT
ENV ORIENTDB_VERSION=3.1.20
# Wed, 06 Mar 2024 14:34:31 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Wed, 06 Mar 2024 14:34:31 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Wed, 06 Mar 2024 14:34:31 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Wed, 06 Mar 2024 14:34:36 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 14:34:42 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 14:34:42 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Wed, 06 Mar 2024 14:34:42 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:34:42 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 14:34:42 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 14:34:43 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 14:34:43 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 14:34:43 GMT
EXPOSE 8182
# Wed, 06 Mar 2024 14:34:43 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8069355d5739c7da6dbe5ac9692d576813db815ada8e298f80c69c9624b46e9b`  
		Last Modified: Wed, 06 Mar 2024 06:07:30 GMT  
		Size: 12.9 MB (12904599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0818127cd97b321529b68d069c224d5847d3d40a93d2ac194b85d97e7d06269`  
		Last Modified: Wed, 06 Mar 2024 06:07:36 GMT  
		Size: 103.6 MB (103601240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db15aff3aedb36071e783b4c821f5244536c6bb5d8d6a4af69a143ebe525c0e3`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8727e407d8afb0bc127215ae7755d265a18fae32a798b36e72e1aa732ade25`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9e6cce5497a7b2ba0314f26e39a4d4d3288faf4b42c62741dabeff44449c25`  
		Last Modified: Wed, 06 Mar 2024 14:35:38 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0beabd9866e4b57c94173dce35a8d31c5a94b32e63ac3a937aca8c847cfdb2f`  
		Last Modified: Wed, 06 Mar 2024 14:35:42 GMT  
		Size: 76.1 MB (76086885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176ed8b7f5b1965a69e9e0db9dfef13134eb1c661d12ec498c86825d4b68c3a8`  
		Last Modified: Wed, 06 Mar 2024 14:35:38 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:8bba0e340d1bc1397d162a7f750038407a353fa4467d421e36b6ec3a462ecef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:f83f55b2fe726168f4360cab01498151099b0d4fa1741917b38137227b1db174
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (200039613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb6f87937571c5e321dde0c0385e719afaafefd842cfded126dba7761a4d4cc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:02:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:02:33 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 06:02:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 06:02:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 06:02:39 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:02:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 14:33:47 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 14:33:47 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 14:34:19 GMT
ENV ORIENTDB_VERSION=3.1.20
# Wed, 06 Mar 2024 14:34:19 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Wed, 06 Mar 2024 14:34:19 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Wed, 06 Mar 2024 14:34:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Wed, 06 Mar 2024 14:34:24 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 14:34:27 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 14:34:27 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:34:27 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 14:34:27 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 14:34:28 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 14:34:28 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 14:34:28 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8069355d5739c7da6dbe5ac9692d576813db815ada8e298f80c69c9624b46e9b`  
		Last Modified: Wed, 06 Mar 2024 06:07:30 GMT  
		Size: 12.9 MB (12904599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0818127cd97b321529b68d069c224d5847d3d40a93d2ac194b85d97e7d06269`  
		Last Modified: Wed, 06 Mar 2024 06:07:36 GMT  
		Size: 103.6 MB (103601240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db15aff3aedb36071e783b4c821f5244536c6bb5d8d6a4af69a143ebe525c0e3`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8727e407d8afb0bc127215ae7755d265a18fae32a798b36e72e1aa732ade25`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0e9bd8a2f2584987d4219e12b4e6c72c3f505569bd0a92e86c601f00957843`  
		Last Modified: Wed, 06 Mar 2024 14:35:26 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e874744ce85db46bfb4199a1ce0e0756201b0f87636c475bf8d431b9571904f9`  
		Last Modified: Wed, 06 Mar 2024 14:35:29 GMT  
		Size: 53.1 MB (53081228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:70c09e66d37fc201cdce7a9474bf1a17f0a6a7b502a85b36444e2a2cd6ae1467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:e5677bac5e9c288a0d8b16c0b24b1d5656aa2eed28348e69b0796daabf83182d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223046649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c657426e4cb6ce23fa1516ce44cbfe6dfb726fd4f4894f1bbc57c15bef66728`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:02:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:02:33 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 06:02:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 06:02:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 06:02:39 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:02:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 14:33:47 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 14:33:47 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 14:34:19 GMT
ENV ORIENTDB_VERSION=3.1.20
# Wed, 06 Mar 2024 14:34:31 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Wed, 06 Mar 2024 14:34:31 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Wed, 06 Mar 2024 14:34:31 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Wed, 06 Mar 2024 14:34:36 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 14:34:42 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 14:34:42 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Wed, 06 Mar 2024 14:34:42 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:34:42 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 14:34:42 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 14:34:43 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 14:34:43 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 14:34:43 GMT
EXPOSE 8182
# Wed, 06 Mar 2024 14:34:43 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8069355d5739c7da6dbe5ac9692d576813db815ada8e298f80c69c9624b46e9b`  
		Last Modified: Wed, 06 Mar 2024 06:07:30 GMT  
		Size: 12.9 MB (12904599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0818127cd97b321529b68d069c224d5847d3d40a93d2ac194b85d97e7d06269`  
		Last Modified: Wed, 06 Mar 2024 06:07:36 GMT  
		Size: 103.6 MB (103601240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db15aff3aedb36071e783b4c821f5244536c6bb5d8d6a4af69a143ebe525c0e3`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8727e407d8afb0bc127215ae7755d265a18fae32a798b36e72e1aa732ade25`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9e6cce5497a7b2ba0314f26e39a4d4d3288faf4b42c62741dabeff44449c25`  
		Last Modified: Wed, 06 Mar 2024 14:35:38 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0beabd9866e4b57c94173dce35a8d31c5a94b32e63ac3a937aca8c847cfdb2f`  
		Last Modified: Wed, 06 Mar 2024 14:35:42 GMT  
		Size: 76.1 MB (76086885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176ed8b7f5b1965a69e9e0db9dfef13134eb1c661d12ec498c86825d4b68c3a8`  
		Last Modified: Wed, 06 Mar 2024 14:35:38 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:ce2d718b9ad1b9f4388f2c02426f1b0cc91a834d925aaaf1d5e1c96cdbeff4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2` - linux; amd64

```console
$ docker pull orientdb@sha256:a7295ad7d967a12abbdd1099f6d7dc24f3e647654203af9015a19031b429fa0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219874120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4688bddab13dcfa4c44f7637db004ae1ad807aed63cf64669f98561afe739b74`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:02:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:02:33 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 06:02:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 06:02:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 06:02:39 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:02:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 14:33:47 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 14:33:47 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_DOWNLOAD_MD5=c189d2795b8b08356318a8b262eeab43
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=af0fc0eee9a106f96d60732a1026ff4cad78e778
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.28/orientdb-community-3.2.28.tar.gz
# Wed, 06 Mar 2024 14:33:54 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 14:33:58 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 14:33:58 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:33:58 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 14:33:58 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 14:33:59 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 14:33:59 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 14:33:59 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8069355d5739c7da6dbe5ac9692d576813db815ada8e298f80c69c9624b46e9b`  
		Last Modified: Wed, 06 Mar 2024 06:07:30 GMT  
		Size: 12.9 MB (12904599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0818127cd97b321529b68d069c224d5847d3d40a93d2ac194b85d97e7d06269`  
		Last Modified: Wed, 06 Mar 2024 06:07:36 GMT  
		Size: 103.6 MB (103601240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db15aff3aedb36071e783b4c821f5244536c6bb5d8d6a4af69a143ebe525c0e3`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8727e407d8afb0bc127215ae7755d265a18fae32a798b36e72e1aa732ade25`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470a50a440c6e00c93f0af5c640761aa79b7a6017053e1b10ec86a31c4c91fd4`  
		Last Modified: Wed, 06 Mar 2024 14:34:56 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f577cf8a842e0bd3a1e1ab196514d912377354bc4383c2ffe6fd1dc63ff240`  
		Last Modified: Wed, 06 Mar 2024 14:35:00 GMT  
		Size: 72.9 MB (72915736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:838a10cac41d33c99bd0424270219654f4f86b667ba9c1f06bfed430fa7f8280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212172831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3b9b6d07760528c89540b9c19fecbe559dc4fb369fa362f099806d3d26d4d1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:16:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 02:16:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:16:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 02:17:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:17:16 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 02:17:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 02:17:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 02:17:32 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 02:17:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 05:26:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 05:26:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 05:26:17 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 05:26:17 GMT
ENV ORIENTDB_DOWNLOAD_MD5=c189d2795b8b08356318a8b262eeab43
# Wed, 06 Mar 2024 05:26:17 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=af0fc0eee9a106f96d60732a1026ff4cad78e778
# Wed, 06 Mar 2024 05:26:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.28/orientdb-community-3.2.28.tar.gz
# Wed, 06 Mar 2024 05:26:24 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:26:32 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 05:26:33 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 05:26:33 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 05:26:33 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 05:26:34 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 05:26:34 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 05:26:35 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ec27e2ded8ffd5739eb9afa16988019dfc7a5185984fd50364954711029c6`  
		Last Modified: Wed, 06 Mar 2024 02:23:08 GMT  
		Size: 12.5 MB (12492077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6476eac220dc15b7b008e7018b3369704012af07c9a9d3269eeeff510bb6534`  
		Last Modified: Wed, 06 Mar 2024 02:23:16 GMT  
		Size: 99.2 MB (99229800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916d4cc71957468e2218be3dc202e2c510c2342d67c66bcc991131af968b0d1`  
		Last Modified: Wed, 06 Mar 2024 02:23:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc776191e565b5ba8f39a35bfd38bb8b67fa31df2f2f909425913f7e02c399c`  
		Last Modified: Wed, 06 Mar 2024 02:23:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a59ceae44055be037f945ec1192c57e5a3c8405cec218742dc7fca595ace3a`  
		Last Modified: Wed, 06 Mar 2024 05:27:15 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4634028dbd07fa153bcc76aff47053819b61db68e5b1823c8d658289da417bdf`  
		Last Modified: Wed, 06 Mar 2024 05:27:21 GMT  
		Size: 72.9 MB (72915775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:eb09b676e196b9de314924453dad5ada53cb4b0b9c61e91b9d109c9d9442017f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216869742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af79ce8f90812c260ef5e983a1b7968fce0995836911165c8377d6166dfd389`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:01:49 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 04:01:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 04:01:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 04:01:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:01:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 08:38:29 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 08:38:29 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_DOWNLOAD_MD5=c189d2795b8b08356318a8b262eeab43
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=af0fc0eee9a106f96d60732a1026ff4cad78e778
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.28/orientdb-community-3.2.28.tar.gz
# Wed, 06 Mar 2024 08:38:38 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 08:38:41 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 08:38:42 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 08:38:42 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 08:38:42 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 08:38:42 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 08:38:42 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 08:38:42 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7620c0cc62807824d2242c6cef9f4c58531a799ce6c124c214d4a7a5ca35d0`  
		Last Modified: Wed, 06 Mar 2024 04:05:53 GMT  
		Size: 102.7 MB (102705771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb2ab6d6d84cb5c81b9029bdb29a31d3845d0aa350868c7a1456dcd93b9778c`  
		Last Modified: Wed, 06 Mar 2024 04:05:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4ca9405ba8d165ed87c13f38e95b6b519f9d8b4d4c97040cb9ac6c5ade21e3`  
		Last Modified: Wed, 06 Mar 2024 04:05:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d70610fff7ecdac052d49693a8607211e537d3063c4c61508902ef53ac7b1d`  
		Last Modified: Wed, 06 Mar 2024 08:39:03 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c8e70152ab74c9ed3872c778e1588015599bce6d13e684016381cb398bb832`  
		Last Modified: Wed, 06 Mar 2024 08:39:07 GMT  
		Size: 72.9 MB (72915721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:d17f9c2518ee12ab3ea537dea8ae7ef16454cfcb3fdb2fb9be1b421df46643ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:7e3d53801581b5ea0ed3db2234baec73c8c56c5972240adba52950d41166169f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247851789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2505db1dd16d32369e236298507b056fc56cedb9d11a7e66992678c016292970`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:02:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:02:33 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 06:02:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 06:02:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 06:02:39 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:02:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 14:33:47 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 14:33:47 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 14:34:04 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cf9819e6d0b2575c64348e6c7c53d40d
# Wed, 06 Mar 2024 14:34:04 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=25df0a72243b3a8317afba691971b168d415907a
# Wed, 06 Mar 2024 14:34:04 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.28/orientdb-tp3-3.2.28.tar.gz
# Wed, 06 Mar 2024 14:34:09 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 14:34:14 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 14:34:15 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Wed, 06 Mar 2024 14:34:15 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:34:15 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 14:34:15 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 14:34:15 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 14:34:15 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 14:34:15 GMT
EXPOSE 8182
# Wed, 06 Mar 2024 14:34:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8069355d5739c7da6dbe5ac9692d576813db815ada8e298f80c69c9624b46e9b`  
		Last Modified: Wed, 06 Mar 2024 06:07:30 GMT  
		Size: 12.9 MB (12904599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0818127cd97b321529b68d069c224d5847d3d40a93d2ac194b85d97e7d06269`  
		Last Modified: Wed, 06 Mar 2024 06:07:36 GMT  
		Size: 103.6 MB (103601240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db15aff3aedb36071e783b4c821f5244536c6bb5d8d6a4af69a143ebe525c0e3`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8727e407d8afb0bc127215ae7755d265a18fae32a798b36e72e1aa732ade25`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a66e2266d344ad268dc7ab7f1a52c09e25ce8c27a2b9d35d982aad1517b263f`  
		Last Modified: Wed, 06 Mar 2024 14:35:11 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d957474616522d2cbe456af7f8009fd1d795c017f45183b9cb65230ff7b89f1c`  
		Last Modified: Wed, 06 Mar 2024 14:35:17 GMT  
		Size: 100.9 MB (100892029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12566aca98437df14cfbe03441a123943f21d10af398c902d6cd5daebae91460`  
		Last Modified: Wed, 06 Mar 2024 14:35:11 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:a2f00667d1836008b355e7a71ee3910ff1f8eba4318a8586149ccc9262888ab9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240150417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca8d7376329c360c43f51de8f48165403c3f2b1bfa18be2dac3a1bd918b6d10`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:16:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 02:16:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:16:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 02:17:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:17:16 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 02:17:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 02:17:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 02:17:32 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 02:17:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 05:26:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 05:26:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 05:26:17 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 05:26:40 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cf9819e6d0b2575c64348e6c7c53d40d
# Wed, 06 Mar 2024 05:26:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=25df0a72243b3a8317afba691971b168d415907a
# Wed, 06 Mar 2024 05:26:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.28/orientdb-tp3-3.2.28.tar.gz
# Wed, 06 Mar 2024 05:26:47 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:26:56 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 05:26:57 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Wed, 06 Mar 2024 05:26:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 05:26:58 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 05:26:58 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 05:26:58 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 05:26:59 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 05:26:59 GMT
EXPOSE 8182
# Wed, 06 Mar 2024 05:26:59 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ec27e2ded8ffd5739eb9afa16988019dfc7a5185984fd50364954711029c6`  
		Last Modified: Wed, 06 Mar 2024 02:23:08 GMT  
		Size: 12.5 MB (12492077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6476eac220dc15b7b008e7018b3369704012af07c9a9d3269eeeff510bb6534`  
		Last Modified: Wed, 06 Mar 2024 02:23:16 GMT  
		Size: 99.2 MB (99229800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916d4cc71957468e2218be3dc202e2c510c2342d67c66bcc991131af968b0d1`  
		Last Modified: Wed, 06 Mar 2024 02:23:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc776191e565b5ba8f39a35bfd38bb8b67fa31df2f2f909425913f7e02c399c`  
		Last Modified: Wed, 06 Mar 2024 02:23:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d4bc116242e93f9812fd40f45507c603ba44b4c579d84230839c1448d392cd`  
		Last Modified: Wed, 06 Mar 2024 05:27:32 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697de7107c93329cb80707b5c28a9c5bd8c03a1c536db2d0b0ac017a97611feb`  
		Last Modified: Wed, 06 Mar 2024 05:27:42 GMT  
		Size: 100.9 MB (100891984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896a16af8f629e964d5fbc458c43c6444ae7097777d9a851b4d85a4ea206996b`  
		Last Modified: Wed, 06 Mar 2024 05:27:32 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:37bc29048adf2951bb089f41632b1759bc92b614040c131fa70d6c5c59a887e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244847385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810b89d08e343df3ad479314c185bdb38d6ce34ec40e025223194115e622e43a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:01:49 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 04:01:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 04:01:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 04:01:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:01:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 08:38:29 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 08:38:29 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 08:38:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cf9819e6d0b2575c64348e6c7c53d40d
# Wed, 06 Mar 2024 08:38:45 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=25df0a72243b3a8317afba691971b168d415907a
# Wed, 06 Mar 2024 08:38:45 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.28/orientdb-tp3-3.2.28.tar.gz
# Wed, 06 Mar 2024 08:38:49 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 08:38:53 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 08:38:54 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Wed, 06 Mar 2024 08:38:54 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 08:38:54 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 08:38:54 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 08:38:54 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 08:38:54 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 08:38:54 GMT
EXPOSE 8182
# Wed, 06 Mar 2024 08:38:55 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7620c0cc62807824d2242c6cef9f4c58531a799ce6c124c214d4a7a5ca35d0`  
		Last Modified: Wed, 06 Mar 2024 04:05:53 GMT  
		Size: 102.7 MB (102705771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb2ab6d6d84cb5c81b9029bdb29a31d3845d0aa350868c7a1456dcd93b9778c`  
		Last Modified: Wed, 06 Mar 2024 04:05:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4ca9405ba8d165ed87c13f38e95b6b519f9d8b4d4c97040cb9ac6c5ade21e3`  
		Last Modified: Wed, 06 Mar 2024 04:05:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984f4c0a0760a440546cb4014f3b07e414b351905ae0d0b71fd6bad6c3cf5f19`  
		Last Modified: Wed, 06 Mar 2024 08:39:17 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71041878fa22655380edb5c2026fc1664c3cdb42150ea8625075c5deb554640`  
		Last Modified: Wed, 06 Mar 2024 08:39:22 GMT  
		Size: 100.9 MB (100891982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92aac00e67ccf2a9e6ded11dfae579c3dd91d53702a5ebe5199c9908c9586ec7`  
		Last Modified: Wed, 06 Mar 2024 08:39:17 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.28`

```console
$ docker pull orientdb@sha256:ce2d718b9ad1b9f4388f2c02426f1b0cc91a834d925aaaf1d5e1c96cdbeff4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2.28` - linux; amd64

```console
$ docker pull orientdb@sha256:a7295ad7d967a12abbdd1099f6d7dc24f3e647654203af9015a19031b429fa0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219874120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4688bddab13dcfa4c44f7637db004ae1ad807aed63cf64669f98561afe739b74`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:02:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:02:33 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 06:02:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 06:02:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 06:02:39 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:02:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 14:33:47 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 14:33:47 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_DOWNLOAD_MD5=c189d2795b8b08356318a8b262eeab43
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=af0fc0eee9a106f96d60732a1026ff4cad78e778
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.28/orientdb-community-3.2.28.tar.gz
# Wed, 06 Mar 2024 14:33:54 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 14:33:58 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 14:33:58 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:33:58 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 14:33:58 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 14:33:59 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 14:33:59 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 14:33:59 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8069355d5739c7da6dbe5ac9692d576813db815ada8e298f80c69c9624b46e9b`  
		Last Modified: Wed, 06 Mar 2024 06:07:30 GMT  
		Size: 12.9 MB (12904599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0818127cd97b321529b68d069c224d5847d3d40a93d2ac194b85d97e7d06269`  
		Last Modified: Wed, 06 Mar 2024 06:07:36 GMT  
		Size: 103.6 MB (103601240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db15aff3aedb36071e783b4c821f5244536c6bb5d8d6a4af69a143ebe525c0e3`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8727e407d8afb0bc127215ae7755d265a18fae32a798b36e72e1aa732ade25`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470a50a440c6e00c93f0af5c640761aa79b7a6017053e1b10ec86a31c4c91fd4`  
		Last Modified: Wed, 06 Mar 2024 14:34:56 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f577cf8a842e0bd3a1e1ab196514d912377354bc4383c2ffe6fd1dc63ff240`  
		Last Modified: Wed, 06 Mar 2024 14:35:00 GMT  
		Size: 72.9 MB (72915736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.28` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:838a10cac41d33c99bd0424270219654f4f86b667ba9c1f06bfed430fa7f8280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212172831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3b9b6d07760528c89540b9c19fecbe559dc4fb369fa362f099806d3d26d4d1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:16:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 02:16:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:16:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 02:17:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:17:16 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 02:17:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 02:17:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 02:17:32 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 02:17:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 05:26:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 05:26:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 05:26:17 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 05:26:17 GMT
ENV ORIENTDB_DOWNLOAD_MD5=c189d2795b8b08356318a8b262eeab43
# Wed, 06 Mar 2024 05:26:17 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=af0fc0eee9a106f96d60732a1026ff4cad78e778
# Wed, 06 Mar 2024 05:26:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.28/orientdb-community-3.2.28.tar.gz
# Wed, 06 Mar 2024 05:26:24 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:26:32 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 05:26:33 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 05:26:33 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 05:26:33 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 05:26:34 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 05:26:34 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 05:26:35 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ec27e2ded8ffd5739eb9afa16988019dfc7a5185984fd50364954711029c6`  
		Last Modified: Wed, 06 Mar 2024 02:23:08 GMT  
		Size: 12.5 MB (12492077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6476eac220dc15b7b008e7018b3369704012af07c9a9d3269eeeff510bb6534`  
		Last Modified: Wed, 06 Mar 2024 02:23:16 GMT  
		Size: 99.2 MB (99229800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916d4cc71957468e2218be3dc202e2c510c2342d67c66bcc991131af968b0d1`  
		Last Modified: Wed, 06 Mar 2024 02:23:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc776191e565b5ba8f39a35bfd38bb8b67fa31df2f2f909425913f7e02c399c`  
		Last Modified: Wed, 06 Mar 2024 02:23:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a59ceae44055be037f945ec1192c57e5a3c8405cec218742dc7fca595ace3a`  
		Last Modified: Wed, 06 Mar 2024 05:27:15 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4634028dbd07fa153bcc76aff47053819b61db68e5b1823c8d658289da417bdf`  
		Last Modified: Wed, 06 Mar 2024 05:27:21 GMT  
		Size: 72.9 MB (72915775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.28` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:eb09b676e196b9de314924453dad5ada53cb4b0b9c61e91b9d109c9d9442017f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216869742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af79ce8f90812c260ef5e983a1b7968fce0995836911165c8377d6166dfd389`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:01:49 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 04:01:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 04:01:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 04:01:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:01:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 08:38:29 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 08:38:29 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_DOWNLOAD_MD5=c189d2795b8b08356318a8b262eeab43
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=af0fc0eee9a106f96d60732a1026ff4cad78e778
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.28/orientdb-community-3.2.28.tar.gz
# Wed, 06 Mar 2024 08:38:38 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 08:38:41 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 08:38:42 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 08:38:42 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 08:38:42 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 08:38:42 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 08:38:42 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 08:38:42 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7620c0cc62807824d2242c6cef9f4c58531a799ce6c124c214d4a7a5ca35d0`  
		Last Modified: Wed, 06 Mar 2024 04:05:53 GMT  
		Size: 102.7 MB (102705771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb2ab6d6d84cb5c81b9029bdb29a31d3845d0aa350868c7a1456dcd93b9778c`  
		Last Modified: Wed, 06 Mar 2024 04:05:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4ca9405ba8d165ed87c13f38e95b6b519f9d8b4d4c97040cb9ac6c5ade21e3`  
		Last Modified: Wed, 06 Mar 2024 04:05:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d70610fff7ecdac052d49693a8607211e537d3063c4c61508902ef53ac7b1d`  
		Last Modified: Wed, 06 Mar 2024 08:39:03 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c8e70152ab74c9ed3872c778e1588015599bce6d13e684016381cb398bb832`  
		Last Modified: Wed, 06 Mar 2024 08:39:07 GMT  
		Size: 72.9 MB (72915721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.28-tp3`

```console
$ docker pull orientdb@sha256:d17f9c2518ee12ab3ea537dea8ae7ef16454cfcb3fdb2fb9be1b421df46643ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2.28-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:7e3d53801581b5ea0ed3db2234baec73c8c56c5972240adba52950d41166169f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247851789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2505db1dd16d32369e236298507b056fc56cedb9d11a7e66992678c016292970`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:02:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:02:33 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 06:02:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 06:02:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 06:02:39 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:02:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 14:33:47 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 14:33:47 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 14:34:04 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cf9819e6d0b2575c64348e6c7c53d40d
# Wed, 06 Mar 2024 14:34:04 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=25df0a72243b3a8317afba691971b168d415907a
# Wed, 06 Mar 2024 14:34:04 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.28/orientdb-tp3-3.2.28.tar.gz
# Wed, 06 Mar 2024 14:34:09 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 14:34:14 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 14:34:15 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Wed, 06 Mar 2024 14:34:15 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:34:15 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 14:34:15 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 14:34:15 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 14:34:15 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 14:34:15 GMT
EXPOSE 8182
# Wed, 06 Mar 2024 14:34:16 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8069355d5739c7da6dbe5ac9692d576813db815ada8e298f80c69c9624b46e9b`  
		Last Modified: Wed, 06 Mar 2024 06:07:30 GMT  
		Size: 12.9 MB (12904599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0818127cd97b321529b68d069c224d5847d3d40a93d2ac194b85d97e7d06269`  
		Last Modified: Wed, 06 Mar 2024 06:07:36 GMT  
		Size: 103.6 MB (103601240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db15aff3aedb36071e783b4c821f5244536c6bb5d8d6a4af69a143ebe525c0e3`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8727e407d8afb0bc127215ae7755d265a18fae32a798b36e72e1aa732ade25`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a66e2266d344ad268dc7ab7f1a52c09e25ce8c27a2b9d35d982aad1517b263f`  
		Last Modified: Wed, 06 Mar 2024 14:35:11 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d957474616522d2cbe456af7f8009fd1d795c017f45183b9cb65230ff7b89f1c`  
		Last Modified: Wed, 06 Mar 2024 14:35:17 GMT  
		Size: 100.9 MB (100892029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12566aca98437df14cfbe03441a123943f21d10af398c902d6cd5daebae91460`  
		Last Modified: Wed, 06 Mar 2024 14:35:11 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.28-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:a2f00667d1836008b355e7a71ee3910ff1f8eba4318a8586149ccc9262888ab9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240150417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca8d7376329c360c43f51de8f48165403c3f2b1bfa18be2dac3a1bd918b6d10`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:16:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 02:16:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:16:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 02:17:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:17:16 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 02:17:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 02:17:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 02:17:32 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 02:17:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 05:26:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 05:26:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 05:26:17 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 05:26:40 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cf9819e6d0b2575c64348e6c7c53d40d
# Wed, 06 Mar 2024 05:26:41 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=25df0a72243b3a8317afba691971b168d415907a
# Wed, 06 Mar 2024 05:26:41 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.28/orientdb-tp3-3.2.28.tar.gz
# Wed, 06 Mar 2024 05:26:47 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:26:56 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 05:26:57 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Wed, 06 Mar 2024 05:26:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 05:26:58 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 05:26:58 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 05:26:58 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 05:26:59 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 05:26:59 GMT
EXPOSE 8182
# Wed, 06 Mar 2024 05:26:59 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ec27e2ded8ffd5739eb9afa16988019dfc7a5185984fd50364954711029c6`  
		Last Modified: Wed, 06 Mar 2024 02:23:08 GMT  
		Size: 12.5 MB (12492077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6476eac220dc15b7b008e7018b3369704012af07c9a9d3269eeeff510bb6534`  
		Last Modified: Wed, 06 Mar 2024 02:23:16 GMT  
		Size: 99.2 MB (99229800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916d4cc71957468e2218be3dc202e2c510c2342d67c66bcc991131af968b0d1`  
		Last Modified: Wed, 06 Mar 2024 02:23:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc776191e565b5ba8f39a35bfd38bb8b67fa31df2f2f909425913f7e02c399c`  
		Last Modified: Wed, 06 Mar 2024 02:23:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d4bc116242e93f9812fd40f45507c603ba44b4c579d84230839c1448d392cd`  
		Last Modified: Wed, 06 Mar 2024 05:27:32 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697de7107c93329cb80707b5c28a9c5bd8c03a1c536db2d0b0ac017a97611feb`  
		Last Modified: Wed, 06 Mar 2024 05:27:42 GMT  
		Size: 100.9 MB (100891984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896a16af8f629e964d5fbc458c43c6444ae7097777d9a851b4d85a4ea206996b`  
		Last Modified: Wed, 06 Mar 2024 05:27:32 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.28-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:37bc29048adf2951bb089f41632b1759bc92b614040c131fa70d6c5c59a887e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244847385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810b89d08e343df3ad479314c185bdb38d6ce34ec40e025223194115e622e43a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:01:49 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 04:01:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 04:01:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 04:01:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:01:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 08:38:29 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 08:38:29 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 08:38:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cf9819e6d0b2575c64348e6c7c53d40d
# Wed, 06 Mar 2024 08:38:45 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=25df0a72243b3a8317afba691971b168d415907a
# Wed, 06 Mar 2024 08:38:45 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.28/orientdb-tp3-3.2.28.tar.gz
# Wed, 06 Mar 2024 08:38:49 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 08:38:53 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 08:38:54 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Wed, 06 Mar 2024 08:38:54 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 08:38:54 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 08:38:54 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 08:38:54 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 08:38:54 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 08:38:54 GMT
EXPOSE 8182
# Wed, 06 Mar 2024 08:38:55 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7620c0cc62807824d2242c6cef9f4c58531a799ce6c124c214d4a7a5ca35d0`  
		Last Modified: Wed, 06 Mar 2024 04:05:53 GMT  
		Size: 102.7 MB (102705771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb2ab6d6d84cb5c81b9029bdb29a31d3845d0aa350868c7a1456dcd93b9778c`  
		Last Modified: Wed, 06 Mar 2024 04:05:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4ca9405ba8d165ed87c13f38e95b6b519f9d8b4d4c97040cb9ac6c5ade21e3`  
		Last Modified: Wed, 06 Mar 2024 04:05:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984f4c0a0760a440546cb4014f3b07e414b351905ae0d0b71fd6bad6c3cf5f19`  
		Last Modified: Wed, 06 Mar 2024 08:39:17 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71041878fa22655380edb5c2026fc1664c3cdb42150ea8625075c5deb554640`  
		Last Modified: Wed, 06 Mar 2024 08:39:22 GMT  
		Size: 100.9 MB (100891982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92aac00e67ccf2a9e6ded11dfae579c3dd91d53702a5ebe5199c9908c9586ec7`  
		Last Modified: Wed, 06 Mar 2024 08:39:17 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:ce2d718b9ad1b9f4388f2c02426f1b0cc91a834d925aaaf1d5e1c96cdbeff4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:a7295ad7d967a12abbdd1099f6d7dc24f3e647654203af9015a19031b429fa0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219874120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4688bddab13dcfa4c44f7637db004ae1ad807aed63cf64669f98561afe739b74`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:02:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:02:33 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 06:02:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 06:02:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 06:02:39 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:02:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 14:33:47 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 14:33:47 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_DOWNLOAD_MD5=c189d2795b8b08356318a8b262eeab43
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=af0fc0eee9a106f96d60732a1026ff4cad78e778
# Wed, 06 Mar 2024 14:33:47 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.28/orientdb-community-3.2.28.tar.gz
# Wed, 06 Mar 2024 14:33:54 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 14:33:58 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 14:33:58 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:33:58 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 14:33:58 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 14:33:59 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 14:33:59 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 14:33:59 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8069355d5739c7da6dbe5ac9692d576813db815ada8e298f80c69c9624b46e9b`  
		Last Modified: Wed, 06 Mar 2024 06:07:30 GMT  
		Size: 12.9 MB (12904599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0818127cd97b321529b68d069c224d5847d3d40a93d2ac194b85d97e7d06269`  
		Last Modified: Wed, 06 Mar 2024 06:07:36 GMT  
		Size: 103.6 MB (103601240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db15aff3aedb36071e783b4c821f5244536c6bb5d8d6a4af69a143ebe525c0e3`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8727e407d8afb0bc127215ae7755d265a18fae32a798b36e72e1aa732ade25`  
		Last Modified: Wed, 06 Mar 2024 06:07:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470a50a440c6e00c93f0af5c640761aa79b7a6017053e1b10ec86a31c4c91fd4`  
		Last Modified: Wed, 06 Mar 2024 14:34:56 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f577cf8a842e0bd3a1e1ab196514d912377354bc4383c2ffe6fd1dc63ff240`  
		Last Modified: Wed, 06 Mar 2024 14:35:00 GMT  
		Size: 72.9 MB (72915736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:838a10cac41d33c99bd0424270219654f4f86b667ba9c1f06bfed430fa7f8280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212172831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3b9b6d07760528c89540b9c19fecbe559dc4fb369fa362f099806d3d26d4d1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:11 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:14 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 27 Feb 2024 18:53:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:16:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 02:16:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:16:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 02:17:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:17:16 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 02:17:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 02:17:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 02:17:32 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 02:17:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 05:26:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 05:26:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 05:26:17 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 05:26:17 GMT
ENV ORIENTDB_DOWNLOAD_MD5=c189d2795b8b08356318a8b262eeab43
# Wed, 06 Mar 2024 05:26:17 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=af0fc0eee9a106f96d60732a1026ff4cad78e778
# Wed, 06 Mar 2024 05:26:18 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.28/orientdb-community-3.2.28.tar.gz
# Wed, 06 Mar 2024 05:26:24 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:26:32 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 05:26:33 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 05:26:33 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 05:26:33 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 05:26:34 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 05:26:34 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 05:26:35 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ec27e2ded8ffd5739eb9afa16988019dfc7a5185984fd50364954711029c6`  
		Last Modified: Wed, 06 Mar 2024 02:23:08 GMT  
		Size: 12.5 MB (12492077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6476eac220dc15b7b008e7018b3369704012af07c9a9d3269eeeff510bb6534`  
		Last Modified: Wed, 06 Mar 2024 02:23:16 GMT  
		Size: 99.2 MB (99229800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916d4cc71957468e2218be3dc202e2c510c2342d67c66bcc991131af968b0d1`  
		Last Modified: Wed, 06 Mar 2024 02:23:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc776191e565b5ba8f39a35bfd38bb8b67fa31df2f2f909425913f7e02c399c`  
		Last Modified: Wed, 06 Mar 2024 02:23:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a59ceae44055be037f945ec1192c57e5a3c8405cec218742dc7fca595ace3a`  
		Last Modified: Wed, 06 Mar 2024 05:27:15 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4634028dbd07fa153bcc76aff47053819b61db68e5b1823c8d658289da417bdf`  
		Last Modified: Wed, 06 Mar 2024 05:27:21 GMT  
		Size: 72.9 MB (72915775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:eb09b676e196b9de314924453dad5ada53cb4b0b9c61e91b9d109c9d9442017f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216869742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af79ce8f90812c260ef5e983a1b7968fce0995836911165c8377d6166dfd389`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:01:49 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 04:01:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 04:01:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 04:01:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:01:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 08:38:29 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 06 Mar 2024 08:38:29 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_VERSION=3.2.28
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_DOWNLOAD_MD5=c189d2795b8b08356318a8b262eeab43
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=af0fc0eee9a106f96d60732a1026ff4cad78e778
# Wed, 06 Mar 2024 08:38:29 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.28/orientdb-community-3.2.28.tar.gz
# Wed, 06 Mar 2024 08:38:38 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 08:38:41 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Wed, 06 Mar 2024 08:38:42 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 08:38:42 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Wed, 06 Mar 2024 08:38:42 GMT
WORKDIR /orientdb
# Wed, 06 Mar 2024 08:38:42 GMT
EXPOSE 2424
# Wed, 06 Mar 2024 08:38:42 GMT
EXPOSE 2480
# Wed, 06 Mar 2024 08:38:42 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7620c0cc62807824d2242c6cef9f4c58531a799ce6c124c214d4a7a5ca35d0`  
		Last Modified: Wed, 06 Mar 2024 04:05:53 GMT  
		Size: 102.7 MB (102705771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb2ab6d6d84cb5c81b9029bdb29a31d3845d0aa350868c7a1456dcd93b9778c`  
		Last Modified: Wed, 06 Mar 2024 04:05:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4ca9405ba8d165ed87c13f38e95b6b519f9d8b4d4c97040cb9ac6c5ade21e3`  
		Last Modified: Wed, 06 Mar 2024 04:05:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d70610fff7ecdac052d49693a8607211e537d3063c4c61508902ef53ac7b1d`  
		Last Modified: Wed, 06 Mar 2024 08:39:03 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c8e70152ab74c9ed3872c778e1588015599bce6d13e684016381cb398bb832`  
		Last Modified: Wed, 06 Mar 2024 08:39:07 GMT  
		Size: 72.9 MB (72915721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
