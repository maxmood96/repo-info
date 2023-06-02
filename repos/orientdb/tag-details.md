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
-	[`orientdb:3.2.19`](#orientdb3219)
-	[`orientdb:3.2.19-tp3`](#orientdb3219-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:2.2`

```console
$ docker pull orientdb@sha256:64fcdfaf9fc93ff47d53ecfb25c94bb4ce0a8c51dde59733cbdd57da00491e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2` - linux; amd64

```console
$ docker pull orientdb@sha256:193d4069c86b0fbe6141a0af39d77ab5a5df717696cbf6033652d65ee8024a09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144054763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3e4f27f5413862a9a3b62ca10c283d2f3488d15513f35e5670b70e2adcfeae`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_VERSION=2.2.37
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Thu, 04 May 2023 15:25:19 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:21 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:21 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:21 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:21 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85226be34e7435205a2adadf68d8f1778e43bd82e5633ac72c58d8d929c447fc`  
		Last Modified: Thu, 04 May 2023 15:26:53 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8f2afbd9c3fa1656ccc97f32d2618e3d19fd75788265a1d96849799e6a469`  
		Last Modified: Thu, 04 May 2023 15:26:56 GMT  
		Size: 46.5 MB (46473896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37`

```console
$ docker pull orientdb@sha256:64fcdfaf9fc93ff47d53ecfb25c94bb4ce0a8c51dde59733cbdd57da00491e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37` - linux; amd64

```console
$ docker pull orientdb@sha256:193d4069c86b0fbe6141a0af39d77ab5a5df717696cbf6033652d65ee8024a09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144054763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3e4f27f5413862a9a3b62ca10c283d2f3488d15513f35e5670b70e2adcfeae`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_VERSION=2.2.37
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Thu, 04 May 2023 15:25:19 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:21 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:21 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:21 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:21 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85226be34e7435205a2adadf68d8f1778e43bd82e5633ac72c58d8d929c447fc`  
		Last Modified: Thu, 04 May 2023 15:26:53 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8f2afbd9c3fa1656ccc97f32d2618e3d19fd75788265a1d96849799e6a469`  
		Last Modified: Thu, 04 May 2023 15:26:56 GMT  
		Size: 46.5 MB (46473896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37-spatial`

```console
$ docker pull orientdb@sha256:2d8c7edd9cc74afca433373fcdfb95f05866a00be63675412ffc9c30fc4a6534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37-spatial` - linux; amd64

```console
$ docker pull orientdb@sha256:52b2133293a58b084ba98d4d925f43ceac3f599bb96d051c18381a6daac01ecc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145257361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5bab68eda90affb614127ee59d481dc0411be5c9abc31b469c4d508641c3df9`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_VERSION=2.2.37
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Thu, 04 May 2023 15:25:15 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Thu, 04 May 2023 15:25:19 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:21 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:21 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:21 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:21 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:21 GMT
CMD ["server.sh"]
# Thu, 04 May 2023 15:25:23 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_MD5=9f64ab5e959f5d9ad9ea5195d6d621d2
# Thu, 04 May 2023 15:25:23 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_SHA1=1748c9779ea7a8cb8fc068fcabf960e1778e8a19
# Thu, 04 May 2023 15:25:23 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-spatial/2.2.37/orientdb-spatial-2.2.37-dist.jar
# Thu, 04 May 2023 15:25:24 GMT
RUN wget $ORIENTDB_DOWNLOAD_SPATIAL_URL     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_MD5 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | md5sum -c -     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_SHA1 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | sha1sum -c -     && mv orientdb-spatial-*-dist.jar /orientdb/lib/
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85226be34e7435205a2adadf68d8f1778e43bd82e5633ac72c58d8d929c447fc`  
		Last Modified: Thu, 04 May 2023 15:26:53 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8f2afbd9c3fa1656ccc97f32d2618e3d19fd75788265a1d96849799e6a469`  
		Last Modified: Thu, 04 May 2023 15:26:56 GMT  
		Size: 46.5 MB (46473896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73c6bebaf8a953ffeb35acbeedbe2552849a92c2afee264a2986fc1b7ed8dca`  
		Last Modified: Thu, 04 May 2023 15:27:04 GMT  
		Size: 1.2 MB (1202598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0`

```console
$ docker pull orientdb@sha256:cbefe268b9b3da5eaa1f0546207d3ecc9f44bcf130753491e73338675cfff8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0` - linux; amd64

```console
$ docker pull orientdb@sha256:069c835f950043ee985e14b210279f659742e5627e59b6ba5cca31485e0c0eca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134645686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce2460f59fcf407115ee388f86e13c88e178643ba77c3c7abd73f5c302c06`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_VERSION=3.0.44
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_MD5=1bdcdb4d9c54fc78a1b56b8375ca990d
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6462dacd0df0725f10f85bee9666a0f6979187a6
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.44/orientdb-community-3.0.44.tar.gz
# Thu, 04 May 2023 15:24:57 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:00 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:00 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:01 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:01 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:01 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:01 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:01 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ca78bb78f397024fa509b4d7126fdd2443c4bdaa5f70e84013515deed6b4fa`  
		Last Modified: Thu, 04 May 2023 15:26:31 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69358d9afc82485abe8b4ebfe75206801459a1c9593787a22158477adc19e1f`  
		Last Modified: Thu, 04 May 2023 15:26:33 GMT  
		Size: 37.1 MB (37064819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0-tp3`

```console
$ docker pull orientdb@sha256:99f5b647a2f9ec81937538fa79e6a984eb97f6644adcd471c4f9281500a22420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:13c968ac755542c1f8f14896b28a2541006dcabae26f35ff3bca66deb4360ab0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161666008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b170d11a08bca919aca70ec93c00f02601fc783db1f744832011a1c2bc2a26`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_VERSION=3.0.44
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_MD5=44f8c96f57f75a4b9e2a3996a3b17512
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c49067782368e13082648d48bf6685969a5ed550
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.44/orientdb-tp3-3.0.44.tar.gz
# Thu, 04 May 2023 15:25:07 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:12 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:12 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 04 May 2023 15:25:12 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:12 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:12 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:12 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:13 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:13 GMT
EXPOSE 8182
# Thu, 04 May 2023 15:25:13 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4989cbb19e207dd073649d73014a93b89c4d4d9a4f6f6ba9b9e2275daf640f`  
		Last Modified: Thu, 04 May 2023 15:26:41 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d9826a8b6d27ac72ae8f7cc52449fc3c8bee8c616f2382593a858e9f55bc26`  
		Last Modified: Thu, 04 May 2023 15:26:45 GMT  
		Size: 64.1 MB (64083764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccf42b9644f34cd8dd55b94ed3e7c14e0d8c6931271e7b8c2c54c377ad273c8`  
		Last Modified: Thu, 04 May 2023 15:26:41 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.44`

```console
$ docker pull orientdb@sha256:cbefe268b9b3da5eaa1f0546207d3ecc9f44bcf130753491e73338675cfff8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.44` - linux; amd64

```console
$ docker pull orientdb@sha256:069c835f950043ee985e14b210279f659742e5627e59b6ba5cca31485e0c0eca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134645686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce2460f59fcf407115ee388f86e13c88e178643ba77c3c7abd73f5c302c06`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_VERSION=3.0.44
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_MD5=1bdcdb4d9c54fc78a1b56b8375ca990d
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6462dacd0df0725f10f85bee9666a0f6979187a6
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.44/orientdb-community-3.0.44.tar.gz
# Thu, 04 May 2023 15:24:57 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:00 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:00 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:01 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:01 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:01 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:01 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:01 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ca78bb78f397024fa509b4d7126fdd2443c4bdaa5f70e84013515deed6b4fa`  
		Last Modified: Thu, 04 May 2023 15:26:31 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69358d9afc82485abe8b4ebfe75206801459a1c9593787a22158477adc19e1f`  
		Last Modified: Thu, 04 May 2023 15:26:33 GMT  
		Size: 37.1 MB (37064819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.44-tp3`

```console
$ docker pull orientdb@sha256:99f5b647a2f9ec81937538fa79e6a984eb97f6644adcd471c4f9281500a22420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.44-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:13c968ac755542c1f8f14896b28a2541006dcabae26f35ff3bca66deb4360ab0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161666008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b170d11a08bca919aca70ec93c00f02601fc783db1f744832011a1c2bc2a26`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:53 GMT
ENV ORIENTDB_VERSION=3.0.44
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_MD5=44f8c96f57f75a4b9e2a3996a3b17512
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c49067782368e13082648d48bf6685969a5ed550
# Thu, 04 May 2023 15:25:03 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.44/orientdb-tp3-3.0.44.tar.gz
# Thu, 04 May 2023 15:25:07 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:25:12 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:25:12 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 04 May 2023 15:25:12 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:25:12 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:25:12 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:25:12 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:25:13 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:25:13 GMT
EXPOSE 8182
# Thu, 04 May 2023 15:25:13 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4989cbb19e207dd073649d73014a93b89c4d4d9a4f6f6ba9b9e2275daf640f`  
		Last Modified: Thu, 04 May 2023 15:26:41 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d9826a8b6d27ac72ae8f7cc52449fc3c8bee8c616f2382593a858e9f55bc26`  
		Last Modified: Thu, 04 May 2023 15:26:45 GMT  
		Size: 64.1 MB (64083764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccf42b9644f34cd8dd55b94ed3e7c14e0d8c6931271e7b8c2c54c377ad273c8`  
		Last Modified: Thu, 04 May 2023 15:26:41 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:36e130ec58149ed8fc02439581faaa176b311e6851151149bb54088e69adcf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:2c485f85cbbdc8b0236c5fff1d9536389372a8b94ce9c33fbec288f4ccc1d57f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150662066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cde820b9f00f1e7378a48e3f6c079a5ee72267574cef6cf0ae06d4cc1bba2d`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Thu, 04 May 2023 15:24:28 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Thu, 04 May 2023 15:24:28 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Thu, 04 May 2023 15:24:31 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:35 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:35 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:36 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:36 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:36 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:36 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:36 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e9295cac4efc25743ced255915288067abb70682db3c510691669eb39c55e5`  
		Last Modified: Thu, 04 May 2023 15:26:07 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1602cb6ba2d624fd2f33952d261c603d5a42cdb526d12e681c86ea960dbf1f27`  
		Last Modified: Thu, 04 May 2023 15:26:10 GMT  
		Size: 53.1 MB (53081198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:0d13dea248cccfccdb2a846564eaa6e2d5b8dbbfac1bac254bed77c4e6d9d106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:a59381a9b847f690e20b52dda8902c8227d04064107bdd1a453df5d0fba29fdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173669093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e47bb2dc5207000b5a8bca959763712a51cb447b709965623871a3584a038d8`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Thu, 04 May 2023 15:24:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:49 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:49 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 04 May 2023 15:24:49 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:49 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:49 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:49 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:50 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:50 GMT
EXPOSE 8182
# Thu, 04 May 2023 15:24:50 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000666c8516011f72b54bc17f9d750bb1c0122904cf9d607fc51d175896a1c6`  
		Last Modified: Thu, 04 May 2023 15:26:18 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f10d6d9a7c31fbf513aff4f5d6d34a67fc04e55a481d6f9bdfa5293cda1d5c`  
		Last Modified: Thu, 04 May 2023 15:26:22 GMT  
		Size: 76.1 MB (76086848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f833b219c82fd8d27f736d549700515305c20a29ec3f810e4110807b0518be0f`  
		Last Modified: Thu, 04 May 2023 15:26:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:36e130ec58149ed8fc02439581faaa176b311e6851151149bb54088e69adcf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:2c485f85cbbdc8b0236c5fff1d9536389372a8b94ce9c33fbec288f4ccc1d57f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150662066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cde820b9f00f1e7378a48e3f6c079a5ee72267574cef6cf0ae06d4cc1bba2d`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Thu, 04 May 2023 15:24:28 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Thu, 04 May 2023 15:24:28 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Thu, 04 May 2023 15:24:31 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:35 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:35 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:36 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:36 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:36 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:36 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:36 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e9295cac4efc25743ced255915288067abb70682db3c510691669eb39c55e5`  
		Last Modified: Thu, 04 May 2023 15:26:07 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1602cb6ba2d624fd2f33952d261c603d5a42cdb526d12e681c86ea960dbf1f27`  
		Last Modified: Thu, 04 May 2023 15:26:10 GMT  
		Size: 53.1 MB (53081198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:0d13dea248cccfccdb2a846564eaa6e2d5b8dbbfac1bac254bed77c4e6d9d106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:a59381a9b847f690e20b52dda8902c8227d04064107bdd1a453df5d0fba29fdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173669093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e47bb2dc5207000b5a8bca959763712a51cb447b709965623871a3584a038d8`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 04 May 2023 15:24:27 GMT
ENV ORIENTDB_VERSION=3.1.20
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Thu, 04 May 2023 15:24:39 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Thu, 04 May 2023 15:24:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 15:24:49 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 04 May 2023 15:24:49 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 04 May 2023 15:24:49 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 15:24:49 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 04 May 2023 15:24:49 GMT
WORKDIR /orientdb
# Thu, 04 May 2023 15:24:49 GMT
EXPOSE 2424
# Thu, 04 May 2023 15:24:50 GMT
EXPOSE 2480
# Thu, 04 May 2023 15:24:50 GMT
EXPOSE 8182
# Thu, 04 May 2023 15:24:50 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000666c8516011f72b54bc17f9d750bb1c0122904cf9d607fc51d175896a1c6`  
		Last Modified: Thu, 04 May 2023 15:26:18 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f10d6d9a7c31fbf513aff4f5d6d34a67fc04e55a481d6f9bdfa5293cda1d5c`  
		Last Modified: Thu, 04 May 2023 15:26:22 GMT  
		Size: 76.1 MB (76086848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f833b219c82fd8d27f736d549700515305c20a29ec3f810e4110807b0518be0f`  
		Last Modified: Thu, 04 May 2023 15:26:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:abe3a3436f8ba9402bbf674e427066d0b29ff603e81df85e33ac477850203772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2` - linux; amd64

```console
$ docker pull orientdb@sha256:c7f99ea2b9ff83a6da9374c31be89281a56ec69386ef986700dbea91ef6e0802
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161609271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8719ec82b986465731486a7e9a094e88f6e3d91b48026e136000a4cd9f969`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 11 May 2023 19:43:53 GMT
ENV ORIENTDB_VERSION=3.2.19
# Thu, 11 May 2023 19:43:53 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5b6d0296d7c43cdcf22fbc07d00782f4
# Thu, 11 May 2023 19:43:53 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c5b1823272532d911c93ce68be4dfcf60c27ab72
# Thu, 11 May 2023 19:43:54 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.19/orientdb-community-3.2.19.tar.gz
# Thu, 11 May 2023 19:44:01 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 11 May 2023 19:44:05 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 11 May 2023 19:44:06 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 May 2023 19:44:06 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 11 May 2023 19:44:06 GMT
WORKDIR /orientdb
# Thu, 11 May 2023 19:44:06 GMT
EXPOSE 2424
# Thu, 11 May 2023 19:44:06 GMT
EXPOSE 2480
# Thu, 11 May 2023 19:44:06 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935982cb97d5e34fcfd2fb7e9e172fae5b058fe33b4fc8ddad2cd481373778f4`  
		Last Modified: Thu, 11 May 2023 19:44:44 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4591d017fb683bbca6328b95bec0073e1c9cf9ea22cec731c5d1c8cb3f82e730`  
		Last Modified: Thu, 11 May 2023 19:44:48 GMT  
		Size: 64.0 MB (64028405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:728c4d36728bbaa377f1aca1b6d624f4c6e13e91843f25dd2cf914cee9fe2e8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153423877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecbe8672f47846bf051c8ce66ae71e32fde85fe66e7e8c25ed81845babc4a81`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 22 May 2023 17:52:13 GMT
ARG RELEASE
# Mon, 22 May 2023 17:52:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:52:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:52:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:52:16 GMT
ADD file:52b34a0d4198b5d30380eb1f293fb8916790394fcba96b4759a3f1beeb373b1a in / 
# Mon, 22 May 2023 17:52:16 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:58:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:58:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:58:23 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 01 Jun 2023 23:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Jun 2023 23:58:34 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Jun 2023 00:40:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Jun 2023 00:40:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_VERSION=3.2.19
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5b6d0296d7c43cdcf22fbc07d00782f4
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c5b1823272532d911c93ce68be4dfcf60c27ab72
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.19/orientdb-community-3.2.19.tar.gz
# Fri, 02 Jun 2023 00:40:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:40:47 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Jun 2023 00:40:47 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 00:40:47 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Jun 2023 00:40:47 GMT
WORKDIR /orientdb
# Fri, 02 Jun 2023 00:40:47 GMT
EXPOSE 2424
# Fri, 02 Jun 2023 00:40:47 GMT
EXPOSE 2480
# Fri, 02 Jun 2023 00:40:48 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:493981aec623882c3786c4f3065d2e731f17ed403c7452a2ece9ff96b2b02ac5`  
		Last Modified: Tue, 23 May 2023 02:04:29 GMT  
		Size: 27.0 MB (27026262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8721978efb71ce00146fd095d3619db0282198145fc4bc2579debaba5ee32ca7`  
		Last Modified: Fri, 02 Jun 2023 00:00:36 GMT  
		Size: 12.1 MB (12063609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2b6efc7a152ed03886df89aae6437905e60b2ebc8995d579a9914bf2c42118`  
		Last Modified: Fri, 02 Jun 2023 00:00:41 GMT  
		Size: 50.3 MB (50305063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6bd2cf912a12f9159ed496b33b46be677c7e53e86fe595443ec7268beff31b`  
		Last Modified: Fri, 02 Jun 2023 00:00:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107d40d259cc96cf0c923843ea106a185ecc3185ff8fbb3f1dd75272a110f7a6`  
		Last Modified: Fri, 02 Jun 2023 00:41:09 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b99ae3bc88ca0c4b10ef75365b0f25a3248aed027afcb291c32a2d1309c003`  
		Last Modified: Fri, 02 Jun 2023 00:41:14 GMT  
		Size: 64.0 MB (64028426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:bd9f37ff8c31c38aa99cf13a2093487c1331fc2c15fd9c9a450865dfa1de33f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158614822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c549c001df7f8ebb2047c15d517ccf71ad118f24c7513982c7c172e130b9ebe3`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:18:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:18:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:18:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:18:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:18:44 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 01 Jun 2023 23:18:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Jun 2023 23:18:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Jun 2023 01:07:03 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Jun 2023 01:07:03 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Jun 2023 01:07:03 GMT
ENV ORIENTDB_VERSION=3.2.19
# Fri, 02 Jun 2023 01:07:03 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5b6d0296d7c43cdcf22fbc07d00782f4
# Fri, 02 Jun 2023 01:07:03 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c5b1823272532d911c93ce68be4dfcf60c27ab72
# Fri, 02 Jun 2023 01:07:04 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.19/orientdb-community-3.2.19.tar.gz
# Fri, 02 Jun 2023 01:07:07 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:07:10 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Jun 2023 01:07:10 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:07:10 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Jun 2023 01:07:10 GMT
WORKDIR /orientdb
# Fri, 02 Jun 2023 01:07:11 GMT
EXPOSE 2424
# Fri, 02 Jun 2023 01:07:11 GMT
EXPOSE 2480
# Fri, 02 Jun 2023 01:07:11 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90f9c81eab3c275d75f3cf9f4840e195cfa7c5372d500bfeb5a040f3fc88262`  
		Last Modified: Thu, 01 Jun 2023 23:21:25 GMT  
		Size: 12.5 MB (12452855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d317acd72006ab4f5c8ac602e8a03a020b84f80202cf8052d85a9b9fc78487`  
		Last Modified: Thu, 01 Jun 2023 23:21:28 GMT  
		Size: 53.7 MB (53744002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc59dd42c66597c65d12cf3d15fed01fbc88ba3e64701e764fcb8fe2704be58`  
		Last Modified: Thu, 01 Jun 2023 23:21:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3e65cec0518b607bbba684f70f44a2a3b491bdc16ff51c404d17b430e96bc9`  
		Last Modified: Fri, 02 Jun 2023 01:07:30 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ef1efbbe0f3273c65e0df1e17569b7685583480c426a899c4798a95f3e5eec`  
		Last Modified: Fri, 02 Jun 2023 01:07:33 GMT  
		Size: 64.0 MB (64028408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:3ded5611d0dc10bc64de076aeeee5f59593182279e75a8d9e72ad8c6f5db2d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:69a64fd23de1e14e1804eca90f61c58e6df1aeb783b8f753087cbe6f3c8919a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189586092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3b29e974d08ca2e06e927c96cfa2530dd61bec5ae14b5a7948104acca84e5c`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 11 May 2023 19:43:53 GMT
ENV ORIENTDB_VERSION=3.2.19
# Thu, 11 May 2023 19:44:10 GMT
ENV ORIENTDB_DOWNLOAD_MD5=43be14ac624a78e4d2f7ef9dfffbd68f
# Thu, 11 May 2023 19:44:10 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a2554326b34f67af3f668313f68b6818eb4cb62f
# Thu, 11 May 2023 19:44:10 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.19/orientdb-tp3-3.2.19.tar.gz
# Thu, 11 May 2023 19:44:14 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 11 May 2023 19:44:19 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 11 May 2023 19:44:19 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Thu, 11 May 2023 19:44:19 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 May 2023 19:44:19 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 11 May 2023 19:44:19 GMT
WORKDIR /orientdb
# Thu, 11 May 2023 19:44:19 GMT
EXPOSE 2424
# Thu, 11 May 2023 19:44:20 GMT
EXPOSE 2480
# Thu, 11 May 2023 19:44:20 GMT
EXPOSE 8182
# Thu, 11 May 2023 19:44:20 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ff255f3b2a382a3e64f121a58ef4d86da37d8af9c8aa800cd4ecf1420a83ee`  
		Last Modified: Thu, 11 May 2023 19:44:58 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363ca5ad4b505d493cbe5ac7f7bc0ecea0a08201085fd0233ca8f427efcb6fca`  
		Last Modified: Thu, 11 May 2023 19:45:04 GMT  
		Size: 92.0 MB (92003850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d635544179c964dd2892a2f127affbd3fee23924946df8f9b9e80489435e43d0`  
		Last Modified: Thu, 11 May 2023 19:44:58 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:f1401375f128a3fcd2ca1a9639da0b4b889aaf12cd30ec58b940425e185b3cab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181400648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ab8e8b60bcd33208c32a4552bb71e291162e7011132310410726164c77babc`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 22 May 2023 17:52:13 GMT
ARG RELEASE
# Mon, 22 May 2023 17:52:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:52:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:52:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:52:16 GMT
ADD file:52b34a0d4198b5d30380eb1f293fb8916790394fcba96b4759a3f1beeb373b1a in / 
# Mon, 22 May 2023 17:52:16 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:58:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:58:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:58:23 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 01 Jun 2023 23:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Jun 2023 23:58:34 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Jun 2023 00:40:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Jun 2023 00:40:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_VERSION=3.2.19
# Fri, 02 Jun 2023 00:40:50 GMT
ENV ORIENTDB_DOWNLOAD_MD5=43be14ac624a78e4d2f7ef9dfffbd68f
# Fri, 02 Jun 2023 00:40:50 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a2554326b34f67af3f668313f68b6818eb4cb62f
# Fri, 02 Jun 2023 00:40:50 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.19/orientdb-tp3-3.2.19.tar.gz
# Fri, 02 Jun 2023 00:40:54 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:41:01 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Jun 2023 00:41:01 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Fri, 02 Jun 2023 00:41:01 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 00:41:01 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Jun 2023 00:41:01 GMT
WORKDIR /orientdb
# Fri, 02 Jun 2023 00:41:01 GMT
EXPOSE 2424
# Fri, 02 Jun 2023 00:41:01 GMT
EXPOSE 2480
# Fri, 02 Jun 2023 00:41:01 GMT
EXPOSE 8182
# Fri, 02 Jun 2023 00:41:02 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:493981aec623882c3786c4f3065d2e731f17ed403c7452a2ece9ff96b2b02ac5`  
		Last Modified: Tue, 23 May 2023 02:04:29 GMT  
		Size: 27.0 MB (27026262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8721978efb71ce00146fd095d3619db0282198145fc4bc2579debaba5ee32ca7`  
		Last Modified: Fri, 02 Jun 2023 00:00:36 GMT  
		Size: 12.1 MB (12063609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2b6efc7a152ed03886df89aae6437905e60b2ebc8995d579a9914bf2c42118`  
		Last Modified: Fri, 02 Jun 2023 00:00:41 GMT  
		Size: 50.3 MB (50305063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6bd2cf912a12f9159ed496b33b46be677c7e53e86fe595443ec7268beff31b`  
		Last Modified: Fri, 02 Jun 2023 00:00:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b7ec2dd81ef679acbe173f17f58e50aa2f1d831c8da5cc13d64c738d71b37`  
		Last Modified: Fri, 02 Jun 2023 00:41:24 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb06e5b04bad89f9525ee2db4398b1d917c8ba637ea2ca0bbd7225e721ec4200`  
		Last Modified: Fri, 02 Jun 2023 00:41:30 GMT  
		Size: 92.0 MB (92003822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262304854f22c5a1ef6dcbbabc6391901f0d3fb5e1722a6fca5db706f48377aa`  
		Last Modified: Fri, 02 Jun 2023 00:41:24 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:ae4fd0012ecac3d02f571df4c452db2b3db768c2697c680a124870284de41379
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186591578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2326d08f66d8e083b15bdf05a3278a4a862f1fe819f95aa33c43d6e6d805473c`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:18:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:18:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:18:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:18:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:18:44 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 01 Jun 2023 23:18:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Jun 2023 23:18:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Jun 2023 01:07:03 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Jun 2023 01:07:03 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Jun 2023 01:07:03 GMT
ENV ORIENTDB_VERSION=3.2.19
# Fri, 02 Jun 2023 01:07:13 GMT
ENV ORIENTDB_DOWNLOAD_MD5=43be14ac624a78e4d2f7ef9dfffbd68f
# Fri, 02 Jun 2023 01:07:13 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a2554326b34f67af3f668313f68b6818eb4cb62f
# Fri, 02 Jun 2023 01:07:13 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.19/orientdb-tp3-3.2.19.tar.gz
# Fri, 02 Jun 2023 01:07:16 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:07:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Jun 2023 01:07:21 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Fri, 02 Jun 2023 01:07:21 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:07:21 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Jun 2023 01:07:21 GMT
WORKDIR /orientdb
# Fri, 02 Jun 2023 01:07:21 GMT
EXPOSE 2424
# Fri, 02 Jun 2023 01:07:21 GMT
EXPOSE 2480
# Fri, 02 Jun 2023 01:07:21 GMT
EXPOSE 8182
# Fri, 02 Jun 2023 01:07:22 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90f9c81eab3c275d75f3cf9f4840e195cfa7c5372d500bfeb5a040f3fc88262`  
		Last Modified: Thu, 01 Jun 2023 23:21:25 GMT  
		Size: 12.5 MB (12452855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d317acd72006ab4f5c8ac602e8a03a020b84f80202cf8052d85a9b9fc78487`  
		Last Modified: Thu, 01 Jun 2023 23:21:28 GMT  
		Size: 53.7 MB (53744002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc59dd42c66597c65d12cf3d15fed01fbc88ba3e64701e764fcb8fe2704be58`  
		Last Modified: Thu, 01 Jun 2023 23:21:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b54faa7f601b2c821758bacecfa6bab3984054af13f44835a79df6ef837942`  
		Last Modified: Fri, 02 Jun 2023 01:07:44 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36fb0030326d8347b35460ff358a63e033aa0f12f3b3c7ae8fffbc862f8198e`  
		Last Modified: Fri, 02 Jun 2023 01:07:48 GMT  
		Size: 92.0 MB (92003789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6835b967321a48046fcb97c2eb09c0290d1cedba3d04ed52ad33b1a1ff1031`  
		Last Modified: Fri, 02 Jun 2023 01:07:44 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.19`

```console
$ docker pull orientdb@sha256:abe3a3436f8ba9402bbf674e427066d0b29ff603e81df85e33ac477850203772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2.19` - linux; amd64

```console
$ docker pull orientdb@sha256:c7f99ea2b9ff83a6da9374c31be89281a56ec69386ef986700dbea91ef6e0802
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161609271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8719ec82b986465731486a7e9a094e88f6e3d91b48026e136000a4cd9f969`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 11 May 2023 19:43:53 GMT
ENV ORIENTDB_VERSION=3.2.19
# Thu, 11 May 2023 19:43:53 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5b6d0296d7c43cdcf22fbc07d00782f4
# Thu, 11 May 2023 19:43:53 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c5b1823272532d911c93ce68be4dfcf60c27ab72
# Thu, 11 May 2023 19:43:54 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.19/orientdb-community-3.2.19.tar.gz
# Thu, 11 May 2023 19:44:01 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 11 May 2023 19:44:05 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 11 May 2023 19:44:06 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 May 2023 19:44:06 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 11 May 2023 19:44:06 GMT
WORKDIR /orientdb
# Thu, 11 May 2023 19:44:06 GMT
EXPOSE 2424
# Thu, 11 May 2023 19:44:06 GMT
EXPOSE 2480
# Thu, 11 May 2023 19:44:06 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935982cb97d5e34fcfd2fb7e9e172fae5b058fe33b4fc8ddad2cd481373778f4`  
		Last Modified: Thu, 11 May 2023 19:44:44 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4591d017fb683bbca6328b95bec0073e1c9cf9ea22cec731c5d1c8cb3f82e730`  
		Last Modified: Thu, 11 May 2023 19:44:48 GMT  
		Size: 64.0 MB (64028405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.19` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:728c4d36728bbaa377f1aca1b6d624f4c6e13e91843f25dd2cf914cee9fe2e8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153423877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecbe8672f47846bf051c8ce66ae71e32fde85fe66e7e8c25ed81845babc4a81`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 22 May 2023 17:52:13 GMT
ARG RELEASE
# Mon, 22 May 2023 17:52:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:52:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:52:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:52:16 GMT
ADD file:52b34a0d4198b5d30380eb1f293fb8916790394fcba96b4759a3f1beeb373b1a in / 
# Mon, 22 May 2023 17:52:16 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:58:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:58:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:58:23 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 01 Jun 2023 23:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Jun 2023 23:58:34 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Jun 2023 00:40:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Jun 2023 00:40:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_VERSION=3.2.19
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5b6d0296d7c43cdcf22fbc07d00782f4
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c5b1823272532d911c93ce68be4dfcf60c27ab72
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.19/orientdb-community-3.2.19.tar.gz
# Fri, 02 Jun 2023 00:40:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:40:47 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Jun 2023 00:40:47 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 00:40:47 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Jun 2023 00:40:47 GMT
WORKDIR /orientdb
# Fri, 02 Jun 2023 00:40:47 GMT
EXPOSE 2424
# Fri, 02 Jun 2023 00:40:47 GMT
EXPOSE 2480
# Fri, 02 Jun 2023 00:40:48 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:493981aec623882c3786c4f3065d2e731f17ed403c7452a2ece9ff96b2b02ac5`  
		Last Modified: Tue, 23 May 2023 02:04:29 GMT  
		Size: 27.0 MB (27026262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8721978efb71ce00146fd095d3619db0282198145fc4bc2579debaba5ee32ca7`  
		Last Modified: Fri, 02 Jun 2023 00:00:36 GMT  
		Size: 12.1 MB (12063609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2b6efc7a152ed03886df89aae6437905e60b2ebc8995d579a9914bf2c42118`  
		Last Modified: Fri, 02 Jun 2023 00:00:41 GMT  
		Size: 50.3 MB (50305063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6bd2cf912a12f9159ed496b33b46be677c7e53e86fe595443ec7268beff31b`  
		Last Modified: Fri, 02 Jun 2023 00:00:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107d40d259cc96cf0c923843ea106a185ecc3185ff8fbb3f1dd75272a110f7a6`  
		Last Modified: Fri, 02 Jun 2023 00:41:09 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b99ae3bc88ca0c4b10ef75365b0f25a3248aed027afcb291c32a2d1309c003`  
		Last Modified: Fri, 02 Jun 2023 00:41:14 GMT  
		Size: 64.0 MB (64028426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.19` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:bd9f37ff8c31c38aa99cf13a2093487c1331fc2c15fd9c9a450865dfa1de33f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158614822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c549c001df7f8ebb2047c15d517ccf71ad118f24c7513982c7c172e130b9ebe3`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:18:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:18:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:18:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:18:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:18:44 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 01 Jun 2023 23:18:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Jun 2023 23:18:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Jun 2023 01:07:03 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Jun 2023 01:07:03 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Jun 2023 01:07:03 GMT
ENV ORIENTDB_VERSION=3.2.19
# Fri, 02 Jun 2023 01:07:03 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5b6d0296d7c43cdcf22fbc07d00782f4
# Fri, 02 Jun 2023 01:07:03 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c5b1823272532d911c93ce68be4dfcf60c27ab72
# Fri, 02 Jun 2023 01:07:04 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.19/orientdb-community-3.2.19.tar.gz
# Fri, 02 Jun 2023 01:07:07 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:07:10 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Jun 2023 01:07:10 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:07:10 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Jun 2023 01:07:10 GMT
WORKDIR /orientdb
# Fri, 02 Jun 2023 01:07:11 GMT
EXPOSE 2424
# Fri, 02 Jun 2023 01:07:11 GMT
EXPOSE 2480
# Fri, 02 Jun 2023 01:07:11 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90f9c81eab3c275d75f3cf9f4840e195cfa7c5372d500bfeb5a040f3fc88262`  
		Last Modified: Thu, 01 Jun 2023 23:21:25 GMT  
		Size: 12.5 MB (12452855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d317acd72006ab4f5c8ac602e8a03a020b84f80202cf8052d85a9b9fc78487`  
		Last Modified: Thu, 01 Jun 2023 23:21:28 GMT  
		Size: 53.7 MB (53744002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc59dd42c66597c65d12cf3d15fed01fbc88ba3e64701e764fcb8fe2704be58`  
		Last Modified: Thu, 01 Jun 2023 23:21:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3e65cec0518b607bbba684f70f44a2a3b491bdc16ff51c404d17b430e96bc9`  
		Last Modified: Fri, 02 Jun 2023 01:07:30 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ef1efbbe0f3273c65e0df1e17569b7685583480c426a899c4798a95f3e5eec`  
		Last Modified: Fri, 02 Jun 2023 01:07:33 GMT  
		Size: 64.0 MB (64028408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.19-tp3`

```console
$ docker pull orientdb@sha256:3ded5611d0dc10bc64de076aeeee5f59593182279e75a8d9e72ad8c6f5db2d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:3.2.19-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:69a64fd23de1e14e1804eca90f61c58e6df1aeb783b8f753087cbe6f3c8919a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189586092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3b29e974d08ca2e06e927c96cfa2530dd61bec5ae14b5a7948104acca84e5c`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 11 May 2023 19:43:53 GMT
ENV ORIENTDB_VERSION=3.2.19
# Thu, 11 May 2023 19:44:10 GMT
ENV ORIENTDB_DOWNLOAD_MD5=43be14ac624a78e4d2f7ef9dfffbd68f
# Thu, 11 May 2023 19:44:10 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a2554326b34f67af3f668313f68b6818eb4cb62f
# Thu, 11 May 2023 19:44:10 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.19/orientdb-tp3-3.2.19.tar.gz
# Thu, 11 May 2023 19:44:14 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 11 May 2023 19:44:19 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 11 May 2023 19:44:19 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Thu, 11 May 2023 19:44:19 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 May 2023 19:44:19 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 11 May 2023 19:44:19 GMT
WORKDIR /orientdb
# Thu, 11 May 2023 19:44:19 GMT
EXPOSE 2424
# Thu, 11 May 2023 19:44:20 GMT
EXPOSE 2480
# Thu, 11 May 2023 19:44:20 GMT
EXPOSE 8182
# Thu, 11 May 2023 19:44:20 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ff255f3b2a382a3e64f121a58ef4d86da37d8af9c8aa800cd4ecf1420a83ee`  
		Last Modified: Thu, 11 May 2023 19:44:58 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363ca5ad4b505d493cbe5ac7f7bc0ecea0a08201085fd0233ca8f427efcb6fca`  
		Last Modified: Thu, 11 May 2023 19:45:04 GMT  
		Size: 92.0 MB (92003850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d635544179c964dd2892a2f127affbd3fee23924946df8f9b9e80489435e43d0`  
		Last Modified: Thu, 11 May 2023 19:44:58 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.19-tp3` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:f1401375f128a3fcd2ca1a9639da0b4b889aaf12cd30ec58b940425e185b3cab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181400648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ab8e8b60bcd33208c32a4552bb71e291162e7011132310410726164c77babc`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 22 May 2023 17:52:13 GMT
ARG RELEASE
# Mon, 22 May 2023 17:52:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:52:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:52:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:52:16 GMT
ADD file:52b34a0d4198b5d30380eb1f293fb8916790394fcba96b4759a3f1beeb373b1a in / 
# Mon, 22 May 2023 17:52:16 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:58:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:58:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:58:23 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 01 Jun 2023 23:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Jun 2023 23:58:34 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Jun 2023 00:40:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Jun 2023 00:40:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_VERSION=3.2.19
# Fri, 02 Jun 2023 00:40:50 GMT
ENV ORIENTDB_DOWNLOAD_MD5=43be14ac624a78e4d2f7ef9dfffbd68f
# Fri, 02 Jun 2023 00:40:50 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a2554326b34f67af3f668313f68b6818eb4cb62f
# Fri, 02 Jun 2023 00:40:50 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.19/orientdb-tp3-3.2.19.tar.gz
# Fri, 02 Jun 2023 00:40:54 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:41:01 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Jun 2023 00:41:01 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Fri, 02 Jun 2023 00:41:01 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 00:41:01 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Jun 2023 00:41:01 GMT
WORKDIR /orientdb
# Fri, 02 Jun 2023 00:41:01 GMT
EXPOSE 2424
# Fri, 02 Jun 2023 00:41:01 GMT
EXPOSE 2480
# Fri, 02 Jun 2023 00:41:01 GMT
EXPOSE 8182
# Fri, 02 Jun 2023 00:41:02 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:493981aec623882c3786c4f3065d2e731f17ed403c7452a2ece9ff96b2b02ac5`  
		Last Modified: Tue, 23 May 2023 02:04:29 GMT  
		Size: 27.0 MB (27026262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8721978efb71ce00146fd095d3619db0282198145fc4bc2579debaba5ee32ca7`  
		Last Modified: Fri, 02 Jun 2023 00:00:36 GMT  
		Size: 12.1 MB (12063609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2b6efc7a152ed03886df89aae6437905e60b2ebc8995d579a9914bf2c42118`  
		Last Modified: Fri, 02 Jun 2023 00:00:41 GMT  
		Size: 50.3 MB (50305063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6bd2cf912a12f9159ed496b33b46be677c7e53e86fe595443ec7268beff31b`  
		Last Modified: Fri, 02 Jun 2023 00:00:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847b7ec2dd81ef679acbe173f17f58e50aa2f1d831c8da5cc13d64c738d71b37`  
		Last Modified: Fri, 02 Jun 2023 00:41:24 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb06e5b04bad89f9525ee2db4398b1d917c8ba637ea2ca0bbd7225e721ec4200`  
		Last Modified: Fri, 02 Jun 2023 00:41:30 GMT  
		Size: 92.0 MB (92003822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262304854f22c5a1ef6dcbbabc6391901f0d3fb5e1722a6fca5db706f48377aa`  
		Last Modified: Fri, 02 Jun 2023 00:41:24 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:3.2.19-tp3` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:ae4fd0012ecac3d02f571df4c452db2b3db768c2697c680a124870284de41379
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186591578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2326d08f66d8e083b15bdf05a3278a4a862f1fe819f95aa33c43d6e6d805473c`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:18:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:18:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:18:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:18:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:18:44 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 01 Jun 2023 23:18:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Jun 2023 23:18:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Jun 2023 01:07:03 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Jun 2023 01:07:03 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Jun 2023 01:07:03 GMT
ENV ORIENTDB_VERSION=3.2.19
# Fri, 02 Jun 2023 01:07:13 GMT
ENV ORIENTDB_DOWNLOAD_MD5=43be14ac624a78e4d2f7ef9dfffbd68f
# Fri, 02 Jun 2023 01:07:13 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a2554326b34f67af3f668313f68b6818eb4cb62f
# Fri, 02 Jun 2023 01:07:13 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.19/orientdb-tp3-3.2.19.tar.gz
# Fri, 02 Jun 2023 01:07:16 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:07:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Jun 2023 01:07:21 GMT
ADD file:d87115ac6b8aa745e38b42aa952f39a6af40310fc4ffb07745e9e1c85874a543 in /orientdb/config 
# Fri, 02 Jun 2023 01:07:21 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:07:21 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Jun 2023 01:07:21 GMT
WORKDIR /orientdb
# Fri, 02 Jun 2023 01:07:21 GMT
EXPOSE 2424
# Fri, 02 Jun 2023 01:07:21 GMT
EXPOSE 2480
# Fri, 02 Jun 2023 01:07:21 GMT
EXPOSE 8182
# Fri, 02 Jun 2023 01:07:22 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90f9c81eab3c275d75f3cf9f4840e195cfa7c5372d500bfeb5a040f3fc88262`  
		Last Modified: Thu, 01 Jun 2023 23:21:25 GMT  
		Size: 12.5 MB (12452855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d317acd72006ab4f5c8ac602e8a03a020b84f80202cf8052d85a9b9fc78487`  
		Last Modified: Thu, 01 Jun 2023 23:21:28 GMT  
		Size: 53.7 MB (53744002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc59dd42c66597c65d12cf3d15fed01fbc88ba3e64701e764fcb8fe2704be58`  
		Last Modified: Thu, 01 Jun 2023 23:21:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b54faa7f601b2c821758bacecfa6bab3984054af13f44835a79df6ef837942`  
		Last Modified: Fri, 02 Jun 2023 01:07:44 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36fb0030326d8347b35460ff358a63e033aa0f12f3b3c7ae8fffbc862f8198e`  
		Last Modified: Fri, 02 Jun 2023 01:07:48 GMT  
		Size: 92.0 MB (92003789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6835b967321a48046fcb97c2eb09c0290d1cedba3d04ed52ad33b1a1ff1031`  
		Last Modified: Fri, 02 Jun 2023 01:07:44 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:abe3a3436f8ba9402bbf674e427066d0b29ff603e81df85e33ac477850203772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:c7f99ea2b9ff83a6da9374c31be89281a56ec69386ef986700dbea91ef6e0802
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161609271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8719ec82b986465731486a7e9a094e88f6e3d91b48026e136000a4cd9f969`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:26:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:26:43 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:48 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 15:24:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 04 May 2023 15:24:04 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 11 May 2023 19:43:53 GMT
ENV ORIENTDB_VERSION=3.2.19
# Thu, 11 May 2023 19:43:53 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5b6d0296d7c43cdcf22fbc07d00782f4
# Thu, 11 May 2023 19:43:53 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c5b1823272532d911c93ce68be4dfcf60c27ab72
# Thu, 11 May 2023 19:43:54 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.19/orientdb-community-3.2.19.tar.gz
# Thu, 11 May 2023 19:44:01 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 11 May 2023 19:44:05 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 11 May 2023 19:44:06 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 May 2023 19:44:06 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 11 May 2023 19:44:06 GMT
WORKDIR /orientdb
# Thu, 11 May 2023 19:44:06 GMT
EXPOSE 2424
# Thu, 11 May 2023 19:44:06 GMT
EXPOSE 2480
# Thu, 11 May 2023 19:44:06 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b02b5411a07f3b354cde2b461caffc1bb184a3413b5736a9e67ee87cb28b2`  
		Last Modified: Thu, 04 May 2023 07:30:02 GMT  
		Size: 12.5 MB (12504170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba27ac9b49ebfb40c9af21d15ae6ed178a95425906b272bcdfacaa9d7e638bc`  
		Last Modified: Thu, 04 May 2023 07:30:06 GMT  
		Size: 54.6 MB (54645965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499670bd4565adf7e28bd3d9b08a84e24bf8ed13ce05e61e65907c57cbfbbb78`  
		Last Modified: Thu, 04 May 2023 07:30:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935982cb97d5e34fcfd2fb7e9e172fae5b058fe33b4fc8ddad2cd481373778f4`  
		Last Modified: Thu, 11 May 2023 19:44:44 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4591d017fb683bbca6328b95bec0073e1c9cf9ea22cec731c5d1c8cb3f82e730`  
		Last Modified: Thu, 11 May 2023 19:44:48 GMT  
		Size: 64.0 MB (64028405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:728c4d36728bbaa377f1aca1b6d624f4c6e13e91843f25dd2cf914cee9fe2e8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153423877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecbe8672f47846bf051c8ce66ae71e32fde85fe66e7e8c25ed81845babc4a81`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 22 May 2023 17:52:13 GMT
ARG RELEASE
# Mon, 22 May 2023 17:52:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:52:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:52:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:52:16 GMT
ADD file:52b34a0d4198b5d30380eb1f293fb8916790394fcba96b4759a3f1beeb373b1a in / 
# Mon, 22 May 2023 17:52:16 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:58:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:58:23 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:58:23 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 01 Jun 2023 23:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Jun 2023 23:58:34 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Jun 2023 00:40:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Jun 2023 00:40:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_VERSION=3.2.19
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5b6d0296d7c43cdcf22fbc07d00782f4
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c5b1823272532d911c93ce68be4dfcf60c27ab72
# Fri, 02 Jun 2023 00:40:39 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.19/orientdb-community-3.2.19.tar.gz
# Fri, 02 Jun 2023 00:40:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:40:47 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Jun 2023 00:40:47 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 00:40:47 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Jun 2023 00:40:47 GMT
WORKDIR /orientdb
# Fri, 02 Jun 2023 00:40:47 GMT
EXPOSE 2424
# Fri, 02 Jun 2023 00:40:47 GMT
EXPOSE 2480
# Fri, 02 Jun 2023 00:40:48 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:493981aec623882c3786c4f3065d2e731f17ed403c7452a2ece9ff96b2b02ac5`  
		Last Modified: Tue, 23 May 2023 02:04:29 GMT  
		Size: 27.0 MB (27026262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8721978efb71ce00146fd095d3619db0282198145fc4bc2579debaba5ee32ca7`  
		Last Modified: Fri, 02 Jun 2023 00:00:36 GMT  
		Size: 12.1 MB (12063609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2b6efc7a152ed03886df89aae6437905e60b2ebc8995d579a9914bf2c42118`  
		Last Modified: Fri, 02 Jun 2023 00:00:41 GMT  
		Size: 50.3 MB (50305063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6bd2cf912a12f9159ed496b33b46be677c7e53e86fe595443ec7268beff31b`  
		Last Modified: Fri, 02 Jun 2023 00:00:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107d40d259cc96cf0c923843ea106a185ecc3185ff8fbb3f1dd75272a110f7a6`  
		Last Modified: Fri, 02 Jun 2023 00:41:09 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b99ae3bc88ca0c4b10ef75365b0f25a3248aed027afcb291c32a2d1309c003`  
		Last Modified: Fri, 02 Jun 2023 00:41:14 GMT  
		Size: 64.0 MB (64028426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:bd9f37ff8c31c38aa99cf13a2093487c1331fc2c15fd9c9a450865dfa1de33f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158614822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c549c001df7f8ebb2047c15d517ccf71ad118f24c7513982c7c172e130b9ebe3`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:18:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:18:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:18:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:18:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:18:44 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 01 Jun 2023 23:18:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 01 Jun 2023 23:18:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 02 Jun 2023 01:07:03 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Fri, 02 Jun 2023 01:07:03 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Fri, 02 Jun 2023 01:07:03 GMT
ENV ORIENTDB_VERSION=3.2.19
# Fri, 02 Jun 2023 01:07:03 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5b6d0296d7c43cdcf22fbc07d00782f4
# Fri, 02 Jun 2023 01:07:03 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c5b1823272532d911c93ce68be4dfcf60c27ab72
# Fri, 02 Jun 2023 01:07:04 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.19/orientdb-community-3.2.19.tar.gz
# Fri, 02 Jun 2023 01:07:07 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:07:10 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Fri, 02 Jun 2023 01:07:10 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:07:10 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Fri, 02 Jun 2023 01:07:10 GMT
WORKDIR /orientdb
# Fri, 02 Jun 2023 01:07:11 GMT
EXPOSE 2424
# Fri, 02 Jun 2023 01:07:11 GMT
EXPOSE 2480
# Fri, 02 Jun 2023 01:07:11 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90f9c81eab3c275d75f3cf9f4840e195cfa7c5372d500bfeb5a040f3fc88262`  
		Last Modified: Thu, 01 Jun 2023 23:21:25 GMT  
		Size: 12.5 MB (12452855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d317acd72006ab4f5c8ac602e8a03a020b84f80202cf8052d85a9b9fc78487`  
		Last Modified: Thu, 01 Jun 2023 23:21:28 GMT  
		Size: 53.7 MB (53744002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc59dd42c66597c65d12cf3d15fed01fbc88ba3e64701e764fcb8fe2704be58`  
		Last Modified: Thu, 01 Jun 2023 23:21:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3e65cec0518b607bbba684f70f44a2a3b491bdc16ff51c404d17b430e96bc9`  
		Last Modified: Fri, 02 Jun 2023 01:07:30 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ef1efbbe0f3273c65e0df1e17569b7685583480c426a899c4798a95f3e5eec`  
		Last Modified: Fri, 02 Jun 2023 01:07:33 GMT  
		Size: 64.0 MB (64028408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
