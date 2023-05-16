## `maven:3-eclipse-temurin-17-focal`

```console
$ docker pull maven@sha256:f429ed28061c243963545646ba5d4c6f8b4c944fade6d92ee1043ca2ece8fd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-eclipse-temurin-17-focal` - linux; amd64

```console
$ docker pull maven@sha256:aead4f741e4f7c8a1432fdb397e7ac169dcc5cbcd5595d703e05ab6b7618ad59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278341946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22395068cf22ed123d413a78a007a82cf03184ab5b6bb2917489b7be7c8b12f0`
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
# Tue, 18 Apr 2023 00:44:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 19:22:46 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Wed, 26 Apr 2023 19:22:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0084272404b89442871e0a1f112779844090532978ad4d4191b8d03fc6adfade';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='e7a84c3e59704588510d7e6cce1f732f397b54a3b558c521912a18a1b4d0abdc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f4366ff1eddb548b1744cd82a1a56ceee60abebbcbad446bfb3ead7ac0f0f85';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='2d75540ae922d0c4162729267a8c741e2414881a468fd2ce4140b4069ba47ca9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e9458b38e97358850902c2936a1bb5f35f6cffc59da9fcd28c63eab8dbbfbc3b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Apr 2023 19:22:57 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Apr 2023 19:22:57 GMT
CMD ["jshell"]
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
	-	`sha256:b493027a1bf3e6a19b932ebe3c6dbfe19dc6a4583dfe39282977a57c89b31e87`  
		Last Modified: Tue, 18 Apr 2023 00:47:39 GMT  
		Size: 20.1 MB (20096839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6dd141d5c93b23da5b6e10fce51a3b7c13bfa38011957619ae7ad2c3304f7e9`  
		Last Modified: Wed, 26 Apr 2023 19:32:47 GMT  
		Size: 192.6 MB (192587870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a942aa62f476c3606b1c2ea5a98487b5a12d0af43021dc45c5ddc54f14b206e3`  
		Last Modified: Wed, 26 Apr 2023 19:32:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81388f47e5e8328ed190894d1eebe4abe67a0272e558be1ccf67e7069994b8c`  
		Last Modified: Wed, 26 Apr 2023 22:59:43 GMT  
		Size: 28.0 MB (27970961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31124129ff15e181219ed77eb65898eac0bb5b6b2ae429161559576207f4cfd`  
		Last Modified: Wed, 26 Apr 2023 22:59:40 GMT  
		Size: 9.1 MB (9106172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6dee3bc6a1a1bddd30986ee563cd1d83d6c1fd026c0ae40bee6846469333b3`  
		Last Modified: Wed, 26 Apr 2023 22:59:39 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbe3fd719a4439aff5274af1f4f98529f826be02958b1370fc8dc1029208320`  
		Last Modified: Wed, 26 Apr 2023 22:59:39 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd01c60e60dec71e4b3b8d287240a9ef5ef4e90ab4f072b98a138f0e09a0107`  
		Last Modified: Wed, 26 Apr 2023 22:59:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17-focal` - linux; arm variant v7

```console
$ docker pull maven@sha256:03c276a36933917e65110353eec5b09928bec19b030dae371e3393483fd9d680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267414274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc3344d263e6939de9a17985c55c5b47e67954519c8842dfeaa1f8449ca4dba`
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
# Tue, 18 Apr 2023 01:53:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 19:59:07 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Wed, 26 Apr 2023 19:59:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0084272404b89442871e0a1f112779844090532978ad4d4191b8d03fc6adfade';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='e7a84c3e59704588510d7e6cce1f732f397b54a3b558c521912a18a1b4d0abdc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f4366ff1eddb548b1744cd82a1a56ceee60abebbcbad446bfb3ead7ac0f0f85';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='2d75540ae922d0c4162729267a8c741e2414881a468fd2ce4140b4069ba47ca9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e9458b38e97358850902c2936a1bb5f35f6cffc59da9fcd28c63eab8dbbfbc3b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Apr 2023 19:59:22 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Apr 2023 19:59:22 GMT
CMD ["jshell"]
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
	-	`sha256:85796ae94aa6103041abcc6b06ff12a50d94cadaf6e06eb70a7394c3872a6748`  
		Last Modified: Tue, 18 Apr 2023 01:55:40 GMT  
		Size: 19.5 MB (19465888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc5c2272de47c36a29d8c0d251614e6a516221fdac7a2c3585cca41d077c09d`  
		Last Modified: Wed, 26 Apr 2023 20:02:04 GMT  
		Size: 189.6 MB (189596727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9396e1993c44089af2d6c90bfd02bfaaaf31bcf122eb6c7790bf2b6eda39fea1`  
		Last Modified: Wed, 26 Apr 2023 20:01:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51065b33d668bd9239e8217a82301999e850acefb31d72fb599c46181c1caf2`  
		Last Modified: Wed, 26 Apr 2023 20:52:08 GMT  
		Size: 24.4 MB (24448731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b935e35526e9a9ed25fb28c5897dcbfb68a9fbf0ba16fa36ff253d7de7984516`  
		Last Modified: Tue, 16 May 2023 18:01:53 GMT  
		Size: 9.3 MB (9314414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4541162ee8daac13922a2c3d330e41490bf4d3ea9280e1268eec58de4f09e0`  
		Last Modified: Tue, 16 May 2023 18:01:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67da8fc51e23216047cfcda623fef1f04d833607392029243522da318deece3`  
		Last Modified: Tue, 16 May 2023 18:01:53 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1425ffd343c3219834646eaf0175805e8df7d29f613dc340a10464a9ab78b6c2`  
		Last Modified: Tue, 16 May 2023 18:01:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17-focal` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fb16b9fb9bc589142a4fc39532a54d5c071550987973a34f9c565bff58ea179f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.5 MB (276516790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a977e2ed2cbd1c6e86f6cd060ab1e657329d92b782cded9a4688da42add87420`
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
# Tue, 18 Apr 2023 01:42:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 19:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Wed, 26 Apr 2023 19:41:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0084272404b89442871e0a1f112779844090532978ad4d4191b8d03fc6adfade';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='e7a84c3e59704588510d7e6cce1f732f397b54a3b558c521912a18a1b4d0abdc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f4366ff1eddb548b1744cd82a1a56ceee60abebbcbad446bfb3ead7ac0f0f85';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='2d75540ae922d0c4162729267a8c741e2414881a468fd2ce4140b4069ba47ca9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e9458b38e97358850902c2936a1bb5f35f6cffc59da9fcd28c63eab8dbbfbc3b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Apr 2023 19:41:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Apr 2023 19:41:44 GMT
CMD ["jshell"]
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
	-	`sha256:4f855dc454f40dbe47d375c509772787d9d27ff505e14349af4f2e3944f28f75`  
		Last Modified: Tue, 18 Apr 2023 01:44:38 GMT  
		Size: 20.8 MB (20815202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cfbead4ab6695e8e5082cf21969d8cddd4af6f02659c98db80315b6bc00b20`  
		Last Modified: Wed, 26 Apr 2023 19:48:47 GMT  
		Size: 191.4 MB (191403797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ab5928b774148eca0fea966342b3695c4c7286fc929cff74ef4fca20bf40f1`  
		Last Modified: Wed, 26 Apr 2023 19:48:36 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448048a0f15953cfc1e72aa04644e7f20b241f633a0fbb6f20c3afd3bf013525`  
		Last Modified: Wed, 26 Apr 2023 21:24:04 GMT  
		Size: 28.0 MB (27993699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9513fe323f0126836f58594032fb7ce4ac6ed0f2fa3958300de2e6e425f575`  
		Last Modified: Wed, 26 Apr 2023 21:24:01 GMT  
		Size: 9.1 MB (9106159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d32a4a403147f2e654654d6c5a7ea62caeb12bd308febaeb5434f2c9e598765`  
		Last Modified: Wed, 26 Apr 2023 21:24:00 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d552616f1e3cffc981397dae154c06306bb91a63054640cc4004f2fb3ae664`  
		Last Modified: Wed, 26 Apr 2023 21:24:00 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c159c03147963f37018d1214409331238ef24155c934eeb464a73c51241522`  
		Last Modified: Wed, 26 Apr 2023 21:24:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17-focal` - linux; ppc64le

```console
$ docker pull maven@sha256:e19edadd3ec8ff73e02312f41f42c7c52ed4f1dcedad62ee3e65ad16f286281a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290855154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9d0d1b7cfd4245242fe80d0ee748da97a2d733cf980d636ac928298f6833f2`
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
# Tue, 18 Apr 2023 01:09:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 19:22:51 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Wed, 26 Apr 2023 19:23:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0084272404b89442871e0a1f112779844090532978ad4d4191b8d03fc6adfade';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='e7a84c3e59704588510d7e6cce1f732f397b54a3b558c521912a18a1b4d0abdc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f4366ff1eddb548b1744cd82a1a56ceee60abebbcbad446bfb3ead7ac0f0f85';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='2d75540ae922d0c4162729267a8c741e2414881a468fd2ce4140b4069ba47ca9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e9458b38e97358850902c2936a1bb5f35f6cffc59da9fcd28c63eab8dbbfbc3b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Apr 2023 19:23:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Apr 2023 19:23:25 GMT
CMD ["jshell"]
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
	-	`sha256:8d16c8f7fe3c69e12b82f6ead20825685acccc07c7db20352690c45095874956`  
		Last Modified: Tue, 18 Apr 2023 01:13:05 GMT  
		Size: 22.1 MB (22066207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ad4f52d96ee8f3ef9f55d7069408a89bf1fd644801a20f63e65b010939f93a`  
		Last Modified: Wed, 26 Apr 2023 19:34:30 GMT  
		Size: 192.0 MB (191966155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12a4ee40a0a3be3abaefe756fffe888567ff312c30182a27314052232b15ec5`  
		Last Modified: Wed, 26 Apr 2023 19:34:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba92f44d924d275da2a9ef2917dc42f0365e360601b35b802587f058c1b932d`  
		Last Modified: Wed, 26 Apr 2023 20:34:12 GMT  
		Size: 34.4 MB (34414121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b2bd42875df0123d3dc9b3bb506ab428affadc732fdc5dfd67792d4505a7a1`  
		Last Modified: Wed, 26 Apr 2023 20:34:02 GMT  
		Size: 9.1 MB (9106150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e600d45261eba693455fd890248a805f841a181690be7f8c5d7a2fd9f7304322`  
		Last Modified: Wed, 26 Apr 2023 20:34:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b37772ae8f820a965d27994472845ca65e6225641a5f103a58683b642ab177b`  
		Last Modified: Wed, 26 Apr 2023 20:34:01 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac3c7d165591a29a53a222cb15fb951f30e89623c92b8ef8d21ddbde6097124`  
		Last Modified: Wed, 26 Apr 2023 20:34:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17-focal` - linux; s390x

```console
$ docker pull maven@sha256:66455fa5dd2a2a2874b611c0a0092a56325130ab6ea8e4aa3ca003cc8b97fefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263553396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3604155c74899d5e1fdc58e6991441514399ad55121602cd7fffa15a7434f2d2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:16:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:17:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 19:43:29 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Wed, 26 Apr 2023 19:43:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0084272404b89442871e0a1f112779844090532978ad4d4191b8d03fc6adfade';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='e7a84c3e59704588510d7e6cce1f732f397b54a3b558c521912a18a1b4d0abdc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f4366ff1eddb548b1744cd82a1a56ceee60abebbcbad446bfb3ead7ac0f0f85';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='2d75540ae922d0c4162729267a8c741e2414881a468fd2ce4140b4069ba47ca9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e9458b38e97358850902c2936a1bb5f35f6cffc59da9fcd28c63eab8dbbfbc3b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 26 Apr 2023 19:43:45 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Apr 2023 19:43:45 GMT
CMD ["jshell"]
# Fri, 05 May 2023 00:05:35 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 May 2023 00:05:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 05 May 2023 00:05:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 05 May 2023 00:05:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 05 May 2023 00:05:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 05 May 2023 00:05:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 05 May 2023 00:05:35 GMT
ARG MAVEN_VERSION=3.9.1
# Fri, 05 May 2023 00:05:35 GMT
ARG USER_HOME_DIR=/root
# Fri, 05 May 2023 00:05:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 05 May 2023 00:05:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 05 May 2023 00:05:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf6c28f706c8f54c079ff27fe5409527f68c7463df6adf843d835f265547cf5`  
		Last Modified: Tue, 18 Apr 2023 01:19:02 GMT  
		Size: 19.5 MB (19532693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c930344e11d361cefd442f9b5ebbfea6a58b35d48fd1e61e9fb3ee89535c9e`  
		Last Modified: Wed, 26 Apr 2023 19:47:12 GMT  
		Size: 180.4 MB (180363062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5c1bce50e8ca9fbfc791aef82493fffb81f337844bfb6a6a62d20a2483d168`  
		Last Modified: Wed, 26 Apr 2023 19:47:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b809be28d1402d0e575eb3751dbf10086923b7dc84b36f5cfc486a021054ebab`  
		Last Modified: Wed, 26 Apr 2023 20:17:56 GMT  
		Size: 27.5 MB (27533568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f23792baf005195236fa277eae392a064ef4befa32609e090e604dadc679db2`  
		Last Modified: Wed, 26 Apr 2023 20:17:53 GMT  
		Size: 9.1 MB (9106161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f53cf1eac10477f95b742fbb621a6cc77b16158f9a6bc00009d7d277173b65b`  
		Last Modified: Wed, 26 Apr 2023 20:17:52 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd876ce015823163850c25c6b9a5ff87bef531b183f48e1ea8c8b90d758c797f`  
		Last Modified: Wed, 26 Apr 2023 20:17:52 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8fbecaa6e18249b51d6ca859154674f9c7cb48d9ee46fe1b057eb10daa7194`  
		Last Modified: Wed, 26 Apr 2023 20:17:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
