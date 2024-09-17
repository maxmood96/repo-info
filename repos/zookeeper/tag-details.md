<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `zookeeper`

-	[`zookeeper:3.7`](#zookeeper37)
-	[`zookeeper:3.7-jre-11`](#zookeeper37-jre-11)
-	[`zookeeper:3.7-jre-17`](#zookeeper37-jre-17)
-	[`zookeeper:3.7.2`](#zookeeper372)
-	[`zookeeper:3.7.2-jre-11`](#zookeeper372-jre-11)
-	[`zookeeper:3.7.2-jre-17`](#zookeeper372-jre-17)
-	[`zookeeper:3.8`](#zookeeper38)
-	[`zookeeper:3.8-jre-17`](#zookeeper38-jre-17)
-	[`zookeeper:3.8.4`](#zookeeper384)
-	[`zookeeper:3.8.4-jre-17`](#zookeeper384-jre-17)
-	[`zookeeper:3.9`](#zookeeper39)
-	[`zookeeper:3.9-jre-17`](#zookeeper39-jre-17)
-	[`zookeeper:3.9.2`](#zookeeper392)
-	[`zookeeper:3.9.2-jre-17`](#zookeeper392-jre-17)
-	[`zookeeper:latest`](#zookeeperlatest)

## `zookeeper:3.7`

```console
$ docker pull zookeeper@sha256:f7b24ec76ae0bc2287db56db41004218f042a06b034eb3c33631e130c5c1ba7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.7` - linux; amd64

```console
$ docker pull zookeeper@sha256:49bec9e4ef73906e1ef815848ebb5606f18f57158b094e46bbf636b18b97c2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109020464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0d7e840425b565fedb1418c0101e2177add1523c8620a513f355f835fe2c64`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f17d82e63e7d03b5c7593a78c97b3e47cbae3a10a73272397b9198b29118dc`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.2 MB (47198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160911679b1063ecd6051528d8a67a77b522a6e2265098a70b7dd4b957ea7188`  
		Last Modified: Tue, 17 Sep 2024 01:09:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc57f7209badbf5d0fdfb0a3134519f8fd3ec56991ba6c688228e2b9d07ad8d`  
		Last Modified: Tue, 17 Sep 2024 01:09:05 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bee863ffa3fcee8682b357ea9d71284e5a14cce82f021892836d8ce9cd46166`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04082e569171eafe6ee925415046eb2e455e88ab8ed56bbc888dfe39936752e0`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 4.4 MB (4365980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bc98bb4a7d42e8f677d99fc12c429932fd09c136c0146bcb159bca157e1315`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 14.1 MB (14139932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e4d6bbbcfa1422b86f4aebc760c60e056a6da792c2e1f078c5931f06802e22`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7` - unknown; unknown

```console
$ docker pull zookeeper@sha256:3ac2fd4377e5c7c1c7f787de484df556426617268902a6c1a7259ec58052a968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97caaa8616bc62e253a20fd9954279a884376abb29ec740595e7ac166084eb3`

```dockerfile
```

-	Layers:
	-	`sha256:7dcdd89acf7403eb159ef48ea1e26ad4ce6d44f83b762fc2204a9e54a7604240`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 3.7 MB (3691210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ff0e0f8a567bf5620c0400a29092ea8ee0cadf74a5e7cede4964e84784627f`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:c5b2e34b13c477fcfc3e209a3693dc89662ca3e0d8283bb6f9f9669ecc2300bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105182005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671ab979eb754ab8e33ee357e97f9725a66d29681acc102e2c2a3000fa92da08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dbb8ab7ebb70bbdbb49ab2085d99ae87968ea251f304e9fa059e7155f13e5`  
		Last Modified: Sat, 17 Aug 2024 01:35:00 GMT  
		Size: 45.6 MB (45557024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ed86303b2ff16bd4b17f7c739a9055711b72b99e566885505d9258cd44e26c`  
		Last Modified: Sat, 17 Aug 2024 01:34:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604cf0e08e3afff9c340aa7610394aaab11665931337af35d9c0e0f3b770c4b`  
		Last Modified: Fri, 23 Aug 2024 19:44:09 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb96a3b62851bd2e4b8518ec62e30d0f300faabe146629138a2f8a97cef1b37`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc83dde9fdedb0c360eadfd1c7f81516081a7e5fc187ecb13fd488826c82ebd`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 4.3 MB (4269748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a546e2aa7b6898ddca2ff1e78bb4ab8492f0928c163edd339ed36fe8006326`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 14.1 MB (14139949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93b1ca6b5cb92e6debc33121aaf09ec2125a62c555cf7a9bab66c10d011ffb`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8b89b9e387ea868aaec7063fc06694a086f83957903a9733b2f43dc5bc8f411e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c807c7912c9c373ee20444ea4f5ee43b122b2fedbcd86a76ed397b83c87c3a`

```dockerfile
```

-	Layers:
	-	`sha256:561ebaa605ddc1a5e348cec02798ac0e3d0ff3fcdaba08a1eb1b968260bd4c0c`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 3.7 MB (3691509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134bae314652251f5d0231fd8e0fefa163c3c0e635bf0ef0f46952128213d14b`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 24.6 KB (24624 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:a98319a27611c47e4a17dcf6f9b5d94d245600684b94633b85cf5dfc0a58dfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111065644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d0e6f0039ae50639a963d87afb21faab1aa8d42aa63241f616fa3fa3d17b96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b50c4b0fab19a16a502b1681ff9177a05eed203d81aa04a49df18907898c34`  
		Last Modified: Sat, 17 Aug 2024 01:01:26 GMT  
		Size: 42.7 MB (42652048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338034862f9398ecf41f81f3eb5a9837d4cbe84271d6141f09462837e4a51105`  
		Last Modified: Sat, 17 Aug 2024 01:01:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a3378494275db0692fa539ce9a900d0fdd467054c1b7a1322760ca73ff5eb2`  
		Last Modified: Fri, 23 Aug 2024 19:23:06 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ecabe37fef307cd1c24d32107c6941b57f8f7d4262129f55f4929aff1527be`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12458516b171038549020e80b57d35e844a5f158820b64bf1edead353209662`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 5.0 MB (4966048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f4e2e656f98538a304d968437b934df9c9da53acbc6cb91c2786405b1ec4f`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 14.1 MB (14139951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe0644314e3d3349d000216b137b05413b99b186855058d96e8ad8acd1da2c9`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7` - unknown; unknown

```console
$ docker pull zookeeper@sha256:2ae6a968f90b0d33b2e602650cf0787577ead125a6353b0b06e9340393d61418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e971ffaf9aa87ebcddf440f00e4bb050afe82a64e9b0070dabba419ebfa2140`

```dockerfile
```

-	Layers:
	-	`sha256:c4dd9d0c8559612a8c28b96464a4f88b18677960d1b55fca55eb0ce8a16c1f67`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 3.7 MB (3695776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6ffb8d1359a260a352514d000b97d678d52467c0e986767eef662657452987`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 24.4 KB (24350 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7` - linux; s390x

```console
$ docker pull zookeeper@sha256:b3cd26c491151245711a477ffe367831a844cec0188d000a369f8a16e652abe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100798240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d21b387f1be15bc58a4b781e1f57a5879432396f61b8495735426fac40c581c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b0d2d51f17dc8c7a928be9c46547313e9a50f29bb15f2cc88dc408556588e2`  
		Last Modified: Tue, 17 Sep 2024 01:39:29 GMT  
		Size: 40.8 MB (40816924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e98695f5534c20f90ede714390d956f690a08aa9bca31099e0d5a5c6853afb0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61849bbb51fce6c876b245ec616269a488aad010dc7f1fb914ab8e3c9f4162d5`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725d3a46e59dd488f43df686e38af7baecd724255bdff884afaf5650e0e851c4`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0509cd6f0dbcc551513f9da6a959b40fb609220913316a79df6c493ed5b294bc`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 4.2 MB (4242062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8eb67e27f3222d42b73f93f816b5d07389491af4938ba681c5d5e0b38a6e3`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 14.1 MB (14139947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f525f40522b2d95f4568e9086b38209b1e4c5a4b7ac683c8fd14be8c9e32222d`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7` - unknown; unknown

```console
$ docker pull zookeeper@sha256:dc205eac2d3ecd0f1218d3d1fba1243954e270a4369470d7b99f44038a75601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c156c6756b28cce43372e9d69cf90671d9c3bcb1000b3e85671ed8ae949259`

```dockerfile
```

-	Layers:
	-	`sha256:cbffe67b123ffe761f9f40769e7e31b932cba3bd69a5394ef7654153d9a04475`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 3.7 MB (3692325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1bb72bbb05b5ee5b03134bfdec027eb7f86def6398495a2105b3da6271bba3`  
		Last Modified: Tue, 17 Sep 2024 03:59:20 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.7-jre-11`

```console
$ docker pull zookeeper@sha256:f7b24ec76ae0bc2287db56db41004218f042a06b034eb3c33631e130c5c1ba7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.7-jre-11` - linux; amd64

```console
$ docker pull zookeeper@sha256:49bec9e4ef73906e1ef815848ebb5606f18f57158b094e46bbf636b18b97c2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109020464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0d7e840425b565fedb1418c0101e2177add1523c8620a513f355f835fe2c64`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f17d82e63e7d03b5c7593a78c97b3e47cbae3a10a73272397b9198b29118dc`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.2 MB (47198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160911679b1063ecd6051528d8a67a77b522a6e2265098a70b7dd4b957ea7188`  
		Last Modified: Tue, 17 Sep 2024 01:09:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc57f7209badbf5d0fdfb0a3134519f8fd3ec56991ba6c688228e2b9d07ad8d`  
		Last Modified: Tue, 17 Sep 2024 01:09:05 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bee863ffa3fcee8682b357ea9d71284e5a14cce82f021892836d8ce9cd46166`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04082e569171eafe6ee925415046eb2e455e88ab8ed56bbc888dfe39936752e0`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 4.4 MB (4365980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bc98bb4a7d42e8f677d99fc12c429932fd09c136c0146bcb159bca157e1315`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 14.1 MB (14139932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e4d6bbbcfa1422b86f4aebc760c60e056a6da792c2e1f078c5931f06802e22`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:3ac2fd4377e5c7c1c7f787de484df556426617268902a6c1a7259ec58052a968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97caaa8616bc62e253a20fd9954279a884376abb29ec740595e7ac166084eb3`

```dockerfile
```

-	Layers:
	-	`sha256:7dcdd89acf7403eb159ef48ea1e26ad4ce6d44f83b762fc2204a9e54a7604240`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 3.7 MB (3691210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ff0e0f8a567bf5620c0400a29092ea8ee0cadf74a5e7cede4964e84784627f`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-11` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:c5b2e34b13c477fcfc3e209a3693dc89662ca3e0d8283bb6f9f9669ecc2300bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105182005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671ab979eb754ab8e33ee357e97f9725a66d29681acc102e2c2a3000fa92da08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dbb8ab7ebb70bbdbb49ab2085d99ae87968ea251f304e9fa059e7155f13e5`  
		Last Modified: Sat, 17 Aug 2024 01:35:00 GMT  
		Size: 45.6 MB (45557024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ed86303b2ff16bd4b17f7c739a9055711b72b99e566885505d9258cd44e26c`  
		Last Modified: Sat, 17 Aug 2024 01:34:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604cf0e08e3afff9c340aa7610394aaab11665931337af35d9c0e0f3b770c4b`  
		Last Modified: Fri, 23 Aug 2024 19:44:09 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb96a3b62851bd2e4b8518ec62e30d0f300faabe146629138a2f8a97cef1b37`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc83dde9fdedb0c360eadfd1c7f81516081a7e5fc187ecb13fd488826c82ebd`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 4.3 MB (4269748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a546e2aa7b6898ddca2ff1e78bb4ab8492f0928c163edd339ed36fe8006326`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 14.1 MB (14139949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93b1ca6b5cb92e6debc33121aaf09ec2125a62c555cf7a9bab66c10d011ffb`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8b89b9e387ea868aaec7063fc06694a086f83957903a9733b2f43dc5bc8f411e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c807c7912c9c373ee20444ea4f5ee43b122b2fedbcd86a76ed397b83c87c3a`

```dockerfile
```

-	Layers:
	-	`sha256:561ebaa605ddc1a5e348cec02798ac0e3d0ff3fcdaba08a1eb1b968260bd4c0c`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 3.7 MB (3691509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134bae314652251f5d0231fd8e0fefa163c3c0e635bf0ef0f46952128213d14b`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 24.6 KB (24624 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-11` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:a98319a27611c47e4a17dcf6f9b5d94d245600684b94633b85cf5dfc0a58dfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111065644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d0e6f0039ae50639a963d87afb21faab1aa8d42aa63241f616fa3fa3d17b96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b50c4b0fab19a16a502b1681ff9177a05eed203d81aa04a49df18907898c34`  
		Last Modified: Sat, 17 Aug 2024 01:01:26 GMT  
		Size: 42.7 MB (42652048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338034862f9398ecf41f81f3eb5a9837d4cbe84271d6141f09462837e4a51105`  
		Last Modified: Sat, 17 Aug 2024 01:01:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a3378494275db0692fa539ce9a900d0fdd467054c1b7a1322760ca73ff5eb2`  
		Last Modified: Fri, 23 Aug 2024 19:23:06 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ecabe37fef307cd1c24d32107c6941b57f8f7d4262129f55f4929aff1527be`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12458516b171038549020e80b57d35e844a5f158820b64bf1edead353209662`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 5.0 MB (4966048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f4e2e656f98538a304d968437b934df9c9da53acbc6cb91c2786405b1ec4f`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 14.1 MB (14139951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe0644314e3d3349d000216b137b05413b99b186855058d96e8ad8acd1da2c9`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:2ae6a968f90b0d33b2e602650cf0787577ead125a6353b0b06e9340393d61418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e971ffaf9aa87ebcddf440f00e4bb050afe82a64e9b0070dabba419ebfa2140`

```dockerfile
```

-	Layers:
	-	`sha256:c4dd9d0c8559612a8c28b96464a4f88b18677960d1b55fca55eb0ce8a16c1f67`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 3.7 MB (3695776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6ffb8d1359a260a352514d000b97d678d52467c0e986767eef662657452987`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 24.4 KB (24350 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-11` - linux; s390x

```console
$ docker pull zookeeper@sha256:b3cd26c491151245711a477ffe367831a844cec0188d000a369f8a16e652abe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100798240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d21b387f1be15bc58a4b781e1f57a5879432396f61b8495735426fac40c581c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b0d2d51f17dc8c7a928be9c46547313e9a50f29bb15f2cc88dc408556588e2`  
		Last Modified: Tue, 17 Sep 2024 01:39:29 GMT  
		Size: 40.8 MB (40816924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e98695f5534c20f90ede714390d956f690a08aa9bca31099e0d5a5c6853afb0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61849bbb51fce6c876b245ec616269a488aad010dc7f1fb914ab8e3c9f4162d5`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725d3a46e59dd488f43df686e38af7baecd724255bdff884afaf5650e0e851c4`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0509cd6f0dbcc551513f9da6a959b40fb609220913316a79df6c493ed5b294bc`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 4.2 MB (4242062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8eb67e27f3222d42b73f93f816b5d07389491af4938ba681c5d5e0b38a6e3`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 14.1 MB (14139947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f525f40522b2d95f4568e9086b38209b1e4c5a4b7ac683c8fd14be8c9e32222d`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:dc205eac2d3ecd0f1218d3d1fba1243954e270a4369470d7b99f44038a75601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c156c6756b28cce43372e9d69cf90671d9c3bcb1000b3e85671ed8ae949259`

```dockerfile
```

-	Layers:
	-	`sha256:cbffe67b123ffe761f9f40769e7e31b932cba3bd69a5394ef7654153d9a04475`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 3.7 MB (3692325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1bb72bbb05b5ee5b03134bfdec027eb7f86def6398495a2105b3da6271bba3`  
		Last Modified: Tue, 17 Sep 2024 03:59:20 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.7-jre-17`

```console
$ docker pull zookeeper@sha256:3d97bc6fa9b093e534aeb46ae99b6c313a13b0cfb96677d1d9305379d97ab663
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.7-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:6d6d2711b38fe11bc52596aaf79a02692a3a578760ccea5537c0c4cd32ae7050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109101826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b45a129fe9de207c483a75cdfc74d2555d3c0f4c2dfdf4125b2cee3a971504`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Mon, 16 Oct 2023 06:33:19 GMT
ARG RELEASE
# Mon, 16 Oct 2023 06:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 16 Oct 2023 06:33:19 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["/bin/bash"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Oct 2023 06:33:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 16 Oct 2023 06:33:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Mon, 16 Oct 2023 06:33:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
VOLUME [/data /datalog /logs]
# Mon, 16 Oct 2023 06:33:19 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Mon, 16 Oct 2023 06:33:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c22e31624601170b91941dc9f9f7292f907fb766e1ac13a1dee00b841b1ef`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873ba3cf8e83afdec75a9eb1ca0d1deabb400cb794ccc8253e7f7086beb740ec`  
		Last Modified: Tue, 17 Sep 2024 02:01:09 GMT  
		Size: 4.4 MB (4365990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a999717163a403c4e8487a8c24253be1b15f3a62eca17cab95396f5c639c13e`  
		Last Modified: Tue, 17 Sep 2024 02:01:10 GMT  
		Size: 14.1 MB (14139969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bc8e39b2930d1acf30446954ce8ac6d37aa83e8ad71341e08decadecac298`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:aa736c5685c121c8230301f4101301098c618e2b24e6cdb01a28385fd466febf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e533315f8694c26a215a6455a0ab8b747618161aa4249455d554b2afe7f3d3`

```dockerfile
```

-	Layers:
	-	`sha256:15455989bcf25afb2e11e7603d3954152dc66e1c8c3ae8d2784afc74e504a96f`  
		Last Modified: Tue, 17 Sep 2024 02:01:09 GMT  
		Size: 3.7 MB (3690610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb3b7282909e88ca70b93a68e3625b3435182901990fd78d3be0087488d4488`  
		Last Modified: Tue, 17 Sep 2024 02:01:09 GMT  
		Size: 23.7 KB (23690 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:2a2a96eb0e232a4d30ac6d0f4f851a5482b2422da402e9ea30e724ebae5fb8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106371237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd65a00581d2a84b76f24eeb7a5e59c36e72abe29824b89391aa577b317eeac3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Mon, 16 Oct 2023 06:33:19 GMT
ARG RELEASE
# Mon, 16 Oct 2023 06:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 16 Oct 2023 06:33:19 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["/bin/bash"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Oct 2023 06:33:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 16 Oct 2023 06:33:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Mon, 16 Oct 2023 06:33:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
VOLUME [/data /datalog /logs]
# Mon, 16 Oct 2023 06:33:19 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Mon, 16 Oct 2023 06:33:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ea18d37e82ca7216449a13fac7f69217b68333c87cf16d6d356794e9c369e`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990c746484df95d66cf384962ed7ec84948d939d53ace21611666c129f2d68`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 4.3 MB (4269684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc57b8429eb99bd70037dad28b49f691b894fa5c5bafca3599cd2099b957b4e`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 14.1 MB (14139980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ca18c6b213052d309f67311c50fdf31e3bb5a71f73e49d03e964a0feeb1199`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7724efa8a868ee886383fffcfbe618b0274d7048e1007c84dc6bf671ce7b54e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e133367c6634092fa92311198b412e9067ba555c246021569c85effc024057d`

```dockerfile
```

-	Layers:
	-	`sha256:a10a64f3c8f618d76b6aa86f0bbee02f271b935694254926a7645d7fad072dab`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 3.7 MB (3690885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0a3d996b535037eefe91df483edea9844c79066dd591bd5d70212ac5fd12ca`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 24.0 KB (23983 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:593d9e5177d5778450dcb7eb94bee7638c132bb69f8e2e39d4d2b17a8a329843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115529600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53e24d3c3fed7f86f9388ea7c712193244c0688546ea074bbc491ee8948d43b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Mon, 16 Oct 2023 06:33:19 GMT
ARG RELEASE
# Mon, 16 Oct 2023 06:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 16 Oct 2023 06:33:19 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["/bin/bash"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Oct 2023 06:33:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 16 Oct 2023 06:33:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Mon, 16 Oct 2023 06:33:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
VOLUME [/data /datalog /logs]
# Mon, 16 Oct 2023 06:33:19 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Mon, 16 Oct 2023 06:33:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc895576af9cea3bc6748630114d80e9d68ab614d0dcd495a557016c4c90d6`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0e26d81209f6a2da5cec43641648e9d9f89d16e14c99d5623d092adea4482`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 5.0 MB (4966005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6570fcb67cbc11d565fa90e05a61887b95a4a58856549a177530ad51be3412`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 14.1 MB (14139984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68ff2949a94eed9954b38b133590e5a76fee00bdfd1662744cb8ec3fe818320`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:a9218c963181c975640745f1ea3e2aacdc07a1027c33566c7b0b175ac90ebea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c94ba56a4591aaf7131642c2e47750789b4d9a66d257a0151d5fbdc47f936b`

```dockerfile
```

-	Layers:
	-	`sha256:037142eeb5c5d774b0344bb2b4ee75f850c7a1aa5e2906ebd052944ebd3d8725`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 3.7 MB (3695164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0935b67e2e1284287638c6585bf2b9f84a682494da56e1548bd0c7c3d69f4ae0`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 23.7 KB (23719 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:43c5a7a90a82efe5d8aae88b81e43a8785f6f0d974dd36c7e2ff05c3c7e0036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103845558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2af09cc6c12c5f2a040dda8b8cba2c69523526806cb6e894fa569da1030128d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Mon, 16 Oct 2023 06:33:19 GMT
ARG RELEASE
# Mon, 16 Oct 2023 06:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 16 Oct 2023 06:33:19 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["/bin/bash"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Oct 2023 06:33:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 16 Oct 2023 06:33:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Mon, 16 Oct 2023 06:33:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
VOLUME [/data /datalog /logs]
# Mon, 16 Oct 2023 06:33:19 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Mon, 16 Oct 2023 06:33:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1eb2e01f4164208070c21c1525ad5da7aaed86dd78dd248957b88c24c71c8`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc844baa2089b0df873e8304e4362d3317a2927ddbd583094f621de0d0fdec`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 4.2 MB (4242071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d1097a74a4de42a49bfa8435b08150498dcbd593d3f2a0223996bfe755f2b6`  
		Last Modified: Tue, 17 Sep 2024 04:00:00 GMT  
		Size: 14.1 MB (14139992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3fa476ce185daa1a022c6a2019607d38f5498e683bb039495967e6f8d2a360`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:32af30278bf380cbd3f6204d79945d5b09489ebe2826af50ca8bd9a18dd29aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4925d3c867753f6f856a7b316f7ed48379c2a35d70b44742f52d991f4c943dbc`

```dockerfile
```

-	Layers:
	-	`sha256:fa1b8cec0ef94d851ba86ab72c79b5c869bc51230c4d71b906307a5934b66876`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 3.7 MB (3691725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd39a30f6993ec39c8a5d0039d7c72f99048250efc51368cf3da573db0f14cbd`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 23.7 KB (23689 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.7.2`

```console
$ docker pull zookeeper@sha256:f7b24ec76ae0bc2287db56db41004218f042a06b034eb3c33631e130c5c1ba7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.7.2` - linux; amd64

```console
$ docker pull zookeeper@sha256:49bec9e4ef73906e1ef815848ebb5606f18f57158b094e46bbf636b18b97c2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109020464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0d7e840425b565fedb1418c0101e2177add1523c8620a513f355f835fe2c64`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f17d82e63e7d03b5c7593a78c97b3e47cbae3a10a73272397b9198b29118dc`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.2 MB (47198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160911679b1063ecd6051528d8a67a77b522a6e2265098a70b7dd4b957ea7188`  
		Last Modified: Tue, 17 Sep 2024 01:09:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc57f7209badbf5d0fdfb0a3134519f8fd3ec56991ba6c688228e2b9d07ad8d`  
		Last Modified: Tue, 17 Sep 2024 01:09:05 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bee863ffa3fcee8682b357ea9d71284e5a14cce82f021892836d8ce9cd46166`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04082e569171eafe6ee925415046eb2e455e88ab8ed56bbc888dfe39936752e0`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 4.4 MB (4365980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bc98bb4a7d42e8f677d99fc12c429932fd09c136c0146bcb159bca157e1315`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 14.1 MB (14139932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e4d6bbbcfa1422b86f4aebc760c60e056a6da792c2e1f078c5931f06802e22`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:3ac2fd4377e5c7c1c7f787de484df556426617268902a6c1a7259ec58052a968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97caaa8616bc62e253a20fd9954279a884376abb29ec740595e7ac166084eb3`

```dockerfile
```

-	Layers:
	-	`sha256:7dcdd89acf7403eb159ef48ea1e26ad4ce6d44f83b762fc2204a9e54a7604240`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 3.7 MB (3691210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ff0e0f8a567bf5620c0400a29092ea8ee0cadf74a5e7cede4964e84784627f`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:c5b2e34b13c477fcfc3e209a3693dc89662ca3e0d8283bb6f9f9669ecc2300bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105182005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671ab979eb754ab8e33ee357e97f9725a66d29681acc102e2c2a3000fa92da08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dbb8ab7ebb70bbdbb49ab2085d99ae87968ea251f304e9fa059e7155f13e5`  
		Last Modified: Sat, 17 Aug 2024 01:35:00 GMT  
		Size: 45.6 MB (45557024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ed86303b2ff16bd4b17f7c739a9055711b72b99e566885505d9258cd44e26c`  
		Last Modified: Sat, 17 Aug 2024 01:34:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604cf0e08e3afff9c340aa7610394aaab11665931337af35d9c0e0f3b770c4b`  
		Last Modified: Fri, 23 Aug 2024 19:44:09 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb96a3b62851bd2e4b8518ec62e30d0f300faabe146629138a2f8a97cef1b37`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc83dde9fdedb0c360eadfd1c7f81516081a7e5fc187ecb13fd488826c82ebd`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 4.3 MB (4269748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a546e2aa7b6898ddca2ff1e78bb4ab8492f0928c163edd339ed36fe8006326`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 14.1 MB (14139949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93b1ca6b5cb92e6debc33121aaf09ec2125a62c555cf7a9bab66c10d011ffb`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8b89b9e387ea868aaec7063fc06694a086f83957903a9733b2f43dc5bc8f411e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c807c7912c9c373ee20444ea4f5ee43b122b2fedbcd86a76ed397b83c87c3a`

```dockerfile
```

-	Layers:
	-	`sha256:561ebaa605ddc1a5e348cec02798ac0e3d0ff3fcdaba08a1eb1b968260bd4c0c`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 3.7 MB (3691509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134bae314652251f5d0231fd8e0fefa163c3c0e635bf0ef0f46952128213d14b`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 24.6 KB (24624 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:a98319a27611c47e4a17dcf6f9b5d94d245600684b94633b85cf5dfc0a58dfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111065644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d0e6f0039ae50639a963d87afb21faab1aa8d42aa63241f616fa3fa3d17b96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b50c4b0fab19a16a502b1681ff9177a05eed203d81aa04a49df18907898c34`  
		Last Modified: Sat, 17 Aug 2024 01:01:26 GMT  
		Size: 42.7 MB (42652048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338034862f9398ecf41f81f3eb5a9837d4cbe84271d6141f09462837e4a51105`  
		Last Modified: Sat, 17 Aug 2024 01:01:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a3378494275db0692fa539ce9a900d0fdd467054c1b7a1322760ca73ff5eb2`  
		Last Modified: Fri, 23 Aug 2024 19:23:06 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ecabe37fef307cd1c24d32107c6941b57f8f7d4262129f55f4929aff1527be`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12458516b171038549020e80b57d35e844a5f158820b64bf1edead353209662`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 5.0 MB (4966048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f4e2e656f98538a304d968437b934df9c9da53acbc6cb91c2786405b1ec4f`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 14.1 MB (14139951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe0644314e3d3349d000216b137b05413b99b186855058d96e8ad8acd1da2c9`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:2ae6a968f90b0d33b2e602650cf0787577ead125a6353b0b06e9340393d61418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e971ffaf9aa87ebcddf440f00e4bb050afe82a64e9b0070dabba419ebfa2140`

```dockerfile
```

-	Layers:
	-	`sha256:c4dd9d0c8559612a8c28b96464a4f88b18677960d1b55fca55eb0ce8a16c1f67`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 3.7 MB (3695776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6ffb8d1359a260a352514d000b97d678d52467c0e986767eef662657452987`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 24.4 KB (24350 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2` - linux; s390x

```console
$ docker pull zookeeper@sha256:b3cd26c491151245711a477ffe367831a844cec0188d000a369f8a16e652abe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100798240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d21b387f1be15bc58a4b781e1f57a5879432396f61b8495735426fac40c581c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b0d2d51f17dc8c7a928be9c46547313e9a50f29bb15f2cc88dc408556588e2`  
		Last Modified: Tue, 17 Sep 2024 01:39:29 GMT  
		Size: 40.8 MB (40816924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e98695f5534c20f90ede714390d956f690a08aa9bca31099e0d5a5c6853afb0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61849bbb51fce6c876b245ec616269a488aad010dc7f1fb914ab8e3c9f4162d5`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725d3a46e59dd488f43df686e38af7baecd724255bdff884afaf5650e0e851c4`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0509cd6f0dbcc551513f9da6a959b40fb609220913316a79df6c493ed5b294bc`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 4.2 MB (4242062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8eb67e27f3222d42b73f93f816b5d07389491af4938ba681c5d5e0b38a6e3`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 14.1 MB (14139947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f525f40522b2d95f4568e9086b38209b1e4c5a4b7ac683c8fd14be8c9e32222d`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:dc205eac2d3ecd0f1218d3d1fba1243954e270a4369470d7b99f44038a75601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c156c6756b28cce43372e9d69cf90671d9c3bcb1000b3e85671ed8ae949259`

```dockerfile
```

-	Layers:
	-	`sha256:cbffe67b123ffe761f9f40769e7e31b932cba3bd69a5394ef7654153d9a04475`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 3.7 MB (3692325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1bb72bbb05b5ee5b03134bfdec027eb7f86def6398495a2105b3da6271bba3`  
		Last Modified: Tue, 17 Sep 2024 03:59:20 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.7.2-jre-11`

```console
$ docker pull zookeeper@sha256:f7b24ec76ae0bc2287db56db41004218f042a06b034eb3c33631e130c5c1ba7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.7.2-jre-11` - linux; amd64

```console
$ docker pull zookeeper@sha256:49bec9e4ef73906e1ef815848ebb5606f18f57158b094e46bbf636b18b97c2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109020464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0d7e840425b565fedb1418c0101e2177add1523c8620a513f355f835fe2c64`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f17d82e63e7d03b5c7593a78c97b3e47cbae3a10a73272397b9198b29118dc`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.2 MB (47198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160911679b1063ecd6051528d8a67a77b522a6e2265098a70b7dd4b957ea7188`  
		Last Modified: Tue, 17 Sep 2024 01:09:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc57f7209badbf5d0fdfb0a3134519f8fd3ec56991ba6c688228e2b9d07ad8d`  
		Last Modified: Tue, 17 Sep 2024 01:09:05 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bee863ffa3fcee8682b357ea9d71284e5a14cce82f021892836d8ce9cd46166`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04082e569171eafe6ee925415046eb2e455e88ab8ed56bbc888dfe39936752e0`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 4.4 MB (4365980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bc98bb4a7d42e8f677d99fc12c429932fd09c136c0146bcb159bca157e1315`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 14.1 MB (14139932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e4d6bbbcfa1422b86f4aebc760c60e056a6da792c2e1f078c5931f06802e22`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:3ac2fd4377e5c7c1c7f787de484df556426617268902a6c1a7259ec58052a968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97caaa8616bc62e253a20fd9954279a884376abb29ec740595e7ac166084eb3`

```dockerfile
```

-	Layers:
	-	`sha256:7dcdd89acf7403eb159ef48ea1e26ad4ce6d44f83b762fc2204a9e54a7604240`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 3.7 MB (3691210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ff0e0f8a567bf5620c0400a29092ea8ee0cadf74a5e7cede4964e84784627f`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-11` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:c5b2e34b13c477fcfc3e209a3693dc89662ca3e0d8283bb6f9f9669ecc2300bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105182005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671ab979eb754ab8e33ee357e97f9725a66d29681acc102e2c2a3000fa92da08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dbb8ab7ebb70bbdbb49ab2085d99ae87968ea251f304e9fa059e7155f13e5`  
		Last Modified: Sat, 17 Aug 2024 01:35:00 GMT  
		Size: 45.6 MB (45557024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ed86303b2ff16bd4b17f7c739a9055711b72b99e566885505d9258cd44e26c`  
		Last Modified: Sat, 17 Aug 2024 01:34:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604cf0e08e3afff9c340aa7610394aaab11665931337af35d9c0e0f3b770c4b`  
		Last Modified: Fri, 23 Aug 2024 19:44:09 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb96a3b62851bd2e4b8518ec62e30d0f300faabe146629138a2f8a97cef1b37`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc83dde9fdedb0c360eadfd1c7f81516081a7e5fc187ecb13fd488826c82ebd`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 4.3 MB (4269748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a546e2aa7b6898ddca2ff1e78bb4ab8492f0928c163edd339ed36fe8006326`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 14.1 MB (14139949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93b1ca6b5cb92e6debc33121aaf09ec2125a62c555cf7a9bab66c10d011ffb`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8b89b9e387ea868aaec7063fc06694a086f83957903a9733b2f43dc5bc8f411e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c807c7912c9c373ee20444ea4f5ee43b122b2fedbcd86a76ed397b83c87c3a`

```dockerfile
```

-	Layers:
	-	`sha256:561ebaa605ddc1a5e348cec02798ac0e3d0ff3fcdaba08a1eb1b968260bd4c0c`  
		Last Modified: Sat, 24 Aug 2024 01:34:29 GMT  
		Size: 3.7 MB (3691509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134bae314652251f5d0231fd8e0fefa163c3c0e635bf0ef0f46952128213d14b`  
		Last Modified: Sat, 24 Aug 2024 01:34:28 GMT  
		Size: 24.6 KB (24624 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-11` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:a98319a27611c47e4a17dcf6f9b5d94d245600684b94633b85cf5dfc0a58dfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111065644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d0e6f0039ae50639a963d87afb21faab1aa8d42aa63241f616fa3fa3d17b96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b50c4b0fab19a16a502b1681ff9177a05eed203d81aa04a49df18907898c34`  
		Last Modified: Sat, 17 Aug 2024 01:01:26 GMT  
		Size: 42.7 MB (42652048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338034862f9398ecf41f81f3eb5a9837d4cbe84271d6141f09462837e4a51105`  
		Last Modified: Sat, 17 Aug 2024 01:01:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a3378494275db0692fa539ce9a900d0fdd467054c1b7a1322760ca73ff5eb2`  
		Last Modified: Fri, 23 Aug 2024 19:23:06 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ecabe37fef307cd1c24d32107c6941b57f8f7d4262129f55f4929aff1527be`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12458516b171038549020e80b57d35e844a5f158820b64bf1edead353209662`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 5.0 MB (4966048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f4e2e656f98538a304d968437b934df9c9da53acbc6cb91c2786405b1ec4f`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 14.1 MB (14139951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe0644314e3d3349d000216b137b05413b99b186855058d96e8ad8acd1da2c9`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:2ae6a968f90b0d33b2e602650cf0787577ead125a6353b0b06e9340393d61418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e971ffaf9aa87ebcddf440f00e4bb050afe82a64e9b0070dabba419ebfa2140`

```dockerfile
```

-	Layers:
	-	`sha256:c4dd9d0c8559612a8c28b96464a4f88b18677960d1b55fca55eb0ce8a16c1f67`  
		Last Modified: Fri, 23 Aug 2024 20:53:53 GMT  
		Size: 3.7 MB (3695776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6ffb8d1359a260a352514d000b97d678d52467c0e986767eef662657452987`  
		Last Modified: Fri, 23 Aug 2024 20:53:52 GMT  
		Size: 24.4 KB (24350 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-11` - linux; s390x

```console
$ docker pull zookeeper@sha256:b3cd26c491151245711a477ffe367831a844cec0188d000a369f8a16e652abe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100798240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d21b387f1be15bc58a4b781e1f57a5879432396f61b8495735426fac40c581c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Sun, 28 Jul 2024 06:22:36 GMT
ARG RELEASE
# Sun, 28 Jul 2024 06:22:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 28 Jul 2024 06:22:36 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 28 Jul 2024 06:22:36 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Jul 2024 06:22:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Sun, 28 Jul 2024 06:22:36 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Sun, 28 Jul 2024 06:22:36 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Sun, 28 Jul 2024 06:22:36 GMT
VOLUME [/data /datalog /logs]
# Sun, 28 Jul 2024 06:22:36 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Sun, 28 Jul 2024 06:22:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Sun, 28 Jul 2024 06:22:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 28 Jul 2024 06:22:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b0d2d51f17dc8c7a928be9c46547313e9a50f29bb15f2cc88dc408556588e2`  
		Last Modified: Tue, 17 Sep 2024 01:39:29 GMT  
		Size: 40.8 MB (40816924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e98695f5534c20f90ede714390d956f690a08aa9bca31099e0d5a5c6853afb0`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61849bbb51fce6c876b245ec616269a488aad010dc7f1fb914ab8e3c9f4162d5`  
		Last Modified: Tue, 17 Sep 2024 01:39:23 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725d3a46e59dd488f43df686e38af7baecd724255bdff884afaf5650e0e851c4`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0509cd6f0dbcc551513f9da6a959b40fb609220913316a79df6c493ed5b294bc`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 4.2 MB (4242062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8eb67e27f3222d42b73f93f816b5d07389491af4938ba681c5d5e0b38a6e3`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 14.1 MB (14139947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f525f40522b2d95f4568e9086b38209b1e4c5a4b7ac683c8fd14be8c9e32222d`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:dc205eac2d3ecd0f1218d3d1fba1243954e270a4369470d7b99f44038a75601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c156c6756b28cce43372e9d69cf90671d9c3bcb1000b3e85671ed8ae949259`

```dockerfile
```

-	Layers:
	-	`sha256:cbffe67b123ffe761f9f40769e7e31b932cba3bd69a5394ef7654153d9a04475`  
		Last Modified: Tue, 17 Sep 2024 03:59:21 GMT  
		Size: 3.7 MB (3692325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1bb72bbb05b5ee5b03134bfdec027eb7f86def6398495a2105b3da6271bba3`  
		Last Modified: Tue, 17 Sep 2024 03:59:20 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.7.2-jre-17`

```console
$ docker pull zookeeper@sha256:3d97bc6fa9b093e534aeb46ae99b6c313a13b0cfb96677d1d9305379d97ab663
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.7.2-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:6d6d2711b38fe11bc52596aaf79a02692a3a578760ccea5537c0c4cd32ae7050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109101826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b45a129fe9de207c483a75cdfc74d2555d3c0f4c2dfdf4125b2cee3a971504`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Mon, 16 Oct 2023 06:33:19 GMT
ARG RELEASE
# Mon, 16 Oct 2023 06:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 16 Oct 2023 06:33:19 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["/bin/bash"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Oct 2023 06:33:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 16 Oct 2023 06:33:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Mon, 16 Oct 2023 06:33:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
VOLUME [/data /datalog /logs]
# Mon, 16 Oct 2023 06:33:19 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Mon, 16 Oct 2023 06:33:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c22e31624601170b91941dc9f9f7292f907fb766e1ac13a1dee00b841b1ef`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873ba3cf8e83afdec75a9eb1ca0d1deabb400cb794ccc8253e7f7086beb740ec`  
		Last Modified: Tue, 17 Sep 2024 02:01:09 GMT  
		Size: 4.4 MB (4365990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a999717163a403c4e8487a8c24253be1b15f3a62eca17cab95396f5c639c13e`  
		Last Modified: Tue, 17 Sep 2024 02:01:10 GMT  
		Size: 14.1 MB (14139969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bc8e39b2930d1acf30446954ce8ac6d37aa83e8ad71341e08decadecac298`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:aa736c5685c121c8230301f4101301098c618e2b24e6cdb01a28385fd466febf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e533315f8694c26a215a6455a0ab8b747618161aa4249455d554b2afe7f3d3`

```dockerfile
```

-	Layers:
	-	`sha256:15455989bcf25afb2e11e7603d3954152dc66e1c8c3ae8d2784afc74e504a96f`  
		Last Modified: Tue, 17 Sep 2024 02:01:09 GMT  
		Size: 3.7 MB (3690610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb3b7282909e88ca70b93a68e3625b3435182901990fd78d3be0087488d4488`  
		Last Modified: Tue, 17 Sep 2024 02:01:09 GMT  
		Size: 23.7 KB (23690 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:2a2a96eb0e232a4d30ac6d0f4f851a5482b2422da402e9ea30e724ebae5fb8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106371237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd65a00581d2a84b76f24eeb7a5e59c36e72abe29824b89391aa577b317eeac3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Mon, 16 Oct 2023 06:33:19 GMT
ARG RELEASE
# Mon, 16 Oct 2023 06:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 16 Oct 2023 06:33:19 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["/bin/bash"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Oct 2023 06:33:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 16 Oct 2023 06:33:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Mon, 16 Oct 2023 06:33:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
VOLUME [/data /datalog /logs]
# Mon, 16 Oct 2023 06:33:19 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Mon, 16 Oct 2023 06:33:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ea18d37e82ca7216449a13fac7f69217b68333c87cf16d6d356794e9c369e`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990c746484df95d66cf384962ed7ec84948d939d53ace21611666c129f2d68`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 4.3 MB (4269684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc57b8429eb99bd70037dad28b49f691b894fa5c5bafca3599cd2099b957b4e`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 14.1 MB (14139980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ca18c6b213052d309f67311c50fdf31e3bb5a71f73e49d03e964a0feeb1199`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7724efa8a868ee886383fffcfbe618b0274d7048e1007c84dc6bf671ce7b54e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e133367c6634092fa92311198b412e9067ba555c246021569c85effc024057d`

```dockerfile
```

-	Layers:
	-	`sha256:a10a64f3c8f618d76b6aa86f0bbee02f271b935694254926a7645d7fad072dab`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 3.7 MB (3690885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0a3d996b535037eefe91df483edea9844c79066dd591bd5d70212ac5fd12ca`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 24.0 KB (23983 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:593d9e5177d5778450dcb7eb94bee7638c132bb69f8e2e39d4d2b17a8a329843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115529600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53e24d3c3fed7f86f9388ea7c712193244c0688546ea074bbc491ee8948d43b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Mon, 16 Oct 2023 06:33:19 GMT
ARG RELEASE
# Mon, 16 Oct 2023 06:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 16 Oct 2023 06:33:19 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["/bin/bash"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Oct 2023 06:33:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 16 Oct 2023 06:33:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Mon, 16 Oct 2023 06:33:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
VOLUME [/data /datalog /logs]
# Mon, 16 Oct 2023 06:33:19 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Mon, 16 Oct 2023 06:33:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc895576af9cea3bc6748630114d80e9d68ab614d0dcd495a557016c4c90d6`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0e26d81209f6a2da5cec43641648e9d9f89d16e14c99d5623d092adea4482`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 5.0 MB (4966005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6570fcb67cbc11d565fa90e05a61887b95a4a58856549a177530ad51be3412`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 14.1 MB (14139984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68ff2949a94eed9954b38b133590e5a76fee00bdfd1662744cb8ec3fe818320`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:a9218c963181c975640745f1ea3e2aacdc07a1027c33566c7b0b175ac90ebea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c94ba56a4591aaf7131642c2e47750789b4d9a66d257a0151d5fbdc47f936b`

```dockerfile
```

-	Layers:
	-	`sha256:037142eeb5c5d774b0344bb2b4ee75f850c7a1aa5e2906ebd052944ebd3d8725`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 3.7 MB (3695164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0935b67e2e1284287638c6585bf2b9f84a682494da56e1548bd0c7c3d69f4ae0`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 23.7 KB (23719 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:43c5a7a90a82efe5d8aae88b81e43a8785f6f0d974dd36c7e2ff05c3c7e0036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103845558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2af09cc6c12c5f2a040dda8b8cba2c69523526806cb6e894fa569da1030128d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Mon, 16 Oct 2023 06:33:19 GMT
ARG RELEASE
# Mon, 16 Oct 2023 06:33:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Oct 2023 06:33:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 16 Oct 2023 06:33:19 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["/bin/bash"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Oct 2023 06:33:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 16 Oct 2023 06:33:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.7.2
# Mon, 16 Oct 2023 06:33:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.7.2 DISTRO_NAME=apache-zookeeper-3.7.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
WORKDIR /apache-zookeeper-3.7.2-bin
# Mon, 16 Oct 2023 06:33:19 GMT
VOLUME [/data /datalog /logs]
# Mon, 16 Oct 2023 06:33:19 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 16 Oct 2023 06:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.7.2-bin/bin ZOOCFGDIR=/conf
# Mon, 16 Oct 2023 06:33:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Oct 2023 06:33:19 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1eb2e01f4164208070c21c1525ad5da7aaed86dd78dd248957b88c24c71c8`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc844baa2089b0df873e8304e4362d3317a2927ddbd583094f621de0d0fdec`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 4.2 MB (4242071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d1097a74a4de42a49bfa8435b08150498dcbd593d3f2a0223996bfe755f2b6`  
		Last Modified: Tue, 17 Sep 2024 04:00:00 GMT  
		Size: 14.1 MB (14139992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3fa476ce185daa1a022c6a2019607d38f5498e683bb039495967e6f8d2a360`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:32af30278bf380cbd3f6204d79945d5b09489ebe2826af50ca8bd9a18dd29aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4925d3c867753f6f856a7b316f7ed48379c2a35d70b44742f52d991f4c943dbc`

```dockerfile
```

-	Layers:
	-	`sha256:fa1b8cec0ef94d851ba86ab72c79b5c869bc51230c4d71b906307a5934b66876`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 3.7 MB (3691725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd39a30f6993ec39c8a5d0039d7c72f99048250efc51368cf3da573db0f14cbd`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 23.7 KB (23689 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8`

```console
$ docker pull zookeeper@sha256:e833246903d79395a0ace119f3610fe992808716703d1322b3283d19d7571ea2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.8` - linux; amd64

```console
$ docker pull zookeeper@sha256:4cee5c60bae83f9fec8d1bd8da64583753ea9e90aa35f879a506f43720cfd041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109644746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb521042e18b827b4ca994175545ab0e2443eaa48a7ec98bc01aa7155864f86`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c22e31624601170b91941dc9f9f7292f907fb766e1ac13a1dee00b841b1ef`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed412f8e1db3e103100d0952d9f239df0502e0d1c7f9c7ce47490bde2027ba4`  
		Last Modified: Tue, 17 Sep 2024 02:01:06 GMT  
		Size: 4.4 MB (4365977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a93332ad68ad0fa57548749079219fc7f08161feb01fbe6835b08604808196`  
		Last Modified: Tue, 17 Sep 2024 02:01:06 GMT  
		Size: 14.7 MB (14682902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bc8e39b2930d1acf30446954ce8ac6d37aa83e8ad71341e08decadecac298`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7f03762bb5d12486206fc9d6dfd64a40eaf25f208093ef4b6d40427ca178566d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827f382d28cdd06610d58a18e44efcc21224d79ba7275019fa55c0219ac9f750`

```dockerfile
```

-	Layers:
	-	`sha256:f66d4d47d61a966f95f9b2cca5736b10398baa10c3bdf6358fd9bfdaffc6993e`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 2.3 KB (2271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8f1d6dc5ffc091b542a024989b504532680447ef73026767403c1f50372234`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:039c64b811f6899ce14fa3a4dfbbc84311990ce425a154dc16ee4134efc62bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106914142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2356f2106dd6637f395be3f692528e85299a01cd31383a9a0714b881bed94cb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ea18d37e82ca7216449a13fac7f69217b68333c87cf16d6d356794e9c369e`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990c746484df95d66cf384962ed7ec84948d939d53ace21611666c129f2d68`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 4.3 MB (4269684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5b85a95f1a10e6e7d26ada6777d99a91c5c5c9007e8dbaa57bf51682a6c7e0`  
		Last Modified: Fri, 23 Aug 2024 23:27:36 GMT  
		Size: 14.7 MB (14682885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a44392360c56a99450248ee6b0e11d0ac62fad68a402b614c50ab6fbd18a418`  
		Last Modified: Fri, 23 Aug 2024 23:27:35 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:62ec2886389278c2c6d4d9084c8f63ae70c0ac1e1320f432cfd8d2c7f00fab05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3717549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbb3dd8135494c36dd528e2b65adb393ff1f0c6b64eb72661f7dc42fdc69533`

```dockerfile
```

-	Layers:
	-	`sha256:7969ff2210332486b6fd98a43b13077da20e3f3bf709e14751e0c0f0309ef7aa`  
		Last Modified: Fri, 23 Aug 2024 23:27:36 GMT  
		Size: 3.7 MB (3692942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf268f9aa6db649a7b978a2992837334008b89874329e2bc5a6045e34055465d`  
		Last Modified: Fri, 23 Aug 2024 23:27:35 GMT  
		Size: 24.6 KB (24607 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:99d716adc47fa48bbfd4fcd9ba0210bd8cc2430ebdc3cbb485d6ad6df524028f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116072468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285b4b8ab121066611015d5a251188eaa1d4a76714bc053f1668761cee83b86d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc895576af9cea3bc6748630114d80e9d68ab614d0dcd495a557016c4c90d6`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0e26d81209f6a2da5cec43641648e9d9f89d16e14c99d5623d092adea4482`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 5.0 MB (4966005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a264621b5c2ea64f2b93eb9cbecf244e24c683db84ab74a8cbdefed52875394d`  
		Last Modified: Fri, 23 Aug 2024 20:55:38 GMT  
		Size: 14.7 MB (14682853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a562dccda972264d6d6e8b44fc49ec803f5f00601a57f32638481f5b2ca3364`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:ad3795f9321c76cdd0da71d775471e95813188354af1f79553ce83f7a5dc837a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b5e3a9b2c1638a5a3a6bd6d35c7b3540ae499043a3d4d10e0f11a866224350`

```dockerfile
```

-	Layers:
	-	`sha256:cf5f87c67060f2e5379633e3072ecd72cd07711d62099a7ad8cf52fce0b71fe4`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 3.7 MB (3697209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ceb627bb3466360ac4de85bc565bba372e4dd0b305b131fc93459952241e93`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 24.3 KB (24332 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; s390x

```console
$ docker pull zookeeper@sha256:052166658ce887c8b6f1954f70540b769f3d9cba6e6e696603eb044164a3bac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104388493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0a950a33f9cec428be2cbd48b79bfbdfa12121c39937d4b4d4d5b5a5d251b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1eb2e01f4164208070c21c1525ad5da7aaed86dd78dd248957b88c24c71c8`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc844baa2089b0df873e8304e4362d3317a2927ddbd583094f621de0d0fdec`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 4.2 MB (4242071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af83382fbe6d2a35f3b74fe13551ce4623caf376e908bcdd348e02dfa276b674`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 14.7 MB (14682927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3681421bc5028ade4e4d997ed8998f51c4cfa0a0d1460512148b800ee18d078`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:cf8b44a0f76cc0295664581b6c04dfabeadbf7ae46348721b64a46f86c022034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9651fc229ad36362b4bc1e19a3ba0ce7077c2d189048fdcfc28dc70f7a222009`

```dockerfile
```

-	Layers:
	-	`sha256:3763e70318a29a586084260e092d62fa1a7bf4e8143818e57ba36fc8389a537f`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 3.7 MB (3693758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82aa081bfb4422af2fdc99d3decba054c3f3e819844260c0490f89a1b495e2e`  
		Last Modified: Tue, 17 Sep 2024 04:00:50 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8-jre-17`

```console
$ docker pull zookeeper@sha256:e833246903d79395a0ace119f3610fe992808716703d1322b3283d19d7571ea2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.8-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:4cee5c60bae83f9fec8d1bd8da64583753ea9e90aa35f879a506f43720cfd041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109644746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb521042e18b827b4ca994175545ab0e2443eaa48a7ec98bc01aa7155864f86`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c22e31624601170b91941dc9f9f7292f907fb766e1ac13a1dee00b841b1ef`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed412f8e1db3e103100d0952d9f239df0502e0d1c7f9c7ce47490bde2027ba4`  
		Last Modified: Tue, 17 Sep 2024 02:01:06 GMT  
		Size: 4.4 MB (4365977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a93332ad68ad0fa57548749079219fc7f08161feb01fbe6835b08604808196`  
		Last Modified: Tue, 17 Sep 2024 02:01:06 GMT  
		Size: 14.7 MB (14682902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bc8e39b2930d1acf30446954ce8ac6d37aa83e8ad71341e08decadecac298`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7f03762bb5d12486206fc9d6dfd64a40eaf25f208093ef4b6d40427ca178566d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827f382d28cdd06610d58a18e44efcc21224d79ba7275019fa55c0219ac9f750`

```dockerfile
```

-	Layers:
	-	`sha256:f66d4d47d61a966f95f9b2cca5736b10398baa10c3bdf6358fd9bfdaffc6993e`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 2.3 KB (2271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8f1d6dc5ffc091b542a024989b504532680447ef73026767403c1f50372234`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:039c64b811f6899ce14fa3a4dfbbc84311990ce425a154dc16ee4134efc62bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106914142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2356f2106dd6637f395be3f692528e85299a01cd31383a9a0714b881bed94cb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ea18d37e82ca7216449a13fac7f69217b68333c87cf16d6d356794e9c369e`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990c746484df95d66cf384962ed7ec84948d939d53ace21611666c129f2d68`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 4.3 MB (4269684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5b85a95f1a10e6e7d26ada6777d99a91c5c5c9007e8dbaa57bf51682a6c7e0`  
		Last Modified: Fri, 23 Aug 2024 23:27:36 GMT  
		Size: 14.7 MB (14682885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a44392360c56a99450248ee6b0e11d0ac62fad68a402b614c50ab6fbd18a418`  
		Last Modified: Fri, 23 Aug 2024 23:27:35 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:62ec2886389278c2c6d4d9084c8f63ae70c0ac1e1320f432cfd8d2c7f00fab05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3717549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbb3dd8135494c36dd528e2b65adb393ff1f0c6b64eb72661f7dc42fdc69533`

```dockerfile
```

-	Layers:
	-	`sha256:7969ff2210332486b6fd98a43b13077da20e3f3bf709e14751e0c0f0309ef7aa`  
		Last Modified: Fri, 23 Aug 2024 23:27:36 GMT  
		Size: 3.7 MB (3692942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf268f9aa6db649a7b978a2992837334008b89874329e2bc5a6045e34055465d`  
		Last Modified: Fri, 23 Aug 2024 23:27:35 GMT  
		Size: 24.6 KB (24607 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:99d716adc47fa48bbfd4fcd9ba0210bd8cc2430ebdc3cbb485d6ad6df524028f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116072468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285b4b8ab121066611015d5a251188eaa1d4a76714bc053f1668761cee83b86d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc895576af9cea3bc6748630114d80e9d68ab614d0dcd495a557016c4c90d6`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0e26d81209f6a2da5cec43641648e9d9f89d16e14c99d5623d092adea4482`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 5.0 MB (4966005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a264621b5c2ea64f2b93eb9cbecf244e24c683db84ab74a8cbdefed52875394d`  
		Last Modified: Fri, 23 Aug 2024 20:55:38 GMT  
		Size: 14.7 MB (14682853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a562dccda972264d6d6e8b44fc49ec803f5f00601a57f32638481f5b2ca3364`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:ad3795f9321c76cdd0da71d775471e95813188354af1f79553ce83f7a5dc837a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b5e3a9b2c1638a5a3a6bd6d35c7b3540ae499043a3d4d10e0f11a866224350`

```dockerfile
```

-	Layers:
	-	`sha256:cf5f87c67060f2e5379633e3072ecd72cd07711d62099a7ad8cf52fce0b71fe4`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 3.7 MB (3697209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ceb627bb3466360ac4de85bc565bba372e4dd0b305b131fc93459952241e93`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 24.3 KB (24332 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:052166658ce887c8b6f1954f70540b769f3d9cba6e6e696603eb044164a3bac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104388493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0a950a33f9cec428be2cbd48b79bfbdfa12121c39937d4b4d4d5b5a5d251b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1eb2e01f4164208070c21c1525ad5da7aaed86dd78dd248957b88c24c71c8`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc844baa2089b0df873e8304e4362d3317a2927ddbd583094f621de0d0fdec`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 4.2 MB (4242071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af83382fbe6d2a35f3b74fe13551ce4623caf376e908bcdd348e02dfa276b674`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 14.7 MB (14682927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3681421bc5028ade4e4d997ed8998f51c4cfa0a0d1460512148b800ee18d078`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:cf8b44a0f76cc0295664581b6c04dfabeadbf7ae46348721b64a46f86c022034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9651fc229ad36362b4bc1e19a3ba0ce7077c2d189048fdcfc28dc70f7a222009`

```dockerfile
```

-	Layers:
	-	`sha256:3763e70318a29a586084260e092d62fa1a7bf4e8143818e57ba36fc8389a537f`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 3.7 MB (3693758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82aa081bfb4422af2fdc99d3decba054c3f3e819844260c0490f89a1b495e2e`  
		Last Modified: Tue, 17 Sep 2024 04:00:50 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8.4`

```console
$ docker pull zookeeper@sha256:e833246903d79395a0ace119f3610fe992808716703d1322b3283d19d7571ea2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.8.4` - linux; amd64

```console
$ docker pull zookeeper@sha256:4cee5c60bae83f9fec8d1bd8da64583753ea9e90aa35f879a506f43720cfd041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109644746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb521042e18b827b4ca994175545ab0e2443eaa48a7ec98bc01aa7155864f86`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c22e31624601170b91941dc9f9f7292f907fb766e1ac13a1dee00b841b1ef`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed412f8e1db3e103100d0952d9f239df0502e0d1c7f9c7ce47490bde2027ba4`  
		Last Modified: Tue, 17 Sep 2024 02:01:06 GMT  
		Size: 4.4 MB (4365977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a93332ad68ad0fa57548749079219fc7f08161feb01fbe6835b08604808196`  
		Last Modified: Tue, 17 Sep 2024 02:01:06 GMT  
		Size: 14.7 MB (14682902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bc8e39b2930d1acf30446954ce8ac6d37aa83e8ad71341e08decadecac298`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7f03762bb5d12486206fc9d6dfd64a40eaf25f208093ef4b6d40427ca178566d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827f382d28cdd06610d58a18e44efcc21224d79ba7275019fa55c0219ac9f750`

```dockerfile
```

-	Layers:
	-	`sha256:f66d4d47d61a966f95f9b2cca5736b10398baa10c3bdf6358fd9bfdaffc6993e`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 2.3 KB (2271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8f1d6dc5ffc091b542a024989b504532680447ef73026767403c1f50372234`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:039c64b811f6899ce14fa3a4dfbbc84311990ce425a154dc16ee4134efc62bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106914142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2356f2106dd6637f395be3f692528e85299a01cd31383a9a0714b881bed94cb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ea18d37e82ca7216449a13fac7f69217b68333c87cf16d6d356794e9c369e`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990c746484df95d66cf384962ed7ec84948d939d53ace21611666c129f2d68`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 4.3 MB (4269684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5b85a95f1a10e6e7d26ada6777d99a91c5c5c9007e8dbaa57bf51682a6c7e0`  
		Last Modified: Fri, 23 Aug 2024 23:27:36 GMT  
		Size: 14.7 MB (14682885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a44392360c56a99450248ee6b0e11d0ac62fad68a402b614c50ab6fbd18a418`  
		Last Modified: Fri, 23 Aug 2024 23:27:35 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:62ec2886389278c2c6d4d9084c8f63ae70c0ac1e1320f432cfd8d2c7f00fab05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3717549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbb3dd8135494c36dd528e2b65adb393ff1f0c6b64eb72661f7dc42fdc69533`

```dockerfile
```

-	Layers:
	-	`sha256:7969ff2210332486b6fd98a43b13077da20e3f3bf709e14751e0c0f0309ef7aa`  
		Last Modified: Fri, 23 Aug 2024 23:27:36 GMT  
		Size: 3.7 MB (3692942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf268f9aa6db649a7b978a2992837334008b89874329e2bc5a6045e34055465d`  
		Last Modified: Fri, 23 Aug 2024 23:27:35 GMT  
		Size: 24.6 KB (24607 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:99d716adc47fa48bbfd4fcd9ba0210bd8cc2430ebdc3cbb485d6ad6df524028f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116072468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285b4b8ab121066611015d5a251188eaa1d4a76714bc053f1668761cee83b86d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc895576af9cea3bc6748630114d80e9d68ab614d0dcd495a557016c4c90d6`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0e26d81209f6a2da5cec43641648e9d9f89d16e14c99d5623d092adea4482`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 5.0 MB (4966005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a264621b5c2ea64f2b93eb9cbecf244e24c683db84ab74a8cbdefed52875394d`  
		Last Modified: Fri, 23 Aug 2024 20:55:38 GMT  
		Size: 14.7 MB (14682853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a562dccda972264d6d6e8b44fc49ec803f5f00601a57f32638481f5b2ca3364`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:ad3795f9321c76cdd0da71d775471e95813188354af1f79553ce83f7a5dc837a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b5e3a9b2c1638a5a3a6bd6d35c7b3540ae499043a3d4d10e0f11a866224350`

```dockerfile
```

-	Layers:
	-	`sha256:cf5f87c67060f2e5379633e3072ecd72cd07711d62099a7ad8cf52fce0b71fe4`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 3.7 MB (3697209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ceb627bb3466360ac4de85bc565bba372e4dd0b305b131fc93459952241e93`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 24.3 KB (24332 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4` - linux; s390x

```console
$ docker pull zookeeper@sha256:052166658ce887c8b6f1954f70540b769f3d9cba6e6e696603eb044164a3bac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104388493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0a950a33f9cec428be2cbd48b79bfbdfa12121c39937d4b4d4d5b5a5d251b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1eb2e01f4164208070c21c1525ad5da7aaed86dd78dd248957b88c24c71c8`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc844baa2089b0df873e8304e4362d3317a2927ddbd583094f621de0d0fdec`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 4.2 MB (4242071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af83382fbe6d2a35f3b74fe13551ce4623caf376e908bcdd348e02dfa276b674`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 14.7 MB (14682927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3681421bc5028ade4e4d997ed8998f51c4cfa0a0d1460512148b800ee18d078`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:cf8b44a0f76cc0295664581b6c04dfabeadbf7ae46348721b64a46f86c022034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9651fc229ad36362b4bc1e19a3ba0ce7077c2d189048fdcfc28dc70f7a222009`

```dockerfile
```

-	Layers:
	-	`sha256:3763e70318a29a586084260e092d62fa1a7bf4e8143818e57ba36fc8389a537f`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 3.7 MB (3693758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82aa081bfb4422af2fdc99d3decba054c3f3e819844260c0490f89a1b495e2e`  
		Last Modified: Tue, 17 Sep 2024 04:00:50 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8.4-jre-17`

```console
$ docker pull zookeeper@sha256:e833246903d79395a0ace119f3610fe992808716703d1322b3283d19d7571ea2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.8.4-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:4cee5c60bae83f9fec8d1bd8da64583753ea9e90aa35f879a506f43720cfd041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109644746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb521042e18b827b4ca994175545ab0e2443eaa48a7ec98bc01aa7155864f86`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7c22e31624601170b91941dc9f9f7292f907fb766e1ac13a1dee00b841b1ef`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed412f8e1db3e103100d0952d9f239df0502e0d1c7f9c7ce47490bde2027ba4`  
		Last Modified: Tue, 17 Sep 2024 02:01:06 GMT  
		Size: 4.4 MB (4365977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a93332ad68ad0fa57548749079219fc7f08161feb01fbe6835b08604808196`  
		Last Modified: Tue, 17 Sep 2024 02:01:06 GMT  
		Size: 14.7 MB (14682902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bc8e39b2930d1acf30446954ce8ac6d37aa83e8ad71341e08decadecac298`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7f03762bb5d12486206fc9d6dfd64a40eaf25f208093ef4b6d40427ca178566d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827f382d28cdd06610d58a18e44efcc21224d79ba7275019fa55c0219ac9f750`

```dockerfile
```

-	Layers:
	-	`sha256:f66d4d47d61a966f95f9b2cca5736b10398baa10c3bdf6358fd9bfdaffc6993e`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 2.3 KB (2271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8f1d6dc5ffc091b542a024989b504532680447ef73026767403c1f50372234`  
		Last Modified: Tue, 17 Sep 2024 02:01:05 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:039c64b811f6899ce14fa3a4dfbbc84311990ce425a154dc16ee4134efc62bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106914142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2356f2106dd6637f395be3f692528e85299a01cd31383a9a0714b881bed94cb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ea18d37e82ca7216449a13fac7f69217b68333c87cf16d6d356794e9c369e`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990c746484df95d66cf384962ed7ec84948d939d53ace21611666c129f2d68`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 4.3 MB (4269684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5b85a95f1a10e6e7d26ada6777d99a91c5c5c9007e8dbaa57bf51682a6c7e0`  
		Last Modified: Fri, 23 Aug 2024 23:27:36 GMT  
		Size: 14.7 MB (14682885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a44392360c56a99450248ee6b0e11d0ac62fad68a402b614c50ab6fbd18a418`  
		Last Modified: Fri, 23 Aug 2024 23:27:35 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:62ec2886389278c2c6d4d9084c8f63ae70c0ac1e1320f432cfd8d2c7f00fab05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3717549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbb3dd8135494c36dd528e2b65adb393ff1f0c6b64eb72661f7dc42fdc69533`

```dockerfile
```

-	Layers:
	-	`sha256:7969ff2210332486b6fd98a43b13077da20e3f3bf709e14751e0c0f0309ef7aa`  
		Last Modified: Fri, 23 Aug 2024 23:27:36 GMT  
		Size: 3.7 MB (3692942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf268f9aa6db649a7b978a2992837334008b89874329e2bc5a6045e34055465d`  
		Last Modified: Fri, 23 Aug 2024 23:27:35 GMT  
		Size: 24.6 KB (24607 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:99d716adc47fa48bbfd4fcd9ba0210bd8cc2430ebdc3cbb485d6ad6df524028f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116072468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285b4b8ab121066611015d5a251188eaa1d4a76714bc053f1668761cee83b86d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc895576af9cea3bc6748630114d80e9d68ab614d0dcd495a557016c4c90d6`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0e26d81209f6a2da5cec43641648e9d9f89d16e14c99d5623d092adea4482`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 5.0 MB (4966005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a264621b5c2ea64f2b93eb9cbecf244e24c683db84ab74a8cbdefed52875394d`  
		Last Modified: Fri, 23 Aug 2024 20:55:38 GMT  
		Size: 14.7 MB (14682853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a562dccda972264d6d6e8b44fc49ec803f5f00601a57f32638481f5b2ca3364`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:ad3795f9321c76cdd0da71d775471e95813188354af1f79553ce83f7a5dc837a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b5e3a9b2c1638a5a3a6bd6d35c7b3540ae499043a3d4d10e0f11a866224350`

```dockerfile
```

-	Layers:
	-	`sha256:cf5f87c67060f2e5379633e3072ecd72cd07711d62099a7ad8cf52fce0b71fe4`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 3.7 MB (3697209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ceb627bb3466360ac4de85bc565bba372e4dd0b305b131fc93459952241e93`  
		Last Modified: Fri, 23 Aug 2024 20:55:37 GMT  
		Size: 24.3 KB (24332 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:052166658ce887c8b6f1954f70540b769f3d9cba6e6e696603eb044164a3bac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104388493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0a950a33f9cec428be2cbd48b79bfbdfa12121c39937d4b4d4d5b5a5d251b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1eb2e01f4164208070c21c1525ad5da7aaed86dd78dd248957b88c24c71c8`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc844baa2089b0df873e8304e4362d3317a2927ddbd583094f621de0d0fdec`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 4.2 MB (4242071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af83382fbe6d2a35f3b74fe13551ce4623caf376e908bcdd348e02dfa276b674`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 14.7 MB (14682927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3681421bc5028ade4e4d997ed8998f51c4cfa0a0d1460512148b800ee18d078`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:cf8b44a0f76cc0295664581b6c04dfabeadbf7ae46348721b64a46f86c022034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9651fc229ad36362b4bc1e19a3ba0ce7077c2d189048fdcfc28dc70f7a222009`

```dockerfile
```

-	Layers:
	-	`sha256:3763e70318a29a586084260e092d62fa1a7bf4e8143818e57ba36fc8389a537f`  
		Last Modified: Tue, 17 Sep 2024 04:00:51 GMT  
		Size: 3.7 MB (3693758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82aa081bfb4422af2fdc99d3decba054c3f3e819844260c0490f89a1b495e2e`  
		Last Modified: Tue, 17 Sep 2024 04:00:50 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9`

```console
$ docker pull zookeeper@sha256:5227911b74724483c6b8e18215eaaaabf08fc2d1deee5ef02ef51e9a631497d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.9` - linux; amd64

```console
$ docker pull zookeeper@sha256:474fe95c1f43906b6d32871361eab97269179a586ce6415e1880defc411b7d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115262063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf61d6ccc3f58a9cbe61253137eebc436b88c3276ba3f91653fffbc06c0e524`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ccaae16b79b071b4ee2d8281163e037eee2e4d20788b4d78fe0600a516bc5e`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24da8fe8aa0ab16e7dd157ede3886ee523592d06f7072aeeca9af59f283ef25e`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 4.4 MB (4365972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d763b264a663fbb3d45f3c5c869ada3559a0e1a5963cdb41254d11acd85cc86`  
		Last Modified: Tue, 17 Sep 2024 02:01:34 GMT  
		Size: 20.3 MB (20300228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03205aee8965c0f064f7a5383523c462b83c36574c522f44731efa54c69c034`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:16531dadd343ab3c3faf1602d2dd4b84ddccdf921f58ec5c5621ebc5990d5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50969f79b142f04ce0ca084a209ebca521848a063ca3a1426af9372e59a72c8`

```dockerfile
```

-	Layers:
	-	`sha256:c690b2d81621462c95ca841b1a13f27df3aad96a3636490c4cf71a0d3c8195e2`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 3.7 MB (3698798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d75a7c65f670fc6ae07f17aef78f30877b45a9dd3e8086cb8000e6c762bfca`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:dc10197152ad268c708186867c5e290e44ad1f4771defc5f4f862b840454ab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112531459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce994ca957015586cfd690305ac22604b633913f9acd4824e070312981da4c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ea18d37e82ca7216449a13fac7f69217b68333c87cf16d6d356794e9c369e`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990c746484df95d66cf384962ed7ec84948d939d53ace21611666c129f2d68`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 4.3 MB (4269684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb4ce0d3af0af14d89458044299e87d9b5c8177ecf3109008745181b2a4c19f`  
		Last Modified: Fri, 23 Aug 2024 23:28:04 GMT  
		Size: 20.3 MB (20300202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87164d8f0fe4f3ca33c760f61688f9e117feb4a2229e4be66e0aa75cb06d7da`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bf1b53e109fa2e06c0524ae9d783091fb72bc78b646f0838fe59b35e489a176e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15272751160b777af5595462975172c42cb66703ba923359cd2a82f554117ce8`

```dockerfile
```

-	Layers:
	-	`sha256:8106a84969a5f0baf9684e4192a704eb49c988baf43c0bb735ac25879b73b18a`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 3.7 MB (3699109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954b3341990e63390ec16a0bf85c43896a25ddd2bff700b278588c57ebf427`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 24.9 KB (24921 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:3cb3116c912f61edb2e66e255a4f47c8eaf985f59e8c323a669f1c7a8d714d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121689817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c87f67c0d91d15276ac177d6bdfda31c895a6159eb2573c0f8ae98e0566ca9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc895576af9cea3bc6748630114d80e9d68ab614d0dcd495a557016c4c90d6`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0e26d81209f6a2da5cec43641648e9d9f89d16e14c99d5623d092adea4482`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 5.0 MB (4966005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca880f0752f32f22a2362e28f5f39e7b38dbad160e0af06688c39e7d040bce4`  
		Last Modified: Fri, 23 Aug 2024 20:56:16 GMT  
		Size: 20.3 MB (20300201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee58e4bd3a35a0b709125f5477606d106bca4f8a1d5739d4a15d22526fde4c3`  
		Last Modified: Fri, 23 Aug 2024 20:56:15 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:6b548e45025c4752629f28e0215dae95b4227143419a528931fe0f05afbb329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c27a0fa9d0e0dfcd93aba5410db4b728043f465f8ace98b98cc86940d8d69a`

```dockerfile
```

-	Layers:
	-	`sha256:f14f8144950db584d23e63e8892d02acaf5a94b5bd40b0b5e7a3744801c3008a`  
		Last Modified: Fri, 23 Aug 2024 20:56:16 GMT  
		Size: 3.7 MB (3703370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea96f1fc2c69adc79da7238116e73087c36b01c9e6579848fcaf2eb42b6a045`  
		Last Modified: Fri, 23 Aug 2024 20:56:15 GMT  
		Size: 24.6 KB (24642 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; s390x

```console
$ docker pull zookeeper@sha256:74bfb2e3d8283ea3fbbf6af630082b91189dafe5317b60f3725aeb85b7d9e3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110005800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a6c1093ccae0f5488ef30d653a0978065deeba5a691695a492826d70392200`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1eb2e01f4164208070c21c1525ad5da7aaed86dd78dd248957b88c24c71c8`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc844baa2089b0df873e8304e4362d3317a2927ddbd583094f621de0d0fdec`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 4.2 MB (4242071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42330a9fac8bb67f1531b4df82e3d5946a9673389c0b0f5c524343df1bed747a`  
		Last Modified: Tue, 17 Sep 2024 04:01:31 GMT  
		Size: 20.3 MB (20300234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a12d7bc619d3adbb30eb7c22e3dc686f652b3af21576eef7023e65f6f235ec`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:684d47275fd4a1df617003f715d54f58e297ce4422840fc372da85a4103ad2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addac4ff1e41a32ea4d814256d37a06cc941910550e693367091c1f13f3dd0df`

```dockerfile
```

-	Layers:
	-	`sha256:3616a0d5a742ca6ceea4ae1ceab645763a54eeb87398f41f26fe8419ba326373`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 3.7 MB (3699913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4022938f091a14e17a3d42645ec53e572b6f69d0727b8c822cfbc87f0b8fa9e`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9-jre-17`

```console
$ docker pull zookeeper@sha256:5227911b74724483c6b8e18215eaaaabf08fc2d1deee5ef02ef51e9a631497d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.9-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:474fe95c1f43906b6d32871361eab97269179a586ce6415e1880defc411b7d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115262063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf61d6ccc3f58a9cbe61253137eebc436b88c3276ba3f91653fffbc06c0e524`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ccaae16b79b071b4ee2d8281163e037eee2e4d20788b4d78fe0600a516bc5e`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24da8fe8aa0ab16e7dd157ede3886ee523592d06f7072aeeca9af59f283ef25e`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 4.4 MB (4365972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d763b264a663fbb3d45f3c5c869ada3559a0e1a5963cdb41254d11acd85cc86`  
		Last Modified: Tue, 17 Sep 2024 02:01:34 GMT  
		Size: 20.3 MB (20300228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03205aee8965c0f064f7a5383523c462b83c36574c522f44731efa54c69c034`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:16531dadd343ab3c3faf1602d2dd4b84ddccdf921f58ec5c5621ebc5990d5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50969f79b142f04ce0ca084a209ebca521848a063ca3a1426af9372e59a72c8`

```dockerfile
```

-	Layers:
	-	`sha256:c690b2d81621462c95ca841b1a13f27df3aad96a3636490c4cf71a0d3c8195e2`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 3.7 MB (3698798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d75a7c65f670fc6ae07f17aef78f30877b45a9dd3e8086cb8000e6c762bfca`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:dc10197152ad268c708186867c5e290e44ad1f4771defc5f4f862b840454ab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112531459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce994ca957015586cfd690305ac22604b633913f9acd4824e070312981da4c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ea18d37e82ca7216449a13fac7f69217b68333c87cf16d6d356794e9c369e`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990c746484df95d66cf384962ed7ec84948d939d53ace21611666c129f2d68`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 4.3 MB (4269684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb4ce0d3af0af14d89458044299e87d9b5c8177ecf3109008745181b2a4c19f`  
		Last Modified: Fri, 23 Aug 2024 23:28:04 GMT  
		Size: 20.3 MB (20300202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87164d8f0fe4f3ca33c760f61688f9e117feb4a2229e4be66e0aa75cb06d7da`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bf1b53e109fa2e06c0524ae9d783091fb72bc78b646f0838fe59b35e489a176e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15272751160b777af5595462975172c42cb66703ba923359cd2a82f554117ce8`

```dockerfile
```

-	Layers:
	-	`sha256:8106a84969a5f0baf9684e4192a704eb49c988baf43c0bb735ac25879b73b18a`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 3.7 MB (3699109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954b3341990e63390ec16a0bf85c43896a25ddd2bff700b278588c57ebf427`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 24.9 KB (24921 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:3cb3116c912f61edb2e66e255a4f47c8eaf985f59e8c323a669f1c7a8d714d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121689817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c87f67c0d91d15276ac177d6bdfda31c895a6159eb2573c0f8ae98e0566ca9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc895576af9cea3bc6748630114d80e9d68ab614d0dcd495a557016c4c90d6`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0e26d81209f6a2da5cec43641648e9d9f89d16e14c99d5623d092adea4482`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 5.0 MB (4966005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca880f0752f32f22a2362e28f5f39e7b38dbad160e0af06688c39e7d040bce4`  
		Last Modified: Fri, 23 Aug 2024 20:56:16 GMT  
		Size: 20.3 MB (20300201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee58e4bd3a35a0b709125f5477606d106bca4f8a1d5739d4a15d22526fde4c3`  
		Last Modified: Fri, 23 Aug 2024 20:56:15 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:6b548e45025c4752629f28e0215dae95b4227143419a528931fe0f05afbb329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c27a0fa9d0e0dfcd93aba5410db4b728043f465f8ace98b98cc86940d8d69a`

```dockerfile
```

-	Layers:
	-	`sha256:f14f8144950db584d23e63e8892d02acaf5a94b5bd40b0b5e7a3744801c3008a`  
		Last Modified: Fri, 23 Aug 2024 20:56:16 GMT  
		Size: 3.7 MB (3703370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea96f1fc2c69adc79da7238116e73087c36b01c9e6579848fcaf2eb42b6a045`  
		Last Modified: Fri, 23 Aug 2024 20:56:15 GMT  
		Size: 24.6 KB (24642 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:74bfb2e3d8283ea3fbbf6af630082b91189dafe5317b60f3725aeb85b7d9e3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110005800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a6c1093ccae0f5488ef30d653a0978065deeba5a691695a492826d70392200`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1eb2e01f4164208070c21c1525ad5da7aaed86dd78dd248957b88c24c71c8`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc844baa2089b0df873e8304e4362d3317a2927ddbd583094f621de0d0fdec`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 4.2 MB (4242071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42330a9fac8bb67f1531b4df82e3d5946a9673389c0b0f5c524343df1bed747a`  
		Last Modified: Tue, 17 Sep 2024 04:01:31 GMT  
		Size: 20.3 MB (20300234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a12d7bc619d3adbb30eb7c22e3dc686f652b3af21576eef7023e65f6f235ec`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:684d47275fd4a1df617003f715d54f58e297ce4422840fc372da85a4103ad2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addac4ff1e41a32ea4d814256d37a06cc941910550e693367091c1f13f3dd0df`

```dockerfile
```

-	Layers:
	-	`sha256:3616a0d5a742ca6ceea4ae1ceab645763a54eeb87398f41f26fe8419ba326373`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 3.7 MB (3699913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4022938f091a14e17a3d42645ec53e572b6f69d0727b8c822cfbc87f0b8fa9e`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9.2`

```console
$ docker pull zookeeper@sha256:5227911b74724483c6b8e18215eaaaabf08fc2d1deee5ef02ef51e9a631497d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.9.2` - linux; amd64

```console
$ docker pull zookeeper@sha256:474fe95c1f43906b6d32871361eab97269179a586ce6415e1880defc411b7d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115262063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf61d6ccc3f58a9cbe61253137eebc436b88c3276ba3f91653fffbc06c0e524`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ccaae16b79b071b4ee2d8281163e037eee2e4d20788b4d78fe0600a516bc5e`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24da8fe8aa0ab16e7dd157ede3886ee523592d06f7072aeeca9af59f283ef25e`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 4.4 MB (4365972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d763b264a663fbb3d45f3c5c869ada3559a0e1a5963cdb41254d11acd85cc86`  
		Last Modified: Tue, 17 Sep 2024 02:01:34 GMT  
		Size: 20.3 MB (20300228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03205aee8965c0f064f7a5383523c462b83c36574c522f44731efa54c69c034`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:16531dadd343ab3c3faf1602d2dd4b84ddccdf921f58ec5c5621ebc5990d5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50969f79b142f04ce0ca084a209ebca521848a063ca3a1426af9372e59a72c8`

```dockerfile
```

-	Layers:
	-	`sha256:c690b2d81621462c95ca841b1a13f27df3aad96a3636490c4cf71a0d3c8195e2`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 3.7 MB (3698798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d75a7c65f670fc6ae07f17aef78f30877b45a9dd3e8086cb8000e6c762bfca`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:dc10197152ad268c708186867c5e290e44ad1f4771defc5f4f862b840454ab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112531459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce994ca957015586cfd690305ac22604b633913f9acd4824e070312981da4c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ea18d37e82ca7216449a13fac7f69217b68333c87cf16d6d356794e9c369e`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990c746484df95d66cf384962ed7ec84948d939d53ace21611666c129f2d68`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 4.3 MB (4269684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb4ce0d3af0af14d89458044299e87d9b5c8177ecf3109008745181b2a4c19f`  
		Last Modified: Fri, 23 Aug 2024 23:28:04 GMT  
		Size: 20.3 MB (20300202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87164d8f0fe4f3ca33c760f61688f9e117feb4a2229e4be66e0aa75cb06d7da`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bf1b53e109fa2e06c0524ae9d783091fb72bc78b646f0838fe59b35e489a176e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15272751160b777af5595462975172c42cb66703ba923359cd2a82f554117ce8`

```dockerfile
```

-	Layers:
	-	`sha256:8106a84969a5f0baf9684e4192a704eb49c988baf43c0bb735ac25879b73b18a`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 3.7 MB (3699109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954b3341990e63390ec16a0bf85c43896a25ddd2bff700b278588c57ebf427`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 24.9 KB (24921 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:3cb3116c912f61edb2e66e255a4f47c8eaf985f59e8c323a669f1c7a8d714d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121689817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c87f67c0d91d15276ac177d6bdfda31c895a6159eb2573c0f8ae98e0566ca9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc895576af9cea3bc6748630114d80e9d68ab614d0dcd495a557016c4c90d6`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0e26d81209f6a2da5cec43641648e9d9f89d16e14c99d5623d092adea4482`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 5.0 MB (4966005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca880f0752f32f22a2362e28f5f39e7b38dbad160e0af06688c39e7d040bce4`  
		Last Modified: Fri, 23 Aug 2024 20:56:16 GMT  
		Size: 20.3 MB (20300201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee58e4bd3a35a0b709125f5477606d106bca4f8a1d5739d4a15d22526fde4c3`  
		Last Modified: Fri, 23 Aug 2024 20:56:15 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:6b548e45025c4752629f28e0215dae95b4227143419a528931fe0f05afbb329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c27a0fa9d0e0dfcd93aba5410db4b728043f465f8ace98b98cc86940d8d69a`

```dockerfile
```

-	Layers:
	-	`sha256:f14f8144950db584d23e63e8892d02acaf5a94b5bd40b0b5e7a3744801c3008a`  
		Last Modified: Fri, 23 Aug 2024 20:56:16 GMT  
		Size: 3.7 MB (3703370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea96f1fc2c69adc79da7238116e73087c36b01c9e6579848fcaf2eb42b6a045`  
		Last Modified: Fri, 23 Aug 2024 20:56:15 GMT  
		Size: 24.6 KB (24642 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2` - linux; s390x

```console
$ docker pull zookeeper@sha256:74bfb2e3d8283ea3fbbf6af630082b91189dafe5317b60f3725aeb85b7d9e3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110005800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a6c1093ccae0f5488ef30d653a0978065deeba5a691695a492826d70392200`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1eb2e01f4164208070c21c1525ad5da7aaed86dd78dd248957b88c24c71c8`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc844baa2089b0df873e8304e4362d3317a2927ddbd583094f621de0d0fdec`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 4.2 MB (4242071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42330a9fac8bb67f1531b4df82e3d5946a9673389c0b0f5c524343df1bed747a`  
		Last Modified: Tue, 17 Sep 2024 04:01:31 GMT  
		Size: 20.3 MB (20300234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a12d7bc619d3adbb30eb7c22e3dc686f652b3af21576eef7023e65f6f235ec`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:684d47275fd4a1df617003f715d54f58e297ce4422840fc372da85a4103ad2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addac4ff1e41a32ea4d814256d37a06cc941910550e693367091c1f13f3dd0df`

```dockerfile
```

-	Layers:
	-	`sha256:3616a0d5a742ca6ceea4ae1ceab645763a54eeb87398f41f26fe8419ba326373`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 3.7 MB (3699913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4022938f091a14e17a3d42645ec53e572b6f69d0727b8c822cfbc87f0b8fa9e`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9.2-jre-17`

```console
$ docker pull zookeeper@sha256:5227911b74724483c6b8e18215eaaaabf08fc2d1deee5ef02ef51e9a631497d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.9.2-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:474fe95c1f43906b6d32871361eab97269179a586ce6415e1880defc411b7d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115262063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf61d6ccc3f58a9cbe61253137eebc436b88c3276ba3f91653fffbc06c0e524`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ccaae16b79b071b4ee2d8281163e037eee2e4d20788b4d78fe0600a516bc5e`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24da8fe8aa0ab16e7dd157ede3886ee523592d06f7072aeeca9af59f283ef25e`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 4.4 MB (4365972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d763b264a663fbb3d45f3c5c869ada3559a0e1a5963cdb41254d11acd85cc86`  
		Last Modified: Tue, 17 Sep 2024 02:01:34 GMT  
		Size: 20.3 MB (20300228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03205aee8965c0f064f7a5383523c462b83c36574c522f44731efa54c69c034`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:16531dadd343ab3c3faf1602d2dd4b84ddccdf921f58ec5c5621ebc5990d5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50969f79b142f04ce0ca084a209ebca521848a063ca3a1426af9372e59a72c8`

```dockerfile
```

-	Layers:
	-	`sha256:c690b2d81621462c95ca841b1a13f27df3aad96a3636490c4cf71a0d3c8195e2`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 3.7 MB (3698798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d75a7c65f670fc6ae07f17aef78f30877b45a9dd3e8086cb8000e6c762bfca`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:dc10197152ad268c708186867c5e290e44ad1f4771defc5f4f862b840454ab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112531459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce994ca957015586cfd690305ac22604b633913f9acd4824e070312981da4c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ea18d37e82ca7216449a13fac7f69217b68333c87cf16d6d356794e9c369e`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990c746484df95d66cf384962ed7ec84948d939d53ace21611666c129f2d68`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 4.3 MB (4269684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb4ce0d3af0af14d89458044299e87d9b5c8177ecf3109008745181b2a4c19f`  
		Last Modified: Fri, 23 Aug 2024 23:28:04 GMT  
		Size: 20.3 MB (20300202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87164d8f0fe4f3ca33c760f61688f9e117feb4a2229e4be66e0aa75cb06d7da`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bf1b53e109fa2e06c0524ae9d783091fb72bc78b646f0838fe59b35e489a176e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15272751160b777af5595462975172c42cb66703ba923359cd2a82f554117ce8`

```dockerfile
```

-	Layers:
	-	`sha256:8106a84969a5f0baf9684e4192a704eb49c988baf43c0bb735ac25879b73b18a`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 3.7 MB (3699109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954b3341990e63390ec16a0bf85c43896a25ddd2bff700b278588c57ebf427`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 24.9 KB (24921 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:3cb3116c912f61edb2e66e255a4f47c8eaf985f59e8c323a669f1c7a8d714d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121689817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c87f67c0d91d15276ac177d6bdfda31c895a6159eb2573c0f8ae98e0566ca9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc895576af9cea3bc6748630114d80e9d68ab614d0dcd495a557016c4c90d6`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0e26d81209f6a2da5cec43641648e9d9f89d16e14c99d5623d092adea4482`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 5.0 MB (4966005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca880f0752f32f22a2362e28f5f39e7b38dbad160e0af06688c39e7d040bce4`  
		Last Modified: Fri, 23 Aug 2024 20:56:16 GMT  
		Size: 20.3 MB (20300201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee58e4bd3a35a0b709125f5477606d106bca4f8a1d5739d4a15d22526fde4c3`  
		Last Modified: Fri, 23 Aug 2024 20:56:15 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:6b548e45025c4752629f28e0215dae95b4227143419a528931fe0f05afbb329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c27a0fa9d0e0dfcd93aba5410db4b728043f465f8ace98b98cc86940d8d69a`

```dockerfile
```

-	Layers:
	-	`sha256:f14f8144950db584d23e63e8892d02acaf5a94b5bd40b0b5e7a3744801c3008a`  
		Last Modified: Fri, 23 Aug 2024 20:56:16 GMT  
		Size: 3.7 MB (3703370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea96f1fc2c69adc79da7238116e73087c36b01c9e6579848fcaf2eb42b6a045`  
		Last Modified: Fri, 23 Aug 2024 20:56:15 GMT  
		Size: 24.6 KB (24642 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:74bfb2e3d8283ea3fbbf6af630082b91189dafe5317b60f3725aeb85b7d9e3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110005800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a6c1093ccae0f5488ef30d653a0978065deeba5a691695a492826d70392200`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1eb2e01f4164208070c21c1525ad5da7aaed86dd78dd248957b88c24c71c8`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc844baa2089b0df873e8304e4362d3317a2927ddbd583094f621de0d0fdec`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 4.2 MB (4242071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42330a9fac8bb67f1531b4df82e3d5946a9673389c0b0f5c524343df1bed747a`  
		Last Modified: Tue, 17 Sep 2024 04:01:31 GMT  
		Size: 20.3 MB (20300234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a12d7bc619d3adbb30eb7c22e3dc686f652b3af21576eef7023e65f6f235ec`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:684d47275fd4a1df617003f715d54f58e297ce4422840fc372da85a4103ad2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addac4ff1e41a32ea4d814256d37a06cc941910550e693367091c1f13f3dd0df`

```dockerfile
```

-	Layers:
	-	`sha256:3616a0d5a742ca6ceea4ae1ceab645763a54eeb87398f41f26fe8419ba326373`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 3.7 MB (3699913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4022938f091a14e17a3d42645ec53e572b6f69d0727b8c822cfbc87f0b8fa9e`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:5227911b74724483c6b8e18215eaaaabf08fc2d1deee5ef02ef51e9a631497d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:latest` - linux; amd64

```console
$ docker pull zookeeper@sha256:474fe95c1f43906b6d32871361eab97269179a586ce6415e1880defc411b7d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115262063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf61d6ccc3f58a9cbe61253137eebc436b88c3276ba3f91653fffbc06c0e524`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ccaae16b79b071b4ee2d8281163e037eee2e4d20788b4d78fe0600a516bc5e`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24da8fe8aa0ab16e7dd157ede3886ee523592d06f7072aeeca9af59f283ef25e`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 4.4 MB (4365972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d763b264a663fbb3d45f3c5c869ada3559a0e1a5963cdb41254d11acd85cc86`  
		Last Modified: Tue, 17 Sep 2024 02:01:34 GMT  
		Size: 20.3 MB (20300228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03205aee8965c0f064f7a5383523c462b83c36574c522f44731efa54c69c034`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:16531dadd343ab3c3faf1602d2dd4b84ddccdf921f58ec5c5621ebc5990d5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50969f79b142f04ce0ca084a209ebca521848a063ca3a1426af9372e59a72c8`

```dockerfile
```

-	Layers:
	-	`sha256:c690b2d81621462c95ca841b1a13f27df3aad96a3636490c4cf71a0d3c8195e2`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 3.7 MB (3698798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d75a7c65f670fc6ae07f17aef78f30877b45a9dd3e8086cb8000e6c762bfca`  
		Last Modified: Tue, 17 Sep 2024 02:01:33 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:dc10197152ad268c708186867c5e290e44ad1f4771defc5f4f862b840454ab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112531459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce994ca957015586cfd690305ac22604b633913f9acd4824e070312981da4c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ea18d37e82ca7216449a13fac7f69217b68333c87cf16d6d356794e9c369e`  
		Last Modified: Fri, 23 Aug 2024 23:27:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990c746484df95d66cf384962ed7ec84948d939d53ace21611666c129f2d68`  
		Last Modified: Fri, 23 Aug 2024 23:27:05 GMT  
		Size: 4.3 MB (4269684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb4ce0d3af0af14d89458044299e87d9b5c8177ecf3109008745181b2a4c19f`  
		Last Modified: Fri, 23 Aug 2024 23:28:04 GMT  
		Size: 20.3 MB (20300202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87164d8f0fe4f3ca33c760f61688f9e117feb4a2229e4be66e0aa75cb06d7da`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bf1b53e109fa2e06c0524ae9d783091fb72bc78b646f0838fe59b35e489a176e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15272751160b777af5595462975172c42cb66703ba923359cd2a82f554117ce8`

```dockerfile
```

-	Layers:
	-	`sha256:8106a84969a5f0baf9684e4192a704eb49c988baf43c0bb735ac25879b73b18a`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 3.7 MB (3699109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63954b3341990e63390ec16a0bf85c43896a25ddd2bff700b278588c57ebf427`  
		Last Modified: Fri, 23 Aug 2024 23:28:03 GMT  
		Size: 24.9 KB (24921 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:3cb3116c912f61edb2e66e255a4f47c8eaf985f59e8c323a669f1c7a8d714d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121689817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c87f67c0d91d15276ac177d6bdfda31c895a6159eb2573c0f8ae98e0566ca9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc895576af9cea3bc6748630114d80e9d68ab614d0dcd495a557016c4c90d6`  
		Last Modified: Fri, 23 Aug 2024 20:54:48 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0e26d81209f6a2da5cec43641648e9d9f89d16e14c99d5623d092adea4482`  
		Last Modified: Fri, 23 Aug 2024 20:54:49 GMT  
		Size: 5.0 MB (4966005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca880f0752f32f22a2362e28f5f39e7b38dbad160e0af06688c39e7d040bce4`  
		Last Modified: Fri, 23 Aug 2024 20:56:16 GMT  
		Size: 20.3 MB (20300201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee58e4bd3a35a0b709125f5477606d106bca4f8a1d5739d4a15d22526fde4c3`  
		Last Modified: Fri, 23 Aug 2024 20:56:15 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:6b548e45025c4752629f28e0215dae95b4227143419a528931fe0f05afbb329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c27a0fa9d0e0dfcd93aba5410db4b728043f465f8ace98b98cc86940d8d69a`

```dockerfile
```

-	Layers:
	-	`sha256:f14f8144950db584d23e63e8892d02acaf5a94b5bd40b0b5e7a3744801c3008a`  
		Last Modified: Fri, 23 Aug 2024 20:56:16 GMT  
		Size: 3.7 MB (3703370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea96f1fc2c69adc79da7238116e73087c36b01c9e6579848fcaf2eb42b6a045`  
		Last Modified: Fri, 23 Aug 2024 20:56:15 GMT  
		Size: 24.6 KB (24642 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; s390x

```console
$ docker pull zookeeper@sha256:74bfb2e3d8283ea3fbbf6af630082b91189dafe5317b60f3725aeb85b7d9e3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110005800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a6c1093ccae0f5488ef30d653a0978065deeba5a691695a492826d70392200`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 14 Mar 2024 05:00:02 GMT
ARG RELEASE
# Thu, 14 Mar 2024 05:00:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 14 Mar 2024 05:00:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 14 Mar 2024 05:00:02 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Thu, 14 Mar 2024 05:00:02 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.2
# Thu, 14 Mar 2024 05:00:02 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.9.2 DISTRO_NAME=apache-zookeeper-3.9.2-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
WORKDIR /apache-zookeeper-3.9.2-bin
# Thu, 14 Mar 2024 05:00:02 GMT
VOLUME [/data /datalog /logs]
# Thu, 14 Mar 2024 05:00:02 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.2-bin/bin ZOOCFGDIR=/conf
# Thu, 14 Mar 2024 05:00:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1eb2e01f4164208070c21c1525ad5da7aaed86dd78dd248957b88c24c71c8`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc844baa2089b0df873e8304e4362d3317a2927ddbd583094f621de0d0fdec`  
		Last Modified: Tue, 17 Sep 2024 03:59:59 GMT  
		Size: 4.2 MB (4242071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42330a9fac8bb67f1531b4df82e3d5946a9673389c0b0f5c524343df1bed747a`  
		Last Modified: Tue, 17 Sep 2024 04:01:31 GMT  
		Size: 20.3 MB (20300234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a12d7bc619d3adbb30eb7c22e3dc686f652b3af21576eef7023e65f6f235ec`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:684d47275fd4a1df617003f715d54f58e297ce4422840fc372da85a4103ad2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addac4ff1e41a32ea4d814256d37a06cc941910550e693367091c1f13f3dd0df`

```dockerfile
```

-	Layers:
	-	`sha256:3616a0d5a742ca6ceea4ae1ceab645763a54eeb87398f41f26fe8419ba326373`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 3.7 MB (3699913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4022938f091a14e17a3d42645ec53e572b6f69d0727b8c822cfbc87f0b8fa9e`  
		Last Modified: Tue, 17 Sep 2024 04:01:30 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json
