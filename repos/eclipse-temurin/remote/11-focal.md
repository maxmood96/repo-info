## `eclipse-temurin:11-focal`

```console
$ docker pull eclipse-temurin@sha256:3dfaa74d8b8d0cdc9c2d8c5db7c8f3d62fe2cd2856e58cd8669b668471d2c22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e3c58718843d0796143a2a3c50cda85906015e1d34ce746b53cb0a2e56f85b37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238414649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064fcc3682105afe0bf9045f5b9ad42fd8ccf4c72d0f82218e837921722f0751`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 04:46:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:47:03 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 04:47:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 04:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:47:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 04:47:15 GMT
CMD ["jshell"]
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
	-	`sha256:8c6bb5a7477231666eb57c4a575e8d78d8892399d36eb625d994189474bb38f8`  
		Last Modified: Fri, 01 Oct 2021 04:50:25 GMT  
		Size: 193.8 MB (193812419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a357057e4b8b6a4cfa56f1c974b47f5bab5201892c297436f5da19d54918f7`  
		Last Modified: Fri, 01 Oct 2021 04:50:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-focal` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:da03e068fb185a16591713ca20fd2edf240ee96f376b1f6d9075f0ab9cf075bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220670527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3775080dec0a16bd5c779541121e0d38df1d0f72b3f40f0a3b183ae313747269`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 02 Oct 2021 05:58:58 GMT
ADD file:17b7faea72ce285877ae2e83ecc15fc88de184361899edfcb561531ea121090b in / 
# Sat, 02 Oct 2021 05:58:59 GMT
CMD ["bash"]
# Sat, 02 Oct 2021 23:26:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Oct 2021 23:26:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 23:28:04 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Sat, 02 Oct 2021 23:28:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 02 Oct 2021 23:28:27 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Oct 2021 23:28:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 02 Oct 2021 23:28:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29a0bfee4452af9c258710b3049350eec1ed6ee85e33634a638e982934e59d83`  
		Last Modified: Sat, 02 Oct 2021 06:03:00 GMT  
		Size: 24.1 MB (24067218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64e2199de8cbbc437199cb30a504a0e04104b5a48bab3447d69fdb35ef7e9fd`  
		Last Modified: Sat, 02 Oct 2021 23:33:01 GMT  
		Size: 14.9 MB (14897772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febd8bba8434a8851302730054590f0e9819ea501b148ea05b81c1543a72ea87`  
		Last Modified: Sat, 02 Oct 2021 23:34:00 GMT  
		Size: 181.7 MB (181705374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b45b93bec49fb5b7c1c9b128a03bad4f3b99b81dd6a4c6f4a5debc07cc3f6`  
		Last Modified: Sat, 02 Oct 2021 23:32:52 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:402bfe8f684f5fe2b77158afc1d0a08c6f03425a5254bb244c0aa4be3452add1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233569586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6a2f00395390944a19c7588ab918dcdcdffb673b2d3a21310ffeb8477886fc`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:30:14 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Fri, 01 Oct 2021 03:30:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:30:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:30:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:30:23 GMT
CMD ["jshell"]
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
	-	`sha256:3f016b17a5bc64c11dde173dde6464a50bb39f659be7d2b10a1054316dd87fb4`  
		Last Modified: Fri, 01 Oct 2021 03:34:27 GMT  
		Size: 190.5 MB (190501799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b67910372911d708dadbe83ac45872796069531eef45ac657380a1e4d22d19`  
		Last Modified: Fri, 01 Oct 2021 03:34:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:8d23cb9481203f19ef4068e026b5ef1d4dca0c5224ad3deb8614ebe888ed90f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226184394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9d996642e2e07dfcbf9c691714e76737208eea377b1e9ad18825f0ed8deeb3`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:54:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:55:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 00:57:23 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Sat, 16 Oct 2021 00:57:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 00:57:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 00:57:51 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 16 Oct 2021 00:57:53 GMT
CMD ["jshell"]
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
	-	`sha256:aaca7a459d94934b461957e71559ffcb47511f54848b2fa0a18b62c831c007ad`  
		Last Modified: Sat, 16 Oct 2021 01:04:27 GMT  
		Size: 175.7 MB (175686484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31127949029231226b0a1198fbf0e913dd0e80d2715727fc19386fd48b6b34`  
		Last Modified: Sat, 16 Oct 2021 01:04:08 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-focal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:70e646cee495e737e7faba2d05550447769c88ec95348603c5cbe3987500003b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.6 MB (211589859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f943b7c411b2e62817701505c86e3a2e59c846be2065092a981a5e0f7a995a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 00:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Sat, 16 Oct 2021 00:59:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='105bdc12fcd54c551e8e8ac96bc82412467244c32063689c41cee29ceb7452a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        armhf|arm)          ESUM='85929246a9d60ed90e2385ea3f4857798c77019c5100f00189c1dd0a093abea7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='234a9bafe029ea6cab5d46f9617b5d016a29faa187a42081d0e066f23647b7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='99c1c61e9d67b01a649687189e5a00f89a2371dc1bfed06bb078d127edfa7995';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8770f600fc3b89bf331213c7aa21f8eedd9ca5d96036d1cd48cb2748a3dbefd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 00:59:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 00:59:05 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 16 Oct 2021 00:59:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9aae3329e8c839bcceb87144b9f18dbe85b59f108d21ca33422ddd42c32344`  
		Last Modified: Sat, 16 Oct 2021 01:01:12 GMT  
		Size: 168.7 MB (168726763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e2babc36c34e9a1804509361ffbefaf3e47cd2aed7c1d7ec038fd85b7f82c1`  
		Last Modified: Sat, 16 Oct 2021 01:01:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
