## `eclipse-temurin:17_35-jdk-focal`

```console
$ docker pull eclipse-temurin@sha256:ce7bb8be9537a989b9f64a76acbf9e809b1ef9bf091b421df474822876b0383c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17_35-jdk-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:485c8cbd22faa14719042dd806976b9355aa52da7d3ad7da46d7ef29aa6ae986
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241316997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dbda718db0a6fa833c47d1e90de7f42354fe7a2ffffa4c30acaa6c79c1112f`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 02:45:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:46:05 GMT
ENV JAVA_VERSION=jdk-17+35
# Sat, 16 Oct 2021 02:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e08e6d8c84da28a2c49ccd511f8835c329fbdd8e4faff662c58fa24cca74021d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_aarch64_linux_hotspot_17_35.tar.gz';          ;;        armhf|arm)          ESUM='77ef6aa6f665373e212097b937c22d0cad2add90e439ec0e90534a7ff0e8a6e9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_arm_linux_hotspot_17_35.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2e58f76fd332b73f323e47c73d0a81b76739debab067e7a32ed6abd73fd64c57';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_ppc64le_linux_hotspot_17_35.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a48159fca62b7f6afd58fb2e9712a3ef1494950212d4631e25598b45d9599b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_s390x_linux_hotspot_17_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6f1335d9a7855159f982dac557420397be9aa85f3f7bc84e111d25871c02c0c7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_linux_hotspot_17_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 02:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 02:46:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 16 Oct 2021 02:46:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1fba688e4817fa2b044e9fc220607825d6d823866f99050e9f3321efdfa28d`  
		Last Modified: Sat, 16 Oct 2021 02:48:44 GMT  
		Size: 19.8 MB (19776863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa3f85b7707d2a0e5b9cfaf0cf5a9d7199087ca0e338ab644579047ef393a6d`  
		Last Modified: Sat, 16 Oct 2021 02:49:26 GMT  
		Size: 193.0 MB (192972872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44775f294646bdb73068b19b88cc690ed61e12eca252616a385bafdcd913dddf`  
		Last Modified: Sat, 16 Oct 2021 02:49:12 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17_35-jdk-focal` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:469e862bfbbc95a3895805d6b3b486a75df3e8b8338faef4190473e1c9ad5be4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233203731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e041b39bc69df2048791fec5f44054878db10788bf690dece219f4378c3e82ed`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Oct 2021 01:12:00 GMT
ADD file:625e3906181f4bd86e59a0e9748f67fcb1391a2e65e36c729e71353381a49757 in / 
# Sat, 16 Oct 2021 01:12:00 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:38:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 02:41:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:41:49 GMT
ENV JAVA_VERSION=jdk-17+35
# Sat, 16 Oct 2021 02:42:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e08e6d8c84da28a2c49ccd511f8835c329fbdd8e4faff662c58fa24cca74021d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_aarch64_linux_hotspot_17_35.tar.gz';          ;;        armhf|arm)          ESUM='77ef6aa6f665373e212097b937c22d0cad2add90e439ec0e90534a7ff0e8a6e9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_arm_linux_hotspot_17_35.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2e58f76fd332b73f323e47c73d0a81b76739debab067e7a32ed6abd73fd64c57';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_ppc64le_linux_hotspot_17_35.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a48159fca62b7f6afd58fb2e9712a3ef1494950212d4631e25598b45d9599b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_s390x_linux_hotspot_17_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6f1335d9a7855159f982dac557420397be9aa85f3f7bc84e111d25871c02c0c7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_linux_hotspot_17_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 02:42:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 02:42:14 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 16 Oct 2021 02:42:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8795d4da4abd6abcafe7285749aa85d3a164999e84720a3845f764e56e306771`  
		Last Modified: Sat, 16 Oct 2021 01:15:01 GMT  
		Size: 24.1 MB (24064451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73092bd78be324813f4a4bdc7c75343bcc4753cf3a97145d91d7c8d8ae1ec9e`  
		Last Modified: Sat, 16 Oct 2021 02:47:09 GMT  
		Size: 19.2 MB (19196446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1064c13554afddb973cfd835b83cd228df95d30d6d0fece99cddbe8c945c7357`  
		Last Modified: Sat, 16 Oct 2021 02:48:11 GMT  
		Size: 189.9 MB (189942672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7ee8a7d282cdb18249ff177cae80de70c5e3edb97c727bf4d5c02cc66710c8`  
		Last Modified: Sat, 16 Oct 2021 02:46:57 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17_35-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c6860cf252999c6b22b69a88fd5b80e6da26684b789ed861db31247e469969c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237552122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e7a6b71d982ee3d8d947589985b765136a45140dd2c366f0875e0d9e3c586e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:31:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:31:30 GMT
ENV JAVA_VERSION=jdk-17+35
# Fri, 01 Oct 2021 03:31:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e08e6d8c84da28a2c49ccd511f8835c329fbdd8e4faff662c58fa24cca74021d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_aarch64_linux_hotspot_17_35.tar.gz';          ;;        armhf|arm)          ESUM='77ef6aa6f665373e212097b937c22d0cad2add90e439ec0e90534a7ff0e8a6e9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_arm_linux_hotspot_17_35.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2e58f76fd332b73f323e47c73d0a81b76739debab067e7a32ed6abd73fd64c57';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_ppc64le_linux_hotspot_17_35.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a48159fca62b7f6afd58fb2e9712a3ef1494950212d4631e25598b45d9599b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_s390x_linux_hotspot_17_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6f1335d9a7855159f982dac557420397be9aa85f3f7bc84e111d25871c02c0c7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_linux_hotspot_17_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:31:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:31:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Oct 2021 03:31:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3309f35a5827721505c550af5d824e1849aa861957dfd0c643e29230e937f2af`  
		Last Modified: Fri, 01 Oct 2021 03:35:06 GMT  
		Size: 20.5 MB (20496372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be734e50b15e568449131e48a222930a5423a5e66dc72a946ed083e5a3b9fa15`  
		Last Modified: Fri, 01 Oct 2021 03:35:56 GMT  
		Size: 189.9 MB (189883185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f46cc134d8558d719af04d971fc742092b0517653531c9d8911521380b25bbe`  
		Last Modified: Fri, 01 Oct 2021 03:35:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17_35-jdk-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5b405284172456904780e0955cbe856631abe4dae9a8e89595ef02c1162d458e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243529649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13eaa28c6cb2554ff5b37b91c3ecd9b9dc076328390717a1eec6d0cbaeba3794`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:54:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:59:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:00:40 GMT
ENV JAVA_VERSION=jdk-17+35
# Sat, 16 Oct 2021 01:01:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e08e6d8c84da28a2c49ccd511f8835c329fbdd8e4faff662c58fa24cca74021d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_aarch64_linux_hotspot_17_35.tar.gz';          ;;        armhf|arm)          ESUM='77ef6aa6f665373e212097b937c22d0cad2add90e439ec0e90534a7ff0e8a6e9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_arm_linux_hotspot_17_35.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2e58f76fd332b73f323e47c73d0a81b76739debab067e7a32ed6abd73fd64c57';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_ppc64le_linux_hotspot_17_35.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a48159fca62b7f6afd58fb2e9712a3ef1494950212d4631e25598b45d9599b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_s390x_linux_hotspot_17_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6f1335d9a7855159f982dac557420397be9aa85f3f7bc84e111d25871c02c0c7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_linux_hotspot_17_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 01:01:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 01:01:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 16 Oct 2021 01:01:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c039cd0909346123aad04b02731eff4b76a8183bac5eb82e2d477f9e3ecd1260`  
		Last Modified: Sat, 16 Oct 2021 01:05:05 GMT  
		Size: 21.7 MB (21691370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfd2de7d19685e6fa2fd563f642aee9263750b7eb94c5192fdbab6ded0ce3c9`  
		Last Modified: Sat, 16 Oct 2021 01:06:02 GMT  
		Size: 188.6 MB (188550881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c694d366736b5f652319c576193e51d7f7b576fb0a76cb475d3c252f808f2183`  
		Last Modified: Sat, 16 Oct 2021 01:05:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17_35-jdk-focal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:883a0cfd9a0b0332ffabd5c3e82bf431974b278f327296ee3ccc125b6e7546a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226693460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20053b7f94c09325b6049562367d4d7711dcf294802a635f42af9e49d3dca8b4`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:59:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 00:59:56 GMT
ENV JAVA_VERSION=jdk-17+35
# Sat, 16 Oct 2021 01:00:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e08e6d8c84da28a2c49ccd511f8835c329fbdd8e4faff662c58fa24cca74021d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_aarch64_linux_hotspot_17_35.tar.gz';          ;;        armhf|arm)          ESUM='77ef6aa6f665373e212097b937c22d0cad2add90e439ec0e90534a7ff0e8a6e9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_arm_linux_hotspot_17_35.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2e58f76fd332b73f323e47c73d0a81b76739debab067e7a32ed6abd73fd64c57';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_ppc64le_linux_hotspot_17_35.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a48159fca62b7f6afd58fb2e9712a3ef1494950212d4631e25598b45d9599b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_s390x_linux_hotspot_17_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='6f1335d9a7855159f982dac557420397be9aa85f3f7bc84e111d25871c02c0c7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_linux_hotspot_17_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 01:00:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 01:00:09 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 16 Oct 2021 01:00:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d62f01df0df55e65f1037a428195076b6423d10d10ef3ae844e054d6a82597a`  
		Last Modified: Sat, 16 Oct 2021 01:01:35 GMT  
		Size: 19.2 MB (19236649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b92ea122802992a5b625fb8381c63856277f4091b6f77f04cf1478b511c910`  
		Last Modified: Sat, 16 Oct 2021 01:02:06 GMT  
		Size: 180.3 MB (180335794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5439a7fc68f20f789ff3dddd3557734805889320153b937f424d98de7d0f6c`  
		Last Modified: Sat, 16 Oct 2021 01:01:55 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
