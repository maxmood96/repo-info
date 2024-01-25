## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:5f84b7d4a254435a9914d2ab88dedf6732b1b96d4dad7bb913fe6665c23cf313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `zookeeper:latest` - linux; amd64

```console
$ docker pull zookeeper@sha256:c390c463811f0a9ef3015ed3e0d796bff704007a996ce781b69cf146a2be5f8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120098752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ed62499f4d42ca6a4bb37acd66cd415ae12c695d061d29a55b0e35218974b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:02 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 02:17:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 25 Jan 2024 02:17:48 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Thu, 25 Jan 2024 02:17:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Thu, 25 Jan 2024 02:17:55 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 25 Jan 2024 02:18:09 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Thu, 25 Jan 2024 02:18:09 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Thu, 25 Jan 2024 02:18:13 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Thu, 25 Jan 2024 02:18:13 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Thu, 25 Jan 2024 02:18:13 GMT
VOLUME [/data /datalog /logs]
# Thu, 25 Jan 2024 02:18:14 GMT
EXPOSE 2181 2888 3888 8080
# Thu, 25 Jan 2024 02:18:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Thu, 25 Jan 2024 02:18:14 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Thu, 25 Jan 2024 02:18:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 02:18:14 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d9b1ebfac2eaf5745419c31e5b28b675eaf3ff3bb8218e4f502a2b755d5c93`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11de097d6e439a0a961d309672b1992d36b84d1485bc04613de1a49dd2b7659f`  
		Last Modified: Thu, 25 Jan 2024 02:19:11 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790680fad89a19ed4c328af5c00b4da7eb4c39206ad3c858361f68255b5fe157`  
		Last Modified: Thu, 25 Jan 2024 02:19:12 GMT  
		Size: 4.6 MB (4607351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaebcfc50e2cdae883cd5955770fc9a41a988830e517f2d0df146bc4fa1822a`  
		Last Modified: Thu, 25 Jan 2024 02:19:33 GMT  
		Size: 20.4 MB (20419368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445f250f20660e6dfa737ae6959cc6c5eb795089118553116a3de349ead781d`  
		Last Modified: Thu, 25 Jan 2024 02:19:31 GMT  
		Size: 774.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:latest` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:f8a1fed5c13af9eb16636913381c7b41039df67dc209131370eef7a8e74bbf7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118832972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1125d6ed6b59ff732ff46a06b32127f5e76a14c16426f6ca57b47e3b2e4c7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:43:49 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:43:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 01:42:49 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 25 Jan 2024 01:42:49 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Thu, 25 Jan 2024 01:42:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Thu, 25 Jan 2024 01:42:54 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 25 Jan 2024 01:43:09 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Thu, 25 Jan 2024 01:43:10 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Thu, 25 Jan 2024 01:43:13 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Thu, 25 Jan 2024 01:43:13 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Thu, 25 Jan 2024 01:43:13 GMT
VOLUME [/data /datalog /logs]
# Thu, 25 Jan 2024 01:43:13 GMT
EXPOSE 2181 2888 3888 8080
# Thu, 25 Jan 2024 01:43:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Thu, 25 Jan 2024 01:43:14 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Thu, 25 Jan 2024 01:43:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:43:14 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30939200340c61d5e4fee7758c3c9ee34908388deb18ebd4162984289a9ac9a9`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940dc18115f047cab53d3be670e2b9a6de9019b3823309dae6000673744b2aa0`  
		Last Modified: Thu, 25 Jan 2024 01:44:11 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e262ad662672becdcdbf806a8d3bcedaae82b235d11c39058cd453a558981e9e`  
		Last Modified: Thu, 25 Jan 2024 01:44:12 GMT  
		Size: 4.5 MB (4510993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889f4b9c23a0eb3a32b5503d77cab1258c7e9bcba3633c77b4240f060f6099ce`  
		Last Modified: Thu, 25 Jan 2024 01:44:31 GMT  
		Size: 20.4 MB (20419382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5e6981630b137b90d19021202103f6adcd4d5bc8634054285dc43ce1def71a`  
		Last Modified: Thu, 25 Jan 2024 01:44:29 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:latest` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:9feae2d02e6044108584c1a5db1a195b03c9490aba54df611eeebf44a7d35c9d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127025829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c167fc728ce2566c50bbfdcd38f32047231b1b6dfc0113dd8dac8e49fc3fe9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:29:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:29:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:29:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:33:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:40:14 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 19:26:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 19:26:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 20:40:38 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 25 Jan 2024 20:40:40 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Thu, 25 Jan 2024 20:40:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Thu, 25 Jan 2024 20:40:57 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 25 Jan 2024 20:41:33 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Thu, 25 Jan 2024 20:41:33 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Thu, 25 Jan 2024 20:41:40 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Thu, 25 Jan 2024 20:41:42 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Thu, 25 Jan 2024 20:41:43 GMT
VOLUME [/data /datalog /logs]
# Thu, 25 Jan 2024 20:41:43 GMT
EXPOSE 2181 2888 3888 8080
# Thu, 25 Jan 2024 20:41:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Thu, 25 Jan 2024 20:41:45 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Thu, 25 Jan 2024 20:41:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 20:41:45 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f95565053a2c917aa3ba2deb3ea392ef7c78d2f7d32e87be656a8d2139ae1d2`  
		Last Modified: Wed, 17 Jan 2024 07:38:06 GMT  
		Size: 18.7 MB (18725652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be66f71a229f18e2fb4b95b19983dfc3bd16fe9b192f1e10886bdf761f00a8b8`  
		Last Modified: Wed, 24 Jan 2024 20:55:01 GMT  
		Size: 47.0 MB (47012774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb10bd25042aab6b76248d72af58819bfa9821ccf6d45fe3ea7e1e0160b705a`  
		Last Modified: Wed, 24 Jan 2024 20:54:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1705edde663dc0bc7b7aa8489dfbe347b084d1ed02b43479222a0114cd038cdc`  
		Last Modified: Thu, 25 Jan 2024 19:30:08 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0138cf80de3713eed9e0556489416c0b60c236433db13bc723654b8363baea6f`  
		Last Modified: Thu, 25 Jan 2024 20:42:57 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5db6d42a4cc838488827413440bf9524bd198dfb433986aa33718e87a400ef`  
		Last Modified: Thu, 25 Jan 2024 20:42:58 GMT  
		Size: 5.2 MB (5207327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ce5726acdd72f637585dbcaf4d7c9cab5d0daa6e0c1ff7f08e443afb495095`  
		Last Modified: Thu, 25 Jan 2024 20:43:21 GMT  
		Size: 20.4 MB (20419368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec8caed7aafe83be910ef549149742796ab3dc53d53ed00bce5e382ead4323a`  
		Last Modified: Thu, 25 Jan 2024 20:43:20 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `zookeeper:latest` - linux; s390x

```console
$ docker pull zookeeper@sha256:d787de97dcd6f24f3fefaadc9ad8f454ba1aaeeafe9f8c15c5de44f59d681a61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114588012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216620b579960416ea893d2d43b691ecbd183f8f0cc11a34e6fafd516ed5f67f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 17:12:07 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:12:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:12:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:12:07 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:12:10 GMT
ADD file:5ae109128826d2e7660949ed9ff9af4b92bbade5ce06a7011ab7b15bb21d8b75 in / 
# Thu, 11 Jan 2024 17:12:10 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 10:46:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 10:46:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 10:46:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 10:54:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 17:29:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Thu, 25 Jan 2024 17:33:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 25 Jan 2024 17:33:44 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 17:33:44 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 17:33:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 20:14:14 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 25 Jan 2024 20:14:14 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Thu, 25 Jan 2024 20:14:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Thu, 25 Jan 2024 20:14:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 25 Jan 2024 20:16:43 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.1
# Thu, 25 Jan 2024 20:16:44 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.1-bin
# Thu, 25 Jan 2024 20:16:47 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.9.1-bin GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.1
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Thu, 25 Jan 2024 20:16:48 GMT
WORKDIR /apache-zookeeper-3.9.1-bin
# Thu, 25 Jan 2024 20:16:48 GMT
VOLUME [/data /datalog /logs]
# Thu, 25 Jan 2024 20:16:49 GMT
EXPOSE 2181 2888 3888 8080
# Thu, 25 Jan 2024 20:16:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.1-bin/bin ZOOCFGDIR=/conf
# Thu, 25 Jan 2024 20:16:49 GMT
COPY file:15946498c7ecbfe405350ae22386ab548cb62ffb5e51b384938a3e1d87a02052 in / 
# Thu, 25 Jan 2024 20:16:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 20:16:49 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:9767f83c892c3413514216ee1180f4118e77f689d61466a79134bd214cf66520`  
		Last Modified: Wed, 17 Jan 2024 10:37:33 GMT  
		Size: 28.7 MB (28654354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40326ebc998b6c443a60efe299eea2a45c3f06018d04e989c62c792f2a235e0`  
		Last Modified: Wed, 17 Jan 2024 11:06:48 GMT  
		Size: 17.3 MB (17261225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25aa4940c8e6163e83480ea07f1ef23cb9ca2d1bd9e1441944a480cfdf0be320`  
		Last Modified: Thu, 25 Jan 2024 17:45:44 GMT  
		Size: 43.8 MB (43765978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57545d865aac97eb6016d5fdc9de37ff1f0e14218481bab1399dc3fa12026295`  
		Last Modified: Thu, 25 Jan 2024 17:45:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ecb285e4372452f5adb3cfa7bdd07812ee4942dc88fc89fc8e70f8f96eeca8`  
		Last Modified: Thu, 25 Jan 2024 17:45:38 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f2cd2289efc5eaf54e2e752a3d3236243e9853e71696e72cf1627a509332f4`  
		Last Modified: Thu, 25 Jan 2024 20:18:40 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e2c7be778a7c23fea22272903e7277a083ad0dfa5494d223277a7c9a7e97ce`  
		Last Modified: Thu, 25 Jan 2024 20:18:40 GMT  
		Size: 4.5 MB (4483524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f3150e5a64bff09136351d78ffb13916afdaee2d63896d497a6b39cd2de338`  
		Last Modified: Thu, 25 Jan 2024 20:18:54 GMT  
		Size: 20.4 MB (20419390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4b4dd9b20bc5e7fe6013cdc825db919f07e3638c03de739f93202faa872697`  
		Last Modified: Thu, 25 Jan 2024 20:18:53 GMT  
		Size: 775.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
