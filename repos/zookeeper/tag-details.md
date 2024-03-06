<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `zookeeper`

-	[`zookeeper:3.7`](#zookeeper37)
-	[`zookeeper:3.7-jre-11`](#zookeeper37-jre-11)
-	[`zookeeper:3.7-jre-17`](#zookeeper37-jre-17)
-	[`zookeeper:3.7.2`](#zookeeper372)
-	[`zookeeper:3.7.2-jre-11`](#zookeeper372-jre-11)
-	[`zookeeper:3.7.2-jre-17`](#zookeeper372-jre-17)
-	[`zookeeper:3.8`](#zookeeper38)
-	[`zookeeper:3.8-jre-11`](#zookeeper38-jre-11)
-	[`zookeeper:3.8-jre-17`](#zookeeper38-jre-17)
-	[`zookeeper:3.8.3`](#zookeeper383)
-	[`zookeeper:3.8.3-jre-11`](#zookeeper383-jre-11)
-	[`zookeeper:3.8.3-jre-17`](#zookeeper383-jre-17)
-	[`zookeeper:3.9`](#zookeeper39)
-	[`zookeeper:3.9-jre-11`](#zookeeper39-jre-11)
-	[`zookeeper:3.9-jre-17`](#zookeeper39-jre-17)
-	[`zookeeper:3.9.1`](#zookeeper391)
-	[`zookeeper:3.9.1-jre-11`](#zookeeper391-jre-11)
-	[`zookeeper:3.9.1-jre-17`](#zookeeper391-jre-17)
-	[`zookeeper:latest`](#zookeeperlatest)

## `zookeeper:3.7`

```console
$ docker pull zookeeper@sha256:a8c3a559ab45b97c68fb063543308171ff19111211c6369a0fd95b09b1d935c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.7` - linux; amd64

```console
$ docker pull zookeeper@sha256:492a1481c3507cee8bf6a7b7a953f132fa4626f6d15b6d4c2036cc1be9826e49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109174259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446078172ae870beb2b17c34fe7fb0d18843456ed567d8c7b55e6978c9236323`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:15 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Fri, 16 Feb 2024 04:43:15 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:20 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:20 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:20 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:20 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:20 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96877b3c6c46bb5d82eafbeaa6b5b7ec7472a5eb174c7463858986ab5ec48717`  
		Last Modified: Fri, 16 Feb 2024 04:44:30 GMT  
		Size: 14.1 MB (14139899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7499525ebd73bf924d9b2a1523cc9b876bb04740afa8c8d77ac4754a2ad15e`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:25e6c2a4099e8932c00c3fe02f8fad45c44a5ec30152cb1bfedbfe0309be98b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105299794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91a3cff40caca3f7f2f2f75b5e47557fc8ecad87ffee3a69a8e90ea68f127a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:12:32 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 12:12:32 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:12:37 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:12:37 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:12:37 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:12:37 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:12:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:12:38 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:12:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:38 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba37258a41e114a24b65baf1fae6f1d2e444db83fb2dd7e0b7decf72b18e51`  
		Last Modified: Wed, 06 Mar 2024 12:15:20 GMT  
		Size: 14.1 MB (14139929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf8ecad0e9a78a1c89aff19160500e54aa621a0c3bb493b42fe5ff51d59c6f`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:511547b95ed4f4923110a1b9bb75e3071fce2841fbae08f0fc08e520015528dc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111233909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df05f541ea22dea3f2afcd23c25f130cadcb926b1f214f5c37689e389e4c7add`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:16:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 04:16:32 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:16:40 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:16:41 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:16:42 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:16:43 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:16:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:16:44 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:16:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:46 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ceebe419d4baade36efb91807bde8faee0944e827ea24e103089a7ee40c386a`  
		Last Modified: Wed, 06 Mar 2024 04:19:16 GMT  
		Size: 14.1 MB (14139918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2a07a32d1f1de8910979cddaa096ffd43920729ab09fe53e65b1a7a2fabb2f`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7` - linux; s390x

```console
$ docker pull zookeeper@sha256:81b240cc056e57066068a6bcecbef3c477ace3bee318887de93fea7a1361c6b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101012169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b86b4e23c76fa7a66e652bd286ae496288035f13caa70b6daa15d29cd63567b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:49:48 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 07:49:48 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:49:52 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:49:53 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:49:53 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:49:53 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:49:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:49:53 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:49:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:54 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709144779947310d4dd84546d4c06e50bd2094a2dd06b28798a8bd28092c4858`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 14.1 MB (14139871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32854dcc8e115ff5be393dc5dccfd0c23f0cfb7ef7109fb7d80810198ab50170`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.7-jre-11`

```console
$ docker pull zookeeper@sha256:a8c3a559ab45b97c68fb063543308171ff19111211c6369a0fd95b09b1d935c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.7-jre-11` - linux; amd64

```console
$ docker pull zookeeper@sha256:492a1481c3507cee8bf6a7b7a953f132fa4626f6d15b6d4c2036cc1be9826e49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109174259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446078172ae870beb2b17c34fe7fb0d18843456ed567d8c7b55e6978c9236323`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:15 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Fri, 16 Feb 2024 04:43:15 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:20 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:20 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:20 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:20 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:20 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96877b3c6c46bb5d82eafbeaa6b5b7ec7472a5eb174c7463858986ab5ec48717`  
		Last Modified: Fri, 16 Feb 2024 04:44:30 GMT  
		Size: 14.1 MB (14139899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7499525ebd73bf924d9b2a1523cc9b876bb04740afa8c8d77ac4754a2ad15e`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7-jre-11` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:25e6c2a4099e8932c00c3fe02f8fad45c44a5ec30152cb1bfedbfe0309be98b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105299794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91a3cff40caca3f7f2f2f75b5e47557fc8ecad87ffee3a69a8e90ea68f127a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:12:32 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 12:12:32 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:12:37 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:12:37 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:12:37 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:12:37 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:12:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:12:38 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:12:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:38 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba37258a41e114a24b65baf1fae6f1d2e444db83fb2dd7e0b7decf72b18e51`  
		Last Modified: Wed, 06 Mar 2024 12:15:20 GMT  
		Size: 14.1 MB (14139929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf8ecad0e9a78a1c89aff19160500e54aa621a0c3bb493b42fe5ff51d59c6f`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7-jre-11` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:511547b95ed4f4923110a1b9bb75e3071fce2841fbae08f0fc08e520015528dc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111233909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df05f541ea22dea3f2afcd23c25f130cadcb926b1f214f5c37689e389e4c7add`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:16:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 04:16:32 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:16:40 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:16:41 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:16:42 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:16:43 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:16:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:16:44 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:16:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:46 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ceebe419d4baade36efb91807bde8faee0944e827ea24e103089a7ee40c386a`  
		Last Modified: Wed, 06 Mar 2024 04:19:16 GMT  
		Size: 14.1 MB (14139918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2a07a32d1f1de8910979cddaa096ffd43920729ab09fe53e65b1a7a2fabb2f`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7-jre-11` - linux; s390x

```console
$ docker pull zookeeper@sha256:81b240cc056e57066068a6bcecbef3c477ace3bee318887de93fea7a1361c6b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101012169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b86b4e23c76fa7a66e652bd286ae496288035f13caa70b6daa15d29cd63567b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:49:48 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 07:49:48 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:49:52 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:49:53 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:49:53 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:49:53 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:49:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:49:53 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:49:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:54 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709144779947310d4dd84546d4c06e50bd2094a2dd06b28798a8bd28092c4858`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 14.1 MB (14139871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32854dcc8e115ff5be393dc5dccfd0c23f0cfb7ef7109fb7d80810198ab50170`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.7-jre-17`

```console
$ docker pull zookeeper@sha256:b79aa63d1a7551d68b9c5607007876f19f3516059afb8ecf96d7bd61d95d71b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.7-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:e07c33157c6a890e71edd9e13ddeb2b39abaefe37360b2541673a6bbefed563d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113822656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c9bdb3c4818b36043a76e20831102a13a4a44a18837e9625627c7adf3a4fec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:40:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:40:28 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 01:40:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:41:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:41:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:41:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:42 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:49 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:50 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Fri, 16 Feb 2024 04:43:50 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:53 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:53 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:53 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:53 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:54 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:54 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3d8439525debaa2452083229854d3cfbf629833edbdd2a1750b5ab22c933f5`  
		Last Modified: Fri, 16 Feb 2024 04:45:12 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17439db14e422559cae0b662560c6631dc7aa8e684bb6323e92bc433e8fcbb`  
		Last Modified: Fri, 16 Feb 2024 04:45:13 GMT  
		Size: 4.6 MB (4607448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a02edf44fd7d73f94e7c24f9cbbdb14d231f6651346879514f25b78ec89742`  
		Last Modified: Fri, 16 Feb 2024 04:45:14 GMT  
		Size: 14.1 MB (14139849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc5edfb104b35b16975de0f3b5cb9c7b29169e115e88bb59f760888f2401cba`  
		Last Modified: Fri, 16 Feb 2024 04:45:12 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:339c3a978c8e1e18af286a1c59925d6cbe3bbf23a299bcec73e0094da4613123
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112552028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae112c0de2aec7d86112c10180c02a1df139f57694679eeec044fe316b78c04e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 04:04:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:04:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:04:08 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:57 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:13:58 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:14:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:14:03 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:14:03 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 12:14:03 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:14:07 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:14:07 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:14:07 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:14:07 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:14:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:14:07 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:14:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:14:07 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799297b6f9210d0b08ff588516d8ab6fe2169cdda6b76a0b5f854b6e76aec0ce`  
		Last Modified: Wed, 06 Mar 2024 04:08:04 GMT  
		Size: 18.9 MB (18857483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0f6cd036a6aa4998c7a9c375b0e7fb43615f3d03dfcb794b88cff90027fff7`  
		Last Modified: Wed, 06 Mar 2024 04:08:44 GMT  
		Size: 46.6 MB (46639407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30140b6dcdeba2a64a4d96bfde851abee456c368a15a215e1b86e3c0484bce`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13614e023aad4adadb99824ffb722959861646971b8c272a4eaf5b1fe098077e`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d091c818ec6a831dfc9715467492df06691587db22de40b4f0b2dcbf927b9`  
		Last Modified: Wed, 06 Mar 2024 12:15:59 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56f1e06395bcc4a843fd848fe18bbb42ad2defb19c646319686d52279e9fdc`  
		Last Modified: Wed, 06 Mar 2024 12:16:00 GMT  
		Size: 4.5 MB (4511047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5806b95be067018eaac3fd331c9f406efed7a8bfa2badf037aab279f0d503016`  
		Last Modified: Wed, 06 Mar 2024 12:16:01 GMT  
		Size: 14.1 MB (14139896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a3ad5f4a330b7f764baab2722499a32114dab365b57b71dc0dfcf1ca8411ac`  
		Last Modified: Wed, 06 Mar 2024 12:15:59 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:8b53e83843e26ad09ec00b9bac45709406f349de2d9bbed27f3859cbc1343b93
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120711357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8412c2bcceb7579908465e5e591793d044788ee657e6342564eba9adfcc3ed72`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:41:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:41:33 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 01:42:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:42:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:42:31 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:42:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:17:43 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:17:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:17:57 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:17:58 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 04:17:58 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:18:04 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:18:05 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:18:05 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:18:06 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:18:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:18:07 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:18:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:18:09 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0d16af6f61058996d0677e521dec0be40a28b566317297f06589f10c1d0be3`  
		Last Modified: Wed, 06 Mar 2024 01:47:33 GMT  
		Size: 18.7 MB (18724998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d47ebd5b078b4cc528e25716cbb14bc9ba058da7d77f221f0a953718682a83`  
		Last Modified: Wed, 06 Mar 2024 01:48:23 GMT  
		Size: 47.0 MB (47012835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92f5b11b6fe41ea9819334d8b551be6db95f2350513af1b8e59dee9f15abd06`  
		Last Modified: Wed, 06 Mar 2024 01:48:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96454b934f9891148d03497f07a6dc87d1b56a117b93bd0fde5f1782e3cb792c`  
		Last Modified: Wed, 06 Mar 2024 01:48:16 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11f0be4a1a4a5e8e84454ef57d0c8765daed8863ec1e7fda57b74131f4a9b9`  
		Last Modified: Wed, 06 Mar 2024 04:20:01 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640a5f8b36fe858fc3b1ee337dd69f6f7326ded72c11cee9fb92dbefc486aac8`  
		Last Modified: Wed, 06 Mar 2024 04:20:02 GMT  
		Size: 5.2 MB (5207345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10a54081c62c6f8d596c8f71300cfb258ed5e6e42d78aca1513be3203a37689`  
		Last Modified: Wed, 06 Mar 2024 04:20:04 GMT  
		Size: 14.1 MB (14139893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a20981be32f0c9e82ea60b91921342182a2fb38c4bf62b0dd70bf5bbe37a9`  
		Last Modified: Wed, 06 Mar 2024 04:20:01 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:a2ecb6a443638bd1b85c86e1c0cd5db55395625f5f45a39348acf61aa92dc436
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108288154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85751a731045d95a3245af8ba90b1d2aa15279552319b2f69ff0b5e1c5ce7cd6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:41:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:41:31 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 03:46:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:46:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:46:15 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:46:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:53:27 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:53:28 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:53:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:53:34 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:53:34 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 07:53:34 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:53:37 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:53:38 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:53:38 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:53:38 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:53:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:53:38 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:53:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:53:38 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ac9a901fa5c1ea7b49c5d68835040a39635587cbb48c866f523885955a0666`  
		Last Modified: Wed, 06 Mar 2024 03:57:40 GMT  
		Size: 17.3 MB (17258499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91cb809e488845124f75544e212468cdb11a2e0608029edad585d6ea2ddbe70`  
		Last Modified: Wed, 06 Mar 2024 03:58:18 GMT  
		Size: 43.8 MB (43765885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b377b22329c61226e8806deb31b4569750cb4f9731347151c457c0d07051ca92`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbd910585f6d3b1a94645b01af3e6f396694f423b57489a516bc47ee7f9df8f`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6a65cab54401d2fc7cd70c4cc5a2a176ff334b9a7a862fd2f8e7e0e45a83d`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05791b9ec4a138f25eb78ad28130353c915edc06a7a5a5edd418e26365f2636`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 4.5 MB (4483641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc064a5aa1afcd52bd73b815317ad7a15da8f5bbbbed1eff06769aecf7fd2512`  
		Last Modified: Wed, 06 Mar 2024 07:57:34 GMT  
		Size: 14.1 MB (14139817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ed509668f0724dbd74fcc85ecbd0a0d6d3fca55eb02a59fa1cc3f172d38085`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.7.2`

```console
$ docker pull zookeeper@sha256:a8c3a559ab45b97c68fb063543308171ff19111211c6369a0fd95b09b1d935c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.7.2` - linux; amd64

```console
$ docker pull zookeeper@sha256:492a1481c3507cee8bf6a7b7a953f132fa4626f6d15b6d4c2036cc1be9826e49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109174259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446078172ae870beb2b17c34fe7fb0d18843456ed567d8c7b55e6978c9236323`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:15 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Fri, 16 Feb 2024 04:43:15 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:20 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:20 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:20 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:20 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:20 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96877b3c6c46bb5d82eafbeaa6b5b7ec7472a5eb174c7463858986ab5ec48717`  
		Last Modified: Fri, 16 Feb 2024 04:44:30 GMT  
		Size: 14.1 MB (14139899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7499525ebd73bf924d9b2a1523cc9b876bb04740afa8c8d77ac4754a2ad15e`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7.2` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:25e6c2a4099e8932c00c3fe02f8fad45c44a5ec30152cb1bfedbfe0309be98b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105299794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91a3cff40caca3f7f2f2f75b5e47557fc8ecad87ffee3a69a8e90ea68f127a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:12:32 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 12:12:32 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:12:37 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:12:37 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:12:37 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:12:37 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:12:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:12:38 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:12:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:38 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba37258a41e114a24b65baf1fae6f1d2e444db83fb2dd7e0b7decf72b18e51`  
		Last Modified: Wed, 06 Mar 2024 12:15:20 GMT  
		Size: 14.1 MB (14139929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf8ecad0e9a78a1c89aff19160500e54aa621a0c3bb493b42fe5ff51d59c6f`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7.2` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:511547b95ed4f4923110a1b9bb75e3071fce2841fbae08f0fc08e520015528dc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111233909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df05f541ea22dea3f2afcd23c25f130cadcb926b1f214f5c37689e389e4c7add`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:16:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 04:16:32 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:16:40 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:16:41 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:16:42 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:16:43 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:16:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:16:44 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:16:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:46 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ceebe419d4baade36efb91807bde8faee0944e827ea24e103089a7ee40c386a`  
		Last Modified: Wed, 06 Mar 2024 04:19:16 GMT  
		Size: 14.1 MB (14139918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2a07a32d1f1de8910979cddaa096ffd43920729ab09fe53e65b1a7a2fabb2f`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7.2` - linux; s390x

```console
$ docker pull zookeeper@sha256:81b240cc056e57066068a6bcecbef3c477ace3bee318887de93fea7a1361c6b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101012169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b86b4e23c76fa7a66e652bd286ae496288035f13caa70b6daa15d29cd63567b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:49:48 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 07:49:48 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:49:52 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:49:53 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:49:53 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:49:53 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:49:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:49:53 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:49:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:54 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709144779947310d4dd84546d4c06e50bd2094a2dd06b28798a8bd28092c4858`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 14.1 MB (14139871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32854dcc8e115ff5be393dc5dccfd0c23f0cfb7ef7109fb7d80810198ab50170`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.7.2-jre-11`

```console
$ docker pull zookeeper@sha256:a8c3a559ab45b97c68fb063543308171ff19111211c6369a0fd95b09b1d935c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.7.2-jre-11` - linux; amd64

```console
$ docker pull zookeeper@sha256:492a1481c3507cee8bf6a7b7a953f132fa4626f6d15b6d4c2036cc1be9826e49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109174259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446078172ae870beb2b17c34fe7fb0d18843456ed567d8c7b55e6978c9236323`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:15 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Fri, 16 Feb 2024 04:43:15 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:20 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:20 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:20 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:20 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:20 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96877b3c6c46bb5d82eafbeaa6b5b7ec7472a5eb174c7463858986ab5ec48717`  
		Last Modified: Fri, 16 Feb 2024 04:44:30 GMT  
		Size: 14.1 MB (14139899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7499525ebd73bf924d9b2a1523cc9b876bb04740afa8c8d77ac4754a2ad15e`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7.2-jre-11` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:25e6c2a4099e8932c00c3fe02f8fad45c44a5ec30152cb1bfedbfe0309be98b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105299794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91a3cff40caca3f7f2f2f75b5e47557fc8ecad87ffee3a69a8e90ea68f127a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:12:32 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 12:12:32 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:12:37 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:12:37 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:12:37 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:12:37 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:12:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:12:38 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:12:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:38 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba37258a41e114a24b65baf1fae6f1d2e444db83fb2dd7e0b7decf72b18e51`  
		Last Modified: Wed, 06 Mar 2024 12:15:20 GMT  
		Size: 14.1 MB (14139929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf8ecad0e9a78a1c89aff19160500e54aa621a0c3bb493b42fe5ff51d59c6f`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7.2-jre-11` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:511547b95ed4f4923110a1b9bb75e3071fce2841fbae08f0fc08e520015528dc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111233909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df05f541ea22dea3f2afcd23c25f130cadcb926b1f214f5c37689e389e4c7add`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:16:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 04:16:32 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:16:40 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:16:41 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:16:42 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:16:43 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:16:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:16:44 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:16:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:46 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ceebe419d4baade36efb91807bde8faee0944e827ea24e103089a7ee40c386a`  
		Last Modified: Wed, 06 Mar 2024 04:19:16 GMT  
		Size: 14.1 MB (14139918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2a07a32d1f1de8910979cddaa096ffd43920729ab09fe53e65b1a7a2fabb2f`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7.2-jre-11` - linux; s390x

```console
$ docker pull zookeeper@sha256:81b240cc056e57066068a6bcecbef3c477ace3bee318887de93fea7a1361c6b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101012169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b86b4e23c76fa7a66e652bd286ae496288035f13caa70b6daa15d29cd63567b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:49:48 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 07:49:48 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:49:52 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:49:53 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:49:53 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:49:53 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:49:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:49:53 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:49:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:54 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709144779947310d4dd84546d4c06e50bd2094a2dd06b28798a8bd28092c4858`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 14.1 MB (14139871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32854dcc8e115ff5be393dc5dccfd0c23f0cfb7ef7109fb7d80810198ab50170`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.7.2-jre-17`

```console
$ docker pull zookeeper@sha256:b79aa63d1a7551d68b9c5607007876f19f3516059afb8ecf96d7bd61d95d71b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.7.2-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:e07c33157c6a890e71edd9e13ddeb2b39abaefe37360b2541673a6bbefed563d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113822656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c9bdb3c4818b36043a76e20831102a13a4a44a18837e9625627c7adf3a4fec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:40:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:40:28 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 01:40:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:41:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:41:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:41:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:42 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:49 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:50 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Fri, 16 Feb 2024 04:43:50 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:53 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:53 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Fri, 16 Feb 2024 04:43:53 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:53 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:54 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:54 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3d8439525debaa2452083229854d3cfbf629833edbdd2a1750b5ab22c933f5`  
		Last Modified: Fri, 16 Feb 2024 04:45:12 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17439db14e422559cae0b662560c6631dc7aa8e684bb6323e92bc433e8fcbb`  
		Last Modified: Fri, 16 Feb 2024 04:45:13 GMT  
		Size: 4.6 MB (4607448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a02edf44fd7d73f94e7c24f9cbbdb14d231f6651346879514f25b78ec89742`  
		Last Modified: Fri, 16 Feb 2024 04:45:14 GMT  
		Size: 14.1 MB (14139849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc5edfb104b35b16975de0f3b5cb9c7b29169e115e88bb59f760888f2401cba`  
		Last Modified: Fri, 16 Feb 2024 04:45:12 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7.2-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:339c3a978c8e1e18af286a1c59925d6cbe3bbf23a299bcec73e0094da4613123
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112552028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae112c0de2aec7d86112c10180c02a1df139f57694679eeec044fe316b78c04e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 04:04:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:04:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:04:08 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:57 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:13:58 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:14:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:14:03 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:14:03 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 12:14:03 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:14:07 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:14:07 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 12:14:07 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:14:07 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:14:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:14:07 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:14:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:14:07 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799297b6f9210d0b08ff588516d8ab6fe2169cdda6b76a0b5f854b6e76aec0ce`  
		Last Modified: Wed, 06 Mar 2024 04:08:04 GMT  
		Size: 18.9 MB (18857483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0f6cd036a6aa4998c7a9c375b0e7fb43615f3d03dfcb794b88cff90027fff7`  
		Last Modified: Wed, 06 Mar 2024 04:08:44 GMT  
		Size: 46.6 MB (46639407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30140b6dcdeba2a64a4d96bfde851abee456c368a15a215e1b86e3c0484bce`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13614e023aad4adadb99824ffb722959861646971b8c272a4eaf5b1fe098077e`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d091c818ec6a831dfc9715467492df06691587db22de40b4f0b2dcbf927b9`  
		Last Modified: Wed, 06 Mar 2024 12:15:59 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56f1e06395bcc4a843fd848fe18bbb42ad2defb19c646319686d52279e9fdc`  
		Last Modified: Wed, 06 Mar 2024 12:16:00 GMT  
		Size: 4.5 MB (4511047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5806b95be067018eaac3fd331c9f406efed7a8bfa2badf037aab279f0d503016`  
		Last Modified: Wed, 06 Mar 2024 12:16:01 GMT  
		Size: 14.1 MB (14139896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a3ad5f4a330b7f764baab2722499a32114dab365b57b71dc0dfcf1ca8411ac`  
		Last Modified: Wed, 06 Mar 2024 12:15:59 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7.2-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:8b53e83843e26ad09ec00b9bac45709406f349de2d9bbed27f3859cbc1343b93
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120711357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8412c2bcceb7579908465e5e591793d044788ee657e6342564eba9adfcc3ed72`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:41:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:41:33 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 01:42:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:42:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:42:31 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:42:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:17:43 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:17:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:17:57 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:17:58 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 04:17:58 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:18:04 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:18:05 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 04:18:05 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:18:06 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:18:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:18:07 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:18:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:18:09 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0d16af6f61058996d0677e521dec0be40a28b566317297f06589f10c1d0be3`  
		Last Modified: Wed, 06 Mar 2024 01:47:33 GMT  
		Size: 18.7 MB (18724998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d47ebd5b078b4cc528e25716cbb14bc9ba058da7d77f221f0a953718682a83`  
		Last Modified: Wed, 06 Mar 2024 01:48:23 GMT  
		Size: 47.0 MB (47012835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92f5b11b6fe41ea9819334d8b551be6db95f2350513af1b8e59dee9f15abd06`  
		Last Modified: Wed, 06 Mar 2024 01:48:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96454b934f9891148d03497f07a6dc87d1b56a117b93bd0fde5f1782e3cb792c`  
		Last Modified: Wed, 06 Mar 2024 01:48:16 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11f0be4a1a4a5e8e84454ef57d0c8765daed8863ec1e7fda57b74131f4a9b9`  
		Last Modified: Wed, 06 Mar 2024 04:20:01 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640a5f8b36fe858fc3b1ee337dd69f6f7326ded72c11cee9fb92dbefc486aac8`  
		Last Modified: Wed, 06 Mar 2024 04:20:02 GMT  
		Size: 5.2 MB (5207345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10a54081c62c6f8d596c8f71300cfb258ed5e6e42d78aca1513be3203a37689`  
		Last Modified: Wed, 06 Mar 2024 04:20:04 GMT  
		Size: 14.1 MB (14139893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a20981be32f0c9e82ea60b91921342182a2fb38c4bf62b0dd70bf5bbe37a9`  
		Last Modified: Wed, 06 Mar 2024 04:20:01 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.7.2-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:a2ecb6a443638bd1b85c86e1c0cd5db55395625f5f45a39348acf61aa92dc436
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108288154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85751a731045d95a3245af8ba90b1d2aa15279552319b2f69ff0b5e1c5ce7cd6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:41:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:41:31 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 03:46:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:46:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:46:15 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:46:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:53:27 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:53:28 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:53:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:53:34 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:53:34 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Wed, 06 Mar 2024 07:53:34 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:53:37 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.7.2-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:53:38 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Wed, 06 Mar 2024 07:53:38 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:53:38 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:53:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:53:38 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:53:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:53:38 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ac9a901fa5c1ea7b49c5d68835040a39635587cbb48c866f523885955a0666`  
		Last Modified: Wed, 06 Mar 2024 03:57:40 GMT  
		Size: 17.3 MB (17258499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91cb809e488845124f75544e212468cdb11a2e0608029edad585d6ea2ddbe70`  
		Last Modified: Wed, 06 Mar 2024 03:58:18 GMT  
		Size: 43.8 MB (43765885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b377b22329c61226e8806deb31b4569750cb4f9731347151c457c0d07051ca92`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbd910585f6d3b1a94645b01af3e6f396694f423b57489a516bc47ee7f9df8f`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6a65cab54401d2fc7cd70c4cc5a2a176ff334b9a7a862fd2f8e7e0e45a83d`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05791b9ec4a138f25eb78ad28130353c915edc06a7a5a5edd418e26365f2636`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 4.5 MB (4483641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc064a5aa1afcd52bd73b815317ad7a15da8f5bbbbed1eff06769aecf7fd2512`  
		Last Modified: Wed, 06 Mar 2024 07:57:34 GMT  
		Size: 14.1 MB (14139817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ed509668f0724dbd74fcc85ecbd0a0d6d3fca55eb02a59fa1cc3f172d38085`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.8`

```console
$ docker pull zookeeper@sha256:14ec30defa249d09486993029bbd8cce24b48cf4a52a8488bf318bc2e8997ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.8` - linux; amd64

```console
$ docker pull zookeeper@sha256:0d9333bbc3baf2886c804e8def57511d6c4312b780697e3cfb8454b33dd8ab77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109843382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1530b1a1b069ff592bdc9aa1c2060ad0424ce1f29f645e51788dacb9a15086a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:24 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Fri, 16 Feb 2024 04:43:24 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:43:27 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:28 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:43:28 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:28 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:28 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:28 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfc0b2568b81b39c4bcf5b5ff778468133835543d648338ce67b3b25498434a`  
		Last Modified: Fri, 16 Feb 2024 04:44:44 GMT  
		Size: 14.8 MB (14809022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3079543e37e64eba744430bf7bfa6e5806a74feb7bafbaee37b78f5b88383a01`  
		Last Modified: Fri, 16 Feb 2024 04:44:42 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:71e0da69c35a1bbe0dab0cbb546327b2bc29f431d5f41588cc7bb114aa7617d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105968923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cced327daa33d098ae48f44e74ae5d3236f2e599adb2c9ff210ada42faf9bc1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:12:40 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 12:12:40 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:13:35 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:13:36 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:13:36 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:13:36 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:13:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:13:36 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:13:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9f817db3576ff4ce99fe019cf058d61caeb50e4423e7a80980e5535a27b03`  
		Last Modified: Wed, 06 Mar 2024 12:15:34 GMT  
		Size: 14.8 MB (14809060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cf8676c631faa61387bade3acdd3e51a065172ee6b6a105b07b6a180feff48`  
		Last Modified: Wed, 06 Mar 2024 12:15:32 GMT  
		Size: 773.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:dd09c540e1d5b0431906d45dce10055e198448a55ac4bfbc5696cef3f9370d5a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111903036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cde499c0dfad4a3526ab271ba49c34362658a03f3b13512a7bf9f7d41b57d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:16:53 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 04:16:53 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:17:16 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:17:17 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:17:18 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:17:18 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:17:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:17:19 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:17:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d00d3bcafb86fa4d41a57a211581e1f63d1d4351badf2944ac9b9e4be0a19e`  
		Last Modified: Wed, 06 Mar 2024 04:19:32 GMT  
		Size: 14.8 MB (14809045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e769ab8196648bb3f320ef9a3a04e33e6f7d7990bbeb5ca759a0c429c2897704`  
		Last Modified: Wed, 06 Mar 2024 04:19:30 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8` - linux; s390x

```console
$ docker pull zookeeper@sha256:d6d04923d09b8d4c30943bf3c179d70325340b6dcfda5acdc5eca4feebc8ed60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101680969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1674d09d93253a2bcc8b3797ef8cf872bc735dbf0f08ca63c757fb5d15b02178`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:50:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 07:50:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:50:57 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:50:57 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:50:57 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:50:57 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:50:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:50:58 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:50:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:50:58 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04252b307e161f92bdb8ffe4c00dfa7994c15d9ad6e2f1503375fc79de4ab4c`  
		Last Modified: Wed, 06 Mar 2024 07:57:16 GMT  
		Size: 14.8 MB (14808671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428a6e2ab628b12365b331b4dd204a4cf1c5ddf530c10985a3159b1d8e28e3fb`  
		Last Modified: Wed, 06 Mar 2024 07:57:15 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.8-jre-11`

```console
$ docker pull zookeeper@sha256:14ec30defa249d09486993029bbd8cce24b48cf4a52a8488bf318bc2e8997ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.8-jre-11` - linux; amd64

```console
$ docker pull zookeeper@sha256:0d9333bbc3baf2886c804e8def57511d6c4312b780697e3cfb8454b33dd8ab77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109843382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1530b1a1b069ff592bdc9aa1c2060ad0424ce1f29f645e51788dacb9a15086a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:24 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Fri, 16 Feb 2024 04:43:24 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:43:27 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:28 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:43:28 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:28 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:28 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:28 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfc0b2568b81b39c4bcf5b5ff778468133835543d648338ce67b3b25498434a`  
		Last Modified: Fri, 16 Feb 2024 04:44:44 GMT  
		Size: 14.8 MB (14809022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3079543e37e64eba744430bf7bfa6e5806a74feb7bafbaee37b78f5b88383a01`  
		Last Modified: Fri, 16 Feb 2024 04:44:42 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8-jre-11` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:71e0da69c35a1bbe0dab0cbb546327b2bc29f431d5f41588cc7bb114aa7617d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105968923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cced327daa33d098ae48f44e74ae5d3236f2e599adb2c9ff210ada42faf9bc1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:12:40 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 12:12:40 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:13:35 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:13:36 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:13:36 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:13:36 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:13:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:13:36 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:13:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9f817db3576ff4ce99fe019cf058d61caeb50e4423e7a80980e5535a27b03`  
		Last Modified: Wed, 06 Mar 2024 12:15:34 GMT  
		Size: 14.8 MB (14809060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cf8676c631faa61387bade3acdd3e51a065172ee6b6a105b07b6a180feff48`  
		Last Modified: Wed, 06 Mar 2024 12:15:32 GMT  
		Size: 773.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8-jre-11` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:dd09c540e1d5b0431906d45dce10055e198448a55ac4bfbc5696cef3f9370d5a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111903036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cde499c0dfad4a3526ab271ba49c34362658a03f3b13512a7bf9f7d41b57d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:16:53 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 04:16:53 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:17:16 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:17:17 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:17:18 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:17:18 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:17:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:17:19 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:17:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d00d3bcafb86fa4d41a57a211581e1f63d1d4351badf2944ac9b9e4be0a19e`  
		Last Modified: Wed, 06 Mar 2024 04:19:32 GMT  
		Size: 14.8 MB (14809045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e769ab8196648bb3f320ef9a3a04e33e6f7d7990bbeb5ca759a0c429c2897704`  
		Last Modified: Wed, 06 Mar 2024 04:19:30 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8-jre-11` - linux; s390x

```console
$ docker pull zookeeper@sha256:d6d04923d09b8d4c30943bf3c179d70325340b6dcfda5acdc5eca4feebc8ed60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101680969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1674d09d93253a2bcc8b3797ef8cf872bc735dbf0f08ca63c757fb5d15b02178`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:50:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 07:50:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:50:57 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:50:57 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:50:57 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:50:57 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:50:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:50:58 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:50:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:50:58 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04252b307e161f92bdb8ffe4c00dfa7994c15d9ad6e2f1503375fc79de4ab4c`  
		Last Modified: Wed, 06 Mar 2024 07:57:16 GMT  
		Size: 14.8 MB (14808671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428a6e2ab628b12365b331b4dd204a4cf1c5ddf530c10985a3159b1d8e28e3fb`  
		Last Modified: Wed, 06 Mar 2024 07:57:15 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.8-jre-17`

```console
$ docker pull zookeeper@sha256:911fd785e568fe0953a50d0782077d003adc1e7ddfda7b9c9143bccf0927857f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.8-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:d8fe2ee942306549827514c7abea60b8e6eabf23143c13935dd2e6abd1aa0c28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114491814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d7ab8f316db824fd0045055c830aa73d0ed486ce914d403044fe0f2296a873`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:40:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:40:28 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 01:40:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:41:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:41:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:41:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:42 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:49 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:59 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Fri, 16 Feb 2024 04:43:59 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:44:02 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:44:03 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:44:03 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:44:03 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:44:03 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:44:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:44:03 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3d8439525debaa2452083229854d3cfbf629833edbdd2a1750b5ab22c933f5`  
		Last Modified: Fri, 16 Feb 2024 04:45:12 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17439db14e422559cae0b662560c6631dc7aa8e684bb6323e92bc433e8fcbb`  
		Last Modified: Fri, 16 Feb 2024 04:45:13 GMT  
		Size: 4.6 MB (4607448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdf74831513c659b3a2edced1b763df9916f9b16e808bc9affcea8931732227`  
		Last Modified: Fri, 16 Feb 2024 04:45:23 GMT  
		Size: 14.8 MB (14809008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa22b2664c9968a5799654c8b117c9c26a658cab3acf63ea587c3b20322f571`  
		Last Modified: Fri, 16 Feb 2024 04:45:22 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:e98c8c593ab9500ab6e54b99ab12bcc5098b0290bfe2c295bfcfc71943734382
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113221119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249992786d91e5e3614669567af0da41aa40b978b211490493908f3f2fea8e62`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 04:04:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:04:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:04:08 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:57 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:13:58 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:14:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:14:03 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:14:11 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 12:14:11 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:14:57 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:14:57 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:14:57 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:14:57 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:14:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:14:57 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:14:57 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799297b6f9210d0b08ff588516d8ab6fe2169cdda6b76a0b5f854b6e76aec0ce`  
		Last Modified: Wed, 06 Mar 2024 04:08:04 GMT  
		Size: 18.9 MB (18857483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0f6cd036a6aa4998c7a9c375b0e7fb43615f3d03dfcb794b88cff90027fff7`  
		Last Modified: Wed, 06 Mar 2024 04:08:44 GMT  
		Size: 46.6 MB (46639407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30140b6dcdeba2a64a4d96bfde851abee456c368a15a215e1b86e3c0484bce`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13614e023aad4adadb99824ffb722959861646971b8c272a4eaf5b1fe098077e`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d091c818ec6a831dfc9715467492df06691587db22de40b4f0b2dcbf927b9`  
		Last Modified: Wed, 06 Mar 2024 12:15:59 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56f1e06395bcc4a843fd848fe18bbb42ad2defb19c646319686d52279e9fdc`  
		Last Modified: Wed, 06 Mar 2024 12:16:00 GMT  
		Size: 4.5 MB (4511047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d210fbdac8298bb8b3f3302dad170ed56ea9b840c6457a15ed0f2446bb9c57a3`  
		Last Modified: Wed, 06 Mar 2024 12:16:10 GMT  
		Size: 14.8 MB (14808987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6782d55a23c7a0b983fc06611cfa70945419315d71f7e786d25bde9ca1e2ffd`  
		Last Modified: Wed, 06 Mar 2024 12:16:09 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:27d19243526c01b9c672a817edee938710afe1e361eab46da9f20d8951c1b665
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121380485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724e41ac13d4b1a187fbc708a056532568526d8dfc902724e45cdaf9b6956095`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:41:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:41:33 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 01:42:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:42:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:42:31 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:42:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:17:43 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:17:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:17:57 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:18:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 04:18:18 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:18:30 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:18:32 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:18:32 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:18:32 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:18:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:18:33 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:18:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:18:35 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0d16af6f61058996d0677e521dec0be40a28b566317297f06589f10c1d0be3`  
		Last Modified: Wed, 06 Mar 2024 01:47:33 GMT  
		Size: 18.7 MB (18724998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d47ebd5b078b4cc528e25716cbb14bc9ba058da7d77f221f0a953718682a83`  
		Last Modified: Wed, 06 Mar 2024 01:48:23 GMT  
		Size: 47.0 MB (47012835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92f5b11b6fe41ea9819334d8b551be6db95f2350513af1b8e59dee9f15abd06`  
		Last Modified: Wed, 06 Mar 2024 01:48:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96454b934f9891148d03497f07a6dc87d1b56a117b93bd0fde5f1782e3cb792c`  
		Last Modified: Wed, 06 Mar 2024 01:48:16 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11f0be4a1a4a5e8e84454ef57d0c8765daed8863ec1e7fda57b74131f4a9b9`  
		Last Modified: Wed, 06 Mar 2024 04:20:01 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640a5f8b36fe858fc3b1ee337dd69f6f7326ded72c11cee9fb92dbefc486aac8`  
		Last Modified: Wed, 06 Mar 2024 04:20:02 GMT  
		Size: 5.2 MB (5207345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44c4eec23de98c38333510ce3cca94be89ed74740e564894aa5ab4ade516dde`  
		Last Modified: Wed, 06 Mar 2024 04:20:15 GMT  
		Size: 14.8 MB (14809021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f0db49457be88af863e37e1d960fdc7e6bc8548db3611704df92d97ce4bca9`  
		Last Modified: Wed, 06 Mar 2024 04:20:13 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:c0107803bf79a9daa9c682ea5876192afef982b5bf47c5d165c26e67e6169e9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108957362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754d842a39b8b8684804017c1fe97ec94f9286b05f5679706d60100cdcb5f0a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:41:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:41:31 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 03:46:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:46:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:46:15 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:46:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:53:27 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:53:28 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:53:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:53:34 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:54:43 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 07:54:43 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:54:47 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:54:48 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:54:48 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:54:48 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:54:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:54:49 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:54:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:54:49 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ac9a901fa5c1ea7b49c5d68835040a39635587cbb48c866f523885955a0666`  
		Last Modified: Wed, 06 Mar 2024 03:57:40 GMT  
		Size: 17.3 MB (17258499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91cb809e488845124f75544e212468cdb11a2e0608029edad585d6ea2ddbe70`  
		Last Modified: Wed, 06 Mar 2024 03:58:18 GMT  
		Size: 43.8 MB (43765885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b377b22329c61226e8806deb31b4569750cb4f9731347151c457c0d07051ca92`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbd910585f6d3b1a94645b01af3e6f396694f423b57489a516bc47ee7f9df8f`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6a65cab54401d2fc7cd70c4cc5a2a176ff334b9a7a862fd2f8e7e0e45a83d`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05791b9ec4a138f25eb78ad28130353c915edc06a7a5a5edd418e26365f2636`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 4.5 MB (4483641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cbdbc828ec7213e079874bc79f31faab34039fd9562a4ef32ab96da180441f`  
		Last Modified: Wed, 06 Mar 2024 07:57:41 GMT  
		Size: 14.8 MB (14809025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51721c1aabb28007172607786d12ce8ffebabb95dcf135ff59706b853315dea`  
		Last Modified: Wed, 06 Mar 2024 07:57:40 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.8.3`

```console
$ docker pull zookeeper@sha256:14ec30defa249d09486993029bbd8cce24b48cf4a52a8488bf318bc2e8997ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.8.3` - linux; amd64

```console
$ docker pull zookeeper@sha256:0d9333bbc3baf2886c804e8def57511d6c4312b780697e3cfb8454b33dd8ab77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109843382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1530b1a1b069ff592bdc9aa1c2060ad0424ce1f29f645e51788dacb9a15086a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:24 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Fri, 16 Feb 2024 04:43:24 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:43:27 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:28 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:43:28 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:28 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:28 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:28 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfc0b2568b81b39c4bcf5b5ff778468133835543d648338ce67b3b25498434a`  
		Last Modified: Fri, 16 Feb 2024 04:44:44 GMT  
		Size: 14.8 MB (14809022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3079543e37e64eba744430bf7bfa6e5806a74feb7bafbaee37b78f5b88383a01`  
		Last Modified: Fri, 16 Feb 2024 04:44:42 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8.3` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:71e0da69c35a1bbe0dab0cbb546327b2bc29f431d5f41588cc7bb114aa7617d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105968923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cced327daa33d098ae48f44e74ae5d3236f2e599adb2c9ff210ada42faf9bc1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:12:40 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 12:12:40 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:13:35 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:13:36 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:13:36 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:13:36 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:13:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:13:36 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:13:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9f817db3576ff4ce99fe019cf058d61caeb50e4423e7a80980e5535a27b03`  
		Last Modified: Wed, 06 Mar 2024 12:15:34 GMT  
		Size: 14.8 MB (14809060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cf8676c631faa61387bade3acdd3e51a065172ee6b6a105b07b6a180feff48`  
		Last Modified: Wed, 06 Mar 2024 12:15:32 GMT  
		Size: 773.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8.3` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:dd09c540e1d5b0431906d45dce10055e198448a55ac4bfbc5696cef3f9370d5a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111903036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cde499c0dfad4a3526ab271ba49c34362658a03f3b13512a7bf9f7d41b57d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:16:53 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 04:16:53 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:17:16 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:17:17 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:17:18 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:17:18 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:17:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:17:19 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:17:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d00d3bcafb86fa4d41a57a211581e1f63d1d4351badf2944ac9b9e4be0a19e`  
		Last Modified: Wed, 06 Mar 2024 04:19:32 GMT  
		Size: 14.8 MB (14809045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e769ab8196648bb3f320ef9a3a04e33e6f7d7990bbeb5ca759a0c429c2897704`  
		Last Modified: Wed, 06 Mar 2024 04:19:30 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8.3` - linux; s390x

```console
$ docker pull zookeeper@sha256:d6d04923d09b8d4c30943bf3c179d70325340b6dcfda5acdc5eca4feebc8ed60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101680969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1674d09d93253a2bcc8b3797ef8cf872bc735dbf0f08ca63c757fb5d15b02178`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:50:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 07:50:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:50:57 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:50:57 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:50:57 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:50:57 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:50:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:50:58 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:50:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:50:58 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04252b307e161f92bdb8ffe4c00dfa7994c15d9ad6e2f1503375fc79de4ab4c`  
		Last Modified: Wed, 06 Mar 2024 07:57:16 GMT  
		Size: 14.8 MB (14808671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428a6e2ab628b12365b331b4dd204a4cf1c5ddf530c10985a3159b1d8e28e3fb`  
		Last Modified: Wed, 06 Mar 2024 07:57:15 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.8.3-jre-11`

```console
$ docker pull zookeeper@sha256:14ec30defa249d09486993029bbd8cce24b48cf4a52a8488bf318bc2e8997ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.8.3-jre-11` - linux; amd64

```console
$ docker pull zookeeper@sha256:0d9333bbc3baf2886c804e8def57511d6c4312b780697e3cfb8454b33dd8ab77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109843382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1530b1a1b069ff592bdc9aa1c2060ad0424ce1f29f645e51788dacb9a15086a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:24 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Fri, 16 Feb 2024 04:43:24 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:43:27 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:28 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:43:28 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:28 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:28 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:28 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfc0b2568b81b39c4bcf5b5ff778468133835543d648338ce67b3b25498434a`  
		Last Modified: Fri, 16 Feb 2024 04:44:44 GMT  
		Size: 14.8 MB (14809022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3079543e37e64eba744430bf7bfa6e5806a74feb7bafbaee37b78f5b88383a01`  
		Last Modified: Fri, 16 Feb 2024 04:44:42 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8.3-jre-11` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:71e0da69c35a1bbe0dab0cbb546327b2bc29f431d5f41588cc7bb114aa7617d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105968923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cced327daa33d098ae48f44e74ae5d3236f2e599adb2c9ff210ada42faf9bc1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:12:40 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 12:12:40 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:13:35 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:13:36 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:13:36 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:13:36 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:13:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:13:36 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:13:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9f817db3576ff4ce99fe019cf058d61caeb50e4423e7a80980e5535a27b03`  
		Last Modified: Wed, 06 Mar 2024 12:15:34 GMT  
		Size: 14.8 MB (14809060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cf8676c631faa61387bade3acdd3e51a065172ee6b6a105b07b6a180feff48`  
		Last Modified: Wed, 06 Mar 2024 12:15:32 GMT  
		Size: 773.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8.3-jre-11` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:dd09c540e1d5b0431906d45dce10055e198448a55ac4bfbc5696cef3f9370d5a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111903036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cde499c0dfad4a3526ab271ba49c34362658a03f3b13512a7bf9f7d41b57d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:16:53 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 04:16:53 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:17:16 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:17:17 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:17:18 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:17:18 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:17:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:17:19 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:17:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d00d3bcafb86fa4d41a57a211581e1f63d1d4351badf2944ac9b9e4be0a19e`  
		Last Modified: Wed, 06 Mar 2024 04:19:32 GMT  
		Size: 14.8 MB (14809045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e769ab8196648bb3f320ef9a3a04e33e6f7d7990bbeb5ca759a0c429c2897704`  
		Last Modified: Wed, 06 Mar 2024 04:19:30 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8.3-jre-11` - linux; s390x

```console
$ docker pull zookeeper@sha256:d6d04923d09b8d4c30943bf3c179d70325340b6dcfda5acdc5eca4feebc8ed60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101680969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1674d09d93253a2bcc8b3797ef8cf872bc735dbf0f08ca63c757fb5d15b02178`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:50:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 07:50:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:50:57 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:50:57 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:50:57 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:50:57 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:50:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:50:58 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:50:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:50:58 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04252b307e161f92bdb8ffe4c00dfa7994c15d9ad6e2f1503375fc79de4ab4c`  
		Last Modified: Wed, 06 Mar 2024 07:57:16 GMT  
		Size: 14.8 MB (14808671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428a6e2ab628b12365b331b4dd204a4cf1c5ddf530c10985a3159b1d8e28e3fb`  
		Last Modified: Wed, 06 Mar 2024 07:57:15 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.8.3-jre-17`

```console
$ docker pull zookeeper@sha256:911fd785e568fe0953a50d0782077d003adc1e7ddfda7b9c9143bccf0927857f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.8.3-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:d8fe2ee942306549827514c7abea60b8e6eabf23143c13935dd2e6abd1aa0c28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114491814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d7ab8f316db824fd0045055c830aa73d0ed486ce914d403044fe0f2296a873`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:40:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:40:28 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 01:40:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:41:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:41:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:41:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:42 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:49 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:59 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Fri, 16 Feb 2024 04:43:59 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:44:02 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:44:03 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Fri, 16 Feb 2024 04:44:03 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:44:03 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:44:03 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:44:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:44:03 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3d8439525debaa2452083229854d3cfbf629833edbdd2a1750b5ab22c933f5`  
		Last Modified: Fri, 16 Feb 2024 04:45:12 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17439db14e422559cae0b662560c6631dc7aa8e684bb6323e92bc433e8fcbb`  
		Last Modified: Fri, 16 Feb 2024 04:45:13 GMT  
		Size: 4.6 MB (4607448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdf74831513c659b3a2edced1b763df9916f9b16e808bc9affcea8931732227`  
		Last Modified: Fri, 16 Feb 2024 04:45:23 GMT  
		Size: 14.8 MB (14809008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa22b2664c9968a5799654c8b117c9c26a658cab3acf63ea587c3b20322f571`  
		Last Modified: Fri, 16 Feb 2024 04:45:22 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8.3-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:e98c8c593ab9500ab6e54b99ab12bcc5098b0290bfe2c295bfcfc71943734382
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113221119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249992786d91e5e3614669567af0da41aa40b978b211490493908f3f2fea8e62`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 04:04:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:04:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:04:08 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:57 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:13:58 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:14:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:14:03 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:14:11 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 12:14:11 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:14:57 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:14:57 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 12:14:57 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:14:57 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:14:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:14:57 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:14:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:14:57 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799297b6f9210d0b08ff588516d8ab6fe2169cdda6b76a0b5f854b6e76aec0ce`  
		Last Modified: Wed, 06 Mar 2024 04:08:04 GMT  
		Size: 18.9 MB (18857483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0f6cd036a6aa4998c7a9c375b0e7fb43615f3d03dfcb794b88cff90027fff7`  
		Last Modified: Wed, 06 Mar 2024 04:08:44 GMT  
		Size: 46.6 MB (46639407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30140b6dcdeba2a64a4d96bfde851abee456c368a15a215e1b86e3c0484bce`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13614e023aad4adadb99824ffb722959861646971b8c272a4eaf5b1fe098077e`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d091c818ec6a831dfc9715467492df06691587db22de40b4f0b2dcbf927b9`  
		Last Modified: Wed, 06 Mar 2024 12:15:59 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56f1e06395bcc4a843fd848fe18bbb42ad2defb19c646319686d52279e9fdc`  
		Last Modified: Wed, 06 Mar 2024 12:16:00 GMT  
		Size: 4.5 MB (4511047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d210fbdac8298bb8b3f3302dad170ed56ea9b840c6457a15ed0f2446bb9c57a3`  
		Last Modified: Wed, 06 Mar 2024 12:16:10 GMT  
		Size: 14.8 MB (14808987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6782d55a23c7a0b983fc06611cfa70945419315d71f7e786d25bde9ca1e2ffd`  
		Last Modified: Wed, 06 Mar 2024 12:16:09 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8.3-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:27d19243526c01b9c672a817edee938710afe1e361eab46da9f20d8951c1b665
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121380485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724e41ac13d4b1a187fbc708a056532568526d8dfc902724e45cdaf9b6956095`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:41:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:41:33 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 01:42:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:42:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:42:31 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:42:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:17:43 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:17:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:17:57 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:18:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 04:18:18 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:18:30 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:18:32 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 04:18:32 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:18:32 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:18:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:18:33 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:18:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:18:35 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0d16af6f61058996d0677e521dec0be40a28b566317297f06589f10c1d0be3`  
		Last Modified: Wed, 06 Mar 2024 01:47:33 GMT  
		Size: 18.7 MB (18724998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d47ebd5b078b4cc528e25716cbb14bc9ba058da7d77f221f0a953718682a83`  
		Last Modified: Wed, 06 Mar 2024 01:48:23 GMT  
		Size: 47.0 MB (47012835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92f5b11b6fe41ea9819334d8b551be6db95f2350513af1b8e59dee9f15abd06`  
		Last Modified: Wed, 06 Mar 2024 01:48:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96454b934f9891148d03497f07a6dc87d1b56a117b93bd0fde5f1782e3cb792c`  
		Last Modified: Wed, 06 Mar 2024 01:48:16 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11f0be4a1a4a5e8e84454ef57d0c8765daed8863ec1e7fda57b74131f4a9b9`  
		Last Modified: Wed, 06 Mar 2024 04:20:01 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640a5f8b36fe858fc3b1ee337dd69f6f7326ded72c11cee9fb92dbefc486aac8`  
		Last Modified: Wed, 06 Mar 2024 04:20:02 GMT  
		Size: 5.2 MB (5207345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44c4eec23de98c38333510ce3cca94be89ed74740e564894aa5ab4ade516dde`  
		Last Modified: Wed, 06 Mar 2024 04:20:15 GMT  
		Size: 14.8 MB (14809021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f0db49457be88af863e37e1d960fdc7e6bc8548db3611704df92d97ce4bca9`  
		Last Modified: Wed, 06 Mar 2024 04:20:13 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.8.3-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:c0107803bf79a9daa9c682ea5876192afef982b5bf47c5d165c26e67e6169e9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108957362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754d842a39b8b8684804017c1fe97ec94f9286b05f5679706d60100cdcb5f0a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:41:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:41:31 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 03:46:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:46:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:46:15 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:46:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:53:27 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:53:28 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:53:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:53:34 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:54:43 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.3
# Wed, 06 Mar 2024 07:54:43 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:54:47 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.8.3-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.3
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:54:48 GMT
WORKDIR /apache-zookeeper-3.8.3-bin
# Wed, 06 Mar 2024 07:54:48 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:54:48 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:54:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.3-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:54:49 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:54:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:54:49 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ac9a901fa5c1ea7b49c5d68835040a39635587cbb48c866f523885955a0666`  
		Last Modified: Wed, 06 Mar 2024 03:57:40 GMT  
		Size: 17.3 MB (17258499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91cb809e488845124f75544e212468cdb11a2e0608029edad585d6ea2ddbe70`  
		Last Modified: Wed, 06 Mar 2024 03:58:18 GMT  
		Size: 43.8 MB (43765885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b377b22329c61226e8806deb31b4569750cb4f9731347151c457c0d07051ca92`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbd910585f6d3b1a94645b01af3e6f396694f423b57489a516bc47ee7f9df8f`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6a65cab54401d2fc7cd70c4cc5a2a176ff334b9a7a862fd2f8e7e0e45a83d`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05791b9ec4a138f25eb78ad28130353c915edc06a7a5a5edd418e26365f2636`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 4.5 MB (4483641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cbdbc828ec7213e079874bc79f31faab34039fd9562a4ef32ab96da180441f`  
		Last Modified: Wed, 06 Mar 2024 07:57:41 GMT  
		Size: 14.8 MB (14809025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51721c1aabb28007172607786d12ce8ffebabb95dcf135ff59706b853315dea`  
		Last Modified: Wed, 06 Mar 2024 07:57:40 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.9`

```console
$ docker pull zookeeper@sha256:c8dff5a105d3e871a3ff1d9d2becc3850591948bc428775f508d1e690dd51a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.9` - linux; amd64

```console
$ docker pull zookeeper@sha256:04ff8e37e6b26bc8c9029cb58e37d8847df3cc3d58c3916ee31bd5b55fa4dfc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115453729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd2c1cd12b193c01526e11a927fca508420b513d3b20d7fa38846c466296c6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Fri, 16 Feb 2024 04:43:31 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:43:37 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:37 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:43:37 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:37 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:37 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:38 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae5c6c895f903c7c55edd6079266ffeafac64f554b060ca75e4057387e9b1b4`  
		Last Modified: Fri, 16 Feb 2024 04:44:59 GMT  
		Size: 20.4 MB (20419369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92eaaeabd557b43c1ada2035b05d066b85e6ac035119d8b1def8f62834f8d4c`  
		Last Modified: Fri, 16 Feb 2024 04:44:57 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:17a2c37304a0672553b1cbd78d1e2c841aec9fe8d3014121b8fa2b6a066209d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111579255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16170563570e1196e25327e3e819b3a41f429a200d92bd6e156f085377ab8d54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:13:49 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 12:13:49 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:13:54 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:13:54 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:13:54 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:13:54 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:13:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:13:54 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:13:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:55 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711b7597a3619ed6a2169523b18bbc3d83e07b20982336f919e65d6eabd1cd9c`  
		Last Modified: Wed, 06 Mar 2024 12:15:47 GMT  
		Size: 20.4 MB (20419393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880be2067bbaf1d165e6bbb7f5e5c0d8628bfa0bd9bebfd1832d6fdda2ceb`  
		Last Modified: Wed, 06 Mar 2024 12:15:46 GMT  
		Size: 772.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:1acc110e7e9b32ce8739e2ddb173c52fd40e915db8c3498b2efb66dab10d3677
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117513352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dc1a1ebdf1f70a2015212208b91bafa6a488933381b48a09e634c8b7e70813`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:17:28 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 04:17:28 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:17:35 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:17:36 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:17:36 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:17:37 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:17:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:17:37 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:17:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:39 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1f481108f4fd58bfcb32a0f7fb83fffdd30b94aa5d54941adc1ebcf0358365`  
		Last Modified: Wed, 06 Mar 2024 04:19:47 GMT  
		Size: 20.4 MB (20419361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f51a0addf508fb3cc3d511b4ab2ea6e2f66eda3a81e43c98c9be147e7e45b6`  
		Last Modified: Wed, 06 Mar 2024 04:19:45 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9` - linux; s390x

```console
$ docker pull zookeeper@sha256:9aa987c74b711a1b844d22af58f29fdaa35d2b403e28eba83cc0d1ac633cb60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107291681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b85b4d83379059e06ac546b8d66a26098d82cebccbbbf8cfe6cf2ed74c4a4b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:52:09 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 07:52:09 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:52:12 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:52:13 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:52:13 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:52:13 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:52:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:52:13 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:52:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:52:13 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f87e4c0ae56a1a490b028e261971cfe731927aee2e43fef553945681ccbce1`  
		Last Modified: Wed, 06 Mar 2024 07:57:25 GMT  
		Size: 20.4 MB (20419383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da29e38ef99f788014c8f41808fb22e0618c7df45a87207f2ee3531e0baaec46`  
		Last Modified: Wed, 06 Mar 2024 07:57:24 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.9-jre-11`

```console
$ docker pull zookeeper@sha256:c8dff5a105d3e871a3ff1d9d2becc3850591948bc428775f508d1e690dd51a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.9-jre-11` - linux; amd64

```console
$ docker pull zookeeper@sha256:04ff8e37e6b26bc8c9029cb58e37d8847df3cc3d58c3916ee31bd5b55fa4dfc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115453729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd2c1cd12b193c01526e11a927fca508420b513d3b20d7fa38846c466296c6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Fri, 16 Feb 2024 04:43:31 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:43:37 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:37 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:43:37 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:37 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:37 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:38 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae5c6c895f903c7c55edd6079266ffeafac64f554b060ca75e4057387e9b1b4`  
		Last Modified: Fri, 16 Feb 2024 04:44:59 GMT  
		Size: 20.4 MB (20419369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92eaaeabd557b43c1ada2035b05d066b85e6ac035119d8b1def8f62834f8d4c`  
		Last Modified: Fri, 16 Feb 2024 04:44:57 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9-jre-11` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:17a2c37304a0672553b1cbd78d1e2c841aec9fe8d3014121b8fa2b6a066209d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111579255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16170563570e1196e25327e3e819b3a41f429a200d92bd6e156f085377ab8d54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:13:49 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 12:13:49 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:13:54 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:13:54 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:13:54 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:13:54 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:13:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:13:54 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:13:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:55 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711b7597a3619ed6a2169523b18bbc3d83e07b20982336f919e65d6eabd1cd9c`  
		Last Modified: Wed, 06 Mar 2024 12:15:47 GMT  
		Size: 20.4 MB (20419393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880be2067bbaf1d165e6bbb7f5e5c0d8628bfa0bd9bebfd1832d6fdda2ceb`  
		Last Modified: Wed, 06 Mar 2024 12:15:46 GMT  
		Size: 772.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9-jre-11` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:1acc110e7e9b32ce8739e2ddb173c52fd40e915db8c3498b2efb66dab10d3677
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117513352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dc1a1ebdf1f70a2015212208b91bafa6a488933381b48a09e634c8b7e70813`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:17:28 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 04:17:28 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:17:35 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:17:36 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:17:36 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:17:37 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:17:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:17:37 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:17:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:39 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1f481108f4fd58bfcb32a0f7fb83fffdd30b94aa5d54941adc1ebcf0358365`  
		Last Modified: Wed, 06 Mar 2024 04:19:47 GMT  
		Size: 20.4 MB (20419361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f51a0addf508fb3cc3d511b4ab2ea6e2f66eda3a81e43c98c9be147e7e45b6`  
		Last Modified: Wed, 06 Mar 2024 04:19:45 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9-jre-11` - linux; s390x

```console
$ docker pull zookeeper@sha256:9aa987c74b711a1b844d22af58f29fdaa35d2b403e28eba83cc0d1ac633cb60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107291681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b85b4d83379059e06ac546b8d66a26098d82cebccbbbf8cfe6cf2ed74c4a4b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:52:09 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 07:52:09 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:52:12 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:52:13 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:52:13 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:52:13 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:52:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:52:13 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:52:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:52:13 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f87e4c0ae56a1a490b028e261971cfe731927aee2e43fef553945681ccbce1`  
		Last Modified: Wed, 06 Mar 2024 07:57:25 GMT  
		Size: 20.4 MB (20419383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da29e38ef99f788014c8f41808fb22e0618c7df45a87207f2ee3531e0baaec46`  
		Last Modified: Wed, 06 Mar 2024 07:57:24 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.9-jre-17`

```console
$ docker pull zookeeper@sha256:d51b77600bb0d9daad944a3c39a1049ff33546bb9023c83160ec0acda864e5a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.9-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:e8edfef1e8a50862880bc9618470d353b0adfa014e19865d39632d65c39fec4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120102169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272d7d45e6ae5860fc494d6fdfab6559d5b3a57eba867aed9640de94988de358`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:40:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:40:28 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 01:40:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:41:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:41:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:41:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:42 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:49 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:44:07 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Fri, 16 Feb 2024 04:44:07 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:44:10 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:44:10 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:44:11 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:44:11 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:44:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:44:11 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:44:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:44:11 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3d8439525debaa2452083229854d3cfbf629833edbdd2a1750b5ab22c933f5`  
		Last Modified: Fri, 16 Feb 2024 04:45:12 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17439db14e422559cae0b662560c6631dc7aa8e684bb6323e92bc433e8fcbb`  
		Last Modified: Fri, 16 Feb 2024 04:45:13 GMT  
		Size: 4.6 MB (4607448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f8b116fd17ec65e8edaae440cf252f4e68b936d17ca93915f7eefdd1827f65`  
		Last Modified: Fri, 16 Feb 2024 04:45:34 GMT  
		Size: 20.4 MB (20419362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc5daf3545b67ad6dc09a471a568888dafbe9e4df9885765d33a5ed3d324d56`  
		Last Modified: Fri, 16 Feb 2024 04:45:32 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:b04d93d08c030ef0f064b10ec389e0b95cf5ae5bd1fb818598794ff07f27d0ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118831503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73adb2c1e7b4b34fcef91448ceaefa2ed48a70fe687c0b85781d50dfe158dfb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 04:04:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:04:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:04:08 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:57 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:13:58 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:14:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:14:03 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:14:59 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 12:14:59 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:15:03 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:15:03 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:15:03 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:15:04 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:15:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:15:04 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:15:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:15:04 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799297b6f9210d0b08ff588516d8ab6fe2169cdda6b76a0b5f854b6e76aec0ce`  
		Last Modified: Wed, 06 Mar 2024 04:08:04 GMT  
		Size: 18.9 MB (18857483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0f6cd036a6aa4998c7a9c375b0e7fb43615f3d03dfcb794b88cff90027fff7`  
		Last Modified: Wed, 06 Mar 2024 04:08:44 GMT  
		Size: 46.6 MB (46639407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30140b6dcdeba2a64a4d96bfde851abee456c368a15a215e1b86e3c0484bce`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13614e023aad4adadb99824ffb722959861646971b8c272a4eaf5b1fe098077e`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d091c818ec6a831dfc9715467492df06691587db22de40b4f0b2dcbf927b9`  
		Last Modified: Wed, 06 Mar 2024 12:15:59 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56f1e06395bcc4a843fd848fe18bbb42ad2defb19c646319686d52279e9fdc`  
		Last Modified: Wed, 06 Mar 2024 12:16:00 GMT  
		Size: 4.5 MB (4511047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a1e05afc47461968287421f3838340f2f28597ce196ec5e8ec4055e8a33f2f`  
		Last Modified: Wed, 06 Mar 2024 12:16:20 GMT  
		Size: 20.4 MB (20419371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b74e721e4af01553f9fa62c92d358ae87654f73b5c7b7c1839d8f750752dc89`  
		Last Modified: Wed, 06 Mar 2024 12:16:18 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:a5288fc095a03e86a476f6ebdd19d3d935f78779026be6e465d544119e28ff1e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126990842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f9e9f5ab4c2e3a93092836d200dc00cb013506c03c166caed61e1d8509d28e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:41:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:41:33 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 01:42:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:42:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:42:31 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:42:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:17:43 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:17:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:17:57 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:18:42 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 04:18:42 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:18:49 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:18:50 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:18:51 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:18:52 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:18:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:18:53 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:18:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:18:54 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0d16af6f61058996d0677e521dec0be40a28b566317297f06589f10c1d0be3`  
		Last Modified: Wed, 06 Mar 2024 01:47:33 GMT  
		Size: 18.7 MB (18724998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d47ebd5b078b4cc528e25716cbb14bc9ba058da7d77f221f0a953718682a83`  
		Last Modified: Wed, 06 Mar 2024 01:48:23 GMT  
		Size: 47.0 MB (47012835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92f5b11b6fe41ea9819334d8b551be6db95f2350513af1b8e59dee9f15abd06`  
		Last Modified: Wed, 06 Mar 2024 01:48:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96454b934f9891148d03497f07a6dc87d1b56a117b93bd0fde5f1782e3cb792c`  
		Last Modified: Wed, 06 Mar 2024 01:48:16 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11f0be4a1a4a5e8e84454ef57d0c8765daed8863ec1e7fda57b74131f4a9b9`  
		Last Modified: Wed, 06 Mar 2024 04:20:01 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640a5f8b36fe858fc3b1ee337dd69f6f7326ded72c11cee9fb92dbefc486aac8`  
		Last Modified: Wed, 06 Mar 2024 04:20:02 GMT  
		Size: 5.2 MB (5207345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4cb370b91b14c8fad88b077b636107afd60d2e5ea6775f90a5620891414934a`  
		Last Modified: Wed, 06 Mar 2024 04:20:26 GMT  
		Size: 20.4 MB (20419378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2227fe2388dea867347157f4dec1b0727118440de7f44fd96092f2ff6f4bca`  
		Last Modified: Wed, 06 Mar 2024 04:20:24 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:ccbef90e11ce587e187a68e30c26998f1e25bc9f01098e76a76111e5cbaa972d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114567731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c325fa64373ba280ed163480beae99813d345f8f129b6dae1c40df133870ec8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:41:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:41:31 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 03:46:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:46:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:46:15 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:46:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:53:27 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:53:28 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:53:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:53:34 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:55:44 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 07:55:44 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:55:47 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:55:48 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:55:48 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:55:48 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:55:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:55:48 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:55:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:55:48 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ac9a901fa5c1ea7b49c5d68835040a39635587cbb48c866f523885955a0666`  
		Last Modified: Wed, 06 Mar 2024 03:57:40 GMT  
		Size: 17.3 MB (17258499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91cb809e488845124f75544e212468cdb11a2e0608029edad585d6ea2ddbe70`  
		Last Modified: Wed, 06 Mar 2024 03:58:18 GMT  
		Size: 43.8 MB (43765885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b377b22329c61226e8806deb31b4569750cb4f9731347151c457c0d07051ca92`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbd910585f6d3b1a94645b01af3e6f396694f423b57489a516bc47ee7f9df8f`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6a65cab54401d2fc7cd70c4cc5a2a176ff334b9a7a862fd2f8e7e0e45a83d`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05791b9ec4a138f25eb78ad28130353c915edc06a7a5a5edd418e26365f2636`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 4.5 MB (4483641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdde4f46644d85b320925c5ba25554cc7dca750f66f1f179dc005870d2891a2`  
		Last Modified: Wed, 06 Mar 2024 07:57:49 GMT  
		Size: 20.4 MB (20419394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb76fe1623e984ff887aa402cd581ffbae20d3dd59f5f11fff4461885cba00b`  
		Last Modified: Wed, 06 Mar 2024 07:57:47 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.9.1`

```console
$ docker pull zookeeper@sha256:c8dff5a105d3e871a3ff1d9d2becc3850591948bc428775f508d1e690dd51a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.9.1` - linux; amd64

```console
$ docker pull zookeeper@sha256:04ff8e37e6b26bc8c9029cb58e37d8847df3cc3d58c3916ee31bd5b55fa4dfc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115453729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd2c1cd12b193c01526e11a927fca508420b513d3b20d7fa38846c466296c6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Fri, 16 Feb 2024 04:43:31 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:43:37 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:37 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:43:37 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:37 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:37 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:38 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae5c6c895f903c7c55edd6079266ffeafac64f554b060ca75e4057387e9b1b4`  
		Last Modified: Fri, 16 Feb 2024 04:44:59 GMT  
		Size: 20.4 MB (20419369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92eaaeabd557b43c1ada2035b05d066b85e6ac035119d8b1def8f62834f8d4c`  
		Last Modified: Fri, 16 Feb 2024 04:44:57 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9.1` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:17a2c37304a0672553b1cbd78d1e2c841aec9fe8d3014121b8fa2b6a066209d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111579255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16170563570e1196e25327e3e819b3a41f429a200d92bd6e156f085377ab8d54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:13:49 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 12:13:49 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:13:54 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:13:54 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:13:54 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:13:54 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:13:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:13:54 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:13:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:55 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711b7597a3619ed6a2169523b18bbc3d83e07b20982336f919e65d6eabd1cd9c`  
		Last Modified: Wed, 06 Mar 2024 12:15:47 GMT  
		Size: 20.4 MB (20419393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880be2067bbaf1d165e6bbb7f5e5c0d8628bfa0bd9bebfd1832d6fdda2ceb`  
		Last Modified: Wed, 06 Mar 2024 12:15:46 GMT  
		Size: 772.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9.1` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:1acc110e7e9b32ce8739e2ddb173c52fd40e915db8c3498b2efb66dab10d3677
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117513352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dc1a1ebdf1f70a2015212208b91bafa6a488933381b48a09e634c8b7e70813`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:17:28 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 04:17:28 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:17:35 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:17:36 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:17:36 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:17:37 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:17:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:17:37 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:17:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:39 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1f481108f4fd58bfcb32a0f7fb83fffdd30b94aa5d54941adc1ebcf0358365`  
		Last Modified: Wed, 06 Mar 2024 04:19:47 GMT  
		Size: 20.4 MB (20419361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f51a0addf508fb3cc3d511b4ab2ea6e2f66eda3a81e43c98c9be147e7e45b6`  
		Last Modified: Wed, 06 Mar 2024 04:19:45 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9.1` - linux; s390x

```console
$ docker pull zookeeper@sha256:9aa987c74b711a1b844d22af58f29fdaa35d2b403e28eba83cc0d1ac633cb60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107291681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b85b4d83379059e06ac546b8d66a26098d82cebccbbbf8cfe6cf2ed74c4a4b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:52:09 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 07:52:09 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:52:12 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:52:13 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:52:13 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:52:13 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:52:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:52:13 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:52:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:52:13 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f87e4c0ae56a1a490b028e261971cfe731927aee2e43fef553945681ccbce1`  
		Last Modified: Wed, 06 Mar 2024 07:57:25 GMT  
		Size: 20.4 MB (20419383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da29e38ef99f788014c8f41808fb22e0618c7df45a87207f2ee3531e0baaec46`  
		Last Modified: Wed, 06 Mar 2024 07:57:24 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.9.1-jre-11`

```console
$ docker pull zookeeper@sha256:c8dff5a105d3e871a3ff1d9d2becc3850591948bc428775f508d1e690dd51a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.9.1-jre-11` - linux; amd64

```console
$ docker pull zookeeper@sha256:04ff8e37e6b26bc8c9029cb58e37d8847df3cc3d58c3916ee31bd5b55fa4dfc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115453729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd2c1cd12b193c01526e11a927fca508420b513d3b20d7fa38846c466296c6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:38:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:39:30 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Fri, 16 Feb 2024 01:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:39:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:39:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:39:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:06 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:07 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:14 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:43:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Fri, 16 Feb 2024 04:43:31 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:43:37 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:43:37 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:43:37 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:43:37 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:43:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:43:37 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:43:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:38 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c59d8a84db554e1b45f0b08a9632fdcb91354f59367a9aef3c832754c3e345`  
		Last Modified: Fri, 16 Feb 2024 01:42:43 GMT  
		Size: 12.9 MB (12906460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3f591e1537a1a24dd157cb9c479040bde8c9a3d3210a317a60a0e01278f02a`  
		Last Modified: Fri, 16 Feb 2024 01:43:55 GMT  
		Size: 47.1 MB (47069222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0374c36aa38d1fbbf1e7d1ac69527ec3d15847425f707161c266ec060cd338f`  
		Last Modified: Fri, 16 Feb 2024 01:43:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b0bb2324f26c63015f06398024bed40130bf404aaedf14f4a9934ae037973`  
		Last Modified: Fri, 16 Feb 2024 01:43:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807ce772e0e4a31400aee14b880848a23cb754b76d9ac63e2e8a7db396297f7`  
		Last Modified: Fri, 16 Feb 2024 04:44:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7895591f467d3d593011999bc5ab0c929f746348fd134a661479418b439cdf3c`  
		Last Modified: Fri, 16 Feb 2024 04:44:29 GMT  
		Size: 4.6 MB (4605052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae5c6c895f903c7c55edd6079266ffeafac64f554b060ca75e4057387e9b1b4`  
		Last Modified: Fri, 16 Feb 2024 04:44:59 GMT  
		Size: 20.4 MB (20419369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92eaaeabd557b43c1ada2035b05d066b85e6ac035119d8b1def8f62834f8d4c`  
		Last Modified: Fri, 16 Feb 2024 04:44:57 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9.1-jre-11` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:17a2c37304a0672553b1cbd78d1e2c841aec9fe8d3014121b8fa2b6a066209d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111579255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16170563570e1196e25327e3e819b3a41f429a200d92bd6e156f085377ab8d54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:02:32 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 04:02:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:12:20 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:12:21 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:12:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:12:32 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:13:49 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 12:13:49 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:13:54 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:13:54 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:13:54 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:13:54 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:13:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:13:54 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:13:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:55 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099ab792921bde3b4856ba4ed7e3ada8617507ba29009035c1b557cfeee153ea`  
		Last Modified: Wed, 06 Mar 2024 04:05:48 GMT  
		Size: 12.8 MB (12846364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6308702f34f1e8b2375a63c8bc39c4ebe0e2acd909c76b8d2b110cd6b47ecb10`  
		Last Modified: Wed, 06 Mar 2024 04:07:32 GMT  
		Size: 45.4 MB (45400863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6f604a9fd77ae5f8db3bb2f562399116fe3c4c19196061bbda789c5659bf34`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebad8469e990061febe29edbf7e63ef98eb34a6d9e3dcf55fde75f553161614`  
		Last Modified: Wed, 06 Mar 2024 04:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d661dfd98d57e0259ad32543b3d4be80ebfdd32029be6b03a746e639cb283ff`  
		Last Modified: Wed, 06 Mar 2024 12:15:18 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8790528be4b9213684312a6927705341f87264d1d0175ce1446ae575dd35f3db`  
		Last Modified: Wed, 06 Mar 2024 12:15:19 GMT  
		Size: 4.5 MB (4508444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711b7597a3619ed6a2169523b18bbc3d83e07b20982336f919e65d6eabd1cd9c`  
		Last Modified: Wed, 06 Mar 2024 12:15:47 GMT  
		Size: 20.4 MB (20419393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880be2067bbaf1d165e6bbb7f5e5c0d8628bfa0bd9bebfd1832d6fdda2ceb`  
		Last Modified: Wed, 06 Mar 2024 12:15:46 GMT  
		Size: 772.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9.1-jre-11` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:1acc110e7e9b32ce8739e2ddb173c52fd40e915db8c3498b2efb66dab10d3677
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117513352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dc1a1ebdf1f70a2015212208b91bafa6a488933381b48a09e634c8b7e70813`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:37:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:38:54 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 01:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:39:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:39:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:39:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:16:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:16:13 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:16:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:16:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:17:28 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 04:17:28 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:17:35 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:17:36 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:17:36 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:17:37 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:17:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:17:37 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:17:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:39 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f1cff61af6fd0e72a43f6e6a9088504a0f097c4ed3137359a1f68c2de524b`  
		Last Modified: Wed, 06 Mar 2024 01:44:42 GMT  
		Size: 13.8 MB (13767879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff245f348df9bcc26429fc6269f431cd16755c6f0f33b8d89a5bea2c4d5940`  
		Last Modified: Wed, 06 Mar 2024 01:46:54 GMT  
		Size: 42.5 MB (42494967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a0a7ebd0b8d24027b95cbd6a3514789e8dd11f98001faa57c231bb906e0f1`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d14970d23509aca245467e5f2e3b72e6771bfc623d24491dc1088208775034`  
		Last Modified: Wed, 06 Mar 2024 01:46:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b36c75b4eded8ddd36c261685d497a594c7d9e46adcb13cb24c8d0c0dd7db5`  
		Last Modified: Wed, 06 Mar 2024 04:19:14 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589bfc1105dec2b0a9f55a2f193d26d90b8368b2bb1abbbe25ed196b93da14bf`  
		Last Modified: Wed, 06 Mar 2024 04:19:15 GMT  
		Size: 5.2 MB (5204854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1f481108f4fd58bfcb32a0f7fb83fffdd30b94aa5d54941adc1ebcf0358365`  
		Last Modified: Wed, 06 Mar 2024 04:19:47 GMT  
		Size: 20.4 MB (20419361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f51a0addf508fb3cc3d511b4ab2ea6e2f66eda3a81e43c98c9be147e7e45b6`  
		Last Modified: Wed, 06 Mar 2024 04:19:45 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9.1-jre-11` - linux; s390x

```console
$ docker pull zookeeper@sha256:9aa987c74b711a1b844d22af58f29fdaa35d2b403e28eba83cc0d1ac633cb60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107291681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b85b4d83379059e06ac546b8d66a26098d82cebccbbbf8cfe6cf2ed74c4a4b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:31:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:31:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 03:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:36:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:36:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:49:41 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:49:41 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:49:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:49:48 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:52:09 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 07:52:09 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:52:12 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:52:13 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:52:13 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:52:13 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:52:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:52:13 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:52:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:52:13 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef062d3d629968872412a7769d950a682dc1b30cb7839adcfc5a08aad1bcde29`  
		Last Modified: Wed, 06 Mar 2024 03:56:33 GMT  
		Size: 13.0 MB (12985098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b4624d5a5be9d30d1ed78f4237be3144f1c8e08bc85b4c0a95ebea62d67169`  
		Last Modified: Wed, 06 Mar 2024 03:57:08 GMT  
		Size: 40.8 MB (40765633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b9818f17b461dbefae870e2f9e44e7ec06d27c6f75318f86cd6093368353c`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83b360259188271e0ffb9b8ab7956a7d750a35f5b4aa941cad20c99bd1339b`  
		Last Modified: Wed, 06 Mar 2024 03:57:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d24f60184fe12e7f4b0f8199cbbca13ffe8c49cfaa8020af917e2c05751baf`  
		Last Modified: Wed, 06 Mar 2024 07:57:06 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e571ac67cadf0ef6b4f225121f1b751598ea24e7e99cd9a9172b2313acb4b90`  
		Last Modified: Wed, 06 Mar 2024 07:57:07 GMT  
		Size: 4.5 MB (4481254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f87e4c0ae56a1a490b028e261971cfe731927aee2e43fef553945681ccbce1`  
		Last Modified: Wed, 06 Mar 2024 07:57:25 GMT  
		Size: 20.4 MB (20419383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da29e38ef99f788014c8f41808fb22e0618c7df45a87207f2ee3531e0baaec46`  
		Last Modified: Wed, 06 Mar 2024 07:57:24 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:3.9.1-jre-17`

```console
$ docker pull zookeeper@sha256:d51b77600bb0d9daad944a3c39a1049ff33546bb9023c83160ec0acda864e5a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:3.9.1-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:e8edfef1e8a50862880bc9618470d353b0adfa014e19865d39632d65c39fec4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120102169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272d7d45e6ae5860fc494d6fdfab6559d5b3a57eba867aed9640de94988de358`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:40:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:40:28 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 01:40:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:41:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:41:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:41:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:42 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:49 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:44:07 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Fri, 16 Feb 2024 04:44:07 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:44:10 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:44:10 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:44:11 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:44:11 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:44:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:44:11 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:44:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:44:11 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3d8439525debaa2452083229854d3cfbf629833edbdd2a1750b5ab22c933f5`  
		Last Modified: Fri, 16 Feb 2024 04:45:12 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17439db14e422559cae0b662560c6631dc7aa8e684bb6323e92bc433e8fcbb`  
		Last Modified: Fri, 16 Feb 2024 04:45:13 GMT  
		Size: 4.6 MB (4607448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f8b116fd17ec65e8edaae440cf252f4e68b936d17ca93915f7eefdd1827f65`  
		Last Modified: Fri, 16 Feb 2024 04:45:34 GMT  
		Size: 20.4 MB (20419362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc5daf3545b67ad6dc09a471a568888dafbe9e4df9885765d33a5ed3d324d56`  
		Last Modified: Fri, 16 Feb 2024 04:45:32 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9.1-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:b04d93d08c030ef0f064b10ec389e0b95cf5ae5bd1fb818598794ff07f27d0ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118831503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73adb2c1e7b4b34fcef91448ceaefa2ed48a70fe687c0b85781d50dfe158dfb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 04:04:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:04:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:04:08 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:57 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:13:58 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:14:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:14:03 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:14:59 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 12:14:59 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:15:03 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:15:03 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:15:03 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:15:04 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:15:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:15:04 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:15:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:15:04 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799297b6f9210d0b08ff588516d8ab6fe2169cdda6b76a0b5f854b6e76aec0ce`  
		Last Modified: Wed, 06 Mar 2024 04:08:04 GMT  
		Size: 18.9 MB (18857483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0f6cd036a6aa4998c7a9c375b0e7fb43615f3d03dfcb794b88cff90027fff7`  
		Last Modified: Wed, 06 Mar 2024 04:08:44 GMT  
		Size: 46.6 MB (46639407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30140b6dcdeba2a64a4d96bfde851abee456c368a15a215e1b86e3c0484bce`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13614e023aad4adadb99824ffb722959861646971b8c272a4eaf5b1fe098077e`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d091c818ec6a831dfc9715467492df06691587db22de40b4f0b2dcbf927b9`  
		Last Modified: Wed, 06 Mar 2024 12:15:59 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56f1e06395bcc4a843fd848fe18bbb42ad2defb19c646319686d52279e9fdc`  
		Last Modified: Wed, 06 Mar 2024 12:16:00 GMT  
		Size: 4.5 MB (4511047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a1e05afc47461968287421f3838340f2f28597ce196ec5e8ec4055e8a33f2f`  
		Last Modified: Wed, 06 Mar 2024 12:16:20 GMT  
		Size: 20.4 MB (20419371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b74e721e4af01553f9fa62c92d358ae87654f73b5c7b7c1839d8f750752dc89`  
		Last Modified: Wed, 06 Mar 2024 12:16:18 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9.1-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:a5288fc095a03e86a476f6ebdd19d3d935f78779026be6e465d544119e28ff1e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126990842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f9e9f5ab4c2e3a93092836d200dc00cb013506c03c166caed61e1d8509d28e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:41:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:41:33 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 01:42:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:42:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:42:31 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:42:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:17:43 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:17:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:17:57 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:18:42 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 04:18:42 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:18:49 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:18:50 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:18:51 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:18:52 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:18:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:18:53 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:18:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:18:54 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0d16af6f61058996d0677e521dec0be40a28b566317297f06589f10c1d0be3`  
		Last Modified: Wed, 06 Mar 2024 01:47:33 GMT  
		Size: 18.7 MB (18724998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d47ebd5b078b4cc528e25716cbb14bc9ba058da7d77f221f0a953718682a83`  
		Last Modified: Wed, 06 Mar 2024 01:48:23 GMT  
		Size: 47.0 MB (47012835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92f5b11b6fe41ea9819334d8b551be6db95f2350513af1b8e59dee9f15abd06`  
		Last Modified: Wed, 06 Mar 2024 01:48:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96454b934f9891148d03497f07a6dc87d1b56a117b93bd0fde5f1782e3cb792c`  
		Last Modified: Wed, 06 Mar 2024 01:48:16 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11f0be4a1a4a5e8e84454ef57d0c8765daed8863ec1e7fda57b74131f4a9b9`  
		Last Modified: Wed, 06 Mar 2024 04:20:01 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640a5f8b36fe858fc3b1ee337dd69f6f7326ded72c11cee9fb92dbefc486aac8`  
		Last Modified: Wed, 06 Mar 2024 04:20:02 GMT  
		Size: 5.2 MB (5207345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4cb370b91b14c8fad88b077b636107afd60d2e5ea6775f90a5620891414934a`  
		Last Modified: Wed, 06 Mar 2024 04:20:26 GMT  
		Size: 20.4 MB (20419378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2227fe2388dea867347157f4dec1b0727118440de7f44fd96092f2ff6f4bca`  
		Last Modified: Wed, 06 Mar 2024 04:20:24 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:3.9.1-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:ccbef90e11ce587e187a68e30c26998f1e25bc9f01098e76a76111e5cbaa972d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114567731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c325fa64373ba280ed163480beae99813d345f8f129b6dae1c40df133870ec8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:41:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:41:31 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 03:46:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:46:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:46:15 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:46:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:53:27 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:53:28 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:53:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:53:34 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:55:44 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 07:55:44 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:55:47 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:55:48 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:55:48 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:55:48 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:55:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:55:48 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:55:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:55:48 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ac9a901fa5c1ea7b49c5d68835040a39635587cbb48c866f523885955a0666`  
		Last Modified: Wed, 06 Mar 2024 03:57:40 GMT  
		Size: 17.3 MB (17258499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91cb809e488845124f75544e212468cdb11a2e0608029edad585d6ea2ddbe70`  
		Last Modified: Wed, 06 Mar 2024 03:58:18 GMT  
		Size: 43.8 MB (43765885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b377b22329c61226e8806deb31b4569750cb4f9731347151c457c0d07051ca92`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbd910585f6d3b1a94645b01af3e6f396694f423b57489a516bc47ee7f9df8f`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6a65cab54401d2fc7cd70c4cc5a2a176ff334b9a7a862fd2f8e7e0e45a83d`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05791b9ec4a138f25eb78ad28130353c915edc06a7a5a5edd418e26365f2636`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 4.5 MB (4483641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdde4f46644d85b320925c5ba25554cc7dca750f66f1f179dc005870d2891a2`  
		Last Modified: Wed, 06 Mar 2024 07:57:49 GMT  
		Size: 20.4 MB (20419394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb76fe1623e984ff887aa402cd581ffbae20d3dd59f5f11fff4461885cba00b`  
		Last Modified: Wed, 06 Mar 2024 07:57:47 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:d51b77600bb0d9daad944a3c39a1049ff33546bb9023c83160ec0acda864e5a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:latest` - linux; amd64

```console
$ docker pull zookeeper@sha256:e8edfef1e8a50862880bc9618470d353b0adfa014e19865d39632d65c39fec4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120102169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272d7d45e6ae5860fc494d6fdfab6559d5b3a57eba867aed9640de94988de358`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:40:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:40:28 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 01:40:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:41:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:41:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:41:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:43:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Feb 2024 04:43:42 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Fri, 16 Feb 2024 04:43:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Fri, 16 Feb 2024 04:43:49 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Feb 2024 04:44:07 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Fri, 16 Feb 2024 04:44:07 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:44:10 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Fri, 16 Feb 2024 04:44:10 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Fri, 16 Feb 2024 04:44:11 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Feb 2024 04:44:11 GMT
EXPOSE 2181 2888 3888 8080
# Fri, 16 Feb 2024 04:44:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Feb 2024 04:44:11 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Fri, 16 Feb 2024 04:44:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 04:44:11 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3d8439525debaa2452083229854d3cfbf629833edbdd2a1750b5ab22c933f5`  
		Last Modified: Fri, 16 Feb 2024 04:45:12 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd17439db14e422559cae0b662560c6631dc7aa8e684bb6323e92bc433e8fcbb`  
		Last Modified: Fri, 16 Feb 2024 04:45:13 GMT  
		Size: 4.6 MB (4607448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f8b116fd17ec65e8edaae440cf252f4e68b936d17ca93915f7eefdd1827f65`  
		Last Modified: Fri, 16 Feb 2024 04:45:34 GMT  
		Size: 20.4 MB (20419362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc5daf3545b67ad6dc09a471a568888dafbe9e4df9885765d33a5ed3d324d56`  
		Last Modified: Fri, 16 Feb 2024 04:45:32 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:latest` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:b04d93d08c030ef0f064b10ec389e0b95cf5ae5bd1fb818598794ff07f27d0ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118831503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73adb2c1e7b4b34fcef91448ceaefa2ed48a70fe687c0b85781d50dfe158dfb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 04:04:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:04:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:04:08 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 12:13:57 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 12:13:58 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 12:14:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 12:14:03 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 12:14:59 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 12:14:59 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:15:03 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 12:15:03 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 12:15:03 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 12:15:04 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 12:15:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 12:15:04 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 12:15:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 12:15:04 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799297b6f9210d0b08ff588516d8ab6fe2169cdda6b76a0b5f854b6e76aec0ce`  
		Last Modified: Wed, 06 Mar 2024 04:08:04 GMT  
		Size: 18.9 MB (18857483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0f6cd036a6aa4998c7a9c375b0e7fb43615f3d03dfcb794b88cff90027fff7`  
		Last Modified: Wed, 06 Mar 2024 04:08:44 GMT  
		Size: 46.6 MB (46639407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30140b6dcdeba2a64a4d96bfde851abee456c368a15a215e1b86e3c0484bce`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13614e023aad4adadb99824ffb722959861646971b8c272a4eaf5b1fe098077e`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d091c818ec6a831dfc9715467492df06691587db22de40b4f0b2dcbf927b9`  
		Last Modified: Wed, 06 Mar 2024 12:15:59 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56f1e06395bcc4a843fd848fe18bbb42ad2defb19c646319686d52279e9fdc`  
		Last Modified: Wed, 06 Mar 2024 12:16:00 GMT  
		Size: 4.5 MB (4511047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a1e05afc47461968287421f3838340f2f28597ce196ec5e8ec4055e8a33f2f`  
		Last Modified: Wed, 06 Mar 2024 12:16:20 GMT  
		Size: 20.4 MB (20419371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b74e721e4af01553f9fa62c92d358ae87654f73b5c7b7c1839d8f750752dc89`  
		Last Modified: Wed, 06 Mar 2024 12:16:18 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:latest` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:a5288fc095a03e86a476f6ebdd19d3d935f78779026be6e465d544119e28ff1e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126990842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f9e9f5ab4c2e3a93092836d200dc00cb013506c03c166caed61e1d8509d28e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:36:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:41:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:41:33 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 01:42:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 01:42:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 01:42:31 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:42:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:17:42 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 04:17:43 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 04:17:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 04:17:57 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 04:18:42 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 04:18:42 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:18:49 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 04:18:50 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 04:18:51 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 04:18:52 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 04:18:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 04:18:53 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 04:18:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 04:18:54 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0d16af6f61058996d0677e521dec0be40a28b566317297f06589f10c1d0be3`  
		Last Modified: Wed, 06 Mar 2024 01:47:33 GMT  
		Size: 18.7 MB (18724998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d47ebd5b078b4cc528e25716cbb14bc9ba058da7d77f221f0a953718682a83`  
		Last Modified: Wed, 06 Mar 2024 01:48:23 GMT  
		Size: 47.0 MB (47012835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92f5b11b6fe41ea9819334d8b551be6db95f2350513af1b8e59dee9f15abd06`  
		Last Modified: Wed, 06 Mar 2024 01:48:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96454b934f9891148d03497f07a6dc87d1b56a117b93bd0fde5f1782e3cb792c`  
		Last Modified: Wed, 06 Mar 2024 01:48:16 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11f0be4a1a4a5e8e84454ef57d0c8765daed8863ec1e7fda57b74131f4a9b9`  
		Last Modified: Wed, 06 Mar 2024 04:20:01 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640a5f8b36fe858fc3b1ee337dd69f6f7326ded72c11cee9fb92dbefc486aac8`  
		Last Modified: Wed, 06 Mar 2024 04:20:02 GMT  
		Size: 5.2 MB (5207345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4cb370b91b14c8fad88b077b636107afd60d2e5ea6775f90a5620891414934a`  
		Last Modified: Wed, 06 Mar 2024 04:20:26 GMT  
		Size: 20.4 MB (20419378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2227fe2388dea867347157f4dec1b0727118440de7f44fd96092f2ff6f4bca`  
		Last Modified: Wed, 06 Mar 2024 04:20:24 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:latest` - linux; s390x

```console
$ docker pull zookeeper@sha256:ccbef90e11ce587e187a68e30c26998f1e25bc9f01098e76a76111e5cbaa972d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114567731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c325fa64373ba280ed163480beae99813d345f8f129b6dae1c40df133870ec8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 03:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:30:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:41:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:41:31 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 03:46:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 03:46:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 03:46:15 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 03:46:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 07:53:27 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 06 Mar 2024 07:53:28 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Wed, 06 Mar 2024 07:53:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 06 Mar 2024 07:53:34 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 06 Mar 2024 07:55:44 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Wed, 06 Mar 2024 07:55:44 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:55:47 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Wed, 06 Mar 2024 07:55:48 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Wed, 06 Mar 2024 07:55:48 GMT
VOLUME [/data /datalog /logs]
# Wed, 06 Mar 2024 07:55:48 GMT
EXPOSE 2181 2888 3888 8080
# Wed, 06 Mar 2024 07:55:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Wed, 06 Mar 2024 07:55:48 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Wed, 06 Mar 2024 07:55:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Mar 2024 07:55:48 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ac9a901fa5c1ea7b49c5d68835040a39635587cbb48c866f523885955a0666`  
		Last Modified: Wed, 06 Mar 2024 03:57:40 GMT  
		Size: 17.3 MB (17258499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91cb809e488845124f75544e212468cdb11a2e0608029edad585d6ea2ddbe70`  
		Last Modified: Wed, 06 Mar 2024 03:58:18 GMT  
		Size: 43.8 MB (43765885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b377b22329c61226e8806deb31b4569750cb4f9731347151c457c0d07051ca92`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbd910585f6d3b1a94645b01af3e6f396694f423b57489a516bc47ee7f9df8f`  
		Last Modified: Wed, 06 Mar 2024 03:58:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6a65cab54401d2fc7cd70c4cc5a2a176ff334b9a7a862fd2f8e7e0e45a83d`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05791b9ec4a138f25eb78ad28130353c915edc06a7a5a5edd418e26365f2636`  
		Last Modified: Wed, 06 Mar 2024 07:57:33 GMT  
		Size: 4.5 MB (4483641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdde4f46644d85b320925c5ba25554cc7dca750f66f1f179dc005870d2891a2`  
		Last Modified: Wed, 06 Mar 2024 07:57:49 GMT  
		Size: 20.4 MB (20419394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb76fe1623e984ff887aa402cd581ffbae20d3dd59f5f11fff4461885cba00b`  
		Last Modified: Wed, 06 Mar 2024 07:57:47 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
