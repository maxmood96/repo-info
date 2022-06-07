## `eclipse-temurin:11-jdk-focal`

```console
$ docker pull eclipse-temurin@sha256:df6530ac71595121c1d70ac76b5ccf44c1a710f0d0ba958152cde0ab066e9066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jdk-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1db6f5c4ca0238156518e48f55d22f3cf616827f71e6f43b5d5b8ffcf1420a60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238686880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e18832bbac6bff66d019b3b8e98071ac7608d3af31b47a7ed855026dcc9c4b1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:12:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:14:23 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 00:14:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 00:14:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca7a4a00fe7d5efa72ecdbb346c7a4ee0e8e43c3a263d2bb79893d52bd4678`  
		Last Modified: Tue, 07 Jun 2022 00:19:21 GMT  
		Size: 16.0 MB (16029798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6099f6cb4c651ca09dc4cb212ae760c08a4bc9b923c7885010f6634d9cdc8672`  
		Last Modified: Tue, 07 Jun 2022 00:20:48 GMT  
		Size: 194.1 MB (194084290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a9f5d5b2e7d47fbe2b6cca47c964b7c3637ebc4eaf2b4bbb7610579cadb2d5`  
		Last Modified: Tue, 07 Jun 2022 00:20:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-focal` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:d933fec1614c3881acb1f8c4333a5cb3fa9e015346bd930423f341afc044886e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220941281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ea2b355d54ab9c4fb698129e0b1d17ade5060c584c28f1e39968f434f0fe4e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:56:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 29 Apr 2022 23:56:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:58:01 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Fri, 29 Apr 2022 23:58:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 29 Apr 2022 23:58:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Apr 2022 23:58:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 29 Apr 2022 23:58:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142d50dc2d1479b31402efb7588259cffeca2de60159fa16b540aa20dcf0cd3f`  
		Last Modified: Sat, 30 Apr 2022 00:04:04 GMT  
		Size: 14.9 MB (14901951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1c13db210336b27633d6f822a2d8a03314495b2554b9a2b401b4b30a493f15`  
		Last Modified: Sat, 30 Apr 2022 00:06:35 GMT  
		Size: 182.0 MB (181965519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03977ab56f4a167960688e767250236f16cc69e309e37cbff6a95df2fc058f3d`  
		Last Modified: Sat, 30 Apr 2022 00:05:25 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3886ed1c18d1e0cd88dbb64d94a1bdd29bfc22097560c58313584e9815ce108e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233914221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e0cf9a94ffbeabe27adf9d20044c16d26bac67edc5952d0be49b441c9ec232`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:59:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 05:00:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:35:32 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:35:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:35:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:35:47 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:35:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15da1b4c110f7cc460fbf968fb55b77c541f0e3ab87b92d5e6a822cc2c593e1`  
		Last Modified: Tue, 07 Jun 2022 05:10:23 GMT  
		Size: 15.9 MB (15898299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2246f583b817221ee4ff9cf491f3f17cc8881295de0bd6c1b213dbe7c8585`  
		Last Modified: Tue, 07 Jun 2022 06:43:20 GMT  
		Size: 190.8 MB (190824584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ec9350bf8b0d1ea50051917adf749e1d1b7675d672e1e9c731b5e937ad271e`  
		Last Modified: Tue, 07 Jun 2022 06:43:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:17edc32042e8edebc9e150e83572a896266d41ccfe9c71902f7079be486149f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226467144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01be18fdaa169912b9aadb4182e98335d67017b3547d67bc50a5d3f2a5fb194d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 07 Jun 2022 05:46:02 GMT
ADD file:86506a94b834ba2b6f10dc0d1955bee539be1cf565e4ccc2c4bc074e0375f115 in / 
# Tue, 07 Jun 2022 05:46:06 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 07:16:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 07:18:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 07:20:45 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 07:21:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 07:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 07:21:20 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 07:21:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f52d061d2d3fdde0d3a099bbeae64080476c9650e9f3ba05de898d5bb5f03e8`  
		Last Modified: Tue, 07 Jun 2022 05:49:10 GMT  
		Size: 33.3 MB (33294345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6c621e52fdf1e59e073b1c51c52e2e5a829be92510ef56949c609a03af2492`  
		Last Modified: Tue, 07 Jun 2022 07:30:19 GMT  
		Size: 17.2 MB (17203633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3af49f521ff9dfa08c26a670e543b7b5cc0f1f50d56cbdb252d987677bd11e3`  
		Last Modified: Tue, 07 Jun 2022 07:31:21 GMT  
		Size: 176.0 MB (175969006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09e78f2c65e8bb444b39a588ddb61f0b738ad40db6483104e03b758230867b6`  
		Last Modified: Tue, 07 Jun 2022 07:31:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-focal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:cdc84f0ce02aeec281090425cbd0e5789115ff1fec221949c7a1b83c8024a32b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211263938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c003ad686798dd6d9d60f8db75422dcac049b7919b04321096a319993b83be5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 07 Jun 2022 04:05:02 GMT
ADD file:6250f895d7d6c591cfe1b9fc991313d21b02167d94c67991db7c5c1c6814c51e in / 
# Tue, 07 Jun 2022 04:05:06 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:11:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 06:11:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:33:03 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Tue, 07 Jun 2022 06:33:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='999fbd90b070f9896142f0eb28354abbeb367cbe49fd86885c626e2999189e0a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.15_10.tar.gz';          ;;        armhf|arm)          ESUM='e21a7660aa322e0d66e6df06885bf4f8aaff9ea4a37cc398e061295f69a8d096';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.15_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a8fba686f6eb8ae1d1a9566821dbd5a85a1108b96ad857fdbac5c1e4649fc56f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.15_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a58fc0361966af0a5d5a31a2d8a208e3c9bb0f54f345596fd80b99ea9a39788b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.15_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5fdb4d5a1662f0cca73fec30f99e67662350b1fa61460fa72e91eb9f66b54d0b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 06:33:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 06:33:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 07 Jun 2022 06:33:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f1fac119b88f55cd8329458ec27c3d6d6cb324b0fe541feacfd9a4ee621a558`  
		Last Modified: Tue, 07 Jun 2022 04:07:45 GMT  
		Size: 27.1 MB (27056020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908ba35702b3545e3156e807426eb36d13103c223acf51195f236f759910d212`  
		Last Modified: Tue, 07 Jun 2022 06:23:28 GMT  
		Size: 15.7 MB (15730049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69669f6b135f258e4726bc7ab1b4f57d11e662688f5b61d5b3f6a8bec28335b`  
		Last Modified: Tue, 07 Jun 2022 06:42:54 GMT  
		Size: 168.5 MB (168477709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb8a0b9cb2910808715d72e822198aaeb8f7e742ec0ddf071eacf207b1b4468`  
		Last Modified: Tue, 07 Jun 2022 06:42:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
