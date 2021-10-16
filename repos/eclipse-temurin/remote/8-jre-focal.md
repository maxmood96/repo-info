## `eclipse-temurin:8-jre-focal`

```console
$ docker pull eclipse-temurin@sha256:b0a19068696f7900ba1afec8cdd00501087797ebb518b5cc24caa7248a21cb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-jre-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d5f47481281a62232433beca7fe9f27e113072044e796b4f960057fd12dc0a13
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86314169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fb51b2ae0c9f5443afa36a984d89cfed3130c955ec297e6343f333648694b1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:46:35 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Fri, 01 Oct 2021 04:46:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9951a36430c14548f78569135956e929db2554bfc706bb3fe0bf9a14acd28055';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0f242dc94b2c46f231e811427e30031cd1c7e5667979f8b403296008863d150e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:46:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:46:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfa0820368ab7e292075aa2118a674d9feccdeb45d31bfc0efa051af8683cc8`  
		Last Modified: Fri, 01 Oct 2021 04:49:34 GMT  
		Size: 16.0 MB (16033156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f24a6f1e7d19d72576ecfaf27c0e8b754641203d440283bc86e230740c74da`  
		Last Modified: Fri, 01 Oct 2021 04:50:00 GMT  
		Size: 41.7 MB (41711939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d61bf3d04f329f4836ad7b128e574fb6eb6b25d5f13433effdc50da1e26428`  
		Last Modified: Fri, 01 Oct 2021 04:49:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:7710323d047f0eca15ba7324b56814129983717daf25eb7018277c3ca8789717
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83811482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc466fd7e773f7155c8041dd2c466befea6b44210f60dfb7eb63453f63b01bcc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Fri, 01 Oct 2021 03:30:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9951a36430c14548f78569135956e929db2554bfc706bb3fe0bf9a14acd28055';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0f242dc94b2c46f231e811427e30031cd1c7e5667979f8b403296008863d150e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:03 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb858a8ef47e865174d4c3dd7ab3ae7c523ba848a3d77bb284a6aca0c7c215`  
		Last Modified: Fri, 01 Oct 2021 03:33:57 GMT  
		Size: 40.7 MB (40743695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdd8b68a69037e3bf7636bf15e043a834909638440dab9e3773f5f3449a12d3`  
		Last Modified: Fri, 01 Oct 2021 03:33:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:9bdf0afbd7b8e4e1af784b57788edce3f3ec8b83f044c550c90f7edf1ec2439a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91634820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c76ad016775564ade9e05344f34b9fa5164594a25cca50eabf0ed3bf5e7668`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:54:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:55:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 00:56:03 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Sat, 16 Oct 2021 00:56:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9951a36430c14548f78569135956e929db2554bfc706bb3fe0bf9a14acd28055';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0f242dc94b2c46f231e811427e30031cd1c7e5667979f8b403296008863d150e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 00:56:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 00:57:08 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c930749dacf55e37561edab7967f5a2f51660034fee0da501c2d71cb783301`  
		Last Modified: Sat, 16 Oct 2021 01:03:26 GMT  
		Size: 17.2 MB (17210510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7b88d52eabdac591f44776c16dbb828f7afc2573ad9b214691f0f1daf560fb`  
		Last Modified: Sat, 16 Oct 2021 01:03:57 GMT  
		Size: 41.1 MB (41136911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507961e392cb50d2126394c22a5398b05a65298de3702e635d049020d2c7ffd5`  
		Last Modified: Sat, 16 Oct 2021 01:03:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
