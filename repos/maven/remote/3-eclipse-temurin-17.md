## `maven:3-eclipse-temurin-17`

```console
$ docker pull maven@sha256:471d9f0b11063569cc12ca07d6b44fa9a0bc17cde17535614275f82d4b0d92b6
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
$ docker pull maven@sha256:7c772dbfb5526a6843d39cf99fd095896785abcc5d6d557d10d44a73b8643984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268165638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf926540505e062ea7543587456ac51e98cf48f5534010bb3db189d7cae6bb87`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 07:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 07:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 07:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 07:28:04 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:28:04 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Thu, 04 May 2023 07:28:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0084272404b89442871e0a1f112779844090532978ad4d4191b8d03fc6adfade';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='e7a84c3e59704588510d7e6cce1f732f397b54a3b558c521912a18a1b4d0abdc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f4366ff1eddb548b1744cd82a1a56ceee60abebbcbad446bfb3ead7ac0f0f85';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='2d75540ae922d0c4162729267a8c741e2414881a468fd2ce4140b4069ba47ca9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e9458b38e97358850902c2936a1bb5f35f6cffc59da9fcd28c63eab8dbbfbc3b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 07:28:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 07:28:15 GMT
CMD ["jshell"]
# Thu, 04 May 2023 07:28:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 May 2023 07:28:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 07:28:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 07:28:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 07:28:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 07:28:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 07:28:15 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 07:28:15 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 07:28:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 07:28:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 07:28:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0e0ecb256ae3e8b7625494ed35189f845766552b7159a17f634706e28a9687`  
		Last Modified: Thu, 04 May 2023 07:31:32 GMT  
		Size: 17.0 MB (17047285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24bf4c725c221ddbb66e056716cf961f79001fedf2e8a0cddab347244398bac`  
		Last Modified: Thu, 04 May 2023 07:31:43 GMT  
		Size: 192.6 MB (192587571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb255c76461d67abc91f408697fa9ebae85009a5d6d94a905e52946bab9baa0`  
		Last Modified: Thu, 04 May 2023 07:31:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d4aead0b1cd9dfb05ef52e1bd3d3124909edb372d7097f7b0b143a05a9f723`  
		Last Modified: Thu, 04 May 2023 14:43:01 GMT  
		Size: 19.0 MB (18992848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc7cecc09be178c52fec802df9a91ea8d5be699446c891ef4979535db7262f0`  
		Last Modified: Thu, 04 May 2023 14:42:59 GMT  
		Size: 9.1 MB (9106173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700cc3fb9292921932556132facb5bfa821cb9f44de40779ba5bcbb4c8b03ad1`  
		Last Modified: Thu, 04 May 2023 14:42:58 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0a0c5ad00f7a35566dd1b6444e364adf00c0f61d18aa55a5a70fc151cdf654`  
		Last Modified: Thu, 04 May 2023 14:42:58 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49224bafae5998c6c3813738af1888254b4bd37f48d312c3c121ee87f0fe8a56`  
		Last Modified: Thu, 04 May 2023 14:42:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17` - linux; arm variant v7

```console
$ docker pull maven@sha256:34a1f5a94d265f6707654559ef48ddbd51b2b2b8d831f62f6b662e9c63470a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265194115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebd6f10f6624d0aa991eb26609f75513c855fc72d3c05f1a50c1b0aac5d44e9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 06:51:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 06:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:51:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 06:53:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:53:21 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Thu, 04 May 2023 06:53:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0084272404b89442871e0a1f112779844090532978ad4d4191b8d03fc6adfade';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='e7a84c3e59704588510d7e6cce1f732f397b54a3b558c521912a18a1b4d0abdc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f4366ff1eddb548b1744cd82a1a56ceee60abebbcbad446bfb3ead7ac0f0f85';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='2d75540ae922d0c4162729267a8c741e2414881a468fd2ce4140b4069ba47ca9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e9458b38e97358850902c2936a1bb5f35f6cffc59da9fcd28c63eab8dbbfbc3b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 06:53:37 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 06:53:37 GMT
CMD ["jshell"]
# Thu, 04 May 2023 06:53:37 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 May 2023 06:53:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 06:53:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 06:53:37 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 06:53:37 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 06:53:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 06:53:37 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 06:53:37 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 06:53:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 06:53:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 06:53:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2561bae7e5e30e2beaf0cb6907571e792834948f12d2a8923229e5ac85134ad4`  
		Last Modified: Wed, 26 Apr 2023 02:07:55 GMT  
		Size: 27.0 MB (27026323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2813bcd6edbef45cf68ef036e0b002ed7c943182304d7236121aea572b1c2de1`  
		Last Modified: Thu, 04 May 2023 06:56:01 GMT  
		Size: 17.2 MB (17166498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48113a819186383d14db09178b6507a6945e1ab1d207701c6d69cc0188421550`  
		Last Modified: Thu, 04 May 2023 06:56:14 GMT  
		Size: 189.6 MB (189596637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df571badf726f6ffd3b2ec4e85d823fcef68b11cf63eeae474101caa40e77396`  
		Last Modified: Thu, 04 May 2023 06:55:58 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dee4f1c04bf5d7f9cbe467d8af8d6a0914a1e426f97694b7e906eae8f9580b4`  
		Last Modified: Thu, 04 May 2023 11:49:02 GMT  
		Size: 22.3 MB (22296955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a26b600a1f28d958733f69fddf6adfe49887b7a301253d2123cc29b5a12ff8`  
		Last Modified: Thu, 04 May 2023 11:48:59 GMT  
		Size: 9.1 MB (9106162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94226b0850faa390652ebe2e78772fe271307298c92ca3814933fd8d59ddd13a`  
		Last Modified: Thu, 04 May 2023 11:48:58 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcdef4169ca20a139392b3ed31e588ce02f590207f78e7d0675f4c63e6e852d`  
		Last Modified: Thu, 04 May 2023 11:48:58 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65dcaecef33f7af85bc0e0190950c033463264bf762cca3e2b328afb397ef0da`  
		Last Modified: Thu, 04 May 2023 11:48:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3e1a2c754914623ba90b6f334c7522fd57b7cdabf659b8c8fae9600876ff310c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266371132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc9b62cf20481a8596f803f278ec68a1599786361a5aa9381386d1cbe8c9b14`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 03:25:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 03:25:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 03:25:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 03:26:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 03:26:25 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Thu, 04 May 2023 03:26:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0084272404b89442871e0a1f112779844090532978ad4d4191b8d03fc6adfade';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='e7a84c3e59704588510d7e6cce1f732f397b54a3b558c521912a18a1b4d0abdc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f4366ff1eddb548b1744cd82a1a56ceee60abebbcbad446bfb3ead7ac0f0f85';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='2d75540ae922d0c4162729267a8c741e2414881a468fd2ce4140b4069ba47ca9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e9458b38e97358850902c2936a1bb5f35f6cffc59da9fcd28c63eab8dbbfbc3b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 03:26:39 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 03:26:39 GMT
CMD ["jshell"]
# Thu, 04 May 2023 03:26:39 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 May 2023 03:26:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 03:26:39 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 03:26:39 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 03:26:39 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 03:26:39 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 03:26:39 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 03:26:39 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 03:26:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 03:26:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 03:26:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da9c27f8f486373408efc6e2d12bdb650ff3041dc480e2fcd2dd0c7e9be9777`  
		Last Modified: Thu, 04 May 2023 03:29:30 GMT  
		Size: 18.5 MB (18471737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e2ea804cf3eb99ede72c4190dd3df195e93e5efa059ac56b5ba6170423f227`  
		Last Modified: Thu, 04 May 2023 03:29:39 GMT  
		Size: 191.4 MB (191400625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad5170cfb57d48d8209d266deda3bd50024fea3a47edc24a73bdbd64ca9f9b2`  
		Last Modified: Thu, 04 May 2023 03:29:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563d878c5f5dbbfdbbce4241d561856727fa47ddbc6bc1c006388f649f9f6b06`  
		Last Modified: Thu, 04 May 2023 12:00:55 GMT  
		Size: 19.0 MB (19001629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556bd6b1c87a50d9f0810d0a643e0f53fa4bfab5056e77cfce546269d399ef42`  
		Last Modified: Thu, 04 May 2023 12:00:53 GMT  
		Size: 9.1 MB (9106167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241bdafedbbe7e3c05e32717b31f6c5a2511c296f9f58e0b3f05daf76417598b`  
		Last Modified: Thu, 04 May 2023 12:00:52 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4734d351054e97a8eeec4734f00b510043869a08e644fa95397d81c6720ea25`  
		Last Modified: Thu, 04 May 2023 12:00:52 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61013e2656d2ebcf422903b3544804b299a5712c97e01f06f90fecafd8c2f72`  
		Last Modified: Thu, 04 May 2023 12:00:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17` - linux; ppc64le

```console
$ docker pull maven@sha256:ad30bfcc6485ccb1be9414e119784c92ae67a616afbaebcf689974a2e31e0672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277322546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe444c884626335bacd10fa4ad0e029293f778919a8452950355c8e79f6213c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:17 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:21 GMT
ADD file:e75f08a67f0576b5441bb2fe454cad4b5b31a9d4efea23be791af62e1e0c712f in / 
# Tue, 25 Apr 2023 17:30:21 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 13:59:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 13:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 13:59:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 May 2023 14:03:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 14:04:00 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Thu, 04 May 2023 14:04:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0084272404b89442871e0a1f112779844090532978ad4d4191b8d03fc6adfade';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='e7a84c3e59704588510d7e6cce1f732f397b54a3b558c521912a18a1b4d0abdc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f4366ff1eddb548b1744cd82a1a56ceee60abebbcbad446bfb3ead7ac0f0f85';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='2d75540ae922d0c4162729267a8c741e2414881a468fd2ce4140b4069ba47ca9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e9458b38e97358850902c2936a1bb5f35f6cffc59da9fcd28c63eab8dbbfbc3b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 04 May 2023 14:04:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 04 May 2023 14:04:29 GMT
CMD ["jshell"]
# Thu, 04 May 2023 14:04:29 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 May 2023 14:04:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 14:04:29 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 14:04:29 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 14:04:29 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 14:04:29 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 14:04:29 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 14:04:29 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 14:04:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 14:04:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 14:04:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f6a63d8cd043e76933823b18cbb7057a55bb4d66d64639c81e15a4700c101582`  
		Last Modified: Wed, 03 May 2023 17:09:07 GMT  
		Size: 35.7 MB (35712706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580404a3efae4fe33e5ee9bb8d7aed2badbd9f1d90751bab72745d14adfd9bc4`  
		Last Modified: Thu, 04 May 2023 14:08:21 GMT  
		Size: 18.3 MB (18329980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e7ce227e75e5d09304ac17952109eccb890984c48e9456bdb82f9d6d0164e7`  
		Last Modified: Thu, 04 May 2023 14:08:40 GMT  
		Size: 192.0 MB (191964935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff58a2a45837aa2a50293050daee1636438df833275b2ac8dcae468a693e63cb`  
		Last Modified: Thu, 04 May 2023 14:08:15 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4e129c083ec36dd70a35ebaf959ac726e1ad93131ed5eeb31e8a4b4068b4e9`  
		Last Modified: Thu, 04 May 2023 18:57:47 GMT  
		Size: 22.2 MB (22207241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae2c77a887f2e93f17f7eedb95a486c9ac5a943551ba23fcf332020f02128f2`  
		Last Modified: Thu, 04 May 2023 18:57:41 GMT  
		Size: 9.1 MB (9106142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b940a90bb20f42dc3228687c4faa868a574dc3173159372091f67fbe9861acbf`  
		Last Modified: Thu, 04 May 2023 18:57:40 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45030475faf26bad41321f821f4b83a6a5abcaf34cd64f4740bf92fb8606d08`  
		Last Modified: Thu, 04 May 2023 18:57:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79d4df0b209df6cf67b2724816c7f15544f80d90674e148fe815c033e0b597c`  
		Last Modified: Thu, 04 May 2023 18:57:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-17` - linux; s390x

```console
$ docker pull maven@sha256:5a4e59e69946bdf268b563297be3456d3adec4e69d3a7b58479e75fe683e3770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 MB (254159398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a5c8a2f3116a3dbc026be951820a859da2d892bdb883dce9fa85cdf5f2246c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
# Fri, 05 May 2023 00:05:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 May 2023 00:05:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 00:05:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 May 2023 00:06:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 00:06:17 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Fri, 05 May 2023 00:06:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0084272404b89442871e0a1f112779844090532978ad4d4191b8d03fc6adfade';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='e7a84c3e59704588510d7e6cce1f732f397b54a3b558c521912a18a1b4d0abdc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f4366ff1eddb548b1744cd82a1a56ceee60abebbcbad446bfb3ead7ac0f0f85';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='2d75540ae922d0c4162729267a8c741e2414881a468fd2ce4140b4069ba47ca9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e9458b38e97358850902c2936a1bb5f35f6cffc59da9fcd28c63eab8dbbfbc3b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 05 May 2023 00:06:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 May 2023 00:06:35 GMT
CMD ["jshell"]
# Fri, 05 May 2023 00:06:35 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 May 2023 00:06:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 05 May 2023 00:06:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 05 May 2023 00:06:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 05 May 2023 00:06:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 05 May 2023 00:06:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 05 May 2023 00:06:35 GMT
ARG MAVEN_VERSION=3.9.1
# Fri, 05 May 2023 00:06:35 GMT
ARG USER_HOME_DIR=/root
# Fri, 05 May 2023 00:06:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 05 May 2023 00:06:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 05 May 2023 00:06:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:78722793f0008ff8422830a0106f21e8bc168fb9aac12cc99fb223799951759e`  
		Last Modified: Wed, 03 May 2023 22:33:36 GMT  
		Size: 28.6 MB (28647905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49b1e85674749d49983d988affa30d35c216175c7425eb7e04b0db0a28be408`  
		Last Modified: Fri, 05 May 2023 00:08:09 GMT  
		Size: 16.8 MB (16823080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce8ba2585974badfb159f3db2ae56db026b7e23f8b21079d1d53563695937b8`  
		Last Modified: Fri, 05 May 2023 00:08:19 GMT  
		Size: 180.4 MB (180361728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d209fd957ebf7d15f0c4c51cca1e06d8a71734f46758285fcb580842a5e8c356`  
		Last Modified: Fri, 05 May 2023 00:08:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7814f5052766f1636c032eb77b98c2a3349eac1e39cfab62fbd89c3bfd28bd6a`  
		Last Modified: Fri, 05 May 2023 04:04:57 GMT  
		Size: 19.2 MB (19218991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258005b8ea244ae2a86aeb67959126a36b11f6b1bdcc1bfb1af29bc1c991fa4f`  
		Last Modified: Fri, 05 May 2023 04:04:54 GMT  
		Size: 9.1 MB (9106161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ca10de3dfb1ad3bab70a876bec5adaf83267d0ce0ba21a98a63c99a233885f`  
		Last Modified: Fri, 05 May 2023 04:04:54 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4ff9c1cdc280ba0ba6087fabe13fbb77107b95cf1d99e8d58697afa8fd8897`  
		Last Modified: Fri, 05 May 2023 04:04:54 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfdbfc416b10b4407aa4a55a59fe694678424524ad81222ee1951b7800b497a`  
		Last Modified: Fri, 05 May 2023 04:04:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
