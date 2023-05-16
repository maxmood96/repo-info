## `maven:3-eclipse-temurin-8-focal`

```console
$ docker pull maven@sha256:7ae9142e539a1037303168a5b5a9ea641faa8b5980e3f887cfea678ece7bf921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-eclipse-temurin-8-focal` - linux; amd64

```console
$ docker pull maven@sha256:87c7d7488ba5b16f0bc6b505c62a27cf8ac041a34427298d0e3d4bfddc2a01bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136820386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b67614ff791c0f272a0c7fbd148e8e30c4f4d3c8c824f9b35aaa3271fd3db3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:43:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 19:19:51 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 07:26:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 07:26:18 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 07:27:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 May 2023 07:27:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 07:27:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 07:27:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 07:27:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 07:27:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 07:27:26 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 07:27:26 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 07:27:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 07:27:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 07:27:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7affba4c9a33ed5dd050532c0d53e38b2c35c2fe490db721d943658feee4c914`  
		Last Modified: Tue, 18 Apr 2023 00:46:23 GMT  
		Size: 16.3 MB (16347011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebffebef5c8648902c2f59bb4f414372237207869699f65e46693470fcf744e`  
		Last Modified: Thu, 04 May 2023 07:29:51 GMT  
		Size: 54.6 MB (54646243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58729dc38ac22e7073914afda5bee4c3756fdc822c6687a63a4e88b51780e3d5`  
		Last Modified: Thu, 04 May 2023 07:29:44 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3af52034cce4c2eb1c0cda3c1f47dd7492340ab5680829fc491dce5e12368f5`  
		Last Modified: Thu, 04 May 2023 14:44:30 GMT  
		Size: 28.1 MB (28140870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2675c435533bf99d1ae81f8244a94afb22caaae48894cb42e13751d5a1fdff`  
		Last Modified: Thu, 04 May 2023 14:44:26 GMT  
		Size: 9.1 MB (9106172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92bae1f9184d4beea7cc8db460c551195c8c288ccaf6ea8df258f5fefbe07e3`  
		Last Modified: Thu, 04 May 2023 14:44:26 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc0f52d66aa7e8393303f3abd6d18656fcee330c56321b29ca4ba7143e4f597`  
		Last Modified: Thu, 04 May 2023 14:44:25 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9755cbeaca5e252a9a0d3b8879201a231883b8cecafe051d634c5f358ce8b4f`  
		Last Modified: Thu, 04 May 2023 14:44:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-8-focal` - linux; arm variant v7

```console
$ docker pull maven@sha256:2adad4012d22dc9bdb6bddc1eb70ece7c1207a983321f55e64c0fbe80cb818fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124203263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23782584e8a0b1b8c88f1d1ac3a1619da0ef439325cefee4153c2af5e70e4085`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:52:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:51:13 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 06:51:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 06:51:37 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 16 May 2023 11:35:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 16 May 2023 11:35:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 16 May 2023 11:35:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 May 2023 11:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 May 2023 11:35:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26020bb58aaff7bb6175448d285783e1d1698e726bcba90502c721abc88f2a2`  
		Last Modified: Tue, 18 Apr 2023 01:54:29 GMT  
		Size: 15.2 MB (15177669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1ac8d86886181a5e3bc7fed8fc3f0f8fd1032b8210f48ce31da29380aa380c`  
		Last Modified: Thu, 04 May 2023 06:54:21 GMT  
		Size: 50.3 MB (50305112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673802021978a78972007b5edc8f46d9dda5be16c62bf4e496c185ff3d34c245`  
		Last Modified: Thu, 04 May 2023 06:54:14 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21279b8b8e2fd3e68ac4dca0013ddbc2ab040a12253bce1e16d405bf6a0f1830`  
		Last Modified: Thu, 04 May 2023 11:49:38 GMT  
		Size: 24.8 MB (24817550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238afc025859b80c07cf194a892af2f28ce855e279bb6713ded7cadf7942e369`  
		Last Modified: Tue, 16 May 2023 18:02:16 GMT  
		Size: 9.3 MB (9314433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41a6d617a0fd16b887b15bd90df9b5e74b665ef6e7de51ffa356c0bfb81b07c`  
		Last Modified: Tue, 16 May 2023 18:02:15 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceed7276ca8be86f967e704ef37ec80176ae66bb78c6d2ff44b96ef966e497be`  
		Last Modified: Tue, 16 May 2023 18:02:15 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c5906b6bbded4b50e482508da02933f97bf4b24cc23e69f0d3fca28470dae4`  
		Last Modified: Tue, 16 May 2023 18:02:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-8-focal` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:55791c8757b62e88d2939479280bfcbd27838ea7a394e3a5b296e8d86004b03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134450852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a611f4e8d0b31449e882b51c234773339c3fa0cc7a104c8c1042624d35efd95`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:41:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 19:39:26 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 03:25:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 03:25:07 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 03:25:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 May 2023 03:25:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 03:25:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 03:25:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 03:25:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 03:25:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 03:25:59 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 03:25:59 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 03:25:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 03:25:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 03:25:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269336393c4662b72ac4a2be29473801366e79f4db6c8b9944509f1903ee3fe6`  
		Last Modified: Tue, 18 Apr 2023 01:43:30 GMT  
		Size: 16.2 MB (16213349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8458dca1b69ff01ddfa6c98929321ceeb6d3de1a5cada07c5852a4086d7a3e94`  
		Last Modified: Thu, 04 May 2023 03:28:02 GMT  
		Size: 53.7 MB (53744559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a79ca23fd90b52cbfec617108c84cb5c00523ffb346e570c9e43e8160308a5e`  
		Last Modified: Thu, 04 May 2023 03:27:57 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa06a2246ab692198be1d61f5ad9af8581f61b972f8f51776014802f219d75cb`  
		Last Modified: Thu, 04 May 2023 12:01:55 GMT  
		Size: 28.2 MB (28188870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee047341ec0b4b49105eb083703fbbd4e8c27ee22be2998e44000010f1dc027`  
		Last Modified: Thu, 04 May 2023 12:01:52 GMT  
		Size: 9.1 MB (9106151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013ab63a23af8c51068b0edbdf448ece1c738a69c261e9227702711501055440`  
		Last Modified: Thu, 04 May 2023 12:01:51 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ee2a6100a21bd9665e03966b5e77fb92e2e8662ad0a7ce48d989d639dfcb76`  
		Last Modified: Thu, 04 May 2023 12:01:52 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f37bdf3cda393ff2e5029d0fde89c2f33ca161339492ea3e437a8a649c18334`  
		Last Modified: Thu, 04 May 2023 12:01:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-8-focal` - linux; ppc64le

```console
$ docker pull maven@sha256:0a0a1f27fad32c805941aa9f1c7e052a7afe4bef03016a61677a13226e91299c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.6 MB (146614401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1290120efe440879d0b68d085860aca58f8e80da8fe0467f67b938abea9f74`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:07:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 19:16:37 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 04 May 2023 13:59:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        armhf|arm)          ESUM='3f4848700a4bf856d3c138dc9c2b305b978879c8fbef5aa7df34a7c2fe1b64b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u372b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Thu, 04 May 2023 13:59:51 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 04 May 2023 14:02:43 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 May 2023 14:02:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 14:02:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 14:02:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 14:02:43 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 14:02:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 14:02:43 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 14:02:43 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 14:02:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 14:02:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 14:02:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4018ee3c8b327c120bbf0427fb12e76c74cb054a92177aeeae16bcf0efa4e86`  
		Last Modified: Tue, 18 Apr 2023 01:11:24 GMT  
		Size: 17.6 MB (17582531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3be13b8e9ed4e188e3a3d9b8057c4147f94ffceae1c7924d78f657b310eec9`  
		Last Modified: Thu, 04 May 2023 14:06:06 GMT  
		Size: 52.1 MB (52134527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b842f3b249e6233542f60734a8bf333111557d6c523208f9af0c95bd956f3fd9`  
		Last Modified: Thu, 04 May 2023 14:05:56 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3842078135871e2255c920725af5263980424bb3a8be89298d3e62c27cad6668`  
		Last Modified: Thu, 04 May 2023 18:59:09 GMT  
		Size: 34.5 MB (34488692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f460fb82108bb06ae0b53014b940107b7478c19d232c8b67213379c5fa883a8`  
		Last Modified: Thu, 04 May 2023 18:59:00 GMT  
		Size: 9.1 MB (9106140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c764e4b9c8ee93585b37ed6eb7552022495669cc1e9e0e0b3c0bce155a5e69f`  
		Last Modified: Thu, 04 May 2023 18:58:59 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c730188fe5ffb3a589412b16b3a125d270ad8d441537b49b05b18b1731283b65`  
		Last Modified: Thu, 04 May 2023 18:58:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7a8fdf529d87509efac30e217390e9c486e731739c6d6798e97c8bdeed70bd`  
		Last Modified: Thu, 04 May 2023 18:58:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
