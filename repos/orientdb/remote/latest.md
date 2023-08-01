## `orientdb:latest`

```console
$ docker pull orientdb@sha256:e05cd3b80b247c7d0d4d9292cccf65433a7b80e94d27f4c272bf1fd6d0b11efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:9ee025a7632913a95ef416506fe16351e6b6d0c071982fc8fcb19b3fe93a7570
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211272182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068b72255d7b027c56529551b2656919733fe881f629a0307cf988132fc8d3fb`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:33:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:34:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:20:13 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:20:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 01 Aug 2023 21:20:19 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 01 Aug 2023 21:49:48 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 01 Aug 2023 21:49:48 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 01 Aug 2023 21:49:48 GMT
ENV ORIENTDB_VERSION=3.2.21
# Tue, 01 Aug 2023 21:49:48 GMT
ENV ORIENTDB_DOWNLOAD_MD5=e556061885a429407bf155084de65773
# Tue, 01 Aug 2023 21:49:48 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=71cf32854a37b0c5f63c93ea57e850f2e93f3c87
# Tue, 01 Aug 2023 21:49:48 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.21/orientdb-community-3.2.21.tar.gz
# Tue, 01 Aug 2023 21:49:52 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Aug 2023 21:49:57 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 01 Aug 2023 21:49:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 21:49:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 01 Aug 2023 21:49:57 GMT
WORKDIR /orientdb
# Tue, 01 Aug 2023 21:49:57 GMT
EXPOSE 2424
# Tue, 01 Aug 2023 21:49:58 GMT
EXPOSE 2480
# Tue, 01 Aug 2023 21:49:58 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db0ad82863deaedd2f9a365e52f595085778d28bd1e6f1d351107590cad806`  
		Last Modified: Tue, 04 Jul 2023 20:39:05 GMT  
		Size: 12.5 MB (12495341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db121c4b01261783a1e06fce8cb2bc77b29752700e5409d773a9e48f65515d6b`  
		Last Modified: Tue, 01 Aug 2023 21:24:56 GMT  
		Size: 103.6 MB (103588607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a27c0b9b244fe72f830b376987f8e7b16dce29c0b6f6c2d47a3fcaaf596787`  
		Last Modified: Tue, 01 Aug 2023 21:24:46 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aeccd19354db8ad12649809ae9acd14c651e56cfaf72d9153e84acacf409adc`  
		Last Modified: Tue, 01 Aug 2023 21:51:39 GMT  
		Size: 808.9 KB (808857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c8cd41587284088a8470119a8fd8fa4634014623bec6c7771b9d5f10450479`  
		Last Modified: Tue, 01 Aug 2023 21:51:45 GMT  
		Size: 63.9 MB (63947987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:latest` - linux; arm variant v7

```console
$ docker pull orientdb@sha256:2ef931ba19f456175fad3a5ba6b9dec537acb07b776dea5dd8bbcc10c1b430bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154090007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1db44079dd0c719b508d925c907c27fdb1f670d1ae430364e366e8d8c3bd601`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 28 Jun 2023 08:41:15 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:41:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:41:18 GMT
ADD file:c13f43a31510c7a4eaa7e4ca90e4f973b19895658b1f9993cab5f93979d4e2dc in / 
# Wed, 28 Jun 2023 08:41:18 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 20:09:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 20:09:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 20:09:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 20:09:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:09:56 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Tue, 04 Jul 2023 20:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 04 Jul 2023 20:10:06 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 05 Jul 2023 05:31:01 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 05 Jul 2023 05:31:01 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 25 Jul 2023 22:39:42 GMT
ENV ORIENTDB_VERSION=3.2.21
# Tue, 25 Jul 2023 22:39:42 GMT
ENV ORIENTDB_DOWNLOAD_MD5=e556061885a429407bf155084de65773
# Tue, 25 Jul 2023 22:39:42 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=71cf32854a37b0c5f63c93ea57e850f2e93f3c87
# Tue, 25 Jul 2023 22:39:42 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.21/orientdb-community-3.2.21.tar.gz
# Tue, 25 Jul 2023 22:40:01 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:40:05 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 25 Jul 2023 22:40:05 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 22:40:06 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 25 Jul 2023 22:40:06 GMT
WORKDIR /orientdb
# Tue, 25 Jul 2023 22:40:06 GMT
EXPOSE 2424
# Tue, 25 Jul 2023 22:40:06 GMT
EXPOSE 2480
# Tue, 25 Jul 2023 22:40:06 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:63b96265cfe95b9cec847027033d4226b783ecd042036f5c809a7386027f56b0`  
		Last Modified: Fri, 30 Jun 2023 02:08:02 GMT  
		Size: 27.0 MB (27026961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d19505228cda33a776bf291d57d8a57fe0581f962ef986e4e0701430f4bfc0`  
		Last Modified: Tue, 04 Jul 2023 20:13:38 GMT  
		Size: 12.1 MB (12063065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632cc6c1665676ae76f3f405185fc47498d930345724b97263114174a1bccb82`  
		Last Modified: Tue, 04 Jul 2023 20:13:43 GMT  
		Size: 50.3 MB (50304323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b00b50c978b455e8e51cc689e5d73c3094d3e031ebb536d6eb959286289aeb`  
		Last Modified: Tue, 04 Jul 2023 20:13:36 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7129f773385e7ac09f8030ec1da944ab6b7c533aa19fe0f70863ffa79b548af4`  
		Last Modified: Tue, 25 Jul 2023 22:40:31 GMT  
		Size: 747.5 KB (747505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a684ec80f8cbd9559a3b4f2e88fc4f7a6fa182d93bff5366a76f3f36346ce707`  
		Last Modified: Tue, 25 Jul 2023 22:40:36 GMT  
		Size: 63.9 MB (63947991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `orientdb:latest` - linux; arm64 variant v8

```console
$ docker pull orientdb@sha256:f837d6385f416a658bc4bc0baeb052e8c1df739703211dce46cb3fa7b484d9d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159340671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a375a5383f08a05d45242269cd955fbee75a92916b1c35414eb6375d7d77c637`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:32:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 15:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 15:32:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 15:32:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:33:00 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Tue, 04 Jul 2023 15:33:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 04 Jul 2023 15:33:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 05 Jul 2023 04:35:24 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Wed, 05 Jul 2023 04:35:24 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 25 Jul 2023 22:31:28 GMT
ENV ORIENTDB_VERSION=3.2.21
# Tue, 25 Jul 2023 22:31:28 GMT
ENV ORIENTDB_DOWNLOAD_MD5=e556061885a429407bf155084de65773
# Tue, 25 Jul 2023 22:31:28 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=71cf32854a37b0c5f63c93ea57e850f2e93f3c87
# Tue, 25 Jul 2023 22:31:28 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.21/orientdb-community-3.2.21.tar.gz
# Tue, 25 Jul 2023 22:31:40 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Jul 2023 22:31:43 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 25 Jul 2023 22:31:44 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 22:31:44 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 25 Jul 2023 22:31:44 GMT
WORKDIR /orientdb
# Tue, 25 Jul 2023 22:31:44 GMT
EXPOSE 2424
# Tue, 25 Jul 2023 22:31:44 GMT
EXPOSE 2480
# Tue, 25 Jul 2023 22:31:44 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d9df805749ad7c4605f0d49a64da6a6173ab190ec361dc2063b6b73af59ab5`  
		Last Modified: Tue, 04 Jul 2023 15:36:55 GMT  
		Size: 12.5 MB (12455497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf1dec2f0590aec75290c088899072011e791aa36dfe51a1a898e8ebf065ea8`  
		Last Modified: Tue, 04 Jul 2023 15:36:58 GMT  
		Size: 53.7 MB (53743961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b246c4762097e5b6fd591705d47b3c4a91f3171e86970259e0986c8a24e55933`  
		Last Modified: Tue, 04 Jul 2023 15:36:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e223b43e6881c92ff41250c3de464f801ff8dc2590790bfae44606dfa320d79e`  
		Last Modified: Tue, 25 Jul 2023 22:32:05 GMT  
		Size: 802.0 KB (802037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1090cde603a4f5ab4f0166ef16efdc7258a472c8393a63f5c461989a76bacc8`  
		Last Modified: Tue, 25 Jul 2023 22:32:09 GMT  
		Size: 63.9 MB (63948005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
