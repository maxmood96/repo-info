## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:fa5922ab101a269854285bfd8aafeff4164497dc9b6fd730634928ab165ea6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:latest` - linux; amd64

```console
$ docker pull zookeeper@sha256:e20c833cce4d3f26f2599bf60976a1bebee9ff2a5d6a79c459238650b12cb4dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120133388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83d6f21f44dd5c70f4801f501358f4812e2e8a638a3f692b715fd8dc72728e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:51:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 05:51:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 05:51:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 13 Oct 2023 05:53:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 05:53:53 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Fri, 13 Oct 2023 05:54:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 13 Oct 2023 05:54:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 13 Oct 2023 05:54:29 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 13 Oct 2023 05:54:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Oct 2023 00:27:19 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Tue, 17 Oct 2023 00:27:19 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Tue, 17 Oct 2023 00:27:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Tue, 17 Oct 2023 00:27:33 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Tue, 17 Oct 2023 00:27:50 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Tue, 17 Oct 2023 00:27:51 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Tue, 17 Oct 2023 00:27:55 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Tue, 17 Oct 2023 00:27:55 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Tue, 17 Oct 2023 00:27:55 GMT
VOLUME [/data /datalog /logs]
# Tue, 17 Oct 2023 00:27:55 GMT
EXPOSE 2181 2888 3888 8080
# Tue, 17 Oct 2023 00:27:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Tue, 17 Oct 2023 00:27:55 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Tue, 17 Oct 2023 00:27:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Oct 2023 00:27:55 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50431c77a77b7f46c78e4929a36d42dcb3551c22e0404d2bee6e8a15cc650640`  
		Last Modified: Fri, 13 Oct 2023 05:59:21 GMT  
		Size: 17.5 MB (17454843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd8e860e67230bfef1a2f42f986d22713cfc307559996493f6aac0f0bfc32c8`  
		Last Modified: Fri, 13 Oct 2023 06:00:06 GMT  
		Size: 47.2 MB (47209787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637e2db99ae6d5d22792dba960463b31fc445d5be9e3383fef9f0be96900a680`  
		Last Modified: Fri, 13 Oct 2023 05:59:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de1c2853278b16ef01c0abfa4065794c145daefc507cb6cb6fb56a1803a58bb`  
		Last Modified: Fri, 13 Oct 2023 05:59:59 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d09d7308b8cbb87cecd1bc95da3bc4e97d74b57cbd30252c61c165fffba4bb7`  
		Last Modified: Tue, 17 Oct 2023 00:29:05 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832676806c5c81fd5c283d9f6e83a6f5a575f8e4add3ce2656f75401ae35b91a`  
		Last Modified: Tue, 17 Oct 2023 00:29:06 GMT  
		Size: 4.6 MB (4606735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e72f3441e1f33264abb4e5e80a1937d45a122dbd0c7ca841527653269c43d8`  
		Last Modified: Tue, 17 Oct 2023 00:29:32 GMT  
		Size: 20.4 MB (20419357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2accac43da8f0b10455fe8a07f95e796a82cc69d8db63a33af823dab4edb7b`  
		Last Modified: Tue, 17 Oct 2023 00:29:30 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:latest` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:5bd24dcf60b4a1fabf7fc8757e454c13c4f7f24147e185fca6ebe47805cbc23c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110841286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ee5b8d306f55b09b1219e21527b2d2bf540cf4ee7c06fd2314b8294ef138a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:46:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 02:46:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 02:46:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 13 Oct 2023 02:46:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 02:47:30 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Fri, 13 Oct 2023 02:47:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 13 Oct 2023 02:47:54 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 13 Oct 2023 02:47:54 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 13 Oct 2023 02:47:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 13 Oct 2023 09:43:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 13 Oct 2023 09:43:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 13 Oct 2023 09:43:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 13 Oct 2023 09:43:51 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 13 Oct 2023 09:43:51 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.0
# Fri, 13 Oct 2023 09:43:51 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.0-bin
# Fri, 13 Oct 2023 09:44:12 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.0-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.0
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 13 Oct 2023 09:44:12 GMT
WORKDIR /apache-zookeeper-3.9.0-bin
# Fri, 13 Oct 2023 09:44:13 GMT
VOLUME [/data /datalog /logs]
# Fri, 13 Oct 2023 09:44:13 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 13 Oct 2023 09:44:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.0-bin/bin ZOOCFGDIR=/conf
# Fri, 13 Oct 2023 09:44:13 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 13 Oct 2023 09:44:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 09:44:13 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0137fa974e870bf950b9443cae72cbb22adb398877f52eca3717d3fa96a8d4`  
		Last Modified: Fri, 13 Oct 2023 02:50:57 GMT  
		Size: 12.8 MB (12843553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7e4c1d47e5a96cbcda29875d98d8600ce48b97fafa22cc9d9614f83800119d`  
		Last Modified: Fri, 13 Oct 2023 02:52:43 GMT  
		Size: 45.2 MB (45190528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85088878238bbee370ba753efe6d04b350f044a2bb1807bd1954d43ec1a33207`  
		Last Modified: Fri, 13 Oct 2023 02:52:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80a23506920ab265c4a3fc3726d5e6e4a3ce8e8089c34ac09851c1dcc3c37f2`  
		Last Modified: Fri, 13 Oct 2023 02:52:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f53f9038dc12f2d14d16aaefad5aaa2acb2a805f8749f624d349397a8ff2b5`  
		Last Modified: Fri, 13 Oct 2023 09:44:29 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64c2eaeecc4f8216ba36142317d0c8b06d40c1f6c6a8dfd3e7306b5d1fdb35`  
		Last Modified: Fri, 13 Oct 2023 09:44:30 GMT  
		Size: 4.5 MB (4509775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac7d349f81e2bf4085100ef7a64b7275c19b363d07df83bccccf50472547cde`  
		Last Modified: Fri, 13 Oct 2023 09:44:59 GMT  
		Size: 19.9 MB (19901940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2215235b1ae9c0ed6d18ca54af56401686d802a49df8ba9262b9f544941879c2`  
		Last Modified: Fri, 13 Oct 2023 09:44:53 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:latest` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:ba765df8afd45bc6eaa8dec093c37339f2052486eb01e6b9973fde5cdbc3c467
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127107997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e87aff09c0a671578e3d172343ee60244a54b76947371ecf1028b8035f0b5cb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:00:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:00:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 08:00:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 13 Oct 2023 08:06:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:06:16 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Fri, 13 Oct 2023 08:07:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 13 Oct 2023 08:07:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 13 Oct 2023 08:07:25 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 13 Oct 2023 08:07:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Oct 2023 00:17:48 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Tue, 17 Oct 2023 00:17:49 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Tue, 17 Oct 2023 00:18:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Tue, 17 Oct 2023 00:18:12 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Tue, 17 Oct 2023 00:18:33 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Tue, 17 Oct 2023 00:18:33 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Tue, 17 Oct 2023 00:18:38 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Tue, 17 Oct 2023 00:18:39 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Tue, 17 Oct 2023 00:18:39 GMT
VOLUME [/data /datalog /logs]
# Tue, 17 Oct 2023 00:18:39 GMT
EXPOSE 2181 2888 3888 8080
# Tue, 17 Oct 2023 00:18:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Tue, 17 Oct 2023 00:18:40 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Tue, 17 Oct 2023 00:18:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Oct 2023 00:18:40 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c559c1eed15ba953e9869061b9d93714ba932b8cafa1144defb5e96eaa9b22`  
		Last Modified: Fri, 13 Oct 2023 08:11:30 GMT  
		Size: 18.7 MB (18729626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6ba24540b23e597af8cb061d7758eb728ca6e332064eb109e92fd1e55bf6f1`  
		Last Modified: Fri, 13 Oct 2023 08:12:19 GMT  
		Size: 47.1 MB (47054832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39be3f0f624ff5b8e5d408104862bfda82809ee16a43eb6da48fe80317c67b2`  
		Last Modified: Fri, 13 Oct 2023 08:12:12 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd5d67710559896ad5605aac507024d610bee77e66eec260bbd54878a680983`  
		Last Modified: Fri, 13 Oct 2023 08:12:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d00b8f53a39b20bcc8001c3f3f3ea8c125f1eea88d1553b599e7cf8884e33d`  
		Last Modified: Tue, 17 Oct 2023 00:19:51 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6916705b2a13e214cc9e3c078a12bb7f07ad4254c01f032cdeb3d8abb0f8738e`  
		Last Modified: Tue, 17 Oct 2023 00:19:52 GMT  
		Size: 5.2 MB (5217774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09df38364fc9254492aed3472405a67cc3e2163a4d20e6251a1d9c31cdfd861`  
		Last Modified: Tue, 17 Oct 2023 00:20:17 GMT  
		Size: 20.4 MB (20419418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa64a1ae93745932264fbf461e2075d5bb5440fa9a66f07f155f9504fecef5c`  
		Last Modified: Tue, 17 Oct 2023 00:20:15 GMT  
		Size: 773.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:latest` - linux; s390x

```console
$ docker pull zookeeper@sha256:bf1dcf5171dde6c3d6c5f53ad8e4c3fd73484585ca2fbb6aa70745cd451c19f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106650081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7f8132109d9205885386ebfa5b0fed1066039510b4b9544a4c8ebaa5a07608`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 05 Oct 2023 07:29:34 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:29:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:29:34 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:29:36 GMT
ADD file:d165475f8f027ab758a463da57c8c29f5d302f0a87a475ac68fdfae30005c7ac in / 
# Thu, 05 Oct 2023 07:29:36 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:09:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:09:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 13 Oct 2023 10:09:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 10:09:54 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Fri, 13 Oct 2023 10:11:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2fc1cc935897312c0bc2515b2e7ea1fa3b267e77305a1b51a8c3917d92af380f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 13 Oct 2023 10:11:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 13 Oct 2023 10:11:29 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 13 Oct 2023 10:11:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 13 Oct 2023 11:54:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 13 Oct 2023 11:54:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 13 Oct 2023 11:54:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 13 Oct 2023 11:54:40 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 13 Oct 2023 11:54:40 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.0
# Fri, 13 Oct 2023 11:54:40 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.0-bin
# Fri, 13 Oct 2023 11:54:53 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.0-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.0
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 13 Oct 2023 11:54:54 GMT
WORKDIR /apache-zookeeper-3.9.0-bin
# Fri, 13 Oct 2023 11:54:54 GMT
VOLUME [/data /datalog /logs]
# Fri, 13 Oct 2023 11:54:54 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 13 Oct 2023 11:54:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.0-bin/bin ZOOCFGDIR=/conf
# Fri, 13 Oct 2023 11:54:54 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 13 Oct 2023 11:54:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 11:54:54 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:818e4e246beb9ab026d2b95bf051fe9610b92dbc0a35b45d09b0cf237b6f3c2e`  
		Last Modified: Fri, 13 Oct 2023 10:16:45 GMT  
		Size: 28.7 MB (28650497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9f2044d37c770d7ef145660592cf889c94feed6d387fc7c44cff98ca049436`  
		Last Modified: Fri, 13 Oct 2023 10:16:42 GMT  
		Size: 13.0 MB (12981177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1c46093d6f9ddc1a362e447a0e332ce169ef399cd6ea73cd38e7af1e004ed4`  
		Last Modified: Fri, 13 Oct 2023 10:17:19 GMT  
		Size: 40.6 MB (40632151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7d88520fde4d443077b4433098e83e0dd0d2a5fb9fe48085564a39793beea1`  
		Last Modified: Fri, 13 Oct 2023 10:17:13 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e87c26d84b3bde79ac40c01cb6698343e1e0f683875b51669827416951dd7f`  
		Last Modified: Fri, 13 Oct 2023 10:17:13 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf3bdd5376bf66f2d91ea56e251ad865bb00a0e489ed0f26907e9e334c9ef9b`  
		Last Modified: Fri, 13 Oct 2023 11:55:14 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d04edf23ee3ab17d06544c75cade186e88b57e703a02df0e9abd1f236547bd8`  
		Last Modified: Fri, 13 Oct 2023 11:55:15 GMT  
		Size: 4.5 MB (4480782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6eb42f2d047f4e1165547ff6352966cafc721a793cb4e29e0f4bb8f4c29e1b`  
		Last Modified: Fri, 13 Oct 2023 11:55:34 GMT  
		Size: 19.9 MB (19901920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5590e82b4e1f409dfce6266f2fd5c03242baa43af8ef73a986b729e55e2e8901`  
		Last Modified: Fri, 13 Oct 2023 11:55:31 GMT  
		Size: 772.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
