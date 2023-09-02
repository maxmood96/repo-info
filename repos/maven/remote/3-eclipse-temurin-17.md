## `maven:3-eclipse-temurin-17`

```console
$ docker pull maven@sha256:9c75f7135457f041560aaf832879eb4678a20a13688083f04007b043cbb276c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-eclipse-temurin-17` - linux; amd64

```console
$ docker pull maven@sha256:fe24b4064c91c1e38f12d1f0f102fa48c40059542fd89529c0c6cb011da70fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221075637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9edb00d940163ca1829251b8ba30b5c8bb82045f05cd85a92e25a984d65f8a9b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:39:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 15:39:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 15:39:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 15:40:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 20:24:02 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:24:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 20:24:13 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:24:13 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:24:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 20:24:13 GMT
CMD ["jshell"]
# Fri, 18 Aug 2023 15:26:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ARG MAVEN_VERSION=3.9.4
# Fri, 18 Aug 2023 15:26:34 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Aug 2023 15:26:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Aug 2023 15:26:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5980221a1ce1b53ecf2261f165c9bf6a24b845a2418dcf3c7aaf2f3f9e43f2a`  
		Last Modified: Wed, 16 Aug 2023 15:44:40 GMT  
		Size: 17.5 MB (17456341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9116811722eb2156806d0a28f3342d0bc1e40025b2278f490d3b624814b240a6`  
		Last Modified: Thu, 31 Aug 2023 20:30:53 GMT  
		Size: 144.8 MB (144778331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975c8543d9801e32d518935ba5a366b48f8579ea306d67f49d62458e14cc7d31`  
		Last Modified: Thu, 31 Aug 2023 20:30:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8246c942adc262687eb76aa319c6fb680086f5bf98e23b15ab346cd2a0bf7b4a`  
		Last Modified: Thu, 31 Aug 2023 20:30:42 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9efac5caff1f178efbceb1af99ca176493e9a44e70ddfadf15cb15f6f7daf7`  
		Last Modified: Thu, 31 Aug 2023 21:37:56 GMT  
		Size: 19.0 MB (18994326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054a8b47b9a83918b90a30dc036ef99bf306badaa33ea577949f25409086f42a`  
		Last Modified: Thu, 31 Aug 2023 21:37:54 GMT  
		Size: 9.4 MB (9406406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a0da154f65bc9b0ceac48622b85e7a44e6ef20ce536c85b3c79e884e2730bb`  
		Last Modified: Thu, 31 Aug 2023 21:37:53 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbbef7a475278b1e2503132b7b3ae171d038ee3ef5913a4bc13efd2200b6582`  
		Last Modified: Thu, 31 Aug 2023 21:37:53 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46be4bfb6732eea1c5d14d00bcd8a1467c6e31a5fddd2ea90b24604c8e453e9f`  
		Last Modified: Thu, 31 Aug 2023 21:37:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17` - linux; arm variant v7

```console
$ docker pull maven@sha256:ebdcda4564bacb0182826b31e79c0e00561b514e62b27b3bedb4768bd995b5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218388505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d86dd9108bd9319deca2eccf43c4e17d2a98f26bbd287f27773bdc0797a34f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Aug 2023 06:08:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:08:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:08:32 GMT
ADD file:e61c6bbfc8728cb119b4cfd4a35d1e5aad76e84c0ac8f2ff9850a7ceec9f3dc5 in / 
# Wed, 16 Aug 2023 06:08:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:34:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Sep 2023 23:34:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Sep 2023 23:34:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Sep 2023 23:36:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:36:59 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Fri, 01 Sep 2023 23:37:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 01 Sep 2023 23:37:14 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Sep 2023 23:37:14 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Sep 2023 23:37:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Sep 2023 23:37:14 GMT
CMD ["jshell"]
# Fri, 18 Aug 2023 15:26:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ARG MAVEN_VERSION=3.9.4
# Fri, 18 Aug 2023 15:26:34 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Aug 2023 15:26:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Aug 2023 15:26:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5987bac23899c422dbd7b7045113aa103f4d6856141a3f9098850e6328563e42`  
		Last Modified: Wed, 16 Aug 2023 13:31:19 GMT  
		Size: 27.0 MB (27027892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e9acc4ff89dd25ddc04510a1667d2cf420b52814b7c376e3b25c38dbf201ac`  
		Last Modified: Fri, 01 Sep 2023 23:39:04 GMT  
		Size: 17.6 MB (17587964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9dddfdf02a32d5e25c7585e507055c327d33597e87aaca6de151f37fefe41`  
		Last Modified: Fri, 01 Sep 2023 23:39:14 GMT  
		Size: 142.1 MB (142064166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a361653c05b461c3a682f1f0fffe057dbb93de4fd720f5b06f13ccece9dbba`  
		Last Modified: Fri, 01 Sep 2023 23:39:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c115ba0f14d100e6ee4796bd460c08347166b0f4fed10f01298c807483fb2e19`  
		Last Modified: Fri, 01 Sep 2023 23:39:01 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dcfae3aba9a85fce20c1044107e804d722092287c6371caa67029406ce4842`  
		Last Modified: Sat, 02 Sep 2023 00:44:59 GMT  
		Size: 22.3 MB (22299769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858944158f6cf1c230fde26e1dbc76e323567545348c9d81951e02c4c45b0b87`  
		Last Modified: Sat, 02 Sep 2023 00:44:56 GMT  
		Size: 9.4 MB (9406444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c711be4de6cbdbb82bfb9d5927227a028d4d7749ce1cb56d394527d80c3a0c9`  
		Last Modified: Sat, 02 Sep 2023 00:44:56 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487ae072486d5c2b6d976e129d755469ecfe01f9bb3aa0424f10d56fdfec1de0`  
		Last Modified: Sat, 02 Sep 2023 00:44:55 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97607b82bea3f278ee2c2250f74ecd58871056062705394ef7fcd6830612fc21`  
		Last Modified: Sat, 02 Sep 2023 00:44:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b6fe9e0212fa3e1562bb9dc3d47510d3fedd4e52f74199bc2231857a120fcf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219218830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2539bef7e1524d721ddf38b10f9eed0ff6553d2f65eca0e8a1e12d686cdd63d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 14:23:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 14:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 14:23:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 14:24:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:42:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 20:42:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:42:41 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:42:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 20:42:41 GMT
CMD ["jshell"]
# Fri, 18 Aug 2023 15:26:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ARG MAVEN_VERSION=3.9.4
# Fri, 18 Aug 2023 15:26:34 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Aug 2023 15:26:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Aug 2023 15:26:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c321f4fb81c9a8d9170f2e66e24c105f438bac179a8c09632ea442be47ef6a3`  
		Last Modified: Wed, 16 Aug 2023 14:28:14 GMT  
		Size: 18.9 MB (18858726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9266f98e718659d81c5f1e04081df883765f44fd6f477d03e82cea7c5253a2a`  
		Last Modified: Thu, 31 Aug 2023 20:47:22 GMT  
		Size: 143.6 MB (143553788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08416aa810918ca83080d76da68525bd0c8481115f9bc7dbfd19ea3e6ea3a26f`  
		Last Modified: Thu, 31 Aug 2023 20:47:13 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a285987651171d9eea599afbf5474065ee8e7dc424480d7a3f0ec8d40eb1fff`  
		Last Modified: Thu, 31 Aug 2023 20:47:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d47e39969ee727516e7ebbfae94d307f8d8a315ddfd63b2f10c862667e04c09`  
		Last Modified: Thu, 31 Aug 2023 22:03:59 GMT  
		Size: 19.0 MB (19005715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc54dc6596e035f2257ebdf8a6580d92d8c82a8443439274510b4c1f37d8ef`  
		Last Modified: Thu, 31 Aug 2023 22:03:57 GMT  
		Size: 9.4 MB (9406424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5598d038d5c92ffd7b8b11473ef5abc4920bd64fcbf461f835d9944d43ff20e`  
		Last Modified: Thu, 31 Aug 2023 22:03:56 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88da197d6e31182774153ca175d51ed7f9e810a7d6e757e8b9860b3a8a66647`  
		Last Modified: Thu, 31 Aug 2023 22:03:56 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437a5bcd003887b91282f75669577540e57f9af8268663edbfcf5e2765ab770c`  
		Last Modified: Thu, 31 Aug 2023 22:03:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17` - linux; ppc64le

```console
$ docker pull maven@sha256:d043a0d31357ca057a58837a1ef0cbe42b1398fe45d8c720fab56ea7c60b07cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230453521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb35483cde97d211e47333b6a6848fceb4b4b9e0175f0cd4b1a26db932f4d72`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
CMD ["/bin/bash"]
# Thu, 17 Aug 2023 07:21:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Aug 2023 07:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 07:21:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Aug 2023 07:24:20 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 20:19:55 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:20:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 20:20:17 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:20:17 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:20:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 20:20:18 GMT
CMD ["jshell"]
# Fri, 18 Aug 2023 15:26:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ARG MAVEN_VERSION=3.9.4
# Fri, 18 Aug 2023 15:26:34 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Aug 2023 15:26:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Aug 2023 15:26:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:09f4821f68917c7929419fff8bc583c406640180ea7d58eea03a95e463b8fb21`  
		Last Modified: Wed, 16 Aug 2023 02:15:01 GMT  
		Size: 35.7 MB (35712693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ac4cfa89e33fa6fac1fbd37e22637c5be91e0cc3a38c83101cd6547c2bacb8`  
		Last Modified: Thu, 17 Aug 2023 07:28:57 GMT  
		Size: 18.7 MB (18729521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c3734d16459edfbc70e0fc498632111fcc32fe287e5db11590e79c6f0d2bbc`  
		Last Modified: Thu, 31 Aug 2023 20:28:03 GMT  
		Size: 144.5 MB (144496326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712e8e66fb8a7803db85095120a3ed4effc046f583c2ba00522ab29f192aeb93`  
		Last Modified: Thu, 31 Aug 2023 20:27:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d694bff18b8695c19f84251d65cebe515febb022551f2e9208a16847842071`  
		Last Modified: Thu, 31 Aug 2023 20:27:43 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb3a4c78d479243ec26cc1a98c0b7ff828851ba66cf495086040762ffe8b81e`  
		Last Modified: Thu, 31 Aug 2023 21:12:16 GMT  
		Size: 22.1 MB (22106294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed86c9d8e341f3f6fa6606537a6f3869c71c16491983f7f28509e833dc171a5`  
		Last Modified: Thu, 31 Aug 2023 21:12:11 GMT  
		Size: 9.4 MB (9406413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9e4757a8763aa8657d02dd054d81c7f881c498ed3b24741513ff7338a9542d`  
		Last Modified: Thu, 31 Aug 2023 21:12:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aace4d6f1aaaf6a7e3ee3a89e7bdaafa901c0ee2061c594dcdbea8e8f8ac931`  
		Last Modified: Thu, 31 Aug 2023 21:12:10 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96ed3850fd3df379a6b0156a192699f8907f6652985c9a3ef7b1f82241607d1`  
		Last Modified: Thu, 31 Aug 2023 21:12:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17` - linux; s390x

```console
$ docker pull maven@sha256:37c2f8ae27a7a9518407b47d04b7eb2886ff52bc42637181c66c3b3df7c1a8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208751234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e9b22163b6a543b1632a0d8c6dd192fb98bc0d43f0b8b204829f3bed2cfd3a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:26:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Sep 2023 23:26:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Sep 2023 23:26:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Sep 2023 23:27:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:27:38 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Fri, 01 Sep 2023 23:27:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b1f1d8b7fcb159a0a8029b6c3106d1d16207cecbb2047f9a4be2a64d29897da5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 01 Sep 2023 23:27:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 01 Sep 2023 23:27:58 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Sep 2023 23:27:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Sep 2023 23:27:58 GMT
CMD ["jshell"]
# Fri, 18 Aug 2023 15:26:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 18 Aug 2023 15:26:34 GMT
ARG MAVEN_VERSION=3.9.4
# Fri, 18 Aug 2023 15:26:34 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Aug 2023 15:26:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Aug 2023 15:26:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Aug 2023 15:26:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e19a32372cc8a39496c7cbc80d6c7213997c1b24d50309e770a59738f35c719d`  
		Last Modified: Fri, 01 Sep 2023 23:23:30 GMT  
		Size: 28.6 MB (28645834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351bc6a2ce88dd5072fe74c40fe5a76147b4c44751fb62974f74bd1eaf40aafb`  
		Last Modified: Fri, 01 Sep 2023 23:29:38 GMT  
		Size: 17.3 MB (17255550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2df682594d614eb39c1767c08d3e9078d528d8cb5081c9a171697a348eba5f`  
		Last Modified: Fri, 01 Sep 2023 23:29:46 GMT  
		Size: 134.2 MB (134217531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb71f98547ff743cd9301ebc43f5b154f089311a93e15001e8c271c703d0e9d`  
		Last Modified: Fri, 01 Sep 2023 23:29:36 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad043f6fb7f10bf8558dfa3cadfe771b6b9ba06e096352d274ccb2bcdd9019b`  
		Last Modified: Fri, 01 Sep 2023 23:29:36 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e414a04550a5d799e8680a27494b901981b92cd442348206b189f29eb197a374`  
		Last Modified: Sat, 02 Sep 2023 00:42:47 GMT  
		Size: 19.2 MB (19223624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83cdffaa2b5549915fb1e2dbd84f5076e71631489be3a460a83b5747e9d8cb8`  
		Last Modified: Sat, 02 Sep 2023 00:42:45 GMT  
		Size: 9.4 MB (9406421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5933f9e2d9577b7bd67787e95a3bcddb75c74a8d586d8d21aa2cde52db081411`  
		Last Modified: Sat, 02 Sep 2023 00:42:44 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcb327c042ae27411e7664b1b94a4af56f8aab4bb5df672676a51701911954a`  
		Last Modified: Sat, 02 Sep 2023 00:42:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f31f3556e76bd66aea43c8d514958cb93d4f9133194b2f4f73a1b236b795269`  
		Last Modified: Sat, 02 Sep 2023 00:42:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
