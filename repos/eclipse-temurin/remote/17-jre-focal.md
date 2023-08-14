## `eclipse-temurin:17-jre-focal`

```console
$ docker pull eclipse-temurin@sha256:fec0b0f6cb7d2c41c0381c6828211a5adedb1ed6822d3f8209596042a9c606e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-jre-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:47bb851c475780124df3e6baa9fb39a6029098113114c66957eb76235574d8ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96453609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1715b9843bd6956671c6d883aedfde81e9a1075c35628be793279f0bcfad7529`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 02:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 02:34:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:23:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:23:35 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 08 Aug 2023 19:24:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42525ae2951a669803c75ba5987dc8333c664dae50c3e12174f736a506b4aa15';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='20fa06a86e1647f5997c511dd19e4d1c9839d2500f835973fc9b3c86b87030a0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1cf2cf7dca98c74860799b162b9f2eeaaf1ad1e78f5cb7479fe7bd1ccfea3227';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='4df17b19510864651c1d620baaf13766a448d43ee7848ea9ff69db10d26467b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='dddbb5f817a77445711528a414678806b00b83c92701fe595c50cdb207758ae9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:24:27 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:11:11 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:11:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c7ccc62e5c5023fda398ded7921663ef21bf901061cd7db06fd23dfa445d7f`  
		Last Modified: Tue, 08 Aug 2023 19:31:43 GMT  
		Size: 20.7 MB (20661907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6081b1f35fa1a64f5185befad5eb4d080335b66d995f4c09e329d5d3e255f9b1`  
		Last Modified: Tue, 08 Aug 2023 19:33:08 GMT  
		Size: 47.2 MB (47210138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd459f76166c7898b5c7341f9783e942f006720baf66f953822c4b15a4a9e98`  
		Last Modified: Tue, 08 Aug 2023 19:33:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4bad9e715557da279879222589f29b51d52dab2ba8ea2312429695961bc3ae`  
		Last Modified: Mon, 14 Aug 2023 18:17:51 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-focal` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:40c08b35d5d4602043e255fd83475b13e4fdaf434c2fdc950198c64eaf73c24e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89274346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39f8d099000291c61ff72d80f1dffb5837aed14d46056060844f99025b5a3ad`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:45 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:49 GMT
ADD file:60aa8465a6ba5538decc41365cc9b78ae86131e8c2cfc9177b4a336354ead988 in / 
# Tue, 01 Aug 2023 06:16:50 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:27:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 01:27:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 01:27:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:00:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:00:52 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 08 Aug 2023 19:01:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42525ae2951a669803c75ba5987dc8333c664dae50c3e12174f736a506b4aa15';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='20fa06a86e1647f5997c511dd19e4d1c9839d2500f835973fc9b3c86b87030a0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1cf2cf7dca98c74860799b162b9f2eeaaf1ad1e78f5cb7479fe7bd1ccfea3227';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='4df17b19510864651c1d620baaf13766a448d43ee7848ea9ff69db10d26467b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='dddbb5f817a77445711528a414678806b00b83c92701fe595c50cdb207758ae9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:01:49 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:09:52 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c429b4536d4b2ab209b0a779f71ba68570f10acf9dd806c7e2011fce49bd5c97`  
		Last Modified: Wed, 02 Aug 2023 04:28:29 GMT  
		Size: 24.6 MB (24591882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e368629986d1fc73b304258f49df92a5019c9e1369991253c332469c3a90619`  
		Last Modified: Tue, 08 Aug 2023 19:05:06 GMT  
		Size: 20.0 MB (19961860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f482bb876f31659118e19dc691d8aac87e9b6875af5957f5b711cdf931e3ed34`  
		Last Modified: Tue, 08 Aug 2023 19:06:03 GMT  
		Size: 44.7 MB (44719712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498dcd852da0543d2b88dd30a531ec5fafe9416822c6ed2da9fbd7a887aab302`  
		Last Modified: Tue, 08 Aug 2023 19:05:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b99a0af9e9ba4b7b1cca950f0cc2819d6063ba606aa8d0cbce51181ed8da02`  
		Last Modified: Mon, 14 Aug 2023 18:11:52 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3b8ea833ccf9aada6328babf593c3d8bd19d784cc9c8e8a840f6827bf9b9c882
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95241891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4579ca00984d2770120046846e2f47ad1f81aeb17c3173c5683078a9545e4641`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:05:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 01:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 01:05:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:42:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:42:11 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 08 Aug 2023 19:42:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42525ae2951a669803c75ba5987dc8333c664dae50c3e12174f736a506b4aa15';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='20fa06a86e1647f5997c511dd19e4d1c9839d2500f835973fc9b3c86b87030a0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1cf2cf7dca98c74860799b162b9f2eeaaf1ad1e78f5cb7479fe7bd1ccfea3227';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='4df17b19510864651c1d620baaf13766a448d43ee7848ea9ff69db10d26467b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='dddbb5f817a77445711528a414678806b00b83c92701fe595c50cdb207758ae9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:42:48 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:09:29 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875232cbc2421e5da851922d68776b50b144eeec92140e53f296882c0ccbadbb`  
		Last Modified: Tue, 08 Aug 2023 19:47:26 GMT  
		Size: 21.4 MB (21378921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cb96f367b9e66805a0d7bbf191398190964e13000d668471963a4a5c92d8a5`  
		Last Modified: Tue, 08 Aug 2023 19:48:36 GMT  
		Size: 46.7 MB (46661489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db69f4aaf0ad93739639b0d1dc8bb4ad0a6b63ba5c53f3280a3c94c1a6c8c85`  
		Last Modified: Tue, 08 Aug 2023 19:48:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8c0d4a1159cc19d67888c8291165de0f40ca5f2a78426a480b54c93cef46af`  
		Last Modified: Mon, 14 Aug 2023 18:13:45 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f2687b13118a5ce1375d973a02a323248f7aa7c417be2c033dd0e323362c3d24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103070746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71acc7827beac3d0ab509f64064086cad2948d404e0c467cb937155bf442241`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:36 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:20:40 GMT
ADD file:822df76493d1d533c1a283ab7bb20ce81309f57279422a0eebb2ffb9fab55963 in / 
# Tue, 01 Aug 2023 06:20:40 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 02:44:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 02:44:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:23:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:23:37 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 08 Aug 2023 19:26:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42525ae2951a669803c75ba5987dc8333c664dae50c3e12174f736a506b4aa15';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='20fa06a86e1647f5997c511dd19e4d1c9839d2500f835973fc9b3c86b87030a0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1cf2cf7dca98c74860799b162b9f2eeaaf1ad1e78f5cb7479fe7bd1ccfea3227';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='4df17b19510864651c1d620baaf13766a448d43ee7848ea9ff69db10d26467b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='dddbb5f817a77445711528a414678806b00b83c92701fe595c50cdb207758ae9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:26:22 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:10:23 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:10:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:be0253994e7bea97e6b44cdeec04bf996c8dd3380e70409de3783a1d1971e747`  
		Last Modified: Thu, 03 Aug 2023 02:50:24 GMT  
		Size: 33.3 MB (33306772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c319e9f2f43271a889bc0a799583ae694861671f43953fbee6291bc1b238d87`  
		Last Modified: Tue, 08 Aug 2023 19:33:50 GMT  
		Size: 22.7 MB (22708501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13fbf13c16b2d99574bfbde54f769257dde4fff39883b7498f211a31cea131`  
		Last Modified: Tue, 08 Aug 2023 19:35:35 GMT  
		Size: 47.1 MB (47054580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444e99d65be517006afc6f148108f3c02f674d7026a9db3f38025d01014ef91a`  
		Last Modified: Tue, 08 Aug 2023 19:35:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd942cd1f86ddd2a581b60fa849e4668a7c8ec3b6b191fa84c23eab48d775cc0`  
		Last Modified: Mon, 14 Aug 2023 18:16:23 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-focal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:2e86462b887f6ae5fa7693dff2d128029491ca3d7fbc002daeccd8cd3db43180
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91017209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e908483f3beeb0002c260208d10345d2df8cdf0ae6dfc3c47760040ed0d9990`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 01 Aug 2023 06:17:39 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:17:41 GMT
ADD file:36efc3ec29bb54e0987fe91be1aa7cc849909b3cd2534af3de2d3d07a03804cf in / 
# Tue, 01 Aug 2023 06:17:41 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 00:24:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 00:24:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:43:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:44:00 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 08 Aug 2023 19:45:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42525ae2951a669803c75ba5987dc8333c664dae50c3e12174f736a506b4aa15';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='20fa06a86e1647f5997c511dd19e4d1c9839d2500f835973fc9b3c86b87030a0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1cf2cf7dca98c74860799b162b9f2eeaaf1ad1e78f5cb7479fe7bd1ccfea3227';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='4df17b19510864651c1d620baaf13766a448d43ee7848ea9ff69db10d26467b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='dddbb5f817a77445711528a414678806b00b83c92701fe595c50cdb207758ae9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:45:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:10:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:10:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:365fa2124eb5f6f369204f3fe0210d9965952628707dfacd4194a8e15caf0420`  
		Last Modified: Thu, 03 Aug 2023 00:03:37 GMT  
		Size: 27.0 MB (27014233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0414709677855fc542ff87fcafa89b2a23938e36f9374a6d9a4d9db9f0723fc`  
		Last Modified: Tue, 08 Aug 2023 19:47:26 GMT  
		Size: 20.1 MB (20141237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a282fa00466629fa573ba04ccd3bf1311eee87de80385832093eeca7064a884c`  
		Last Modified: Tue, 08 Aug 2023 19:48:14 GMT  
		Size: 43.9 MB (43860846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b876e53b2f1c3082c75cfa7c099a165c825680098c3159fbceeca64c22bcf6`  
		Last Modified: Tue, 08 Aug 2023 19:48:08 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8a5ae8c8298682321de09e157f3b6f5a6afbe0c3a2a0c683fa6bfda54beee6`  
		Last Modified: Mon, 14 Aug 2023 18:12:02 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
