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
$ docker pull zookeeper@sha256:2120807173bcca520b44eb939989e34e221579cae7c50593ae526dc2f0fe9f98
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
$ docker pull zookeeper@sha256:6f3f1d96401f53da033fb25b4ff65634b1535acd915ccc80be172409367f2321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109020699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b4c9d0c10e9ec3f19fbfc227b8ccd51489b16b5ff8e0a36773405d4c93776a`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a880dee0d8e92fc9854fd2480b4c183eba1429a09ed63d9e60edad44fa8edf01`  
		Last Modified: Sat, 17 Aug 2024 01:12:06 GMT  
		Size: 47.2 MB (47198423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5deab9cbd68168c5b0fe4bf55d9d3be31e0a75abb267f5e59e8973d11616df`  
		Last Modified: Sat, 17 Aug 2024 01:11:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8f4b62f2e68572eaac926164f20363d2538aab091cf56cf29b9e83ddba7d83`  
		Last Modified: Sat, 17 Aug 2024 01:11:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e30c076ff973e39cd03deeffb7204d74a93c06b813da1d5178926f670685fd3`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af32927c69a5d88e858d0cf97d105ab6fa2fbf03d9946123955cf77ad4558b5`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 4.4 MB (4366102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa50b8c2ba69cb928ea1191e2cd196f63e5cbe0c8e07beea944232174b17df2`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 14.1 MB (14139962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2a1d39c2297887e1919d1849432de9b2ad32626ad97465dba9e4b03409715e`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7` - unknown; unknown

```console
$ docker pull zookeeper@sha256:c969cd0ae284082bd1d31a56bc8ef7d197a4514531546a09e7b98c744ff85419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068f123e9f9d44771a7ee97156d870b8ae54c5efcb6e29d3ada9b18579856ad2`

```dockerfile
```

-	Layers:
	-	`sha256:4c145fae10af433d33f875e225780c518d043921a6280d4723bc6bf1d5d4eea3`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 3.7 MB (3691210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:426468f9ac61988fce090b6614bc9d653f1486ba4eb89b7bf9d2e29ab6d7e893`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:b99166d01eb5631cde7b6835050824fb5d2975ffe04c8ac5d7e713958777fff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105185345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c0eab2bf1057009afa0d8d7662a935c82d341d32e9c76afda99ee123e700a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d58831d522892ce028e096d708f4963a33b2dc3b558164d3313f356dabd19d`  
		Last Modified: Wed, 24 Jul 2024 00:51:51 GMT  
		Size: 45.6 MB (45556956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa827b9912bf9e3d5ef6d2883b57eeed2f37a2c5ce1991e48a9d95dd21a9157`  
		Last Modified: Wed, 24 Jul 2024 00:51:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540541fd55f683cce44751b8b0d963a525ce593430a6ab7d691a1a562de60ab9`  
		Last Modified: Thu, 25 Jul 2024 17:45:22 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb684c8a22cd6c25b8c5de4b6b6c49d3d7f468cf25e46791215cb3610fa21b`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112cdf7716e1e047e5254657970ad30266224683be8e465a7667aeb3af9c96c6`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 4.3 MB (4269685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07075617dbeff131e7d4cc7f81de6695e2aac1354e21318791fa8ff12a6d7495`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 14.1 MB (14139979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884a8421920d7f13f023e1f5bb715f763fd9643d3cc591af3a1cad199fb61bcb`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4111d69d598feed02e0d29173f84496485b8d9d40df7f1acd815abbb965bf61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b283ff53807c3da9618325f357006a786b9b6d3e125c9ae7ea6b06660cdc2253`

```dockerfile
```

-	Layers:
	-	`sha256:be2ae2cf14c1cabd856b656faf1bd559facedc4113a528ae2479a3413a06fecb`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 3.7 MB (3691505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b52c4cca675e200519987c4a151a0a4a6241a432d0bd837e23b42a0effdff1`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 24.6 KB (24625 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:a8662e826df8c7d59ff958cd8ede6515d3c25fa999d209e2d752fe1364e39c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111065814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12069b4193bcf49c5275feef85571b5ed57e24e67c204f2762df66d9af80910`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da97c9c39a2705e0c230778cd8d4fcf249043af05b48e303a3545c34c4343aaa`  
		Last Modified: Wed, 24 Jul 2024 04:13:22 GMT  
		Size: 42.7 MB (42652022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aceb46896a9422332ed4b2fa4506a228081c7abc8ef8689fb8c058f9b3e8df35`  
		Last Modified: Wed, 24 Jul 2024 04:13:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320eff7aa0a1e4012bdf117660974682761d5db624113ae2f680b96e07b2834a`  
		Last Modified: Thu, 25 Jul 2024 17:24:27 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc24699b287aed67b5eadf26d7f1065de03757931c57c3687b2b725e9272d450`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1413b88160460e55d1e74ec6bc00a25262a8da9349894558d146e3edbbd18`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 5.0 MB (4965979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad938b0618d0f20248396287bed6d3be18f22c7c36cb48d7b4b6e1c125a0d54`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 14.1 MB (14139989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add795f4298ef9f074148376610a2446a7d61fe7bf93f145771ca24543cc7270`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7` - unknown; unknown

```console
$ docker pull zookeeper@sha256:87fb1d54294b09b9873c9ea3de53ca96421c9230d535b2f6122ec707c0512e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5d203b69917ea0fb8a9e1fca66b015a4561b8a1e5f1dda7d714b20ecdec4a`

```dockerfile
```

-	Layers:
	-	`sha256:9e814c013e1e3360d451782b2a82eb657a42c52b7a5375b38c1804d09b9b3ddc`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 3.7 MB (3695772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844813704ca2c3792ce8c09b3f4f64cb9a22b6e9db1299368d786af1ebbd0fc3`  
		Last Modified: Mon, 29 Jul 2024 18:58:55 GMT  
		Size: 24.4 KB (24350 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7` - linux; s390x

```console
$ docker pull zookeeper@sha256:dd7fa2d45d0fadeec38b7f21352e47c39d2c998c0fa1ef81bbb688b70efacdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100797452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cad5266a5d46ef144e94b52cc4193c125c2e7efa1dc3d575dde36fb8e8b540`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53d190393eca7947899727783f31b4d629b8cb328dd252d9cf9e1f57f52823`  
		Last Modified: Sat, 17 Aug 2024 01:33:01 GMT  
		Size: 40.8 MB (40817132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7494c9a7e12442d8d3b7e7296f1a1231b234cdff9fa8892908bd413186609079`  
		Last Modified: Sat, 17 Aug 2024 01:32:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74526df9c0366d211932ec56c4d441e07aaf847b38fc0ff252ab750aa945325`  
		Last Modified: Sat, 17 Aug 2024 01:32:55 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a58e989d0834e23c48f000c64ed41ce570e4594457b6a20174cf85817590c7`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1036cc20552a730ae5940b51527e36b560b2daaa56b9ea748695b5bf9c234fc1`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 4.2 MB (4242038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897bdd1486524e1f1c21935a61e18703178e632a451a8faa8b2cdbccc3a21576`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 14.1 MB (14139968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d85a7859ea3c8e325fc0c903188cc88d037b2c61055946ce382bf0338fdeb65`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bf4668fc88b4f62a7232f341888c9802c4546a1a75c395db81e46b207a6997ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a223abf925253783a8a1527b2e9ac0be6eeaead64a15646c29e30f136cc077e4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a92a302f034b6c86bfae0853c4b2083afc2443e9ce249868e754fe96ac9fdd`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 3.7 MB (3692325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76747ff01c9411efdb58be87a36683f487ec32f8cfba642578e29c59f20f83a1`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.7-jre-11`

```console
$ docker pull zookeeper@sha256:2120807173bcca520b44eb939989e34e221579cae7c50593ae526dc2f0fe9f98
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
$ docker pull zookeeper@sha256:6f3f1d96401f53da033fb25b4ff65634b1535acd915ccc80be172409367f2321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109020699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b4c9d0c10e9ec3f19fbfc227b8ccd51489b16b5ff8e0a36773405d4c93776a`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a880dee0d8e92fc9854fd2480b4c183eba1429a09ed63d9e60edad44fa8edf01`  
		Last Modified: Sat, 17 Aug 2024 01:12:06 GMT  
		Size: 47.2 MB (47198423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5deab9cbd68168c5b0fe4bf55d9d3be31e0a75abb267f5e59e8973d11616df`  
		Last Modified: Sat, 17 Aug 2024 01:11:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8f4b62f2e68572eaac926164f20363d2538aab091cf56cf29b9e83ddba7d83`  
		Last Modified: Sat, 17 Aug 2024 01:11:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e30c076ff973e39cd03deeffb7204d74a93c06b813da1d5178926f670685fd3`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af32927c69a5d88e858d0cf97d105ab6fa2fbf03d9946123955cf77ad4558b5`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 4.4 MB (4366102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa50b8c2ba69cb928ea1191e2cd196f63e5cbe0c8e07beea944232174b17df2`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 14.1 MB (14139962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2a1d39c2297887e1919d1849432de9b2ad32626ad97465dba9e4b03409715e`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:c969cd0ae284082bd1d31a56bc8ef7d197a4514531546a09e7b98c744ff85419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068f123e9f9d44771a7ee97156d870b8ae54c5efcb6e29d3ada9b18579856ad2`

```dockerfile
```

-	Layers:
	-	`sha256:4c145fae10af433d33f875e225780c518d043921a6280d4723bc6bf1d5d4eea3`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 3.7 MB (3691210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:426468f9ac61988fce090b6614bc9d653f1486ba4eb89b7bf9d2e29ab6d7e893`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-11` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:b99166d01eb5631cde7b6835050824fb5d2975ffe04c8ac5d7e713958777fff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105185345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c0eab2bf1057009afa0d8d7662a935c82d341d32e9c76afda99ee123e700a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d58831d522892ce028e096d708f4963a33b2dc3b558164d3313f356dabd19d`  
		Last Modified: Wed, 24 Jul 2024 00:51:51 GMT  
		Size: 45.6 MB (45556956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa827b9912bf9e3d5ef6d2883b57eeed2f37a2c5ce1991e48a9d95dd21a9157`  
		Last Modified: Wed, 24 Jul 2024 00:51:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540541fd55f683cce44751b8b0d963a525ce593430a6ab7d691a1a562de60ab9`  
		Last Modified: Thu, 25 Jul 2024 17:45:22 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb684c8a22cd6c25b8c5de4b6b6c49d3d7f468cf25e46791215cb3610fa21b`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112cdf7716e1e047e5254657970ad30266224683be8e465a7667aeb3af9c96c6`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 4.3 MB (4269685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07075617dbeff131e7d4cc7f81de6695e2aac1354e21318791fa8ff12a6d7495`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 14.1 MB (14139979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884a8421920d7f13f023e1f5bb715f763fd9643d3cc591af3a1cad199fb61bcb`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4111d69d598feed02e0d29173f84496485b8d9d40df7f1acd815abbb965bf61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b283ff53807c3da9618325f357006a786b9b6d3e125c9ae7ea6b06660cdc2253`

```dockerfile
```

-	Layers:
	-	`sha256:be2ae2cf14c1cabd856b656faf1bd559facedc4113a528ae2479a3413a06fecb`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 3.7 MB (3691505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b52c4cca675e200519987c4a151a0a4a6241a432d0bd837e23b42a0effdff1`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 24.6 KB (24625 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-11` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:a8662e826df8c7d59ff958cd8ede6515d3c25fa999d209e2d752fe1364e39c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111065814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12069b4193bcf49c5275feef85571b5ed57e24e67c204f2762df66d9af80910`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da97c9c39a2705e0c230778cd8d4fcf249043af05b48e303a3545c34c4343aaa`  
		Last Modified: Wed, 24 Jul 2024 04:13:22 GMT  
		Size: 42.7 MB (42652022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aceb46896a9422332ed4b2fa4506a228081c7abc8ef8689fb8c058f9b3e8df35`  
		Last Modified: Wed, 24 Jul 2024 04:13:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320eff7aa0a1e4012bdf117660974682761d5db624113ae2f680b96e07b2834a`  
		Last Modified: Thu, 25 Jul 2024 17:24:27 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc24699b287aed67b5eadf26d7f1065de03757931c57c3687b2b725e9272d450`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1413b88160460e55d1e74ec6bc00a25262a8da9349894558d146e3edbbd18`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 5.0 MB (4965979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad938b0618d0f20248396287bed6d3be18f22c7c36cb48d7b4b6e1c125a0d54`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 14.1 MB (14139989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add795f4298ef9f074148376610a2446a7d61fe7bf93f145771ca24543cc7270`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:87fb1d54294b09b9873c9ea3de53ca96421c9230d535b2f6122ec707c0512e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5d203b69917ea0fb8a9e1fca66b015a4561b8a1e5f1dda7d714b20ecdec4a`

```dockerfile
```

-	Layers:
	-	`sha256:9e814c013e1e3360d451782b2a82eb657a42c52b7a5375b38c1804d09b9b3ddc`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 3.7 MB (3695772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844813704ca2c3792ce8c09b3f4f64cb9a22b6e9db1299368d786af1ebbd0fc3`  
		Last Modified: Mon, 29 Jul 2024 18:58:55 GMT  
		Size: 24.4 KB (24350 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-11` - linux; s390x

```console
$ docker pull zookeeper@sha256:dd7fa2d45d0fadeec38b7f21352e47c39d2c998c0fa1ef81bbb688b70efacdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100797452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cad5266a5d46ef144e94b52cc4193c125c2e7efa1dc3d575dde36fb8e8b540`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53d190393eca7947899727783f31b4d629b8cb328dd252d9cf9e1f57f52823`  
		Last Modified: Sat, 17 Aug 2024 01:33:01 GMT  
		Size: 40.8 MB (40817132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7494c9a7e12442d8d3b7e7296f1a1231b234cdff9fa8892908bd413186609079`  
		Last Modified: Sat, 17 Aug 2024 01:32:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74526df9c0366d211932ec56c4d441e07aaf847b38fc0ff252ab750aa945325`  
		Last Modified: Sat, 17 Aug 2024 01:32:55 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a58e989d0834e23c48f000c64ed41ce570e4594457b6a20174cf85817590c7`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1036cc20552a730ae5940b51527e36b560b2daaa56b9ea748695b5bf9c234fc1`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 4.2 MB (4242038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897bdd1486524e1f1c21935a61e18703178e632a451a8faa8b2cdbccc3a21576`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 14.1 MB (14139968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d85a7859ea3c8e325fc0c903188cc88d037b2c61055946ce382bf0338fdeb65`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bf4668fc88b4f62a7232f341888c9802c4546a1a75c395db81e46b207a6997ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a223abf925253783a8a1527b2e9ac0be6eeaead64a15646c29e30f136cc077e4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a92a302f034b6c86bfae0853c4b2083afc2443e9ce249868e754fe96ac9fdd`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 3.7 MB (3692325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76747ff01c9411efdb58be87a36683f487ec32f8cfba642578e29c59f20f83a1`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.7-jre-17`

```console
$ docker pull zookeeper@sha256:43248e82596c841b62c7745a93ef5a8f61864b5bb74e10345951ffe9dda435a7
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
$ docker pull zookeeper@sha256:101fdeb434871ed7d6af4ea44f5273a7c6fc0e5dfb460fdb16d5496a11652101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109102493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c540b47ea3c38f9604558f7e0235c1d16cda6dd8bddf1b2e4b35c1630593583d`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda6f29d7384ad93e0957dd7f4e8303a1de05fdabc82f82b3533d8c7f9a93fff`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a3869c8dac8f386f8e24c0aa5dac07c677da48330560c07787ad8cda231739`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 4.4 MB (4366102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13d99a17225284a156943d76241a84d1b0ca183d53d0123dffeab7d499499ce`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 14.1 MB (14139965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74854c9deb6c61d7237d96ed4fbf9ce1d1cfb6c5c96db15aa6f752d3de98e505`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4e829fc6f732967b0073a78d42c5efa9b3b35ab53927891919e2016f52e4fa6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e571c7943e8f7802249f2da788a7a17a3b667534d9262c27fb21d1f3056de29`

```dockerfile
```

-	Layers:
	-	`sha256:ab52f7b8fa8cb7bee778afe733d3a6caeca63bcfa276009b1ae59c554c2360be`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 3.7 MB (3690610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e4be9a6fe096551bcd719eb1edf4622ed7089d99efd305dafe0c71527c2c7de`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 23.7 KB (23690 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:975f821692c488f12cb6c3b8cc9c2fa6829e37cf6b5f31280193aa1eb0f28922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106374700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6c7c591db9a9509377b1ba8953006f4790aab15a890007e222f3476b8bdc5d`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15870975e17127e7a443d39d43abbf4963d9a1f62811cec1a91dffc2d612a256`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15648f55b06df51e69a53c8b202a2d88efbc1c8bc2a617c745eb76c2de085c`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 4.3 MB (4269669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e007519bbf360a2691374408fa680a9caafdc302d208f54ae0c6b99f71b4048`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 14.1 MB (14139943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14bda0e6efcc25a622f791c52397c7ccfdf7dd208399f23945eee0c2529378c`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:98786e11626c2fe6463155d4ec8c756295a2995556f76ed4d68e5e852092540e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb9bb48ed458b60045582eebe8c8ec9bd6b1c772e90a19ec12d32725c73547f`

```dockerfile
```

-	Layers:
	-	`sha256:b0fc35857c155911f86a05e04252cddb8f000b3102c8ed661f8751e6267b4015`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 3.7 MB (3690881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45433e5af2d35ef0e5652b7905bfac9ee2c5b29c255dc1c339d9381b6ff28fe`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 24.0 KB (23982 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:520fce0ae9133311c8515451d8a0c479dd84b94264961ba8e2fc39d9067a29ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115529733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a8a7b1aca176932dd3df7198f91b98c3ffe1dc5886ce5135097a3475a9afe8`
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
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1b8f6e7bffef1f98daaa768f140a921205e1bf2023baffce3674e6750ac3`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3d3cea284fe9c435685752db6cde417c8c9b30493750c6e58a4fe94a58933`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 5.0 MB (4965940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454525068d69b9d86595b32ad5933c5c407d1f23abd8e072e996516098abaf1c`  
		Last Modified: Thu, 25 Jul 2024 19:52:15 GMT  
		Size: 14.1 MB (14139993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bcfb94d8adace85584fbd5cbc7d180244347ddf07e14b4c9b5d54eeaa97ef0`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:9a3b8b5d1fe8ea11c4aeeff58231ccc379251033f59f21ed9d6e3a3fac359b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5697ada5db4beebe4298bf24c8f2bdc67324978805d188a58560733d254514cb`

```dockerfile
```

-	Layers:
	-	`sha256:e73bc5fc9b042e79e631a9378687084c502bde323d3f380f453d953c7a8eed37`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 3.7 MB (3695160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca2e4e42f16f67f87b8a3a0e6d668ababaed69d22a25fde10fededf7fec46e9`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 23.7 KB (23720 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:89a80c350efdf3d869662531a859b7b9549cfcaf22a33694f503c4a4c9cd0472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103844431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0b6a6f495183c6ca504357919fe09ed5088c53e71f70570770d3f2f4d1c2f3`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238133ff9a6cd66afdf7c2fcaac74cbfe7115b2beedf9ff46f9a3c9528d71de`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b972c6d58c217b00136bf4cc4fc998e690b0e88be3e23d0ae04b686d617f28`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 4.2 MB (4242011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3042f83024a259b1e23639d91dc842dc202148d77e06cc32355c92c753279ed`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 14.1 MB (14139974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad03c12194e4a15d3befb17012e15e94eaf99868ae8cd77b13d7a12038f01021`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:d03d3366d3780d8ccd54e50028619a98c76ed8edf93da19b3f4c1d3d907b8344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ea28fb1ee9a9d9821de93255afd69e8746ec8fb427bfa53ebbb0cffa3304a`

```dockerfile
```

-	Layers:
	-	`sha256:7564685c303f8370e86c7fd3b5f30557267eb0a99fd8e61548587e4285f46b79`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 3.7 MB (3691725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9a97e62bc46257ce56ef04257a428f9b3034db6725c4c21c34e25c8533cf46`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 23.7 KB (23690 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.7.2`

```console
$ docker pull zookeeper@sha256:2120807173bcca520b44eb939989e34e221579cae7c50593ae526dc2f0fe9f98
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
$ docker pull zookeeper@sha256:6f3f1d96401f53da033fb25b4ff65634b1535acd915ccc80be172409367f2321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109020699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b4c9d0c10e9ec3f19fbfc227b8ccd51489b16b5ff8e0a36773405d4c93776a`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a880dee0d8e92fc9854fd2480b4c183eba1429a09ed63d9e60edad44fa8edf01`  
		Last Modified: Sat, 17 Aug 2024 01:12:06 GMT  
		Size: 47.2 MB (47198423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5deab9cbd68168c5b0fe4bf55d9d3be31e0a75abb267f5e59e8973d11616df`  
		Last Modified: Sat, 17 Aug 2024 01:11:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8f4b62f2e68572eaac926164f20363d2538aab091cf56cf29b9e83ddba7d83`  
		Last Modified: Sat, 17 Aug 2024 01:11:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e30c076ff973e39cd03deeffb7204d74a93c06b813da1d5178926f670685fd3`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af32927c69a5d88e858d0cf97d105ab6fa2fbf03d9946123955cf77ad4558b5`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 4.4 MB (4366102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa50b8c2ba69cb928ea1191e2cd196f63e5cbe0c8e07beea944232174b17df2`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 14.1 MB (14139962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2a1d39c2297887e1919d1849432de9b2ad32626ad97465dba9e4b03409715e`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:c969cd0ae284082bd1d31a56bc8ef7d197a4514531546a09e7b98c744ff85419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068f123e9f9d44771a7ee97156d870b8ae54c5efcb6e29d3ada9b18579856ad2`

```dockerfile
```

-	Layers:
	-	`sha256:4c145fae10af433d33f875e225780c518d043921a6280d4723bc6bf1d5d4eea3`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 3.7 MB (3691210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:426468f9ac61988fce090b6614bc9d653f1486ba4eb89b7bf9d2e29ab6d7e893`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:b99166d01eb5631cde7b6835050824fb5d2975ffe04c8ac5d7e713958777fff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105185345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c0eab2bf1057009afa0d8d7662a935c82d341d32e9c76afda99ee123e700a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d58831d522892ce028e096d708f4963a33b2dc3b558164d3313f356dabd19d`  
		Last Modified: Wed, 24 Jul 2024 00:51:51 GMT  
		Size: 45.6 MB (45556956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa827b9912bf9e3d5ef6d2883b57eeed2f37a2c5ce1991e48a9d95dd21a9157`  
		Last Modified: Wed, 24 Jul 2024 00:51:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540541fd55f683cce44751b8b0d963a525ce593430a6ab7d691a1a562de60ab9`  
		Last Modified: Thu, 25 Jul 2024 17:45:22 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb684c8a22cd6c25b8c5de4b6b6c49d3d7f468cf25e46791215cb3610fa21b`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112cdf7716e1e047e5254657970ad30266224683be8e465a7667aeb3af9c96c6`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 4.3 MB (4269685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07075617dbeff131e7d4cc7f81de6695e2aac1354e21318791fa8ff12a6d7495`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 14.1 MB (14139979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884a8421920d7f13f023e1f5bb715f763fd9643d3cc591af3a1cad199fb61bcb`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4111d69d598feed02e0d29173f84496485b8d9d40df7f1acd815abbb965bf61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b283ff53807c3da9618325f357006a786b9b6d3e125c9ae7ea6b06660cdc2253`

```dockerfile
```

-	Layers:
	-	`sha256:be2ae2cf14c1cabd856b656faf1bd559facedc4113a528ae2479a3413a06fecb`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 3.7 MB (3691505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b52c4cca675e200519987c4a151a0a4a6241a432d0bd837e23b42a0effdff1`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 24.6 KB (24625 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:a8662e826df8c7d59ff958cd8ede6515d3c25fa999d209e2d752fe1364e39c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111065814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12069b4193bcf49c5275feef85571b5ed57e24e67c204f2762df66d9af80910`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da97c9c39a2705e0c230778cd8d4fcf249043af05b48e303a3545c34c4343aaa`  
		Last Modified: Wed, 24 Jul 2024 04:13:22 GMT  
		Size: 42.7 MB (42652022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aceb46896a9422332ed4b2fa4506a228081c7abc8ef8689fb8c058f9b3e8df35`  
		Last Modified: Wed, 24 Jul 2024 04:13:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320eff7aa0a1e4012bdf117660974682761d5db624113ae2f680b96e07b2834a`  
		Last Modified: Thu, 25 Jul 2024 17:24:27 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc24699b287aed67b5eadf26d7f1065de03757931c57c3687b2b725e9272d450`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1413b88160460e55d1e74ec6bc00a25262a8da9349894558d146e3edbbd18`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 5.0 MB (4965979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad938b0618d0f20248396287bed6d3be18f22c7c36cb48d7b4b6e1c125a0d54`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 14.1 MB (14139989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add795f4298ef9f074148376610a2446a7d61fe7bf93f145771ca24543cc7270`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:87fb1d54294b09b9873c9ea3de53ca96421c9230d535b2f6122ec707c0512e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5d203b69917ea0fb8a9e1fca66b015a4561b8a1e5f1dda7d714b20ecdec4a`

```dockerfile
```

-	Layers:
	-	`sha256:9e814c013e1e3360d451782b2a82eb657a42c52b7a5375b38c1804d09b9b3ddc`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 3.7 MB (3695772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844813704ca2c3792ce8c09b3f4f64cb9a22b6e9db1299368d786af1ebbd0fc3`  
		Last Modified: Mon, 29 Jul 2024 18:58:55 GMT  
		Size: 24.4 KB (24350 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2` - linux; s390x

```console
$ docker pull zookeeper@sha256:dd7fa2d45d0fadeec38b7f21352e47c39d2c998c0fa1ef81bbb688b70efacdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100797452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cad5266a5d46ef144e94b52cc4193c125c2e7efa1dc3d575dde36fb8e8b540`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53d190393eca7947899727783f31b4d629b8cb328dd252d9cf9e1f57f52823`  
		Last Modified: Sat, 17 Aug 2024 01:33:01 GMT  
		Size: 40.8 MB (40817132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7494c9a7e12442d8d3b7e7296f1a1231b234cdff9fa8892908bd413186609079`  
		Last Modified: Sat, 17 Aug 2024 01:32:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74526df9c0366d211932ec56c4d441e07aaf847b38fc0ff252ab750aa945325`  
		Last Modified: Sat, 17 Aug 2024 01:32:55 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a58e989d0834e23c48f000c64ed41ce570e4594457b6a20174cf85817590c7`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1036cc20552a730ae5940b51527e36b560b2daaa56b9ea748695b5bf9c234fc1`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 4.2 MB (4242038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897bdd1486524e1f1c21935a61e18703178e632a451a8faa8b2cdbccc3a21576`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 14.1 MB (14139968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d85a7859ea3c8e325fc0c903188cc88d037b2c61055946ce382bf0338fdeb65`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bf4668fc88b4f62a7232f341888c9802c4546a1a75c395db81e46b207a6997ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a223abf925253783a8a1527b2e9ac0be6eeaead64a15646c29e30f136cc077e4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a92a302f034b6c86bfae0853c4b2083afc2443e9ce249868e754fe96ac9fdd`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 3.7 MB (3692325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76747ff01c9411efdb58be87a36683f487ec32f8cfba642578e29c59f20f83a1`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.7.2-jre-11`

```console
$ docker pull zookeeper@sha256:2120807173bcca520b44eb939989e34e221579cae7c50593ae526dc2f0fe9f98
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
$ docker pull zookeeper@sha256:6f3f1d96401f53da033fb25b4ff65634b1535acd915ccc80be172409367f2321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109020699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b4c9d0c10e9ec3f19fbfc227b8ccd51489b16b5ff8e0a36773405d4c93776a`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a880dee0d8e92fc9854fd2480b4c183eba1429a09ed63d9e60edad44fa8edf01`  
		Last Modified: Sat, 17 Aug 2024 01:12:06 GMT  
		Size: 47.2 MB (47198423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5deab9cbd68168c5b0fe4bf55d9d3be31e0a75abb267f5e59e8973d11616df`  
		Last Modified: Sat, 17 Aug 2024 01:11:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8f4b62f2e68572eaac926164f20363d2538aab091cf56cf29b9e83ddba7d83`  
		Last Modified: Sat, 17 Aug 2024 01:11:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e30c076ff973e39cd03deeffb7204d74a93c06b813da1d5178926f670685fd3`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af32927c69a5d88e858d0cf97d105ab6fa2fbf03d9946123955cf77ad4558b5`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 4.4 MB (4366102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa50b8c2ba69cb928ea1191e2cd196f63e5cbe0c8e07beea944232174b17df2`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 14.1 MB (14139962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2a1d39c2297887e1919d1849432de9b2ad32626ad97465dba9e4b03409715e`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:c969cd0ae284082bd1d31a56bc8ef7d197a4514531546a09e7b98c744ff85419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068f123e9f9d44771a7ee97156d870b8ae54c5efcb6e29d3ada9b18579856ad2`

```dockerfile
```

-	Layers:
	-	`sha256:4c145fae10af433d33f875e225780c518d043921a6280d4723bc6bf1d5d4eea3`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 3.7 MB (3691210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:426468f9ac61988fce090b6614bc9d653f1486ba4eb89b7bf9d2e29ab6d7e893`  
		Last Modified: Sat, 17 Aug 2024 02:06:16 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-11` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:b99166d01eb5631cde7b6835050824fb5d2975ffe04c8ac5d7e713958777fff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105185345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c0eab2bf1057009afa0d8d7662a935c82d341d32e9c76afda99ee123e700a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d58831d522892ce028e096d708f4963a33b2dc3b558164d3313f356dabd19d`  
		Last Modified: Wed, 24 Jul 2024 00:51:51 GMT  
		Size: 45.6 MB (45556956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa827b9912bf9e3d5ef6d2883b57eeed2f37a2c5ce1991e48a9d95dd21a9157`  
		Last Modified: Wed, 24 Jul 2024 00:51:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540541fd55f683cce44751b8b0d963a525ce593430a6ab7d691a1a562de60ab9`  
		Last Modified: Thu, 25 Jul 2024 17:45:22 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb684c8a22cd6c25b8c5de4b6b6c49d3d7f468cf25e46791215cb3610fa21b`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112cdf7716e1e047e5254657970ad30266224683be8e465a7667aeb3af9c96c6`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 4.3 MB (4269685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07075617dbeff131e7d4cc7f81de6695e2aac1354e21318791fa8ff12a6d7495`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 14.1 MB (14139979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884a8421920d7f13f023e1f5bb715f763fd9643d3cc591af3a1cad199fb61bcb`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4111d69d598feed02e0d29173f84496485b8d9d40df7f1acd815abbb965bf61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b283ff53807c3da9618325f357006a786b9b6d3e125c9ae7ea6b06660cdc2253`

```dockerfile
```

-	Layers:
	-	`sha256:be2ae2cf14c1cabd856b656faf1bd559facedc4113a528ae2479a3413a06fecb`  
		Last Modified: Mon, 29 Jul 2024 19:23:43 GMT  
		Size: 3.7 MB (3691505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b52c4cca675e200519987c4a151a0a4a6241a432d0bd837e23b42a0effdff1`  
		Last Modified: Mon, 29 Jul 2024 19:23:42 GMT  
		Size: 24.6 KB (24625 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-11` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:a8662e826df8c7d59ff958cd8ede6515d3c25fa999d209e2d752fe1364e39c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111065814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12069b4193bcf49c5275feef85571b5ed57e24e67c204f2762df66d9af80910`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da97c9c39a2705e0c230778cd8d4fcf249043af05b48e303a3545c34c4343aaa`  
		Last Modified: Wed, 24 Jul 2024 04:13:22 GMT  
		Size: 42.7 MB (42652022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aceb46896a9422332ed4b2fa4506a228081c7abc8ef8689fb8c058f9b3e8df35`  
		Last Modified: Wed, 24 Jul 2024 04:13:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320eff7aa0a1e4012bdf117660974682761d5db624113ae2f680b96e07b2834a`  
		Last Modified: Thu, 25 Jul 2024 17:24:27 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc24699b287aed67b5eadf26d7f1065de03757931c57c3687b2b725e9272d450`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1413b88160460e55d1e74ec6bc00a25262a8da9349894558d146e3edbbd18`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 5.0 MB (4965979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad938b0618d0f20248396287bed6d3be18f22c7c36cb48d7b4b6e1c125a0d54`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 14.1 MB (14139989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add795f4298ef9f074148376610a2446a7d61fe7bf93f145771ca24543cc7270`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:87fb1d54294b09b9873c9ea3de53ca96421c9230d535b2f6122ec707c0512e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5d203b69917ea0fb8a9e1fca66b015a4561b8a1e5f1dda7d714b20ecdec4a`

```dockerfile
```

-	Layers:
	-	`sha256:9e814c013e1e3360d451782b2a82eb657a42c52b7a5375b38c1804d09b9b3ddc`  
		Last Modified: Mon, 29 Jul 2024 18:58:56 GMT  
		Size: 3.7 MB (3695772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844813704ca2c3792ce8c09b3f4f64cb9a22b6e9db1299368d786af1ebbd0fc3`  
		Last Modified: Mon, 29 Jul 2024 18:58:55 GMT  
		Size: 24.4 KB (24350 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-11` - linux; s390x

```console
$ docker pull zookeeper@sha256:dd7fa2d45d0fadeec38b7f21352e47c39d2c998c0fa1ef81bbb688b70efacdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100797452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cad5266a5d46ef144e94b52cc4193c125c2e7efa1dc3d575dde36fb8e8b540`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Sun, 28 Jul 2024 06:22:36 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53d190393eca7947899727783f31b4d629b8cb328dd252d9cf9e1f57f52823`  
		Last Modified: Sat, 17 Aug 2024 01:33:01 GMT  
		Size: 40.8 MB (40817132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7494c9a7e12442d8d3b7e7296f1a1231b234cdff9fa8892908bd413186609079`  
		Last Modified: Sat, 17 Aug 2024 01:32:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74526df9c0366d211932ec56c4d441e07aaf847b38fc0ff252ab750aa945325`  
		Last Modified: Sat, 17 Aug 2024 01:32:55 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a58e989d0834e23c48f000c64ed41ce570e4594457b6a20174cf85817590c7`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1036cc20552a730ae5940b51527e36b560b2daaa56b9ea748695b5bf9c234fc1`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 4.2 MB (4242038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897bdd1486524e1f1c21935a61e18703178e632a451a8faa8b2cdbccc3a21576`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 14.1 MB (14139968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d85a7859ea3c8e325fc0c903188cc88d037b2c61055946ce382bf0338fdeb65`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-11` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bf4668fc88b4f62a7232f341888c9802c4546a1a75c395db81e46b207a6997ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a223abf925253783a8a1527b2e9ac0be6eeaead64a15646c29e30f136cc077e4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a92a302f034b6c86bfae0853c4b2083afc2443e9ce249868e754fe96ac9fdd`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 3.7 MB (3692325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76747ff01c9411efdb58be87a36683f487ec32f8cfba642578e29c59f20f83a1`  
		Last Modified: Sat, 17 Aug 2024 05:20:03 GMT  
		Size: 24.3 KB (24308 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.7.2-jre-17`

```console
$ docker pull zookeeper@sha256:43248e82596c841b62c7745a93ef5a8f61864b5bb74e10345951ffe9dda435a7
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
$ docker pull zookeeper@sha256:101fdeb434871ed7d6af4ea44f5273a7c6fc0e5dfb460fdb16d5496a11652101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109102493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c540b47ea3c38f9604558f7e0235c1d16cda6dd8bddf1b2e4b35c1630593583d`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda6f29d7384ad93e0957dd7f4e8303a1de05fdabc82f82b3533d8c7f9a93fff`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a3869c8dac8f386f8e24c0aa5dac07c677da48330560c07787ad8cda231739`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 4.4 MB (4366102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13d99a17225284a156943d76241a84d1b0ca183d53d0123dffeab7d499499ce`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 14.1 MB (14139965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74854c9deb6c61d7237d96ed4fbf9ce1d1cfb6c5c96db15aa6f752d3de98e505`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4e829fc6f732967b0073a78d42c5efa9b3b35ab53927891919e2016f52e4fa6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e571c7943e8f7802249f2da788a7a17a3b667534d9262c27fb21d1f3056de29`

```dockerfile
```

-	Layers:
	-	`sha256:ab52f7b8fa8cb7bee778afe733d3a6caeca63bcfa276009b1ae59c554c2360be`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 3.7 MB (3690610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e4be9a6fe096551bcd719eb1edf4622ed7089d99efd305dafe0c71527c2c7de`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 23.7 KB (23690 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:975f821692c488f12cb6c3b8cc9c2fa6829e37cf6b5f31280193aa1eb0f28922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106374700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6c7c591db9a9509377b1ba8953006f4790aab15a890007e222f3476b8bdc5d`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15870975e17127e7a443d39d43abbf4963d9a1f62811cec1a91dffc2d612a256`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15648f55b06df51e69a53c8b202a2d88efbc1c8bc2a617c745eb76c2de085c`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 4.3 MB (4269669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e007519bbf360a2691374408fa680a9caafdc302d208f54ae0c6b99f71b4048`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 14.1 MB (14139943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14bda0e6efcc25a622f791c52397c7ccfdf7dd208399f23945eee0c2529378c`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:98786e11626c2fe6463155d4ec8c756295a2995556f76ed4d68e5e852092540e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb9bb48ed458b60045582eebe8c8ec9bd6b1c772e90a19ec12d32725c73547f`

```dockerfile
```

-	Layers:
	-	`sha256:b0fc35857c155911f86a05e04252cddb8f000b3102c8ed661f8751e6267b4015`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 3.7 MB (3690881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45433e5af2d35ef0e5652b7905bfac9ee2c5b29c255dc1c339d9381b6ff28fe`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 24.0 KB (23982 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:520fce0ae9133311c8515451d8a0c479dd84b94264961ba8e2fc39d9067a29ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115529733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a8a7b1aca176932dd3df7198f91b98c3ffe1dc5886ce5135097a3475a9afe8`
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
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1b8f6e7bffef1f98daaa768f140a921205e1bf2023baffce3674e6750ac3`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3d3cea284fe9c435685752db6cde417c8c9b30493750c6e58a4fe94a58933`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 5.0 MB (4965940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454525068d69b9d86595b32ad5933c5c407d1f23abd8e072e996516098abaf1c`  
		Last Modified: Thu, 25 Jul 2024 19:52:15 GMT  
		Size: 14.1 MB (14139993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bcfb94d8adace85584fbd5cbc7d180244347ddf07e14b4c9b5d54eeaa97ef0`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:9a3b8b5d1fe8ea11c4aeeff58231ccc379251033f59f21ed9d6e3a3fac359b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5697ada5db4beebe4298bf24c8f2bdc67324978805d188a58560733d254514cb`

```dockerfile
```

-	Layers:
	-	`sha256:e73bc5fc9b042e79e631a9378687084c502bde323d3f380f453d953c7a8eed37`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 3.7 MB (3695160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca2e4e42f16f67f87b8a3a0e6d668ababaed69d22a25fde10fededf7fec46e9`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 23.7 KB (23720 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.7.2-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:89a80c350efdf3d869662531a859b7b9549cfcaf22a33694f503c4a4c9cd0472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103844431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0b6a6f495183c6ca504357919fe09ed5088c53e71f70570770d3f2f4d1c2f3`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 16 Oct 2023 06:33:19 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238133ff9a6cd66afdf7c2fcaac74cbfe7115b2beedf9ff46f9a3c9528d71de`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b972c6d58c217b00136bf4cc4fc998e690b0e88be3e23d0ae04b686d617f28`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 4.2 MB (4242011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3042f83024a259b1e23639d91dc842dc202148d77e06cc32355c92c753279ed`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 14.1 MB (14139974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad03c12194e4a15d3befb17012e15e94eaf99868ae8cd77b13d7a12038f01021`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.7.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:d03d3366d3780d8ccd54e50028619a98c76ed8edf93da19b3f4c1d3d907b8344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ea28fb1ee9a9d9821de93255afd69e8746ec8fb427bfa53ebbb0cffa3304a`

```dockerfile
```

-	Layers:
	-	`sha256:7564685c303f8370e86c7fd3b5f30557267eb0a99fd8e61548587e4285f46b79`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 3.7 MB (3691725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9a97e62bc46257ce56ef04257a428f9b3034db6725c4c21c34e25c8533cf46`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 23.7 KB (23690 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8`

```console
$ docker pull zookeeper@sha256:7975aa6dc8383c3dbbe59cfd8c06bf9797be7a3df5cfdd68ad728e2945c7eb68
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
$ docker pull zookeeper@sha256:4d48f8685fac03719f1d07a8352ea22e829a41437289138fd8f4372eb9994aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109645323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a804a133f9a0c101a62d8f2e977dc8057b09b4b3a5d9f6c6a72aa5c6a187a6`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb9aab5e496f2b75f2c6b8db8743a344918804c77d8920bfa60ca160b356fb`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb02b55711761ed841333a0ac05dfdc46775f52e3371eabd63cf6f176d294913`  
		Last Modified: Sat, 17 Aug 2024 02:06:29 GMT  
		Size: 4.4 MB (4366041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f0905ea5858bb2e7dd553cfd6c7c707ff5f239f367415ce8ba9cbb808cc260`  
		Last Modified: Sat, 17 Aug 2024 02:06:29 GMT  
		Size: 14.7 MB (14682856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74854c9deb6c61d7237d96ed4fbf9ce1d1cfb6c5c96db15aa6f752d3de98e505`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:68eadd4ab6a74d7eb35d3de9614774909519d1815b2bae4eeff3fb8ed6ff377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d86196cb99b3a1ae4307279872d879081a638fe2fd7e06ca28f775ccd18e6`

```dockerfile
```

-	Layers:
	-	`sha256:061abd4e9609f49dfeafe478d5a0722edebb0f6bbef5d7e4e151c4fbbb17475d`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 3.7 MB (3692643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c79acac601bb32e9284200f3700167ffaf0beee80a0259b4a712194aaf8355a8`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 24.3 KB (24289 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:a848e1abc7f62c5a935922ce5b49c72016a4314c8f2416fcd702f5bf56c26a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106917655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edef5875167a352f76b5a53f59b0bfa0d7cdc312f4bb3306cfc26a56f9d2bb52`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15870975e17127e7a443d39d43abbf4963d9a1f62811cec1a91dffc2d612a256`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15648f55b06df51e69a53c8b202a2d88efbc1c8bc2a617c745eb76c2de085c`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 4.3 MB (4269669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997986f26d7bc3200c109f836f90037233f986f451bee5fe577007403c395927`  
		Last Modified: Thu, 25 Jul 2024 23:24:01 GMT  
		Size: 14.7 MB (14682898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc105f29c12502685a7d5641dd572d0079afbfc1267ace056b723cc690e98bdc`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:175a1e5a6c958fd4668aef1f9179a897648ac60fc0c521caabe504fc6f255f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3717545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4038ca25a42cf3e3090204ffbae23c8d152e94cc2f53f00816e05c8cde1317`

```dockerfile
```

-	Layers:
	-	`sha256:88ab37d5b25993ecdc7e041fb9ec32170d48e96c4eb2f59f1913d9bf15186c43`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 3.7 MB (3692938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0910728e3a0d5ee1595c00f413fdb2336680bee71dee54bafc20bbc2d612a9`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 24.6 KB (24607 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:e043535dd0cb6d44110ddbccdf8c347ffdfd375d627b1ecef600c822a5a4a6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116072666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8a2ba8d783e90171095785de1374ed9a5d1e9679a48336fe5bf0bd792cf0b3`
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
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1b8f6e7bffef1f98daaa768f140a921205e1bf2023baffce3674e6750ac3`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3d3cea284fe9c435685752db6cde417c8c9b30493750c6e58a4fe94a58933`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 5.0 MB (4965940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876381a76e84f1c0e3d36de8f4ea762b03286854166e12f37f6ed7093c87faac`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 14.7 MB (14682925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce2718da781c97df2fc9e523d360962e79b1b40ccbef726690e727977057737`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:714fb1718ddfe1a880cf7e19413ad01a406a5e8e65931584cd497672ea0d0eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c096b231cb347fc298ed6164b26eeeb4c24ac9cb6f82abd16e398ccd2c321022`

```dockerfile
```

-	Layers:
	-	`sha256:920787445e7e6564babb44dcbaa93be77a6c485bc1d451b824dd2921e46eae16`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 3.7 MB (3697205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c670071fa7ff6c324b34b5e9f184375957e051eed4aaa2000dd07caf0029a85e`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 24.3 KB (24331 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; s390x

```console
$ docker pull zookeeper@sha256:033045354bf5cfe6fae129c60ea68aeb0a8a0973501094f366e5ca83dac401bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104387371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48edcefad5788b920e48d6c87cc4ee3d144e21b3c11c47de4f8ca74b2c438fc`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238133ff9a6cd66afdf7c2fcaac74cbfe7115b2beedf9ff46f9a3c9528d71de`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b972c6d58c217b00136bf4cc4fc998e690b0e88be3e23d0ae04b686d617f28`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 4.2 MB (4242011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca380b31eff308eaee4b8ffc14ec5f180e6cbcec7478eddace51cc2b7f6b58a`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 14.7 MB (14682914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab75c5259daf526c518c9f998b93296fc409f0877b6f481b0f8d54ecc603266d`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:6fba472a430e1edc79f0e0a6a0a3b6e9aca1af8fb138ebb178f6f71738677955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5686f1c7396e4220484fa48112be4eae8fc3e5fc19c777dc817b4e9e194dff7`

```dockerfile
```

-	Layers:
	-	`sha256:4822c77ee8e44425535528966273d3d25865f0d50959773f3314fd6185377da5`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 3.7 MB (3693758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5599b695a82594613ccc7dbdb7e09def855563224cdcd1221596aa05bf49e33c`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8-jre-17`

```console
$ docker pull zookeeper@sha256:7975aa6dc8383c3dbbe59cfd8c06bf9797be7a3df5cfdd68ad728e2945c7eb68
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
$ docker pull zookeeper@sha256:4d48f8685fac03719f1d07a8352ea22e829a41437289138fd8f4372eb9994aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109645323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a804a133f9a0c101a62d8f2e977dc8057b09b4b3a5d9f6c6a72aa5c6a187a6`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb9aab5e496f2b75f2c6b8db8743a344918804c77d8920bfa60ca160b356fb`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb02b55711761ed841333a0ac05dfdc46775f52e3371eabd63cf6f176d294913`  
		Last Modified: Sat, 17 Aug 2024 02:06:29 GMT  
		Size: 4.4 MB (4366041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f0905ea5858bb2e7dd553cfd6c7c707ff5f239f367415ce8ba9cbb808cc260`  
		Last Modified: Sat, 17 Aug 2024 02:06:29 GMT  
		Size: 14.7 MB (14682856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74854c9deb6c61d7237d96ed4fbf9ce1d1cfb6c5c96db15aa6f752d3de98e505`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:68eadd4ab6a74d7eb35d3de9614774909519d1815b2bae4eeff3fb8ed6ff377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d86196cb99b3a1ae4307279872d879081a638fe2fd7e06ca28f775ccd18e6`

```dockerfile
```

-	Layers:
	-	`sha256:061abd4e9609f49dfeafe478d5a0722edebb0f6bbef5d7e4e151c4fbbb17475d`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 3.7 MB (3692643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c79acac601bb32e9284200f3700167ffaf0beee80a0259b4a712194aaf8355a8`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 24.3 KB (24289 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:a848e1abc7f62c5a935922ce5b49c72016a4314c8f2416fcd702f5bf56c26a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106917655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edef5875167a352f76b5a53f59b0bfa0d7cdc312f4bb3306cfc26a56f9d2bb52`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15870975e17127e7a443d39d43abbf4963d9a1f62811cec1a91dffc2d612a256`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15648f55b06df51e69a53c8b202a2d88efbc1c8bc2a617c745eb76c2de085c`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 4.3 MB (4269669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997986f26d7bc3200c109f836f90037233f986f451bee5fe577007403c395927`  
		Last Modified: Thu, 25 Jul 2024 23:24:01 GMT  
		Size: 14.7 MB (14682898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc105f29c12502685a7d5641dd572d0079afbfc1267ace056b723cc690e98bdc`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:175a1e5a6c958fd4668aef1f9179a897648ac60fc0c521caabe504fc6f255f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3717545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4038ca25a42cf3e3090204ffbae23c8d152e94cc2f53f00816e05c8cde1317`

```dockerfile
```

-	Layers:
	-	`sha256:88ab37d5b25993ecdc7e041fb9ec32170d48e96c4eb2f59f1913d9bf15186c43`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 3.7 MB (3692938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0910728e3a0d5ee1595c00f413fdb2336680bee71dee54bafc20bbc2d612a9`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 24.6 KB (24607 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:e043535dd0cb6d44110ddbccdf8c347ffdfd375d627b1ecef600c822a5a4a6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116072666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8a2ba8d783e90171095785de1374ed9a5d1e9679a48336fe5bf0bd792cf0b3`
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
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1b8f6e7bffef1f98daaa768f140a921205e1bf2023baffce3674e6750ac3`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3d3cea284fe9c435685752db6cde417c8c9b30493750c6e58a4fe94a58933`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 5.0 MB (4965940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876381a76e84f1c0e3d36de8f4ea762b03286854166e12f37f6ed7093c87faac`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 14.7 MB (14682925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce2718da781c97df2fc9e523d360962e79b1b40ccbef726690e727977057737`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:714fb1718ddfe1a880cf7e19413ad01a406a5e8e65931584cd497672ea0d0eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c096b231cb347fc298ed6164b26eeeb4c24ac9cb6f82abd16e398ccd2c321022`

```dockerfile
```

-	Layers:
	-	`sha256:920787445e7e6564babb44dcbaa93be77a6c485bc1d451b824dd2921e46eae16`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 3.7 MB (3697205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c670071fa7ff6c324b34b5e9f184375957e051eed4aaa2000dd07caf0029a85e`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 24.3 KB (24331 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:033045354bf5cfe6fae129c60ea68aeb0a8a0973501094f366e5ca83dac401bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104387371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48edcefad5788b920e48d6c87cc4ee3d144e21b3c11c47de4f8ca74b2c438fc`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238133ff9a6cd66afdf7c2fcaac74cbfe7115b2beedf9ff46f9a3c9528d71de`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b972c6d58c217b00136bf4cc4fc998e690b0e88be3e23d0ae04b686d617f28`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 4.2 MB (4242011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca380b31eff308eaee4b8ffc14ec5f180e6cbcec7478eddace51cc2b7f6b58a`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 14.7 MB (14682914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab75c5259daf526c518c9f998b93296fc409f0877b6f481b0f8d54ecc603266d`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:6fba472a430e1edc79f0e0a6a0a3b6e9aca1af8fb138ebb178f6f71738677955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5686f1c7396e4220484fa48112be4eae8fc3e5fc19c777dc817b4e9e194dff7`

```dockerfile
```

-	Layers:
	-	`sha256:4822c77ee8e44425535528966273d3d25865f0d50959773f3314fd6185377da5`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 3.7 MB (3693758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5599b695a82594613ccc7dbdb7e09def855563224cdcd1221596aa05bf49e33c`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8.4`

```console
$ docker pull zookeeper@sha256:7975aa6dc8383c3dbbe59cfd8c06bf9797be7a3df5cfdd68ad728e2945c7eb68
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
$ docker pull zookeeper@sha256:4d48f8685fac03719f1d07a8352ea22e829a41437289138fd8f4372eb9994aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109645323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a804a133f9a0c101a62d8f2e977dc8057b09b4b3a5d9f6c6a72aa5c6a187a6`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb9aab5e496f2b75f2c6b8db8743a344918804c77d8920bfa60ca160b356fb`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb02b55711761ed841333a0ac05dfdc46775f52e3371eabd63cf6f176d294913`  
		Last Modified: Sat, 17 Aug 2024 02:06:29 GMT  
		Size: 4.4 MB (4366041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f0905ea5858bb2e7dd553cfd6c7c707ff5f239f367415ce8ba9cbb808cc260`  
		Last Modified: Sat, 17 Aug 2024 02:06:29 GMT  
		Size: 14.7 MB (14682856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74854c9deb6c61d7237d96ed4fbf9ce1d1cfb6c5c96db15aa6f752d3de98e505`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:68eadd4ab6a74d7eb35d3de9614774909519d1815b2bae4eeff3fb8ed6ff377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d86196cb99b3a1ae4307279872d879081a638fe2fd7e06ca28f775ccd18e6`

```dockerfile
```

-	Layers:
	-	`sha256:061abd4e9609f49dfeafe478d5a0722edebb0f6bbef5d7e4e151c4fbbb17475d`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 3.7 MB (3692643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c79acac601bb32e9284200f3700167ffaf0beee80a0259b4a712194aaf8355a8`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 24.3 KB (24289 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:a848e1abc7f62c5a935922ce5b49c72016a4314c8f2416fcd702f5bf56c26a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106917655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edef5875167a352f76b5a53f59b0bfa0d7cdc312f4bb3306cfc26a56f9d2bb52`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15870975e17127e7a443d39d43abbf4963d9a1f62811cec1a91dffc2d612a256`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15648f55b06df51e69a53c8b202a2d88efbc1c8bc2a617c745eb76c2de085c`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 4.3 MB (4269669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997986f26d7bc3200c109f836f90037233f986f451bee5fe577007403c395927`  
		Last Modified: Thu, 25 Jul 2024 23:24:01 GMT  
		Size: 14.7 MB (14682898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc105f29c12502685a7d5641dd572d0079afbfc1267ace056b723cc690e98bdc`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:175a1e5a6c958fd4668aef1f9179a897648ac60fc0c521caabe504fc6f255f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3717545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4038ca25a42cf3e3090204ffbae23c8d152e94cc2f53f00816e05c8cde1317`

```dockerfile
```

-	Layers:
	-	`sha256:88ab37d5b25993ecdc7e041fb9ec32170d48e96c4eb2f59f1913d9bf15186c43`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 3.7 MB (3692938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0910728e3a0d5ee1595c00f413fdb2336680bee71dee54bafc20bbc2d612a9`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 24.6 KB (24607 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:e043535dd0cb6d44110ddbccdf8c347ffdfd375d627b1ecef600c822a5a4a6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116072666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8a2ba8d783e90171095785de1374ed9a5d1e9679a48336fe5bf0bd792cf0b3`
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
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1b8f6e7bffef1f98daaa768f140a921205e1bf2023baffce3674e6750ac3`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3d3cea284fe9c435685752db6cde417c8c9b30493750c6e58a4fe94a58933`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 5.0 MB (4965940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876381a76e84f1c0e3d36de8f4ea762b03286854166e12f37f6ed7093c87faac`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 14.7 MB (14682925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce2718da781c97df2fc9e523d360962e79b1b40ccbef726690e727977057737`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:714fb1718ddfe1a880cf7e19413ad01a406a5e8e65931584cd497672ea0d0eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c096b231cb347fc298ed6164b26eeeb4c24ac9cb6f82abd16e398ccd2c321022`

```dockerfile
```

-	Layers:
	-	`sha256:920787445e7e6564babb44dcbaa93be77a6c485bc1d451b824dd2921e46eae16`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 3.7 MB (3697205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c670071fa7ff6c324b34b5e9f184375957e051eed4aaa2000dd07caf0029a85e`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 24.3 KB (24331 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4` - linux; s390x

```console
$ docker pull zookeeper@sha256:033045354bf5cfe6fae129c60ea68aeb0a8a0973501094f366e5ca83dac401bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104387371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48edcefad5788b920e48d6c87cc4ee3d144e21b3c11c47de4f8ca74b2c438fc`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238133ff9a6cd66afdf7c2fcaac74cbfe7115b2beedf9ff46f9a3c9528d71de`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b972c6d58c217b00136bf4cc4fc998e690b0e88be3e23d0ae04b686d617f28`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 4.2 MB (4242011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca380b31eff308eaee4b8ffc14ec5f180e6cbcec7478eddace51cc2b7f6b58a`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 14.7 MB (14682914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab75c5259daf526c518c9f998b93296fc409f0877b6f481b0f8d54ecc603266d`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:6fba472a430e1edc79f0e0a6a0a3b6e9aca1af8fb138ebb178f6f71738677955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5686f1c7396e4220484fa48112be4eae8fc3e5fc19c777dc817b4e9e194dff7`

```dockerfile
```

-	Layers:
	-	`sha256:4822c77ee8e44425535528966273d3d25865f0d50959773f3314fd6185377da5`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 3.7 MB (3693758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5599b695a82594613ccc7dbdb7e09def855563224cdcd1221596aa05bf49e33c`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8.4-jre-17`

```console
$ docker pull zookeeper@sha256:7975aa6dc8383c3dbbe59cfd8c06bf9797be7a3df5cfdd68ad728e2945c7eb68
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
$ docker pull zookeeper@sha256:4d48f8685fac03719f1d07a8352ea22e829a41437289138fd8f4372eb9994aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109645323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a804a133f9a0c101a62d8f2e977dc8057b09b4b3a5d9f6c6a72aa5c6a187a6`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb9aab5e496f2b75f2c6b8db8743a344918804c77d8920bfa60ca160b356fb`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb02b55711761ed841333a0ac05dfdc46775f52e3371eabd63cf6f176d294913`  
		Last Modified: Sat, 17 Aug 2024 02:06:29 GMT  
		Size: 4.4 MB (4366041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f0905ea5858bb2e7dd553cfd6c7c707ff5f239f367415ce8ba9cbb808cc260`  
		Last Modified: Sat, 17 Aug 2024 02:06:29 GMT  
		Size: 14.7 MB (14682856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74854c9deb6c61d7237d96ed4fbf9ce1d1cfb6c5c96db15aa6f752d3de98e505`  
		Last Modified: Sat, 17 Aug 2024 02:06:27 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:68eadd4ab6a74d7eb35d3de9614774909519d1815b2bae4eeff3fb8ed6ff377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d86196cb99b3a1ae4307279872d879081a638fe2fd7e06ca28f775ccd18e6`

```dockerfile
```

-	Layers:
	-	`sha256:061abd4e9609f49dfeafe478d5a0722edebb0f6bbef5d7e4e151c4fbbb17475d`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 3.7 MB (3692643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c79acac601bb32e9284200f3700167ffaf0beee80a0259b4a712194aaf8355a8`  
		Last Modified: Sat, 17 Aug 2024 02:06:28 GMT  
		Size: 24.3 KB (24289 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:a848e1abc7f62c5a935922ce5b49c72016a4314c8f2416fcd702f5bf56c26a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106917655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edef5875167a352f76b5a53f59b0bfa0d7cdc312f4bb3306cfc26a56f9d2bb52`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15870975e17127e7a443d39d43abbf4963d9a1f62811cec1a91dffc2d612a256`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15648f55b06df51e69a53c8b202a2d88efbc1c8bc2a617c745eb76c2de085c`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 4.3 MB (4269669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997986f26d7bc3200c109f836f90037233f986f451bee5fe577007403c395927`  
		Last Modified: Thu, 25 Jul 2024 23:24:01 GMT  
		Size: 14.7 MB (14682898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc105f29c12502685a7d5641dd572d0079afbfc1267ace056b723cc690e98bdc`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:175a1e5a6c958fd4668aef1f9179a897648ac60fc0c521caabe504fc6f255f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3717545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4038ca25a42cf3e3090204ffbae23c8d152e94cc2f53f00816e05c8cde1317`

```dockerfile
```

-	Layers:
	-	`sha256:88ab37d5b25993ecdc7e041fb9ec32170d48e96c4eb2f59f1913d9bf15186c43`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 3.7 MB (3692938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0910728e3a0d5ee1595c00f413fdb2336680bee71dee54bafc20bbc2d612a9`  
		Last Modified: Thu, 25 Jul 2024 23:24:00 GMT  
		Size: 24.6 KB (24607 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:e043535dd0cb6d44110ddbccdf8c347ffdfd375d627b1ecef600c822a5a4a6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116072666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8a2ba8d783e90171095785de1374ed9a5d1e9679a48336fe5bf0bd792cf0b3`
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
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1b8f6e7bffef1f98daaa768f140a921205e1bf2023baffce3674e6750ac3`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3d3cea284fe9c435685752db6cde417c8c9b30493750c6e58a4fe94a58933`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 5.0 MB (4965940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876381a76e84f1c0e3d36de8f4ea762b03286854166e12f37f6ed7093c87faac`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 14.7 MB (14682925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce2718da781c97df2fc9e523d360962e79b1b40ccbef726690e727977057737`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:714fb1718ddfe1a880cf7e19413ad01a406a5e8e65931584cd497672ea0d0eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c096b231cb347fc298ed6164b26eeeb4c24ac9cb6f82abd16e398ccd2c321022`

```dockerfile
```

-	Layers:
	-	`sha256:920787445e7e6564babb44dcbaa93be77a6c485bc1d451b824dd2921e46eae16`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 3.7 MB (3697205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c670071fa7ff6c324b34b5e9f184375957e051eed4aaa2000dd07caf0029a85e`  
		Last Modified: Thu, 25 Jul 2024 19:52:57 GMT  
		Size: 24.3 KB (24331 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:033045354bf5cfe6fae129c60ea68aeb0a8a0973501094f366e5ca83dac401bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104387371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48edcefad5788b920e48d6c87cc4ee3d144e21b3c11c47de4f8ca74b2c438fc`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238133ff9a6cd66afdf7c2fcaac74cbfe7115b2beedf9ff46f9a3c9528d71de`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b972c6d58c217b00136bf4cc4fc998e690b0e88be3e23d0ae04b686d617f28`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 4.2 MB (4242011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca380b31eff308eaee4b8ffc14ec5f180e6cbcec7478eddace51cc2b7f6b58a`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 14.7 MB (14682914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab75c5259daf526c518c9f998b93296fc409f0877b6f481b0f8d54ecc603266d`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:6fba472a430e1edc79f0e0a6a0a3b6e9aca1af8fb138ebb178f6f71738677955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5686f1c7396e4220484fa48112be4eae8fc3e5fc19c777dc817b4e9e194dff7`

```dockerfile
```

-	Layers:
	-	`sha256:4822c77ee8e44425535528966273d3d25865f0d50959773f3314fd6185377da5`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 3.7 MB (3693758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5599b695a82594613ccc7dbdb7e09def855563224cdcd1221596aa05bf49e33c`  
		Last Modified: Sat, 17 Aug 2024 05:21:21 GMT  
		Size: 24.3 KB (24290 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9`

```console
$ docker pull zookeeper@sha256:d6c878806cddff9b5332e7b72b656702223e3ddf485b186df149ce08c4a83bc5
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
$ docker pull zookeeper@sha256:5d0eeae1ac0bc849263fad77e1fd7f307c2ae18129298c2608e3087510712259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115262774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4777364d8f9c57f4583cbfdb9f518bfb2e737978be76bd7bed8a04692059faf2`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bc24e43d0c762bf9cb27d8a2b827809e7d266320d09f0f38a256968469558`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ab09606e504d0607d074ab6348003e5dbdeb584fcf1e9dcda83223743ada48`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 4.4 MB (4366140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d8ca367f2955fcf8791a0c33d2f01250a5b55afa818d97364c425836964efa`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 20.3 MB (20300206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc73fa90c8aab2c5214bd61e0c9bb276086781ad9046e068de950ae250539941`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:90a031436d30416d6eb03cb5533ad369b4acf05b5d11839c03e55e05acd93332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9097a75028afaa2cfb70a66f52d978761ec873ad1c6ad802c8fa196c8a6ef7`

```dockerfile
```

-	Layers:
	-	`sha256:7ff0f2dd40795c20db8b203933301ae325dcd030e35506ab42b0c73b87b557a1`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 3.7 MB (3698798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d802dc6c9c4f5db2b8922bbcbd62d5e51f0dc34619fb3487be4d1ace57161c`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 24.6 KB (24593 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:a9bd668af1ce5eb33d0ae12bf19820b2fb2f5b04eaa7a0c21eeb6831ddbcfab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112534954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6cda4d9baeebbf25edf6b724469e0e907a68a89f7dcbca8dcf6106990719ca`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15870975e17127e7a443d39d43abbf4963d9a1f62811cec1a91dffc2d612a256`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15648f55b06df51e69a53c8b202a2d88efbc1c8bc2a617c745eb76c2de085c`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 4.3 MB (4269669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39797bb9936c13a2134dcce87b51093c90a778fb2fd59f5b39fca19925413848`  
		Last Modified: Thu, 25 Jul 2024 23:25:23 GMT  
		Size: 20.3 MB (20300197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b026b6fb1149f9343cbc1300ec15eb956e711e6a82427f86edc2c9d0fec22413`  
		Last Modified: Thu, 25 Jul 2024 23:25:22 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:a31575f2f34be702561c7f82a9ec1a2f330a9a609a7cdc2d6e0f2a677eb86e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6199604ee81dda182d3ee4066fc8290c25cc341e7b2605f53bd6828cdfde0960`

```dockerfile
```

-	Layers:
	-	`sha256:08dd1029f8b0d40ce83d8c52d90407a4d5485d46f56f1933a4182ff103f8abcc`  
		Last Modified: Thu, 25 Jul 2024 23:25:23 GMT  
		Size: 3.7 MB (3699105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d7970a7e9ba69fad2173ea820eb41acd611c432d31ab3eaeb8f6f47a75024d5`  
		Last Modified: Thu, 25 Jul 2024 23:25:22 GMT  
		Size: 24.9 KB (24923 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:52cc6b54ab463c414c96af3a7acbc45c4fe2977a0dbe45c4d51d722f9e53f101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121689669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a4bdfd994d6e2cc0f06d5f89483ec140ddae445bf8a550baaaa7af05a1515b`
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
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1b8f6e7bffef1f98daaa768f140a921205e1bf2023baffce3674e6750ac3`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3d3cea284fe9c435685752db6cde417c8c9b30493750c6e58a4fe94a58933`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 5.0 MB (4965940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac7d7764ba2277c6510ad8003413688a697392c243b0bf72b855dc7717903e`  
		Last Modified: Thu, 25 Jul 2024 19:53:39 GMT  
		Size: 20.3 MB (20299928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287021a98137995e9674ccbb70d719222ec7c4d520596294335757407fb21b95`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4070ba9386362ca3a0c66029211455d3abc240d99c3a92da44383b6b6bf15d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731b66ae391488382292e0dc99862e6a2e2b4eab3bf7db8aca1f41215ae2ad25`

```dockerfile
```

-	Layers:
	-	`sha256:0f77aba2cb2c0a7d51516c49cc6a160bd0fbaa1720f2ef075d453477a6a3641c`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 3.7 MB (3703366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46cfd64a689b5c2338cd7bc9ec998c978befc3ba1eeeccff50aea8e53688846`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 24.6 KB (24642 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; s390x

```console
$ docker pull zookeeper@sha256:1f407ae269540432b6b2165e19daa62ef302aef9aab271d73a766f16817289e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110004417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da6b54fda6f2f05c1dedbdc0f8c2eebc186af237e1defa3b31133e595ecb8da`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238133ff9a6cd66afdf7c2fcaac74cbfe7115b2beedf9ff46f9a3c9528d71de`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b972c6d58c217b00136bf4cc4fc998e690b0e88be3e23d0ae04b686d617f28`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 4.2 MB (4242011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206f2fa595ecc38363ffc2d9f1f2143502ee8d5caed3ab593501891b96139c80`  
		Last Modified: Sat, 17 Aug 2024 05:21:57 GMT  
		Size: 20.3 MB (20299960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c12fad4247efc0fc7acbc6e6407c994457f2393c231bba7225ba118895bc9`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:77014a16f6fe0089be6459d2a316786f1c20c5e7cdf2963085d214633bc07431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2a832b9838abda2675560733e1c0724e63f98136cb6a22a7b3aac4ec81d072`

```dockerfile
```

-	Layers:
	-	`sha256:1c761c63baf36b60ae3f076c228cb7e52f9780b8fde9ef9b2af51f5ba5a49bc5`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 3.7 MB (3699913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b9c57d1a846f9ab14e5555884493bd30085ee0ae01461b4fcfeac783a6ad53`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9-jre-17`

```console
$ docker pull zookeeper@sha256:d6c878806cddff9b5332e7b72b656702223e3ddf485b186df149ce08c4a83bc5
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
$ docker pull zookeeper@sha256:5d0eeae1ac0bc849263fad77e1fd7f307c2ae18129298c2608e3087510712259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115262774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4777364d8f9c57f4583cbfdb9f518bfb2e737978be76bd7bed8a04692059faf2`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bc24e43d0c762bf9cb27d8a2b827809e7d266320d09f0f38a256968469558`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ab09606e504d0607d074ab6348003e5dbdeb584fcf1e9dcda83223743ada48`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 4.4 MB (4366140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d8ca367f2955fcf8791a0c33d2f01250a5b55afa818d97364c425836964efa`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 20.3 MB (20300206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc73fa90c8aab2c5214bd61e0c9bb276086781ad9046e068de950ae250539941`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:90a031436d30416d6eb03cb5533ad369b4acf05b5d11839c03e55e05acd93332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9097a75028afaa2cfb70a66f52d978761ec873ad1c6ad802c8fa196c8a6ef7`

```dockerfile
```

-	Layers:
	-	`sha256:7ff0f2dd40795c20db8b203933301ae325dcd030e35506ab42b0c73b87b557a1`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 3.7 MB (3698798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d802dc6c9c4f5db2b8922bbcbd62d5e51f0dc34619fb3487be4d1ace57161c`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 24.6 KB (24593 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:a9bd668af1ce5eb33d0ae12bf19820b2fb2f5b04eaa7a0c21eeb6831ddbcfab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112534954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6cda4d9baeebbf25edf6b724469e0e907a68a89f7dcbca8dcf6106990719ca`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15870975e17127e7a443d39d43abbf4963d9a1f62811cec1a91dffc2d612a256`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15648f55b06df51e69a53c8b202a2d88efbc1c8bc2a617c745eb76c2de085c`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 4.3 MB (4269669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39797bb9936c13a2134dcce87b51093c90a778fb2fd59f5b39fca19925413848`  
		Last Modified: Thu, 25 Jul 2024 23:25:23 GMT  
		Size: 20.3 MB (20300197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b026b6fb1149f9343cbc1300ec15eb956e711e6a82427f86edc2c9d0fec22413`  
		Last Modified: Thu, 25 Jul 2024 23:25:22 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:a31575f2f34be702561c7f82a9ec1a2f330a9a609a7cdc2d6e0f2a677eb86e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6199604ee81dda182d3ee4066fc8290c25cc341e7b2605f53bd6828cdfde0960`

```dockerfile
```

-	Layers:
	-	`sha256:08dd1029f8b0d40ce83d8c52d90407a4d5485d46f56f1933a4182ff103f8abcc`  
		Last Modified: Thu, 25 Jul 2024 23:25:23 GMT  
		Size: 3.7 MB (3699105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d7970a7e9ba69fad2173ea820eb41acd611c432d31ab3eaeb8f6f47a75024d5`  
		Last Modified: Thu, 25 Jul 2024 23:25:22 GMT  
		Size: 24.9 KB (24923 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:52cc6b54ab463c414c96af3a7acbc45c4fe2977a0dbe45c4d51d722f9e53f101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121689669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a4bdfd994d6e2cc0f06d5f89483ec140ddae445bf8a550baaaa7af05a1515b`
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
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1b8f6e7bffef1f98daaa768f140a921205e1bf2023baffce3674e6750ac3`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3d3cea284fe9c435685752db6cde417c8c9b30493750c6e58a4fe94a58933`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 5.0 MB (4965940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac7d7764ba2277c6510ad8003413688a697392c243b0bf72b855dc7717903e`  
		Last Modified: Thu, 25 Jul 2024 19:53:39 GMT  
		Size: 20.3 MB (20299928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287021a98137995e9674ccbb70d719222ec7c4d520596294335757407fb21b95`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4070ba9386362ca3a0c66029211455d3abc240d99c3a92da44383b6b6bf15d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731b66ae391488382292e0dc99862e6a2e2b4eab3bf7db8aca1f41215ae2ad25`

```dockerfile
```

-	Layers:
	-	`sha256:0f77aba2cb2c0a7d51516c49cc6a160bd0fbaa1720f2ef075d453477a6a3641c`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 3.7 MB (3703366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46cfd64a689b5c2338cd7bc9ec998c978befc3ba1eeeccff50aea8e53688846`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 24.6 KB (24642 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:1f407ae269540432b6b2165e19daa62ef302aef9aab271d73a766f16817289e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110004417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da6b54fda6f2f05c1dedbdc0f8c2eebc186af237e1defa3b31133e595ecb8da`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238133ff9a6cd66afdf7c2fcaac74cbfe7115b2beedf9ff46f9a3c9528d71de`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b972c6d58c217b00136bf4cc4fc998e690b0e88be3e23d0ae04b686d617f28`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 4.2 MB (4242011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206f2fa595ecc38363ffc2d9f1f2143502ee8d5caed3ab593501891b96139c80`  
		Last Modified: Sat, 17 Aug 2024 05:21:57 GMT  
		Size: 20.3 MB (20299960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c12fad4247efc0fc7acbc6e6407c994457f2393c231bba7225ba118895bc9`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:77014a16f6fe0089be6459d2a316786f1c20c5e7cdf2963085d214633bc07431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2a832b9838abda2675560733e1c0724e63f98136cb6a22a7b3aac4ec81d072`

```dockerfile
```

-	Layers:
	-	`sha256:1c761c63baf36b60ae3f076c228cb7e52f9780b8fde9ef9b2af51f5ba5a49bc5`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 3.7 MB (3699913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b9c57d1a846f9ab14e5555884493bd30085ee0ae01461b4fcfeac783a6ad53`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9.2`

```console
$ docker pull zookeeper@sha256:d6c878806cddff9b5332e7b72b656702223e3ddf485b186df149ce08c4a83bc5
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
$ docker pull zookeeper@sha256:5d0eeae1ac0bc849263fad77e1fd7f307c2ae18129298c2608e3087510712259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115262774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4777364d8f9c57f4583cbfdb9f518bfb2e737978be76bd7bed8a04692059faf2`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bc24e43d0c762bf9cb27d8a2b827809e7d266320d09f0f38a256968469558`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ab09606e504d0607d074ab6348003e5dbdeb584fcf1e9dcda83223743ada48`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 4.4 MB (4366140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d8ca367f2955fcf8791a0c33d2f01250a5b55afa818d97364c425836964efa`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 20.3 MB (20300206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc73fa90c8aab2c5214bd61e0c9bb276086781ad9046e068de950ae250539941`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:90a031436d30416d6eb03cb5533ad369b4acf05b5d11839c03e55e05acd93332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9097a75028afaa2cfb70a66f52d978761ec873ad1c6ad802c8fa196c8a6ef7`

```dockerfile
```

-	Layers:
	-	`sha256:7ff0f2dd40795c20db8b203933301ae325dcd030e35506ab42b0c73b87b557a1`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 3.7 MB (3698798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d802dc6c9c4f5db2b8922bbcbd62d5e51f0dc34619fb3487be4d1ace57161c`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 24.6 KB (24593 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:a9bd668af1ce5eb33d0ae12bf19820b2fb2f5b04eaa7a0c21eeb6831ddbcfab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112534954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6cda4d9baeebbf25edf6b724469e0e907a68a89f7dcbca8dcf6106990719ca`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15870975e17127e7a443d39d43abbf4963d9a1f62811cec1a91dffc2d612a256`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15648f55b06df51e69a53c8b202a2d88efbc1c8bc2a617c745eb76c2de085c`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 4.3 MB (4269669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39797bb9936c13a2134dcce87b51093c90a778fb2fd59f5b39fca19925413848`  
		Last Modified: Thu, 25 Jul 2024 23:25:23 GMT  
		Size: 20.3 MB (20300197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b026b6fb1149f9343cbc1300ec15eb956e711e6a82427f86edc2c9d0fec22413`  
		Last Modified: Thu, 25 Jul 2024 23:25:22 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:a31575f2f34be702561c7f82a9ec1a2f330a9a609a7cdc2d6e0f2a677eb86e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6199604ee81dda182d3ee4066fc8290c25cc341e7b2605f53bd6828cdfde0960`

```dockerfile
```

-	Layers:
	-	`sha256:08dd1029f8b0d40ce83d8c52d90407a4d5485d46f56f1933a4182ff103f8abcc`  
		Last Modified: Thu, 25 Jul 2024 23:25:23 GMT  
		Size: 3.7 MB (3699105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d7970a7e9ba69fad2173ea820eb41acd611c432d31ab3eaeb8f6f47a75024d5`  
		Last Modified: Thu, 25 Jul 2024 23:25:22 GMT  
		Size: 24.9 KB (24923 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:52cc6b54ab463c414c96af3a7acbc45c4fe2977a0dbe45c4d51d722f9e53f101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121689669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a4bdfd994d6e2cc0f06d5f89483ec140ddae445bf8a550baaaa7af05a1515b`
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
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1b8f6e7bffef1f98daaa768f140a921205e1bf2023baffce3674e6750ac3`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3d3cea284fe9c435685752db6cde417c8c9b30493750c6e58a4fe94a58933`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 5.0 MB (4965940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac7d7764ba2277c6510ad8003413688a697392c243b0bf72b855dc7717903e`  
		Last Modified: Thu, 25 Jul 2024 19:53:39 GMT  
		Size: 20.3 MB (20299928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287021a98137995e9674ccbb70d719222ec7c4d520596294335757407fb21b95`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4070ba9386362ca3a0c66029211455d3abc240d99c3a92da44383b6b6bf15d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731b66ae391488382292e0dc99862e6a2e2b4eab3bf7db8aca1f41215ae2ad25`

```dockerfile
```

-	Layers:
	-	`sha256:0f77aba2cb2c0a7d51516c49cc6a160bd0fbaa1720f2ef075d453477a6a3641c`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 3.7 MB (3703366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46cfd64a689b5c2338cd7bc9ec998c978befc3ba1eeeccff50aea8e53688846`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 24.6 KB (24642 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2` - linux; s390x

```console
$ docker pull zookeeper@sha256:1f407ae269540432b6b2165e19daa62ef302aef9aab271d73a766f16817289e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110004417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da6b54fda6f2f05c1dedbdc0f8c2eebc186af237e1defa3b31133e595ecb8da`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238133ff9a6cd66afdf7c2fcaac74cbfe7115b2beedf9ff46f9a3c9528d71de`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b972c6d58c217b00136bf4cc4fc998e690b0e88be3e23d0ae04b686d617f28`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 4.2 MB (4242011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206f2fa595ecc38363ffc2d9f1f2143502ee8d5caed3ab593501891b96139c80`  
		Last Modified: Sat, 17 Aug 2024 05:21:57 GMT  
		Size: 20.3 MB (20299960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c12fad4247efc0fc7acbc6e6407c994457f2393c231bba7225ba118895bc9`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2` - unknown; unknown

```console
$ docker pull zookeeper@sha256:77014a16f6fe0089be6459d2a316786f1c20c5e7cdf2963085d214633bc07431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2a832b9838abda2675560733e1c0724e63f98136cb6a22a7b3aac4ec81d072`

```dockerfile
```

-	Layers:
	-	`sha256:1c761c63baf36b60ae3f076c228cb7e52f9780b8fde9ef9b2af51f5ba5a49bc5`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 3.7 MB (3699913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b9c57d1a846f9ab14e5555884493bd30085ee0ae01461b4fcfeac783a6ad53`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9.2-jre-17`

```console
$ docker pull zookeeper@sha256:d6c878806cddff9b5332e7b72b656702223e3ddf485b186df149ce08c4a83bc5
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
$ docker pull zookeeper@sha256:5d0eeae1ac0bc849263fad77e1fd7f307c2ae18129298c2608e3087510712259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115262774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4777364d8f9c57f4583cbfdb9f518bfb2e737978be76bd7bed8a04692059faf2`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bc24e43d0c762bf9cb27d8a2b827809e7d266320d09f0f38a256968469558`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ab09606e504d0607d074ab6348003e5dbdeb584fcf1e9dcda83223743ada48`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 4.4 MB (4366140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d8ca367f2955fcf8791a0c33d2f01250a5b55afa818d97364c425836964efa`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 20.3 MB (20300206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc73fa90c8aab2c5214bd61e0c9bb276086781ad9046e068de950ae250539941`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:90a031436d30416d6eb03cb5533ad369b4acf05b5d11839c03e55e05acd93332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9097a75028afaa2cfb70a66f52d978761ec873ad1c6ad802c8fa196c8a6ef7`

```dockerfile
```

-	Layers:
	-	`sha256:7ff0f2dd40795c20db8b203933301ae325dcd030e35506ab42b0c73b87b557a1`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 3.7 MB (3698798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d802dc6c9c4f5db2b8922bbcbd62d5e51f0dc34619fb3487be4d1ace57161c`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 24.6 KB (24593 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:a9bd668af1ce5eb33d0ae12bf19820b2fb2f5b04eaa7a0c21eeb6831ddbcfab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112534954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6cda4d9baeebbf25edf6b724469e0e907a68a89f7dcbca8dcf6106990719ca`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15870975e17127e7a443d39d43abbf4963d9a1f62811cec1a91dffc2d612a256`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15648f55b06df51e69a53c8b202a2d88efbc1c8bc2a617c745eb76c2de085c`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 4.3 MB (4269669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39797bb9936c13a2134dcce87b51093c90a778fb2fd59f5b39fca19925413848`  
		Last Modified: Thu, 25 Jul 2024 23:25:23 GMT  
		Size: 20.3 MB (20300197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b026b6fb1149f9343cbc1300ec15eb956e711e6a82427f86edc2c9d0fec22413`  
		Last Modified: Thu, 25 Jul 2024 23:25:22 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:a31575f2f34be702561c7f82a9ec1a2f330a9a609a7cdc2d6e0f2a677eb86e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6199604ee81dda182d3ee4066fc8290c25cc341e7b2605f53bd6828cdfde0960`

```dockerfile
```

-	Layers:
	-	`sha256:08dd1029f8b0d40ce83d8c52d90407a4d5485d46f56f1933a4182ff103f8abcc`  
		Last Modified: Thu, 25 Jul 2024 23:25:23 GMT  
		Size: 3.7 MB (3699105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d7970a7e9ba69fad2173ea820eb41acd611c432d31ab3eaeb8f6f47a75024d5`  
		Last Modified: Thu, 25 Jul 2024 23:25:22 GMT  
		Size: 24.9 KB (24923 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:52cc6b54ab463c414c96af3a7acbc45c4fe2977a0dbe45c4d51d722f9e53f101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121689669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a4bdfd994d6e2cc0f06d5f89483ec140ddae445bf8a550baaaa7af05a1515b`
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
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1b8f6e7bffef1f98daaa768f140a921205e1bf2023baffce3674e6750ac3`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3d3cea284fe9c435685752db6cde417c8c9b30493750c6e58a4fe94a58933`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 5.0 MB (4965940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac7d7764ba2277c6510ad8003413688a697392c243b0bf72b855dc7717903e`  
		Last Modified: Thu, 25 Jul 2024 19:53:39 GMT  
		Size: 20.3 MB (20299928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287021a98137995e9674ccbb70d719222ec7c4d520596294335757407fb21b95`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4070ba9386362ca3a0c66029211455d3abc240d99c3a92da44383b6b6bf15d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731b66ae391488382292e0dc99862e6a2e2b4eab3bf7db8aca1f41215ae2ad25`

```dockerfile
```

-	Layers:
	-	`sha256:0f77aba2cb2c0a7d51516c49cc6a160bd0fbaa1720f2ef075d453477a6a3641c`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 3.7 MB (3703366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46cfd64a689b5c2338cd7bc9ec998c978befc3ba1eeeccff50aea8e53688846`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 24.6 KB (24642 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.2-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:1f407ae269540432b6b2165e19daa62ef302aef9aab271d73a766f16817289e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110004417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da6b54fda6f2f05c1dedbdc0f8c2eebc186af237e1defa3b31133e595ecb8da`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238133ff9a6cd66afdf7c2fcaac74cbfe7115b2beedf9ff46f9a3c9528d71de`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b972c6d58c217b00136bf4cc4fc998e690b0e88be3e23d0ae04b686d617f28`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 4.2 MB (4242011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206f2fa595ecc38363ffc2d9f1f2143502ee8d5caed3ab593501891b96139c80`  
		Last Modified: Sat, 17 Aug 2024 05:21:57 GMT  
		Size: 20.3 MB (20299960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c12fad4247efc0fc7acbc6e6407c994457f2393c231bba7225ba118895bc9`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.2-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:77014a16f6fe0089be6459d2a316786f1c20c5e7cdf2963085d214633bc07431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2a832b9838abda2675560733e1c0724e63f98136cb6a22a7b3aac4ec81d072`

```dockerfile
```

-	Layers:
	-	`sha256:1c761c63baf36b60ae3f076c228cb7e52f9780b8fde9ef9b2af51f5ba5a49bc5`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 3.7 MB (3699913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b9c57d1a846f9ab14e5555884493bd30085ee0ae01461b4fcfeac783a6ad53`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:d6c878806cddff9b5332e7b72b656702223e3ddf485b186df149ce08c4a83bc5
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
$ docker pull zookeeper@sha256:5d0eeae1ac0bc849263fad77e1fd7f307c2ae18129298c2608e3087510712259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115262774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4777364d8f9c57f4583cbfdb9f518bfb2e737978be76bd7bed8a04692059faf2`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bc24e43d0c762bf9cb27d8a2b827809e7d266320d09f0f38a256968469558`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ab09606e504d0607d074ab6348003e5dbdeb584fcf1e9dcda83223743ada48`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 4.4 MB (4366140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d8ca367f2955fcf8791a0c33d2f01250a5b55afa818d97364c425836964efa`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 20.3 MB (20300206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc73fa90c8aab2c5214bd61e0c9bb276086781ad9046e068de950ae250539941`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:90a031436d30416d6eb03cb5533ad369b4acf05b5d11839c03e55e05acd93332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9097a75028afaa2cfb70a66f52d978761ec873ad1c6ad802c8fa196c8a6ef7`

```dockerfile
```

-	Layers:
	-	`sha256:7ff0f2dd40795c20db8b203933301ae325dcd030e35506ab42b0c73b87b557a1`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 3.7 MB (3698798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d802dc6c9c4f5db2b8922bbcbd62d5e51f0dc34619fb3487be4d1ace57161c`  
		Last Modified: Sat, 17 Aug 2024 02:06:19 GMT  
		Size: 24.6 KB (24593 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:a9bd668af1ce5eb33d0ae12bf19820b2fb2f5b04eaa7a0c21eeb6831ddbcfab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112534954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6cda4d9baeebbf25edf6b724469e0e907a68a89f7dcbca8dcf6106990719ca`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15870975e17127e7a443d39d43abbf4963d9a1f62811cec1a91dffc2d612a256`  
		Last Modified: Thu, 25 Jul 2024 23:23:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15648f55b06df51e69a53c8b202a2d88efbc1c8bc2a617c745eb76c2de085c`  
		Last Modified: Thu, 25 Jul 2024 23:23:35 GMT  
		Size: 4.3 MB (4269669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39797bb9936c13a2134dcce87b51093c90a778fb2fd59f5b39fca19925413848`  
		Last Modified: Thu, 25 Jul 2024 23:25:23 GMT  
		Size: 20.3 MB (20300197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b026b6fb1149f9343cbc1300ec15eb956e711e6a82427f86edc2c9d0fec22413`  
		Last Modified: Thu, 25 Jul 2024 23:25:22 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:a31575f2f34be702561c7f82a9ec1a2f330a9a609a7cdc2d6e0f2a677eb86e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6199604ee81dda182d3ee4066fc8290c25cc341e7b2605f53bd6828cdfde0960`

```dockerfile
```

-	Layers:
	-	`sha256:08dd1029f8b0d40ce83d8c52d90407a4d5485d46f56f1933a4182ff103f8abcc`  
		Last Modified: Thu, 25 Jul 2024 23:25:23 GMT  
		Size: 3.7 MB (3699105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d7970a7e9ba69fad2173ea820eb41acd611c432d31ab3eaeb8f6f47a75024d5`  
		Last Modified: Thu, 25 Jul 2024 23:25:22 GMT  
		Size: 24.9 KB (24923 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:52cc6b54ab463c414c96af3a7acbc45c4fe2977a0dbe45c4d51d722f9e53f101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121689669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a4bdfd994d6e2cc0f06d5f89483ec140ddae445bf8a550baaaa7af05a1515b`
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
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4501dd6074b80358d89c6239634e02c9e3c7a407dbd612dfd6dc085f1934d3`  
		Last Modified: Tue, 23 Jul 2024 01:44:18 GMT  
		Size: 47.1 MB (47115976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2d9c80b85759626527777e1505c9b01d07cbe4f2094ffd7ee9742ce0930f3`  
		Last Modified: Tue, 23 Jul 2024 01:44:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c0fab528a21acd3e451ea592d4bb22003788b0452ac550512edb35b726fc4`  
		Last Modified: Thu, 25 Jul 2024 17:25:29 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39df1b8f6e7bffef1f98daaa768f140a921205e1bf2023baffce3674e6750ac3`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3d3cea284fe9c435685752db6cde417c8c9b30493750c6e58a4fe94a58933`  
		Last Modified: Thu, 25 Jul 2024 19:52:14 GMT  
		Size: 5.0 MB (4965940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac7d7764ba2277c6510ad8003413688a697392c243b0bf72b855dc7717903e`  
		Last Modified: Thu, 25 Jul 2024 19:53:39 GMT  
		Size: 20.3 MB (20299928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287021a98137995e9674ccbb70d719222ec7c4d520596294335757407fb21b95`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4070ba9386362ca3a0c66029211455d3abc240d99c3a92da44383b6b6bf15d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731b66ae391488382292e0dc99862e6a2e2b4eab3bf7db8aca1f41215ae2ad25`

```dockerfile
```

-	Layers:
	-	`sha256:0f77aba2cb2c0a7d51516c49cc6a160bd0fbaa1720f2ef075d453477a6a3641c`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 3.7 MB (3703366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46cfd64a689b5c2338cd7bc9ec998c978befc3ba1eeeccff50aea8e53688846`  
		Last Modified: Thu, 25 Jul 2024 19:53:38 GMT  
		Size: 24.6 KB (24642 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; s390x

```console
$ docker pull zookeeper@sha256:1f407ae269540432b6b2165e19daa62ef302aef9aab271d73a766f16817289e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110004417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da6b54fda6f2f05c1dedbdc0f8c2eebc186af237e1defa3b31133e595ecb8da`
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
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238133ff9a6cd66afdf7c2fcaac74cbfe7115b2beedf9ff46f9a3c9528d71de`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b972c6d58c217b00136bf4cc4fc998e690b0e88be3e23d0ae04b686d617f28`  
		Last Modified: Sat, 17 Aug 2024 05:20:40 GMT  
		Size: 4.2 MB (4242011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206f2fa595ecc38363ffc2d9f1f2143502ee8d5caed3ab593501891b96139c80`  
		Last Modified: Sat, 17 Aug 2024 05:21:57 GMT  
		Size: 20.3 MB (20299960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c12fad4247efc0fc7acbc6e6407c994457f2393c231bba7225ba118895bc9`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:77014a16f6fe0089be6459d2a316786f1c20c5e7cdf2963085d214633bc07431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2a832b9838abda2675560733e1c0724e63f98136cb6a22a7b3aac4ec81d072`

```dockerfile
```

-	Layers:
	-	`sha256:1c761c63baf36b60ae3f076c228cb7e52f9780b8fde9ef9b2af51f5ba5a49bc5`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 3.7 MB (3699913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b9c57d1a846f9ab14e5555884493bd30085ee0ae01461b4fcfeac783a6ad53`  
		Last Modified: Sat, 17 Aug 2024 05:21:56 GMT  
		Size: 24.6 KB (24594 bytes)  
		MIME: application/vnd.in-toto+json
