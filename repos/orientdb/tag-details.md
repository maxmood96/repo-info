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
-	[`orientdb:3.2.12`](#orientdb3212)
-	[`orientdb:3.2.12-tp3`](#orientdb3212-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:2.2`

```console
$ docker pull orientdb@sha256:e654074183da8e927ec02c1b5e7cc759d3e632265fe6bedb96e9d6766238392a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2` - linux; amd64

```console
$ docker pull orientdb@sha256:06b4dd8ddc075c86429abc944f3ce0eb6dd24261629c00bc150a56f3757fd553
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192869816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c15c48b6c6b652266dfeb9120a6cb31289df42bd37bd68e63fac785bba5c6e`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_VERSION=2.2.37
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Sat, 05 Nov 2022 01:31:39 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 01:31:41 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 05 Nov 2022 01:31:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:31:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 05 Nov 2022 01:31:42 GMT
WORKDIR /orientdb
# Sat, 05 Nov 2022 01:31:42 GMT
EXPOSE 2424
# Sat, 05 Nov 2022 01:31:42 GMT
EXPOSE 2480
# Sat, 05 Nov 2022 01:31:42 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a548a3c635bb232c3e6414a5c9feb13fb9a60de12cef7b4cc7963d3c4f955796`  
		Last Modified: Sat, 05 Nov 2022 01:33:35 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdde58255d054a72af86fe6da78f85a2f1992f2da761e04b733119a3d61683d`  
		Last Modified: Sat, 05 Nov 2022 01:33:39 GMT  
		Size: 46.5 MB (46473871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37`

```console
$ docker pull orientdb@sha256:e654074183da8e927ec02c1b5e7cc759d3e632265fe6bedb96e9d6766238392a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37` - linux; amd64

```console
$ docker pull orientdb@sha256:06b4dd8ddc075c86429abc944f3ce0eb6dd24261629c00bc150a56f3757fd553
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192869816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c15c48b6c6b652266dfeb9120a6cb31289df42bd37bd68e63fac785bba5c6e`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_VERSION=2.2.37
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Sat, 05 Nov 2022 01:31:39 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 01:31:41 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 05 Nov 2022 01:31:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:31:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 05 Nov 2022 01:31:42 GMT
WORKDIR /orientdb
# Sat, 05 Nov 2022 01:31:42 GMT
EXPOSE 2424
# Sat, 05 Nov 2022 01:31:42 GMT
EXPOSE 2480
# Sat, 05 Nov 2022 01:31:42 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a548a3c635bb232c3e6414a5c9feb13fb9a60de12cef7b4cc7963d3c4f955796`  
		Last Modified: Sat, 05 Nov 2022 01:33:35 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdde58255d054a72af86fe6da78f85a2f1992f2da761e04b733119a3d61683d`  
		Last Modified: Sat, 05 Nov 2022 01:33:39 GMT  
		Size: 46.5 MB (46473871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37-spatial`

```console
$ docker pull orientdb@sha256:9938fdf6048dd30a6f2dbdf6164539abf2fb2cea4f1b5478ea0209398b716114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37-spatial` - linux; amd64

```console
$ docker pull orientdb@sha256:2c360efed85f9aec4011927866ac31cb515f5302b80ea7eeeec3fadcce816a56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194072409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cbca16186ca147fdfe01adcf128ec92bc2ba796b5dff0168f6f092772bbb8c`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_VERSION=2.2.37
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Sat, 05 Nov 2022 01:31:35 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Sat, 05 Nov 2022 01:31:39 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 01:31:41 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 05 Nov 2022 01:31:41 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:31:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 05 Nov 2022 01:31:42 GMT
WORKDIR /orientdb
# Sat, 05 Nov 2022 01:31:42 GMT
EXPOSE 2424
# Sat, 05 Nov 2022 01:31:42 GMT
EXPOSE 2480
# Sat, 05 Nov 2022 01:31:42 GMT
CMD ["server.sh"]
# Sat, 05 Nov 2022 01:31:45 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_MD5=9f64ab5e959f5d9ad9ea5195d6d621d2
# Sat, 05 Nov 2022 01:31:45 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_SHA1=1748c9779ea7a8cb8fc068fcabf960e1778e8a19
# Sat, 05 Nov 2022 01:31:45 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-spatial/2.2.37/orientdb-spatial-2.2.37-dist.jar
# Sat, 05 Nov 2022 01:31:46 GMT
RUN wget $ORIENTDB_DOWNLOAD_SPATIAL_URL     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_MD5 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | md5sum -c -     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_SHA1 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | sha1sum -c -     && mv orientdb-spatial-*-dist.jar /orientdb/lib/
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a548a3c635bb232c3e6414a5c9feb13fb9a60de12cef7b4cc7963d3c4f955796`  
		Last Modified: Sat, 05 Nov 2022 01:33:35 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdde58255d054a72af86fe6da78f85a2f1992f2da761e04b733119a3d61683d`  
		Last Modified: Sat, 05 Nov 2022 01:33:39 GMT  
		Size: 46.5 MB (46473871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8527d0a400478be3e6813a8000321dae53ee5a3e2a64eb376ba4d74f6ecead8f`  
		Last Modified: Sat, 05 Nov 2022 01:33:50 GMT  
		Size: 1.2 MB (1202593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0`

```console
$ docker pull orientdb@sha256:4e4797b971104b04e573274a821427fdc66561a8858a6e47062ebef7d359fa44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0` - linux; amd64

```console
$ docker pull orientdb@sha256:4cf1e1ade5f610056c97e9f197263083f55a6f1972925a40ddd5efb9a4596834
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183460809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c32ba57ab55f6180035faeec32cc55e7548e184858e67fede4b938374396f6`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 05 Nov 2022 01:31:12 GMT
ENV ORIENTDB_VERSION=3.0.44
# Sat, 05 Nov 2022 01:31:12 GMT
ENV ORIENTDB_DOWNLOAD_MD5=1bdcdb4d9c54fc78a1b56b8375ca990d
# Sat, 05 Nov 2022 01:31:12 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6462dacd0df0725f10f85bee9666a0f6979187a6
# Sat, 05 Nov 2022 01:31:12 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.44/orientdb-community-3.0.44.tar.gz
# Sat, 05 Nov 2022 01:31:16 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 01:31:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 05 Nov 2022 01:31:20 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:31:20 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 05 Nov 2022 01:31:20 GMT
WORKDIR /orientdb
# Sat, 05 Nov 2022 01:31:20 GMT
EXPOSE 2424
# Sat, 05 Nov 2022 01:31:20 GMT
EXPOSE 2480
# Sat, 05 Nov 2022 01:31:20 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae118398c9f60de12c48289437e5c52c5be61f3c652fd69d3876976715c6c20`  
		Last Modified: Sat, 05 Nov 2022 01:33:09 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6852af76085670bf1a0a4e4ab8899881ce98eeceb8844fc23048f872378fb5`  
		Last Modified: Sat, 05 Nov 2022 01:33:11 GMT  
		Size: 37.1 MB (37064865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0-tp3`

```console
$ docker pull orientdb@sha256:8fd4a5483c71d6da20b16457fb057f3b9d37621e5eec45acb3a1dd73cef2e67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:8b0da4cb1f601dbad5fb2d8fd13b0f079d93786839b44d79fb3434548db69d0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210481082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec1bf44bacb31e578885e2eff729322ee39ce95238110dcb5c4e113f446e922`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 05 Nov 2022 01:31:12 GMT
ENV ORIENTDB_VERSION=3.0.44
# Sat, 05 Nov 2022 01:31:23 GMT
ENV ORIENTDB_DOWNLOAD_MD5=44f8c96f57f75a4b9e2a3996a3b17512
# Sat, 05 Nov 2022 01:31:23 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c49067782368e13082648d48bf6685969a5ed550
# Sat, 05 Nov 2022 01:31:24 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.44/orientdb-tp3-3.0.44.tar.gz
# Sat, 05 Nov 2022 01:31:27 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 01:31:30 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 05 Nov 2022 01:31:31 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Sat, 05 Nov 2022 01:31:31 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:31:31 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 05 Nov 2022 01:31:31 GMT
WORKDIR /orientdb
# Sat, 05 Nov 2022 01:31:31 GMT
EXPOSE 2424
# Sat, 05 Nov 2022 01:31:31 GMT
EXPOSE 2480
# Sat, 05 Nov 2022 01:31:31 GMT
EXPOSE 8182
# Sat, 05 Nov 2022 01:31:32 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b75b87af2d7e0aabe95fa8ed6ddf119ca38b4bdc29272fd3d514e77e241857`  
		Last Modified: Sat, 05 Nov 2022 01:33:22 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cb162a855ef9aa6ef63bc30b61baf9e361b47daa562466625a1d4fdfc97567`  
		Last Modified: Sat, 05 Nov 2022 01:33:25 GMT  
		Size: 64.1 MB (64083761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478199d75b47cc50deb9f3e54427133c405b17712a6286d515b070bd0129c46d`  
		Last Modified: Sat, 05 Nov 2022 01:33:21 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.44`

```console
$ docker pull orientdb@sha256:4e4797b971104b04e573274a821427fdc66561a8858a6e47062ebef7d359fa44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.44` - linux; amd64

```console
$ docker pull orientdb@sha256:4cf1e1ade5f610056c97e9f197263083f55a6f1972925a40ddd5efb9a4596834
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183460809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c32ba57ab55f6180035faeec32cc55e7548e184858e67fede4b938374396f6`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 05 Nov 2022 01:31:12 GMT
ENV ORIENTDB_VERSION=3.0.44
# Sat, 05 Nov 2022 01:31:12 GMT
ENV ORIENTDB_DOWNLOAD_MD5=1bdcdb4d9c54fc78a1b56b8375ca990d
# Sat, 05 Nov 2022 01:31:12 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=6462dacd0df0725f10f85bee9666a0f6979187a6
# Sat, 05 Nov 2022 01:31:12 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.44/orientdb-community-3.0.44.tar.gz
# Sat, 05 Nov 2022 01:31:16 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 01:31:20 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 05 Nov 2022 01:31:20 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:31:20 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 05 Nov 2022 01:31:20 GMT
WORKDIR /orientdb
# Sat, 05 Nov 2022 01:31:20 GMT
EXPOSE 2424
# Sat, 05 Nov 2022 01:31:20 GMT
EXPOSE 2480
# Sat, 05 Nov 2022 01:31:20 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae118398c9f60de12c48289437e5c52c5be61f3c652fd69d3876976715c6c20`  
		Last Modified: Sat, 05 Nov 2022 01:33:09 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6852af76085670bf1a0a4e4ab8899881ce98eeceb8844fc23048f872378fb5`  
		Last Modified: Sat, 05 Nov 2022 01:33:11 GMT  
		Size: 37.1 MB (37064865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.44-tp3`

```console
$ docker pull orientdb@sha256:8fd4a5483c71d6da20b16457fb057f3b9d37621e5eec45acb3a1dd73cef2e67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.44-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:8b0da4cb1f601dbad5fb2d8fd13b0f079d93786839b44d79fb3434548db69d0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210481082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec1bf44bacb31e578885e2eff729322ee39ce95238110dcb5c4e113f446e922`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 05 Nov 2022 01:31:12 GMT
ENV ORIENTDB_VERSION=3.0.44
# Sat, 05 Nov 2022 01:31:23 GMT
ENV ORIENTDB_DOWNLOAD_MD5=44f8c96f57f75a4b9e2a3996a3b17512
# Sat, 05 Nov 2022 01:31:23 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c49067782368e13082648d48bf6685969a5ed550
# Sat, 05 Nov 2022 01:31:24 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.44/orientdb-tp3-3.0.44.tar.gz
# Sat, 05 Nov 2022 01:31:27 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 01:31:30 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 05 Nov 2022 01:31:31 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Sat, 05 Nov 2022 01:31:31 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:31:31 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 05 Nov 2022 01:31:31 GMT
WORKDIR /orientdb
# Sat, 05 Nov 2022 01:31:31 GMT
EXPOSE 2424
# Sat, 05 Nov 2022 01:31:31 GMT
EXPOSE 2480
# Sat, 05 Nov 2022 01:31:31 GMT
EXPOSE 8182
# Sat, 05 Nov 2022 01:31:32 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b75b87af2d7e0aabe95fa8ed6ddf119ca38b4bdc29272fd3d514e77e241857`  
		Last Modified: Sat, 05 Nov 2022 01:33:22 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cb162a855ef9aa6ef63bc30b61baf9e361b47daa562466625a1d4fdfc97567`  
		Last Modified: Sat, 05 Nov 2022 01:33:25 GMT  
		Size: 64.1 MB (64083761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478199d75b47cc50deb9f3e54427133c405b17712a6286d515b070bd0129c46d`  
		Last Modified: Sat, 05 Nov 2022 01:33:21 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:27edefd678283e82c70728479def71cc164d4a7b99dc5ceb57e7dde95e3734f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:add4d0e68b3992b87bfbf67311ad7484c5835417e5be046213f3e64773400250
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199477154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00db3b0ce55b35dc17e285a76674b842c1f704ab77b4cddf262fe9f532c73ad`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 05 Nov 2022 01:30:50 GMT
ENV ORIENTDB_VERSION=3.1.20
# Sat, 05 Nov 2022 01:30:50 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Sat, 05 Nov 2022 01:30:50 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Sat, 05 Nov 2022 01:30:50 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Sat, 05 Nov 2022 01:30:54 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 01:30:57 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 05 Nov 2022 01:30:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:30:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 05 Nov 2022 01:30:58 GMT
WORKDIR /orientdb
# Sat, 05 Nov 2022 01:30:58 GMT
EXPOSE 2424
# Sat, 05 Nov 2022 01:30:58 GMT
EXPOSE 2480
# Sat, 05 Nov 2022 01:30:58 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377d80972e14db10610be6b5e1706eb8bcb387e6d321b06c53b6953db783bb85`  
		Last Modified: Sat, 05 Nov 2022 01:32:42 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939368a7243690f17fadfbcb3494c9691be60006bb8311ad985fb64e8b95e474`  
		Last Modified: Sat, 05 Nov 2022 01:32:45 GMT  
		Size: 53.1 MB (53081207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:6b5241c78cdbd4d1d27397b6d864f6c56e7887a536a933b4e70b2932e0032a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:6c7c4ace10fd0349aa2fcbc0c69c55c0df417e386074fdecbb4999e482899671
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 MB (222484212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e1956713978bfa7c5b9495a99b794c9251366092f9e147c2ef09366a729ee9`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 05 Nov 2022 01:30:50 GMT
ENV ORIENTDB_VERSION=3.1.20
# Sat, 05 Nov 2022 01:31:00 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Sat, 05 Nov 2022 01:31:00 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Sat, 05 Nov 2022 01:31:00 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Sat, 05 Nov 2022 01:31:04 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 01:31:08 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 05 Nov 2022 01:31:08 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Sat, 05 Nov 2022 01:31:08 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:31:08 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 05 Nov 2022 01:31:08 GMT
WORKDIR /orientdb
# Sat, 05 Nov 2022 01:31:08 GMT
EXPOSE 2424
# Sat, 05 Nov 2022 01:31:09 GMT
EXPOSE 2480
# Sat, 05 Nov 2022 01:31:09 GMT
EXPOSE 8182
# Sat, 05 Nov 2022 01:31:09 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9877810e05869a589842d6c5d9f16020f6584aef19896009f131624c5062d427`  
		Last Modified: Sat, 05 Nov 2022 01:32:55 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef73d4d1e0664ce97d3da4d9d4f20dec36dbd31b9663a66397ff1dc8be6321cb`  
		Last Modified: Sat, 05 Nov 2022 01:32:59 GMT  
		Size: 76.1 MB (76086891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b88bc58200b5d9edfc0ce8902691d6ea9a9f253573bce4be487d5a15a1872f`  
		Last Modified: Sat, 05 Nov 2022 01:32:55 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.20`

```console
$ docker pull orientdb@sha256:27edefd678283e82c70728479def71cc164d4a7b99dc5ceb57e7dde95e3734f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.20` - linux; amd64

```console
$ docker pull orientdb@sha256:add4d0e68b3992b87bfbf67311ad7484c5835417e5be046213f3e64773400250
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199477154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00db3b0ce55b35dc17e285a76674b842c1f704ab77b4cddf262fe9f532c73ad`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 05 Nov 2022 01:30:50 GMT
ENV ORIENTDB_VERSION=3.1.20
# Sat, 05 Nov 2022 01:30:50 GMT
ENV ORIENTDB_DOWNLOAD_MD5=751c6a02fe142c6c2dbfca56e73ec315
# Sat, 05 Nov 2022 01:30:50 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1be782682b0dbf97fc90f8623b7b65ec32283a14
# Sat, 05 Nov 2022 01:30:50 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.20/orientdb-community-3.1.20.tar.gz
# Sat, 05 Nov 2022 01:30:54 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 01:30:57 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 05 Nov 2022 01:30:57 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:30:57 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 05 Nov 2022 01:30:58 GMT
WORKDIR /orientdb
# Sat, 05 Nov 2022 01:30:58 GMT
EXPOSE 2424
# Sat, 05 Nov 2022 01:30:58 GMT
EXPOSE 2480
# Sat, 05 Nov 2022 01:30:58 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377d80972e14db10610be6b5e1706eb8bcb387e6d321b06c53b6953db783bb85`  
		Last Modified: Sat, 05 Nov 2022 01:32:42 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939368a7243690f17fadfbcb3494c9691be60006bb8311ad985fb64e8b95e474`  
		Last Modified: Sat, 05 Nov 2022 01:32:45 GMT  
		Size: 53.1 MB (53081207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.20-tp3`

```console
$ docker pull orientdb@sha256:6b5241c78cdbd4d1d27397b6d864f6c56e7887a536a933b4e70b2932e0032a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.20-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:6c7c4ace10fd0349aa2fcbc0c69c55c0df417e386074fdecbb4999e482899671
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 MB (222484212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e1956713978bfa7c5b9495a99b794c9251366092f9e147c2ef09366a729ee9`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 05 Nov 2022 01:30:50 GMT
ENV ORIENTDB_VERSION=3.1.20
# Sat, 05 Nov 2022 01:31:00 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59a038b1b313052f9b39d369667ae713
# Sat, 05 Nov 2022 01:31:00 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=9f2d7a9299744862caf60894222ae156c065b174
# Sat, 05 Nov 2022 01:31:00 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.20/orientdb-tp3-3.1.20.tar.gz
# Sat, 05 Nov 2022 01:31:04 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 01:31:08 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 05 Nov 2022 01:31:08 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Sat, 05 Nov 2022 01:31:08 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:31:08 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 05 Nov 2022 01:31:08 GMT
WORKDIR /orientdb
# Sat, 05 Nov 2022 01:31:08 GMT
EXPOSE 2424
# Sat, 05 Nov 2022 01:31:09 GMT
EXPOSE 2480
# Sat, 05 Nov 2022 01:31:09 GMT
EXPOSE 8182
# Sat, 05 Nov 2022 01:31:09 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9877810e05869a589842d6c5d9f16020f6584aef19896009f131624c5062d427`  
		Last Modified: Sat, 05 Nov 2022 01:32:55 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef73d4d1e0664ce97d3da4d9d4f20dec36dbd31b9663a66397ff1dc8be6321cb`  
		Last Modified: Sat, 05 Nov 2022 01:32:59 GMT  
		Size: 76.1 MB (76086891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b88bc58200b5d9edfc0ce8902691d6ea9a9f253573bce4be487d5a15a1872f`  
		Last Modified: Sat, 05 Nov 2022 01:32:55 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:c3d7c036ecc5746b84cbfe4c4b3ed3e45cee12842b3a84d12d398c099226ff4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2` - linux; amd64

```console
$ docker pull orientdb@sha256:548c8a71d142319abe0f1c10dbbf2832bce37f66c7dae0e7e9b9937ff8d79d8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209717637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56757d9b3dbd89536541c2d612d4c9ee726742f1b748015d7f5fb11b296024f2`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_VERSION=3.2.12
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5ae25a2db8ba57073f4b91c48394ed0d
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eadd8d05c9f0862fdf7a02b9fe85c50db7ceadac
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.12/orientdb-community-3.2.12.tar.gz
# Thu, 10 Nov 2022 21:06:28 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Nov 2022 21:06:31 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 10 Nov 2022 21:06:32 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Nov 2022 21:06:32 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 10 Nov 2022 21:06:32 GMT
WORKDIR /orientdb
# Thu, 10 Nov 2022 21:06:32 GMT
EXPOSE 2424
# Thu, 10 Nov 2022 21:06:32 GMT
EXPOSE 2480
# Thu, 10 Nov 2022 21:06:32 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff4973369986c457bc8ebf6c53cff4136557a6db7b096aef98dd22acbcf6f43`  
		Last Modified: Thu, 10 Nov 2022 21:07:20 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbacec3046dbc76e0b5a90110f9389637e1ab913808df49b6c8998d244330b4`  
		Last Modified: Thu, 10 Nov 2022 21:07:24 GMT  
		Size: 63.3 MB (63321691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:1281247cc5bca5494422ceb49b117fa19418b9ba7bf6b59477a628194ab10991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:7f4c5c8f800775b2d859e9cecadcaebe5c7c32b0f3fb072c9d179650f5736434
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235592872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083315223aa77c90d370f69fb238ca09040b41343b4682d55da53c45ec3dfa9e`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_VERSION=3.2.12
# Thu, 10 Nov 2022 21:06:36 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cfa7353c82e2fbc672380faa3a3a8e7f
# Thu, 10 Nov 2022 21:06:36 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=5336a589221f104ca41d3f4d31ebc21dced5d518
# Thu, 10 Nov 2022 21:06:36 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.12/orientdb-tp3-3.2.12.tar.gz
# Thu, 10 Nov 2022 21:06:40 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Nov 2022 21:06:45 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 10 Nov 2022 21:06:46 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 10 Nov 2022 21:06:46 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Nov 2022 21:06:46 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 10 Nov 2022 21:06:46 GMT
WORKDIR /orientdb
# Thu, 10 Nov 2022 21:06:46 GMT
EXPOSE 2424
# Thu, 10 Nov 2022 21:06:46 GMT
EXPOSE 2480
# Thu, 10 Nov 2022 21:06:46 GMT
EXPOSE 8182
# Thu, 10 Nov 2022 21:06:47 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3527025a26f03a309d3ba81881bb810681d2586c3a0cb2442a1e82a864d8622`  
		Last Modified: Thu, 10 Nov 2022 21:07:36 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3300b7623b022d4c423d6128d7076a798ebf806b2364d93b0d2b522b005e8862`  
		Last Modified: Thu, 10 Nov 2022 21:07:41 GMT  
		Size: 89.2 MB (89195550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e272220d591ee161a54612573ad7ede058035e8ebb2cbb7f3e4847ac298049`  
		Last Modified: Thu, 10 Nov 2022 21:07:36 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.12`

```console
$ docker pull orientdb@sha256:c3d7c036ecc5746b84cbfe4c4b3ed3e45cee12842b3a84d12d398c099226ff4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2.12` - linux; amd64

```console
$ docker pull orientdb@sha256:548c8a71d142319abe0f1c10dbbf2832bce37f66c7dae0e7e9b9937ff8d79d8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209717637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56757d9b3dbd89536541c2d612d4c9ee726742f1b748015d7f5fb11b296024f2`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_VERSION=3.2.12
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5ae25a2db8ba57073f4b91c48394ed0d
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eadd8d05c9f0862fdf7a02b9fe85c50db7ceadac
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.12/orientdb-community-3.2.12.tar.gz
# Thu, 10 Nov 2022 21:06:28 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Nov 2022 21:06:31 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 10 Nov 2022 21:06:32 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Nov 2022 21:06:32 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 10 Nov 2022 21:06:32 GMT
WORKDIR /orientdb
# Thu, 10 Nov 2022 21:06:32 GMT
EXPOSE 2424
# Thu, 10 Nov 2022 21:06:32 GMT
EXPOSE 2480
# Thu, 10 Nov 2022 21:06:32 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff4973369986c457bc8ebf6c53cff4136557a6db7b096aef98dd22acbcf6f43`  
		Last Modified: Thu, 10 Nov 2022 21:07:20 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbacec3046dbc76e0b5a90110f9389637e1ab913808df49b6c8998d244330b4`  
		Last Modified: Thu, 10 Nov 2022 21:07:24 GMT  
		Size: 63.3 MB (63321691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.12-tp3`

```console
$ docker pull orientdb@sha256:1281247cc5bca5494422ceb49b117fa19418b9ba7bf6b59477a628194ab10991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2.12-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:7f4c5c8f800775b2d859e9cecadcaebe5c7c32b0f3fb072c9d179650f5736434
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235592872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083315223aa77c90d370f69fb238ca09040b41343b4682d55da53c45ec3dfa9e`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_VERSION=3.2.12
# Thu, 10 Nov 2022 21:06:36 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cfa7353c82e2fbc672380faa3a3a8e7f
# Thu, 10 Nov 2022 21:06:36 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=5336a589221f104ca41d3f4d31ebc21dced5d518
# Thu, 10 Nov 2022 21:06:36 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.12/orientdb-tp3-3.2.12.tar.gz
# Thu, 10 Nov 2022 21:06:40 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Nov 2022 21:06:45 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 10 Nov 2022 21:06:46 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 10 Nov 2022 21:06:46 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Nov 2022 21:06:46 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 10 Nov 2022 21:06:46 GMT
WORKDIR /orientdb
# Thu, 10 Nov 2022 21:06:46 GMT
EXPOSE 2424
# Thu, 10 Nov 2022 21:06:46 GMT
EXPOSE 2480
# Thu, 10 Nov 2022 21:06:46 GMT
EXPOSE 8182
# Thu, 10 Nov 2022 21:06:47 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3527025a26f03a309d3ba81881bb810681d2586c3a0cb2442a1e82a864d8622`  
		Last Modified: Thu, 10 Nov 2022 21:07:36 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3300b7623b022d4c423d6128d7076a798ebf806b2364d93b0d2b522b005e8862`  
		Last Modified: Thu, 10 Nov 2022 21:07:41 GMT  
		Size: 89.2 MB (89195550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e272220d591ee161a54612573ad7ede058035e8ebb2cbb7f3e4847ac298049`  
		Last Modified: Thu, 10 Nov 2022 21:07:36 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:c3d7c036ecc5746b84cbfe4c4b3ed3e45cee12842b3a84d12d398c099226ff4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:548c8a71d142319abe0f1c10dbbf2832bce37f66c7dae0e7e9b9937ff8d79d8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209717637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56757d9b3dbd89536541c2d612d4c9ee726742f1b748015d7f5fb11b296024f2`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='c9126fe87ebec147af2f237424d9b77f7ea5a9844999e8c90d046fdb741bf463';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 01:30:26 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 05 Nov 2022 01:30:26 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_VERSION=3.2.12
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_DOWNLOAD_MD5=5ae25a2db8ba57073f4b91c48394ed0d
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=eadd8d05c9f0862fdf7a02b9fe85c50db7ceadac
# Thu, 10 Nov 2022 21:06:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.12/orientdb-community-3.2.12.tar.gz
# Thu, 10 Nov 2022 21:06:28 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Nov 2022 21:06:31 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 10 Nov 2022 21:06:32 GMT
ENV PATH=/orientdb/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Nov 2022 21:06:32 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 10 Nov 2022 21:06:32 GMT
WORKDIR /orientdb
# Thu, 10 Nov 2022 21:06:32 GMT
EXPOSE 2424
# Thu, 10 Nov 2022 21:06:32 GMT
EXPOSE 2480
# Thu, 10 Nov 2022 21:06:32 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cd2b580a647650c8d650377e6ad35526f51d10dd0c29b4e054402fdc90955a`  
		Last Modified: Fri, 04 Nov 2022 23:25:35 GMT  
		Size: 103.5 MB (103530821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191e5a2019b63444c66595f90922ab90da59ba089d35c72bc534874fc829341c`  
		Last Modified: Fri, 04 Nov 2022 23:25:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff4973369986c457bc8ebf6c53cff4136557a6db7b096aef98dd22acbcf6f43`  
		Last Modified: Thu, 10 Nov 2022 21:07:20 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbacec3046dbc76e0b5a90110f9389637e1ab913808df49b6c8998d244330b4`  
		Last Modified: Thu, 10 Nov 2022 21:07:24 GMT  
		Size: 63.3 MB (63321691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
