## `eclipse-temurin:8-jdk`

```console
$ docker pull eclipse-temurin@sha256:019f810cc052d5eb3c35d912a3f6e8bcf98155828a7356e6a0d511939fc737d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:8-jdk` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d9b38d87a3add4695e169f4d6a97732344096d5237306b58237204fef513adf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146923524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6767b0cedfca446f25588d84eceba6e2365fa90bd40e3c367d8b95e78cfb28`
-	Entrypoint: `["\/entrypoint.sh"]`

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
# Tue, 08 Aug 2023 19:21:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:21:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 08 Aug 2023 19:21:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 08 Aug 2023 19:21:08 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 08 Aug 2023 19:21:08 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d9603a2223f0c0337b5489031adc59113c119d64dfce6852f6114f42f2f05`  
		Last Modified: Tue, 08 Aug 2023 19:27:08 GMT  
		Size: 12.9 MB (12902861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40550a0c5d133478b15fd627676299c94bf4eed229af0acdadf2aeddfc7e8199`  
		Last Modified: Tue, 08 Aug 2023 19:27:15 GMT  
		Size: 103.6 MB (103588608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031298b013cc8d2e3047fb86fdec2ac169d050fd13b543899d763de8d96836bf`  
		Last Modified: Tue, 08 Aug 2023 19:27:06 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa19e27489f72fc86f51432f51cf22d7e50923dca679880f00b05226a1b14852`  
		Last Modified: Tue, 08 Aug 2023 19:27:06 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:31886d6616234540bc62edaac2dcc2f34d1e321143e6fa4cdd8887047e70bc7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139521295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb99b86fac9efb25f1df4beed36fb6e0dc4dc07a7a0e67b114a4c1149d509ee3`
-	Entrypoint: `["\/entrypoint.sh"]`

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
# Tue, 08 Aug 2023 18:59:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 18:59:01 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 08 Aug 2023 18:59:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 08 Aug 2023 18:59:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 08 Aug 2023 18:59:15 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 18:59:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:63b96265cfe95b9cec847027033d4226b783ecd042036f5c809a7386027f56b0`  
		Last Modified: Fri, 30 Jun 2023 02:08:02 GMT  
		Size: 27.0 MB (27026961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791f420277f117d4cbc9798bac0e3991df4d76dcb209a6289b5474d81f4c32d0`  
		Last Modified: Tue, 08 Aug 2023 19:02:56 GMT  
		Size: 12.5 MB (12491020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2f32c73cbce14ea257044e5d62157d17f6b149768a91245c8f11a897a4c196`  
		Last Modified: Tue, 08 Aug 2023 19:03:04 GMT  
		Size: 100.0 MB (100002488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36babc27fff1c55a88a19c92530167a71d3d51ac39f2777326ebd384997eeeed`  
		Last Modified: Tue, 08 Aug 2023 19:02:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faead8d34952e633ffc9c48780c8c86af578ab4aa38589bd2273745e50251a59`  
		Last Modified: Tue, 08 Aug 2023 19:02:53 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:374f5f8016b2742daa3eea3be1cd63669665a7a29301dd9ec33dfb561ffbba7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143926742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8d200766b2641f81b97eb7bcf848cae4bab55d61738e289fa0f0921e53638c`
-	Entrypoint: `["\/entrypoint.sh"]`

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
# Tue, 08 Aug 2023 19:40:41 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:40:41 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 08 Aug 2023 19:40:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 08 Aug 2023 19:40:47 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 08 Aug 2023 19:40:47 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:40:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91712d801b234a271df55fd60b35e7d2918ce5ae0fb7ce56a8de0edb8151fd0e`  
		Last Modified: Tue, 08 Aug 2023 19:44:21 GMT  
		Size: 12.8 MB (12844180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607b1286780546fce088171b2f2aa2121f48ef1c1c93d22c5af61e69cee07ea6`  
		Last Modified: Tue, 08 Aug 2023 19:44:28 GMT  
		Size: 102.7 MB (102690724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbf276f4de69f052a42094434f602edabd2603dbaad24657afcf211b04b6913`  
		Last Modified: Tue, 08 Aug 2023 19:44:19 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177eae88468753c91f0a40d1db961d25a16c558da98f84b44541a0e9461a4c3f`  
		Last Modified: Tue, 08 Aug 2023 19:44:19 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:3cefd2757689541a3c96088cf811a5952122314f0d81bc785bdbfafe3f9e48fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150534016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a928e15e4a8e8691a70fe7f6c347932bc57c7212e9a226389dee3ac6a75c503`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 00:18:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 00:18:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 00:18:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:19:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:19:32 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 08 Aug 2023 19:19:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='5d805ff157f272acf0f7d192f21af4a3b68c840333ca95568e4e07142efc369d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 08 Aug 2023 19:19:51 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 08 Aug 2023 19:19:53 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:19:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2f5a106d782ce62a5cf92c2a7f53d1b6067d5198e321d1c74bf914ae7b208f`  
		Last Modified: Tue, 08 Aug 2023 19:28:59 GMT  
		Size: 13.8 MB (13770640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e8e6b78cf5cfd7332b4e0e9d45ba3cf5ac7da2eda7d9dd99a3f0a4d9286b44`  
		Last Modified: Tue, 08 Aug 2023 19:29:10 GMT  
		Size: 101.1 MB (101051081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fe27c195e4a649c91d1ea134dc4b24d9d485dbc2ba78da2dab02d91549bfb`  
		Last Modified: Tue, 08 Aug 2023 19:28:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b2428080cb3ff6e6b1066bfa1cc98bc9505006dfc54616bcc5e3c16b986183`  
		Last Modified: Tue, 08 Aug 2023 19:28:55 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:e71b471fa9131a92985abb93a1f113f9d4c1bb6776cfdd73adcd4d08824c6030
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1928925505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35520fc0e6a02fc714884d548b4e9207c2eda54f86df9cf2174b1822af5dff0f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 20:29:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 01 Aug 2023 21:15:34 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:16:24 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_windows_hotspot_8u382b05.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_windows_hotspot_8u382b05.msi ;     Write-Host ('Verifying sha256 (da10c23aa318764adc8361df0e0363fa50f885abe97b229fb0e4d4fe8c9f9679) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'da10c23aa318764adc8361df0e0363fa50f885abe97b229fb0e4d4fe8c9f9679') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 01 Aug 2023 21:16:55 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e3828ab9c4326158b6161915d8bad87619b3107529ab32863eb31b684d127`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f10afe20b66865bd2b731ab779ba9190c0cb4792de048a223b28ed26f44c8`  
		Last Modified: Tue, 01 Aug 2023 21:30:22 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8c7bdb5f9ccddf1ccfcf47856f54d5d22b16a63dfd25ad2f96f43f07d5a3be`  
		Last Modified: Tue, 01 Aug 2023 21:30:38 GMT  
		Size: 191.3 MB (191269072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cf343484c98f2fac0bf61a68a5101a98d104d9dc1501d125c15693b3524581`  
		Last Modified: Tue, 01 Aug 2023 21:30:22 GMT  
		Size: 288.4 KB (288353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:344ac5b15214e2ccf2fb3cab37a6f019ea7fae546c309398984f7a31c7e58b85
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2131214418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f5d9b41f92214b21ab8c12b7044c1852e43e3c739232c897510399d1104507`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 01 Aug 2023 21:17:02 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 21:18:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_windows_hotspot_8u382b05.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_windows_hotspot_8u382b05.msi ;     Write-Host ('Verifying sha256 (da10c23aa318764adc8361df0e0363fa50f885abe97b229fb0e4d4fe8c9f9679) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'da10c23aa318764adc8361df0e0363fa50f885abe97b229fb0e4d4fe8c9f9679') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 01 Aug 2023 21:19:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012cfd51e6f1a0af073a5bacf5e453f75dbb81635a4d0dab218cb05828a76f61`  
		Last Modified: Tue, 01 Aug 2023 21:30:50 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a0074b5962db8b81e00e02436a95bc241bbffdae1e52862b76ae11f9a91279`  
		Last Modified: Tue, 01 Aug 2023 21:31:06 GMT  
		Size: 191.3 MB (191299030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a61544bd600fd8a32b8e40507a62e2d94adde84af7682054ac5e1c8bc0c69aa`  
		Last Modified: Tue, 01 Aug 2023 21:30:50 GMT  
		Size: 223.5 KB (223517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
