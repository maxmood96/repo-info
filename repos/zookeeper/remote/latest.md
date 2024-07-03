## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:cc374404fd9aa981c7f2fa5a3bc2995d7f03ceda0487bd7d3cec55c8be29f99b
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
$ docker pull zookeeper@sha256:caba39d05a173c044de066f2fb61bc705c043e1436d16c4c50efc529a1ea5ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115236726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9b99b28acfa01f3c32f7804f8cd0c1657a5c3e24a43f3c94eb4f12b215c830`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
ENV JAVA_VERSION=jdk-17.0.11+9
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ea69141092d083d2011e4bef99d88179238845830f3d13a4e385c22865b7d3`  
		Last Modified: Tue, 02 Jul 2024 06:02:20 GMT  
		Size: 47.3 MB (47256035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d590beb7c559e52929bdee57763bf9b4d6993efef2a777ce420cefdbefbf6fc`  
		Last Modified: Tue, 02 Jul 2024 06:02:13 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb850744c99279a291a7993996d6f9a8b25a5cec4bfad603897080ded3217e1b`  
		Last Modified: Tue, 02 Jul 2024 06:02:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256de2e4320930c2931d9f2810054f5ef6fb1fa043767f2c6dce80705cf68bcf`  
		Last Modified: Tue, 02 Jul 2024 07:11:14 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa6eedd08749acf801de25968eb72c3d1ec652dbf4abeee64d06aa885b7eb09`  
		Last Modified: Tue, 02 Jul 2024 07:11:15 GMT  
		Size: 4.4 MB (4366071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8376222ff5d36ff0bf43a509f04c64c640f7b94bdeaef4f98c62ca9dd5f0d1e`  
		Last Modified: Tue, 02 Jul 2024 07:11:16 GMT  
		Size: 20.3 MB (20300192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce29f180f2b872b0dc92f83f364194b79071171d6424bacde70f4a3dd1f7791c`  
		Last Modified: Tue, 02 Jul 2024 07:11:14 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:f088a4466647e9060a176fa8584b9d4b0fbd8081036674e3beaaa3315465b511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a9a73f1a518d8db06f46877a8196896a816dd8737f43f34b27a2ea3051c174`

```dockerfile
```

-	Layers:
	-	`sha256:241caef456a57b80f063a7f4959408cd21bc28ccdd15d0e1cbcec9b3f4ca9e7e`  
		Last Modified: Tue, 02 Jul 2024 07:11:14 GMT  
		Size: 3.7 MB (3663102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a922befe4492233bfc01c0ac8048c4199f9ddd2cfde3880e9eff68056e1fb12e`  
		Last Modified: Tue, 02 Jul 2024 07:11:14 GMT  
		Size: 24.6 KB (24586 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:82896d4c5f3b88c3c7fa9e28effbc4c42b9b144418a7681a900f90423a32feca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112541358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713e214b4e1d582016c44caa0496a17840addde84f929c5c55f0d62392c4175e`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
ENV JAVA_VERSION=jdk-17.0.11+9
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa963c04773e39efb3eb3c080a80fe1bccbf8410a480f24229a7a06fc307c532`  
		Last Modified: Wed, 05 Jun 2024 04:57:44 GMT  
		Size: 46.7 MB (46716398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382cfd76d96df44a0a5e200f1841a3fc8d1bdbfa5fb655a2f2795bc3b4e16ec3`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0792dc21c67221e401d3c4b78ebea1705a045fbcc6461558ac50bfbe911989a`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4e2ab9484bee70b53771c0a94686124e624ea0fb70fc7218bd9b498eac346b`  
		Last Modified: Wed, 05 Jun 2024 18:34:34 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24bb4c7943f312610ef896e1c670b636d272e79f7854c698e05a20e252c24ac`  
		Last Modified: Wed, 05 Jun 2024 18:34:34 GMT  
		Size: 4.3 MB (4271095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8be4ab693dc2f621552e189ac8dc282bab7ebe66a68ce2330d51e94898eaea0`  
		Last Modified: Wed, 05 Jun 2024 18:35:32 GMT  
		Size: 20.3 MB (20300224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdbc7f919845add36e6618fb351f9b52e66f75d6665fafe692b213fee2dcc60`  
		Last Modified: Wed, 05 Jun 2024 18:35:31 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:a26fd2e3b7d2e671ee97d1ff5cbb3e750ae197851565dc5b73489377833e324e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843c57bc84263f53c42201e6f8839a0ae6009572fec5c65945be36d397193d50`

```dockerfile
```

-	Layers:
	-	`sha256:8355a3c661c50805f8152f08364c4faad033f5a0e6acb169de9181558b3be02d`  
		Last Modified: Wed, 05 Jun 2024 18:35:32 GMT  
		Size: 3.7 MB (3663408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:434d79b198955dfa9b1e027d6e1fc01376ac3093406c8d9ffa82b76ce09ddb00`  
		Last Modified: Wed, 05 Jun 2024 18:35:31 GMT  
		Size: 24.9 KB (24868 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:ba288e8f44af007d126cc68b574eec6de92566d8038d429ba12bd410b4b02639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121713910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a9a252c1d78ad2b359f510564c22545a1b5fe77f6053e9535d3f76675cbde0`
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
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
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
ENV JAVA_VERSION=jdk-17.0.11+9
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f84268a93862af92928dd1cc1dc31937bbffd50302e61f899397e5223399d`  
		Last Modified: Wed, 05 Jun 2024 04:00:20 GMT  
		Size: 13.8 MB (13766991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676100559a99985f64736a666f697d928a23c66769e960c3e31c5ef8fe4c552c`  
		Last Modified: Wed, 05 Jun 2024 04:03:33 GMT  
		Size: 47.1 MB (47089007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd6fa680040cf2ae03302753037f5fdc994b1977711465d5e545119fc80d6cd`  
		Last Modified: Wed, 05 Jun 2024 04:03:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0ae4c33bf15517a9774fc82d8a6e9833eb57db57545edab094bf4ca6ae391c`  
		Last Modified: Wed, 05 Jun 2024 04:03:26 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c39d847e0e25c31e59227133ec5d7fff824fe315d9b385186af895f5383bd7f`  
		Last Modified: Wed, 05 Jun 2024 15:21:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07858fc49932ef888bdbf3275bfb289f767b779741d7e7110cc773aedee67716`  
		Last Modified: Wed, 05 Jun 2024 15:21:14 GMT  
		Size: 5.0 MB (4965969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693aaa9f0953bb11264192dc71d297e9822de17a07a7c11dcc0f50bd8f128433`  
		Last Modified: Wed, 05 Jun 2024 15:22:32 GMT  
		Size: 20.3 MB (20300117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00987614855077acbd0900f893a8338cc69568b7966569c96ac07f1064e5855`  
		Last Modified: Wed, 05 Jun 2024 15:22:31 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:818583269d3fa7166a0d33f68fe24cabfa9e3f3baa00ca8e4f1ff4d2a081d590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3edec69c95ab0d53cd6749c6c21ca3efce432ee0d6792feadb6900c7ac26c69`

```dockerfile
```

-	Layers:
	-	`sha256:e5a0b416ef44356c967d71b9dff33ec6814a99f6c64379b75243903554e5b75b`  
		Last Modified: Wed, 05 Jun 2024 15:22:31 GMT  
		Size: 3.7 MB (3667669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49909c15e81c0e5157b782f0c28b76e73a84fac0992d4fe5757d382245c8fdc0`  
		Last Modified: Wed, 05 Jun 2024 15:22:31 GMT  
		Size: 24.6 KB (24586 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; s390x

```console
$ docker pull zookeeper@sha256:f84a96953076c574925f5c42aef6e9d248443057c63769392c36e68e121cb579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cca83bd5dc9102e54d8082dd70860c77178bfb72c026dd0de6f5fb2b14c7635`
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
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
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
ENV JAVA_VERSION=jdk-17.0.11+9
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98eaa70dc31cdad42121b062dd92b14960ba0a992a5bedede9795f6d11bf4a38`  
		Last Modified: Tue, 02 Jul 2024 03:54:48 GMT  
		Size: 13.0 MB (12954922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e143ddbbbd26d9c01c98413ba531196dcc7140c1ec8308b5dcebf8f159bb199`  
		Last Modified: Tue, 02 Jul 2024 03:55:45 GMT  
		Size: 43.8 MB (43830806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce75fac2d557a16d779924919519ada01974a403b583da2903eff0f02e09fc48`  
		Last Modified: Tue, 02 Jul 2024 03:55:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72378e2f6e774945c663149a026ee53475bff2ed8057d8ecdd30044256231a7c`  
		Last Modified: Tue, 02 Jul 2024 03:55:39 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b406fe5f801e479be0630fbd3bb2dbfc8d8f53223fcae07a3f9dd06ac126`  
		Last Modified: Tue, 02 Jul 2024 21:18:14 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7ab356b885db1f2d9d8fb941b27fb34dc778a6dd9e826b83759a93ec1fb2cb`  
		Last Modified: Tue, 02 Jul 2024 21:18:15 GMT  
		Size: 4.2 MB (4241981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263967a74c190b05b19ded161eac1423a6fbf9a550de7ac39c10c05a1705bfc`  
		Last Modified: Tue, 02 Jul 2024 21:19:29 GMT  
		Size: 20.3 MB (20300194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aff85971ee94f718b79232c94283bdad11495f94d3c87e140913da133b07a81`  
		Last Modified: Tue, 02 Jul 2024 21:19:28 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:a3f3c2b5f4df4192eb448f1d08290b789a56fb088c29083b089c509e194f0cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69a4d82ea0446f6ea0656b619d72f49de5508c5d7991991fb44bc679e85fa79`

```dockerfile
```

-	Layers:
	-	`sha256:e013de715b4e9d392ae4eef0d332ea0f22f869e3fe9724293bbeaf43daf743a1`  
		Last Modified: Tue, 02 Jul 2024 21:19:29 GMT  
		Size: 3.7 MB (3664360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1be03e4e316736d8dc53221c5d56ea8c70a43a640a30203492cfe5b2417bc23`  
		Last Modified: Tue, 02 Jul 2024 21:19:28 GMT  
		Size: 24.6 KB (24588 bytes)  
		MIME: application/vnd.in-toto+json
