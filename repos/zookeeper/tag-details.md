<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `zookeeper`

-	[`zookeeper:3.8`](#zookeeper38)
-	[`zookeeper:3.8-jre-17`](#zookeeper38-jre-17)
-	[`zookeeper:3.8.4`](#zookeeper384)
-	[`zookeeper:3.8.4-jre-17`](#zookeeper384-jre-17)
-	[`zookeeper:3.9`](#zookeeper39)
-	[`zookeeper:3.9-jre-17`](#zookeeper39-jre-17)
-	[`zookeeper:3.9.3`](#zookeeper393)
-	[`zookeeper:3.9.3-jre-17`](#zookeeper393-jre-17)
-	[`zookeeper:latest`](#zookeeperlatest)

## `zookeeper:3.8`

```console
$ docker pull zookeeper@sha256:c5e8575b207cd93a96d3ac293a6c9f4dad66e559a09ff9bb3204abb6d2e090a7
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
$ docker pull zookeeper@sha256:b1aaf3bcc38c65fef78af13d0307aad1d59b3444cbab2d1cacef22a6633d2f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108455286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbfb2475a468cd19955e5eb220c2756c7606a20d50b3f013c98e71f3f1fb718`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd17295498def236b64aeae81f61201e1366f6fa5832e4ef44713be496e18e8`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02330ba0f4788913d6cd619efffd2a9a9986649e00a00ed5a2dcc63a4d8c82ab`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 1.1 MB (1144080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120269fdbd7b4d5ad4f5550f2d49562ad11e05597a578278416a986b740a725`  
		Last Modified: Fri, 31 Jan 2025 02:13:40 GMT  
		Size: 14.7 MB (14682907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04491f0d7e460ed1eaba50cdc4e3738993edf4197506e5849a0a905a809bfc9a`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:31eab28b1336ee3d2034d40315810ec3610fe8b2c4e951e3dd828c4deae19d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3805796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b294e591bb4863aced74720f43021528217c5fd17423e27af0baa6e43bebba69`

```dockerfile
```

-	Layers:
	-	`sha256:c1ae870abc02d91b16bbd53b628ea8552bd4effa61fc1daff9cd73a9e1076e51`  
		Last Modified: Fri, 31 Jan 2025 02:13:40 GMT  
		Size: 3.8 MB (3781480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0bd0e41862da59114cc730d0cf98dc73aab0c081b506968e0ae8fcfc28f874`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 24.3 KB (24316 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:03d386418b4d78454838a080172685c76df023a792bca2c2f4dced11ccacccb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105645126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56811b3afc53d9d295c181c9d866923aa4f1f0b92f383765afb3ac9f921ddf9e`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0973fbeb41c9a280ddd2a5231976081b3e144f214b1f8e797cab794b099c2e`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbefce51f5c275db2eae4e5a9891c31ca59fe9263dc1b26a6332ee0a5deaeb1c`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.1 MB (1073319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa1a25a58b33686267997a798afc63cdc22531a11f7cf7e32b7f547d5f24f08`  
		Last Modified: Fri, 31 Jan 2025 04:45:49 GMT  
		Size: 14.7 MB (14682898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b0fe005c4b10161eda690c61ddef8cdf3e98b73a95a293905539f5ab3eb3b2`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:786422ad58d4556a61c0d3ff49dd41c6871d3d954a27b8d80d51ef859ea9afa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee223a32dca03061100cc41be7409174191f73ed95c06ed4eb8929cc30753103`

```dockerfile
```

-	Layers:
	-	`sha256:fa87d51c7d8211f60e94d513243305bb125cfeb5b67cb1275ed28dbc711ea71f`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 3.8 MB (3783038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07436bd9152621f800fb03b1cde63ece3288cf563fa203595a6e8d6a45455204`  
		Last Modified: Fri, 31 Jan 2025 04:45:47 GMT  
		Size: 24.4 KB (24450 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:e6ad074a8f870cdbe492161ee76de07cb520f7c51cf4bbd6156a9f24d4f6e74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114647202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf719b1a38ca1ecc15dfb27d04f54c200383689c599c7c74d85b553a41749e6`
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
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1549ab3d8e534df8d96c792f2811628e2e2df295e9f3a0f7b600693d70ea4054`  
		Last Modified: Wed, 22 Jan 2025 18:30:54 GMT  
		Size: 17.7 MB (17651386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0adfe1116944f60bc9086d8430625fc17a62d6d3c33f38bebe372b09008b9e7`  
		Last Modified: Fri, 31 Jan 2025 04:51:32 GMT  
		Size: 46.8 MB (46769686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37654f19ec6d92e72c255e64a181b0f0438b4032e516977695b878aeb999248`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a978d624bef09843b3a9bd929f94a3d7b958919206064439abe8869992b8120c`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0333ef06de8c79f090ece86e015d0fdf5a1ea3bb8f55ac5a351d71cf9a1f48c`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae8eee43a0b144a5152c7e29e56d2eaea341bc2804b53047b900efd04343a47`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 1.1 MB (1089900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb8aeeb1f37db6f7180a00b3315e0a1edd31ecb2f918c988a3f3bf823d5e6d`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 14.7 MB (14682942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c16a8f853d7d4d2323553273fb0146c90d58ca26c6c5c1f57d4e056a6bb6aa5`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:914ac8bae09a6a1cf7e2e07f4d7f26226ccf30e9df54bdc3c21a518eea541ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6b6cd74bc6b6f1cdece1233b5d1fa2b1f8b3e3fca3fa17d34ebd5761f2ad87`

```dockerfile
```

-	Layers:
	-	`sha256:e5f2b1bd35501c57bda9d1c4b3bd0630fb352d46d01e8f77562f8fcf4a15abef`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 3.8 MB (3787305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5452767268e72ec3130ae90e844e4ba7589bd1d59c743cf1bf9221b997a9753a`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 24.4 KB (24364 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; s390x

```console
$ docker pull zookeeper@sha256:a2ce9e9ebabcfaa89634cac97f3b04b1f99f26df5fc06c02b8040de6b00378d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103888168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ddbc39761ef398ed9cfbc742c83d8339c6fc51c3b46daf3e9aa4e346f73712`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce8df2d77e2997c97b30184cdfa23846196d4e5dfd005da96d8f36dcbc641a`  
		Last Modified: Wed, 22 Jan 2025 21:43:35 GMT  
		Size: 16.1 MB (16142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269211f1ea045e884f1175d77556df415d3093969647d5f33b870d33c557999`  
		Last Modified: Fri, 31 Jan 2025 01:43:28 GMT  
		Size: 43.9 MB (43949613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469f3a85ca4aad23caca93275437a25893f78888c8e35dcf3b777dfeec31c5e`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b248eed509cdcce48e80c1834adc9f5fb2a6d150447ac1b88ef4c81f5801ce`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6260fe841bd8ff183feb4f3b23be356af2587159a25957dce20b13c0486558e`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937294ed5c2b876156e6dd80cf376217fabd65bb3998c49c322b5a5c38fe8a5`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.1 MB (1106992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346bd8224b0dcd0740c1619d367c98c7521386f7aaf85f5df087f3a35d545356`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 14.7 MB (14682914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59353f0f486fb70341d3163a161f190dec1ed1c971e10e1002bdb14656f74e91`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:ccf606e342c3126040c7f08df72f1717df53a9362794b640fe51eaac92557258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc3d12d218ca5a1060d3d66481fa4c65b0cd078f7200ccbde85edacd6a65238`

```dockerfile
```

-	Layers:
	-	`sha256:d623cdeef492617087e33c53e5804757427bfbb2a043943c5fa22f1d1f7100d7`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 3.8 MB (3784946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e5931fbc277e90565b074cacae4750725418b7d38e339421593651eb85854b`  
		Last Modified: Fri, 31 Jan 2025 03:00:41 GMT  
		Size: 24.3 KB (24316 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8-jre-17`

```console
$ docker pull zookeeper@sha256:c5e8575b207cd93a96d3ac293a6c9f4dad66e559a09ff9bb3204abb6d2e090a7
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
$ docker pull zookeeper@sha256:b1aaf3bcc38c65fef78af13d0307aad1d59b3444cbab2d1cacef22a6633d2f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108455286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbfb2475a468cd19955e5eb220c2756c7606a20d50b3f013c98e71f3f1fb718`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd17295498def236b64aeae81f61201e1366f6fa5832e4ef44713be496e18e8`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02330ba0f4788913d6cd619efffd2a9a9986649e00a00ed5a2dcc63a4d8c82ab`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 1.1 MB (1144080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120269fdbd7b4d5ad4f5550f2d49562ad11e05597a578278416a986b740a725`  
		Last Modified: Fri, 31 Jan 2025 02:13:40 GMT  
		Size: 14.7 MB (14682907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04491f0d7e460ed1eaba50cdc4e3738993edf4197506e5849a0a905a809bfc9a`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:31eab28b1336ee3d2034d40315810ec3610fe8b2c4e951e3dd828c4deae19d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3805796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b294e591bb4863aced74720f43021528217c5fd17423e27af0baa6e43bebba69`

```dockerfile
```

-	Layers:
	-	`sha256:c1ae870abc02d91b16bbd53b628ea8552bd4effa61fc1daff9cd73a9e1076e51`  
		Last Modified: Fri, 31 Jan 2025 02:13:40 GMT  
		Size: 3.8 MB (3781480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0bd0e41862da59114cc730d0cf98dc73aab0c081b506968e0ae8fcfc28f874`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 24.3 KB (24316 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:03d386418b4d78454838a080172685c76df023a792bca2c2f4dced11ccacccb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105645126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56811b3afc53d9d295c181c9d866923aa4f1f0b92f383765afb3ac9f921ddf9e`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0973fbeb41c9a280ddd2a5231976081b3e144f214b1f8e797cab794b099c2e`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbefce51f5c275db2eae4e5a9891c31ca59fe9263dc1b26a6332ee0a5deaeb1c`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.1 MB (1073319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa1a25a58b33686267997a798afc63cdc22531a11f7cf7e32b7f547d5f24f08`  
		Last Modified: Fri, 31 Jan 2025 04:45:49 GMT  
		Size: 14.7 MB (14682898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b0fe005c4b10161eda690c61ddef8cdf3e98b73a95a293905539f5ab3eb3b2`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:786422ad58d4556a61c0d3ff49dd41c6871d3d954a27b8d80d51ef859ea9afa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee223a32dca03061100cc41be7409174191f73ed95c06ed4eb8929cc30753103`

```dockerfile
```

-	Layers:
	-	`sha256:fa87d51c7d8211f60e94d513243305bb125cfeb5b67cb1275ed28dbc711ea71f`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 3.8 MB (3783038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07436bd9152621f800fb03b1cde63ece3288cf563fa203595a6e8d6a45455204`  
		Last Modified: Fri, 31 Jan 2025 04:45:47 GMT  
		Size: 24.4 KB (24450 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:e6ad074a8f870cdbe492161ee76de07cb520f7c51cf4bbd6156a9f24d4f6e74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114647202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf719b1a38ca1ecc15dfb27d04f54c200383689c599c7c74d85b553a41749e6`
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
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1549ab3d8e534df8d96c792f2811628e2e2df295e9f3a0f7b600693d70ea4054`  
		Last Modified: Wed, 22 Jan 2025 18:30:54 GMT  
		Size: 17.7 MB (17651386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0adfe1116944f60bc9086d8430625fc17a62d6d3c33f38bebe372b09008b9e7`  
		Last Modified: Fri, 31 Jan 2025 04:51:32 GMT  
		Size: 46.8 MB (46769686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37654f19ec6d92e72c255e64a181b0f0438b4032e516977695b878aeb999248`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a978d624bef09843b3a9bd929f94a3d7b958919206064439abe8869992b8120c`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0333ef06de8c79f090ece86e015d0fdf5a1ea3bb8f55ac5a351d71cf9a1f48c`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae8eee43a0b144a5152c7e29e56d2eaea341bc2804b53047b900efd04343a47`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 1.1 MB (1089900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb8aeeb1f37db6f7180a00b3315e0a1edd31ecb2f918c988a3f3bf823d5e6d`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 14.7 MB (14682942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c16a8f853d7d4d2323553273fb0146c90d58ca26c6c5c1f57d4e056a6bb6aa5`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:914ac8bae09a6a1cf7e2e07f4d7f26226ccf30e9df54bdc3c21a518eea541ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6b6cd74bc6b6f1cdece1233b5d1fa2b1f8b3e3fca3fa17d34ebd5761f2ad87`

```dockerfile
```

-	Layers:
	-	`sha256:e5f2b1bd35501c57bda9d1c4b3bd0630fb352d46d01e8f77562f8fcf4a15abef`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 3.8 MB (3787305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5452767268e72ec3130ae90e844e4ba7589bd1d59c743cf1bf9221b997a9753a`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 24.4 KB (24364 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:a2ce9e9ebabcfaa89634cac97f3b04b1f99f26df5fc06c02b8040de6b00378d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103888168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ddbc39761ef398ed9cfbc742c83d8339c6fc51c3b46daf3e9aa4e346f73712`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce8df2d77e2997c97b30184cdfa23846196d4e5dfd005da96d8f36dcbc641a`  
		Last Modified: Wed, 22 Jan 2025 21:43:35 GMT  
		Size: 16.1 MB (16142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269211f1ea045e884f1175d77556df415d3093969647d5f33b870d33c557999`  
		Last Modified: Fri, 31 Jan 2025 01:43:28 GMT  
		Size: 43.9 MB (43949613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469f3a85ca4aad23caca93275437a25893f78888c8e35dcf3b777dfeec31c5e`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b248eed509cdcce48e80c1834adc9f5fb2a6d150447ac1b88ef4c81f5801ce`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6260fe841bd8ff183feb4f3b23be356af2587159a25957dce20b13c0486558e`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937294ed5c2b876156e6dd80cf376217fabd65bb3998c49c322b5a5c38fe8a5`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.1 MB (1106992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346bd8224b0dcd0740c1619d367c98c7521386f7aaf85f5df087f3a35d545356`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 14.7 MB (14682914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59353f0f486fb70341d3163a161f190dec1ed1c971e10e1002bdb14656f74e91`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:ccf606e342c3126040c7f08df72f1717df53a9362794b640fe51eaac92557258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc3d12d218ca5a1060d3d66481fa4c65b0cd078f7200ccbde85edacd6a65238`

```dockerfile
```

-	Layers:
	-	`sha256:d623cdeef492617087e33c53e5804757427bfbb2a043943c5fa22f1d1f7100d7`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 3.8 MB (3784946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e5931fbc277e90565b074cacae4750725418b7d38e339421593651eb85854b`  
		Last Modified: Fri, 31 Jan 2025 03:00:41 GMT  
		Size: 24.3 KB (24316 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8.4`

```console
$ docker pull zookeeper@sha256:c5e8575b207cd93a96d3ac293a6c9f4dad66e559a09ff9bb3204abb6d2e090a7
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
$ docker pull zookeeper@sha256:b1aaf3bcc38c65fef78af13d0307aad1d59b3444cbab2d1cacef22a6633d2f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108455286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbfb2475a468cd19955e5eb220c2756c7606a20d50b3f013c98e71f3f1fb718`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd17295498def236b64aeae81f61201e1366f6fa5832e4ef44713be496e18e8`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02330ba0f4788913d6cd619efffd2a9a9986649e00a00ed5a2dcc63a4d8c82ab`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 1.1 MB (1144080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120269fdbd7b4d5ad4f5550f2d49562ad11e05597a578278416a986b740a725`  
		Last Modified: Fri, 31 Jan 2025 02:13:40 GMT  
		Size: 14.7 MB (14682907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04491f0d7e460ed1eaba50cdc4e3738993edf4197506e5849a0a905a809bfc9a`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:31eab28b1336ee3d2034d40315810ec3610fe8b2c4e951e3dd828c4deae19d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3805796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b294e591bb4863aced74720f43021528217c5fd17423e27af0baa6e43bebba69`

```dockerfile
```

-	Layers:
	-	`sha256:c1ae870abc02d91b16bbd53b628ea8552bd4effa61fc1daff9cd73a9e1076e51`  
		Last Modified: Fri, 31 Jan 2025 02:13:40 GMT  
		Size: 3.8 MB (3781480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0bd0e41862da59114cc730d0cf98dc73aab0c081b506968e0ae8fcfc28f874`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 24.3 KB (24316 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:03d386418b4d78454838a080172685c76df023a792bca2c2f4dced11ccacccb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105645126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56811b3afc53d9d295c181c9d866923aa4f1f0b92f383765afb3ac9f921ddf9e`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0973fbeb41c9a280ddd2a5231976081b3e144f214b1f8e797cab794b099c2e`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbefce51f5c275db2eae4e5a9891c31ca59fe9263dc1b26a6332ee0a5deaeb1c`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.1 MB (1073319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa1a25a58b33686267997a798afc63cdc22531a11f7cf7e32b7f547d5f24f08`  
		Last Modified: Fri, 31 Jan 2025 04:45:49 GMT  
		Size: 14.7 MB (14682898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b0fe005c4b10161eda690c61ddef8cdf3e98b73a95a293905539f5ab3eb3b2`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:786422ad58d4556a61c0d3ff49dd41c6871d3d954a27b8d80d51ef859ea9afa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee223a32dca03061100cc41be7409174191f73ed95c06ed4eb8929cc30753103`

```dockerfile
```

-	Layers:
	-	`sha256:fa87d51c7d8211f60e94d513243305bb125cfeb5b67cb1275ed28dbc711ea71f`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 3.8 MB (3783038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07436bd9152621f800fb03b1cde63ece3288cf563fa203595a6e8d6a45455204`  
		Last Modified: Fri, 31 Jan 2025 04:45:47 GMT  
		Size: 24.4 KB (24450 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:e6ad074a8f870cdbe492161ee76de07cb520f7c51cf4bbd6156a9f24d4f6e74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114647202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf719b1a38ca1ecc15dfb27d04f54c200383689c599c7c74d85b553a41749e6`
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
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1549ab3d8e534df8d96c792f2811628e2e2df295e9f3a0f7b600693d70ea4054`  
		Last Modified: Wed, 22 Jan 2025 18:30:54 GMT  
		Size: 17.7 MB (17651386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0adfe1116944f60bc9086d8430625fc17a62d6d3c33f38bebe372b09008b9e7`  
		Last Modified: Fri, 31 Jan 2025 04:51:32 GMT  
		Size: 46.8 MB (46769686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37654f19ec6d92e72c255e64a181b0f0438b4032e516977695b878aeb999248`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a978d624bef09843b3a9bd929f94a3d7b958919206064439abe8869992b8120c`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0333ef06de8c79f090ece86e015d0fdf5a1ea3bb8f55ac5a351d71cf9a1f48c`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae8eee43a0b144a5152c7e29e56d2eaea341bc2804b53047b900efd04343a47`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 1.1 MB (1089900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb8aeeb1f37db6f7180a00b3315e0a1edd31ecb2f918c988a3f3bf823d5e6d`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 14.7 MB (14682942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c16a8f853d7d4d2323553273fb0146c90d58ca26c6c5c1f57d4e056a6bb6aa5`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:914ac8bae09a6a1cf7e2e07f4d7f26226ccf30e9df54bdc3c21a518eea541ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6b6cd74bc6b6f1cdece1233b5d1fa2b1f8b3e3fca3fa17d34ebd5761f2ad87`

```dockerfile
```

-	Layers:
	-	`sha256:e5f2b1bd35501c57bda9d1c4b3bd0630fb352d46d01e8f77562f8fcf4a15abef`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 3.8 MB (3787305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5452767268e72ec3130ae90e844e4ba7589bd1d59c743cf1bf9221b997a9753a`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 24.4 KB (24364 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4` - linux; s390x

```console
$ docker pull zookeeper@sha256:a2ce9e9ebabcfaa89634cac97f3b04b1f99f26df5fc06c02b8040de6b00378d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103888168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ddbc39761ef398ed9cfbc742c83d8339c6fc51c3b46daf3e9aa4e346f73712`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce8df2d77e2997c97b30184cdfa23846196d4e5dfd005da96d8f36dcbc641a`  
		Last Modified: Wed, 22 Jan 2025 21:43:35 GMT  
		Size: 16.1 MB (16142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269211f1ea045e884f1175d77556df415d3093969647d5f33b870d33c557999`  
		Last Modified: Fri, 31 Jan 2025 01:43:28 GMT  
		Size: 43.9 MB (43949613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469f3a85ca4aad23caca93275437a25893f78888c8e35dcf3b777dfeec31c5e`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b248eed509cdcce48e80c1834adc9f5fb2a6d150447ac1b88ef4c81f5801ce`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6260fe841bd8ff183feb4f3b23be356af2587159a25957dce20b13c0486558e`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937294ed5c2b876156e6dd80cf376217fabd65bb3998c49c322b5a5c38fe8a5`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.1 MB (1106992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346bd8224b0dcd0740c1619d367c98c7521386f7aaf85f5df087f3a35d545356`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 14.7 MB (14682914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59353f0f486fb70341d3163a161f190dec1ed1c971e10e1002bdb14656f74e91`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:ccf606e342c3126040c7f08df72f1717df53a9362794b640fe51eaac92557258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc3d12d218ca5a1060d3d66481fa4c65b0cd078f7200ccbde85edacd6a65238`

```dockerfile
```

-	Layers:
	-	`sha256:d623cdeef492617087e33c53e5804757427bfbb2a043943c5fa22f1d1f7100d7`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 3.8 MB (3784946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e5931fbc277e90565b074cacae4750725418b7d38e339421593651eb85854b`  
		Last Modified: Fri, 31 Jan 2025 03:00:41 GMT  
		Size: 24.3 KB (24316 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8.4-jre-17`

```console
$ docker pull zookeeper@sha256:c5e8575b207cd93a96d3ac293a6c9f4dad66e559a09ff9bb3204abb6d2e090a7
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
$ docker pull zookeeper@sha256:b1aaf3bcc38c65fef78af13d0307aad1d59b3444cbab2d1cacef22a6633d2f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108455286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbfb2475a468cd19955e5eb220c2756c7606a20d50b3f013c98e71f3f1fb718`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd17295498def236b64aeae81f61201e1366f6fa5832e4ef44713be496e18e8`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02330ba0f4788913d6cd619efffd2a9a9986649e00a00ed5a2dcc63a4d8c82ab`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 1.1 MB (1144080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120269fdbd7b4d5ad4f5550f2d49562ad11e05597a578278416a986b740a725`  
		Last Modified: Fri, 31 Jan 2025 02:13:40 GMT  
		Size: 14.7 MB (14682907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04491f0d7e460ed1eaba50cdc4e3738993edf4197506e5849a0a905a809bfc9a`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:31eab28b1336ee3d2034d40315810ec3610fe8b2c4e951e3dd828c4deae19d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3805796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b294e591bb4863aced74720f43021528217c5fd17423e27af0baa6e43bebba69`

```dockerfile
```

-	Layers:
	-	`sha256:c1ae870abc02d91b16bbd53b628ea8552bd4effa61fc1daff9cd73a9e1076e51`  
		Last Modified: Fri, 31 Jan 2025 02:13:40 GMT  
		Size: 3.8 MB (3781480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0bd0e41862da59114cc730d0cf98dc73aab0c081b506968e0ae8fcfc28f874`  
		Last Modified: Fri, 31 Jan 2025 02:13:39 GMT  
		Size: 24.3 KB (24316 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:03d386418b4d78454838a080172685c76df023a792bca2c2f4dced11ccacccb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105645126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56811b3afc53d9d295c181c9d866923aa4f1f0b92f383765afb3ac9f921ddf9e`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0973fbeb41c9a280ddd2a5231976081b3e144f214b1f8e797cab794b099c2e`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbefce51f5c275db2eae4e5a9891c31ca59fe9263dc1b26a6332ee0a5deaeb1c`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.1 MB (1073319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa1a25a58b33686267997a798afc63cdc22531a11f7cf7e32b7f547d5f24f08`  
		Last Modified: Fri, 31 Jan 2025 04:45:49 GMT  
		Size: 14.7 MB (14682898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b0fe005c4b10161eda690c61ddef8cdf3e98b73a95a293905539f5ab3eb3b2`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:786422ad58d4556a61c0d3ff49dd41c6871d3d954a27b8d80d51ef859ea9afa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee223a32dca03061100cc41be7409174191f73ed95c06ed4eb8929cc30753103`

```dockerfile
```

-	Layers:
	-	`sha256:fa87d51c7d8211f60e94d513243305bb125cfeb5b67cb1275ed28dbc711ea71f`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 3.8 MB (3783038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07436bd9152621f800fb03b1cde63ece3288cf563fa203595a6e8d6a45455204`  
		Last Modified: Fri, 31 Jan 2025 04:45:47 GMT  
		Size: 24.4 KB (24450 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:e6ad074a8f870cdbe492161ee76de07cb520f7c51cf4bbd6156a9f24d4f6e74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114647202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf719b1a38ca1ecc15dfb27d04f54c200383689c599c7c74d85b553a41749e6`
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
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 14 Mar 2024 05:00:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Mar 2024 05:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Mar 2024 05:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1549ab3d8e534df8d96c792f2811628e2e2df295e9f3a0f7b600693d70ea4054`  
		Last Modified: Wed, 22 Jan 2025 18:30:54 GMT  
		Size: 17.7 MB (17651386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0adfe1116944f60bc9086d8430625fc17a62d6d3c33f38bebe372b09008b9e7`  
		Last Modified: Fri, 31 Jan 2025 04:51:32 GMT  
		Size: 46.8 MB (46769686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37654f19ec6d92e72c255e64a181b0f0438b4032e516977695b878aeb999248`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a978d624bef09843b3a9bd929f94a3d7b958919206064439abe8869992b8120c`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0333ef06de8c79f090ece86e015d0fdf5a1ea3bb8f55ac5a351d71cf9a1f48c`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae8eee43a0b144a5152c7e29e56d2eaea341bc2804b53047b900efd04343a47`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 1.1 MB (1089900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb8aeeb1f37db6f7180a00b3315e0a1edd31ecb2f918c988a3f3bf823d5e6d`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 14.7 MB (14682942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c16a8f853d7d4d2323553273fb0146c90d58ca26c6c5c1f57d4e056a6bb6aa5`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:914ac8bae09a6a1cf7e2e07f4d7f26226ccf30e9df54bdc3c21a518eea541ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6b6cd74bc6b6f1cdece1233b5d1fa2b1f8b3e3fca3fa17d34ebd5761f2ad87`

```dockerfile
```

-	Layers:
	-	`sha256:e5f2b1bd35501c57bda9d1c4b3bd0630fb352d46d01e8f77562f8fcf4a15abef`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 3.8 MB (3787305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5452767268e72ec3130ae90e844e4ba7589bd1d59c743cf1bf9221b997a9753a`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 24.4 KB (24364 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.4-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:a2ce9e9ebabcfaa89634cac97f3b04b1f99f26df5fc06c02b8040de6b00378d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103888168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ddbc39761ef398ed9cfbc742c83d8339c6fc51c3b46daf3e9aa4e346f73712`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Mar 2024 05:00:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 14 Mar 2024 05:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce8df2d77e2997c97b30184cdfa23846196d4e5dfd005da96d8f36dcbc641a`  
		Last Modified: Wed, 22 Jan 2025 21:43:35 GMT  
		Size: 16.1 MB (16142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269211f1ea045e884f1175d77556df415d3093969647d5f33b870d33c557999`  
		Last Modified: Fri, 31 Jan 2025 01:43:28 GMT  
		Size: 43.9 MB (43949613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469f3a85ca4aad23caca93275437a25893f78888c8e35dcf3b777dfeec31c5e`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b248eed509cdcce48e80c1834adc9f5fb2a6d150447ac1b88ef4c81f5801ce`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6260fe841bd8ff183feb4f3b23be356af2587159a25957dce20b13c0486558e`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937294ed5c2b876156e6dd80cf376217fabd65bb3998c49c322b5a5c38fe8a5`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.1 MB (1106992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346bd8224b0dcd0740c1619d367c98c7521386f7aaf85f5df087f3a35d545356`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 14.7 MB (14682914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59353f0f486fb70341d3163a161f190dec1ed1c971e10e1002bdb14656f74e91`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:ccf606e342c3126040c7f08df72f1717df53a9362794b640fe51eaac92557258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc3d12d218ca5a1060d3d66481fa4c65b0cd078f7200ccbde85edacd6a65238`

```dockerfile
```

-	Layers:
	-	`sha256:d623cdeef492617087e33c53e5804757427bfbb2a043943c5fa22f1d1f7100d7`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 3.8 MB (3784946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e5931fbc277e90565b074cacae4750725418b7d38e339421593651eb85854b`  
		Last Modified: Fri, 31 Jan 2025 03:00:41 GMT  
		Size: 24.3 KB (24316 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9`

```console
$ docker pull zookeeper@sha256:f307fbf52d25609d47e3ac7704152577b0a002133aa212743e89908b567c35cf
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
$ docker pull zookeeper@sha256:aa6ec3db1a0960092086d220d02d0186c77c71172319dce506e27556ed1edde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114510925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6bd4b9a4138c3e5e8ee511ea6f5345852ce6a634c87f98ba7b2a9eef72009e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e0eb3ffb6314e0f9d31875847014be83d559907650166922294849a90067c`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d82f79248ff8f2c414866300c27772194c01d7f0bcca8d562e81b32985168`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 1.1 MB (1144074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d042f58baf6e8fcbfdc60b3d8769eeab68730d2a3418ced0999d5d87624c382`  
		Last Modified: Fri, 31 Jan 2025 02:17:25 GMT  
		Size: 20.7 MB (20738551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67463b93523af12e3e99fe23651b019a2613ace59f0088c1cc73958d2d6c2c3a`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:846a88c4b16b98554834c23c1de123935cb5ac57f3ff52b0923ca13758a5e5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49b42309840c1a36aafd63cc339bcbdc7ef61728433d93c9ee868cbad2ef371`

```dockerfile
```

-	Layers:
	-	`sha256:f33967c4fd801614c92bef87c91a60d9c95715b70734393b17d674a33942457f`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 3.8 MB (3788256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25abaa992310182c1eb48c410d83c9650c10da9240b5ab9039dedc02a7f5fe36`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:e8fef66f98939710ee60c784ac359e96a325fde422e7e6f7e064b09bff42e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111700833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb02eaf6d705617dd2538aa6b9e05b801b352b5d3fa77c1e0009bd88eab3943`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0973fbeb41c9a280ddd2a5231976081b3e144f214b1f8e797cab794b099c2e`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbefce51f5c275db2eae4e5a9891c31ca59fe9263dc1b26a6332ee0a5deaeb1c`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.1 MB (1073319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04182fd92029cf704a610af0d38ece6c62fa932d646e0fbbb4d0a7eb3ce60fe`  
		Last Modified: Fri, 31 Jan 2025 04:46:10 GMT  
		Size: 20.7 MB (20738605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b0a2d27c017a1159e2807e8e34b6b68dfd2960934e64373e40b153739fca34`  
		Last Modified: Fri, 31 Jan 2025 04:46:09 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:5169832127f3f1aa04eadab7e35568b638da0c8622f72d4e8d3ab2e8be7b1067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3814592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210328231554dc9443310a4bce02e52e2a65f9aab63298949688d65e7adc5488`

```dockerfile
```

-	Layers:
	-	`sha256:174064e8530e42e1c6989654c2b2592886517e0baad4fa14b2a4aa382f915b1c`  
		Last Modified: Fri, 31 Jan 2025 04:46:09 GMT  
		Size: 3.8 MB (3789826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfee6029b833b262f6b8fe0147209d93c0e39393ceb93776ff055677218fd95d`  
		Last Modified: Fri, 31 Jan 2025 04:46:08 GMT  
		Size: 24.8 KB (24766 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:dc497481b9c796f4a26e3c82fecad41d90165fe6da1629b0f35940ee4363e005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120702842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d23abfda56556ae606214e1fc9eee51e0156f55c7b3c1fa63e4755ea5ab497c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1549ab3d8e534df8d96c792f2811628e2e2df295e9f3a0f7b600693d70ea4054`  
		Last Modified: Wed, 22 Jan 2025 18:30:54 GMT  
		Size: 17.7 MB (17651386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0adfe1116944f60bc9086d8430625fc17a62d6d3c33f38bebe372b09008b9e7`  
		Last Modified: Fri, 31 Jan 2025 04:51:32 GMT  
		Size: 46.8 MB (46769686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37654f19ec6d92e72c255e64a181b0f0438b4032e516977695b878aeb999248`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a978d624bef09843b3a9bd929f94a3d7b958919206064439abe8869992b8120c`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0333ef06de8c79f090ece86e015d0fdf5a1ea3bb8f55ac5a351d71cf9a1f48c`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae8eee43a0b144a5152c7e29e56d2eaea341bc2804b53047b900efd04343a47`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 1.1 MB (1089900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86903258effb23d771e5cfd71350c9948e4f30942cc1d15e804fcbe71bb7ee4c`  
		Last Modified: Fri, 31 Jan 2025 06:31:22 GMT  
		Size: 20.7 MB (20738582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408708c03d628c27719f2736f4439f49452f30107211ca7a2346ff661f216de4`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:163f0dbd4aec276441ce404db504a2399a41a5573f8d3bfd3309001eb015ce14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3818760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cb24a3ba3f15cd65ccacd881bb6a9ed7311b37e8ae812e2f2732ed6f32e298`

```dockerfile
```

-	Layers:
	-	`sha256:b09d7351d95570310b99a82892a6ea185a9bc452669a6d70570c49a81b91766a`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 3.8 MB (3794087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc62e1e9bc60f7411befb81e713df1c1e04c619c4fcf0c214f5d70f4fdd6d9b`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 24.7 KB (24673 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; s390x

```console
$ docker pull zookeeper@sha256:43700ef351003c66ded8b4b5fbb590a0f354640e47c422fdb0a88f8604cd95d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109943849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9504a9b2eb126ddfea724393dba83486c9d8d621c421c60fcc63a02c44215561`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce8df2d77e2997c97b30184cdfa23846196d4e5dfd005da96d8f36dcbc641a`  
		Last Modified: Wed, 22 Jan 2025 21:43:35 GMT  
		Size: 16.1 MB (16142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269211f1ea045e884f1175d77556df415d3093969647d5f33b870d33c557999`  
		Last Modified: Fri, 31 Jan 2025 01:43:28 GMT  
		Size: 43.9 MB (43949613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469f3a85ca4aad23caca93275437a25893f78888c8e35dcf3b777dfeec31c5e`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b248eed509cdcce48e80c1834adc9f5fb2a6d150447ac1b88ef4c81f5801ce`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6260fe841bd8ff183feb4f3b23be356af2587159a25957dce20b13c0486558e`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937294ed5c2b876156e6dd80cf376217fabd65bb3998c49c322b5a5c38fe8a5`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.1 MB (1106992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549988002ba8e52ba256a8f9d80b6bf108a1d30c7ddfd6e2b0fbba95329d3997`  
		Last Modified: Fri, 31 Jan 2025 03:06:00 GMT  
		Size: 20.7 MB (20738595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c181f6a200c29666bf284727fd36c83cc195e4256c6191833945198a7d621cd4`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:2f1f3fcb6282f645dab37295581e0cb96eb0abe6ca05c0b73901575b11b47877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66e1f839d5d0dfe7e3b0545284aa2343dc2bf4afe5298181c171bfe8133ae0e`

```dockerfile
```

-	Layers:
	-	`sha256:bd390fe31e5b1e6fbf3a8f394df26d0adaa6533984929212d60a0167fa92f9f3`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 3.8 MB (3791722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfae3079dd604603e30212b6ac374e782d770a95bb60ad1f5ad32b1678b1771f`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 24.6 KB (24619 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9-jre-17`

```console
$ docker pull zookeeper@sha256:f307fbf52d25609d47e3ac7704152577b0a002133aa212743e89908b567c35cf
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
$ docker pull zookeeper@sha256:aa6ec3db1a0960092086d220d02d0186c77c71172319dce506e27556ed1edde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114510925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6bd4b9a4138c3e5e8ee511ea6f5345852ce6a634c87f98ba7b2a9eef72009e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e0eb3ffb6314e0f9d31875847014be83d559907650166922294849a90067c`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d82f79248ff8f2c414866300c27772194c01d7f0bcca8d562e81b32985168`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 1.1 MB (1144074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d042f58baf6e8fcbfdc60b3d8769eeab68730d2a3418ced0999d5d87624c382`  
		Last Modified: Fri, 31 Jan 2025 02:17:25 GMT  
		Size: 20.7 MB (20738551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67463b93523af12e3e99fe23651b019a2613ace59f0088c1cc73958d2d6c2c3a`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:846a88c4b16b98554834c23c1de123935cb5ac57f3ff52b0923ca13758a5e5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49b42309840c1a36aafd63cc339bcbdc7ef61728433d93c9ee868cbad2ef371`

```dockerfile
```

-	Layers:
	-	`sha256:f33967c4fd801614c92bef87c91a60d9c95715b70734393b17d674a33942457f`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 3.8 MB (3788256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25abaa992310182c1eb48c410d83c9650c10da9240b5ab9039dedc02a7f5fe36`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:e8fef66f98939710ee60c784ac359e96a325fde422e7e6f7e064b09bff42e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111700833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb02eaf6d705617dd2538aa6b9e05b801b352b5d3fa77c1e0009bd88eab3943`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0973fbeb41c9a280ddd2a5231976081b3e144f214b1f8e797cab794b099c2e`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbefce51f5c275db2eae4e5a9891c31ca59fe9263dc1b26a6332ee0a5deaeb1c`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.1 MB (1073319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04182fd92029cf704a610af0d38ece6c62fa932d646e0fbbb4d0a7eb3ce60fe`  
		Last Modified: Fri, 31 Jan 2025 04:46:10 GMT  
		Size: 20.7 MB (20738605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b0a2d27c017a1159e2807e8e34b6b68dfd2960934e64373e40b153739fca34`  
		Last Modified: Fri, 31 Jan 2025 04:46:09 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:5169832127f3f1aa04eadab7e35568b638da0c8622f72d4e8d3ab2e8be7b1067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3814592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210328231554dc9443310a4bce02e52e2a65f9aab63298949688d65e7adc5488`

```dockerfile
```

-	Layers:
	-	`sha256:174064e8530e42e1c6989654c2b2592886517e0baad4fa14b2a4aa382f915b1c`  
		Last Modified: Fri, 31 Jan 2025 04:46:09 GMT  
		Size: 3.8 MB (3789826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfee6029b833b262f6b8fe0147209d93c0e39393ceb93776ff055677218fd95d`  
		Last Modified: Fri, 31 Jan 2025 04:46:08 GMT  
		Size: 24.8 KB (24766 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:dc497481b9c796f4a26e3c82fecad41d90165fe6da1629b0f35940ee4363e005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120702842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d23abfda56556ae606214e1fc9eee51e0156f55c7b3c1fa63e4755ea5ab497c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1549ab3d8e534df8d96c792f2811628e2e2df295e9f3a0f7b600693d70ea4054`  
		Last Modified: Wed, 22 Jan 2025 18:30:54 GMT  
		Size: 17.7 MB (17651386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0adfe1116944f60bc9086d8430625fc17a62d6d3c33f38bebe372b09008b9e7`  
		Last Modified: Fri, 31 Jan 2025 04:51:32 GMT  
		Size: 46.8 MB (46769686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37654f19ec6d92e72c255e64a181b0f0438b4032e516977695b878aeb999248`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a978d624bef09843b3a9bd929f94a3d7b958919206064439abe8869992b8120c`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0333ef06de8c79f090ece86e015d0fdf5a1ea3bb8f55ac5a351d71cf9a1f48c`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae8eee43a0b144a5152c7e29e56d2eaea341bc2804b53047b900efd04343a47`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 1.1 MB (1089900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86903258effb23d771e5cfd71350c9948e4f30942cc1d15e804fcbe71bb7ee4c`  
		Last Modified: Fri, 31 Jan 2025 06:31:22 GMT  
		Size: 20.7 MB (20738582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408708c03d628c27719f2736f4439f49452f30107211ca7a2346ff661f216de4`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:163f0dbd4aec276441ce404db504a2399a41a5573f8d3bfd3309001eb015ce14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3818760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cb24a3ba3f15cd65ccacd881bb6a9ed7311b37e8ae812e2f2732ed6f32e298`

```dockerfile
```

-	Layers:
	-	`sha256:b09d7351d95570310b99a82892a6ea185a9bc452669a6d70570c49a81b91766a`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 3.8 MB (3794087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc62e1e9bc60f7411befb81e713df1c1e04c619c4fcf0c214f5d70f4fdd6d9b`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 24.7 KB (24673 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:43700ef351003c66ded8b4b5fbb590a0f354640e47c422fdb0a88f8604cd95d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109943849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9504a9b2eb126ddfea724393dba83486c9d8d621c421c60fcc63a02c44215561`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce8df2d77e2997c97b30184cdfa23846196d4e5dfd005da96d8f36dcbc641a`  
		Last Modified: Wed, 22 Jan 2025 21:43:35 GMT  
		Size: 16.1 MB (16142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269211f1ea045e884f1175d77556df415d3093969647d5f33b870d33c557999`  
		Last Modified: Fri, 31 Jan 2025 01:43:28 GMT  
		Size: 43.9 MB (43949613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469f3a85ca4aad23caca93275437a25893f78888c8e35dcf3b777dfeec31c5e`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b248eed509cdcce48e80c1834adc9f5fb2a6d150447ac1b88ef4c81f5801ce`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6260fe841bd8ff183feb4f3b23be356af2587159a25957dce20b13c0486558e`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937294ed5c2b876156e6dd80cf376217fabd65bb3998c49c322b5a5c38fe8a5`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.1 MB (1106992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549988002ba8e52ba256a8f9d80b6bf108a1d30c7ddfd6e2b0fbba95329d3997`  
		Last Modified: Fri, 31 Jan 2025 03:06:00 GMT  
		Size: 20.7 MB (20738595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c181f6a200c29666bf284727fd36c83cc195e4256c6191833945198a7d621cd4`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:2f1f3fcb6282f645dab37295581e0cb96eb0abe6ca05c0b73901575b11b47877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66e1f839d5d0dfe7e3b0545284aa2343dc2bf4afe5298181c171bfe8133ae0e`

```dockerfile
```

-	Layers:
	-	`sha256:bd390fe31e5b1e6fbf3a8f394df26d0adaa6533984929212d60a0167fa92f9f3`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 3.8 MB (3791722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfae3079dd604603e30212b6ac374e782d770a95bb60ad1f5ad32b1678b1771f`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 24.6 KB (24619 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9.3`

```console
$ docker pull zookeeper@sha256:f307fbf52d25609d47e3ac7704152577b0a002133aa212743e89908b567c35cf
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

### `zookeeper:3.9.3` - linux; amd64

```console
$ docker pull zookeeper@sha256:aa6ec3db1a0960092086d220d02d0186c77c71172319dce506e27556ed1edde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114510925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6bd4b9a4138c3e5e8ee511ea6f5345852ce6a634c87f98ba7b2a9eef72009e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e0eb3ffb6314e0f9d31875847014be83d559907650166922294849a90067c`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d82f79248ff8f2c414866300c27772194c01d7f0bcca8d562e81b32985168`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 1.1 MB (1144074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d042f58baf6e8fcbfdc60b3d8769eeab68730d2a3418ced0999d5d87624c382`  
		Last Modified: Fri, 31 Jan 2025 02:17:25 GMT  
		Size: 20.7 MB (20738551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67463b93523af12e3e99fe23651b019a2613ace59f0088c1cc73958d2d6c2c3a`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.3` - unknown; unknown

```console
$ docker pull zookeeper@sha256:846a88c4b16b98554834c23c1de123935cb5ac57f3ff52b0923ca13758a5e5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49b42309840c1a36aafd63cc339bcbdc7ef61728433d93c9ee868cbad2ef371`

```dockerfile
```

-	Layers:
	-	`sha256:f33967c4fd801614c92bef87c91a60d9c95715b70734393b17d674a33942457f`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 3.8 MB (3788256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25abaa992310182c1eb48c410d83c9650c10da9240b5ab9039dedc02a7f5fe36`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.3` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:e8fef66f98939710ee60c784ac359e96a325fde422e7e6f7e064b09bff42e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111700833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb02eaf6d705617dd2538aa6b9e05b801b352b5d3fa77c1e0009bd88eab3943`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0973fbeb41c9a280ddd2a5231976081b3e144f214b1f8e797cab794b099c2e`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbefce51f5c275db2eae4e5a9891c31ca59fe9263dc1b26a6332ee0a5deaeb1c`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.1 MB (1073319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04182fd92029cf704a610af0d38ece6c62fa932d646e0fbbb4d0a7eb3ce60fe`  
		Last Modified: Fri, 31 Jan 2025 04:46:10 GMT  
		Size: 20.7 MB (20738605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b0a2d27c017a1159e2807e8e34b6b68dfd2960934e64373e40b153739fca34`  
		Last Modified: Fri, 31 Jan 2025 04:46:09 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.3` - unknown; unknown

```console
$ docker pull zookeeper@sha256:5169832127f3f1aa04eadab7e35568b638da0c8622f72d4e8d3ab2e8be7b1067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3814592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210328231554dc9443310a4bce02e52e2a65f9aab63298949688d65e7adc5488`

```dockerfile
```

-	Layers:
	-	`sha256:174064e8530e42e1c6989654c2b2592886517e0baad4fa14b2a4aa382f915b1c`  
		Last Modified: Fri, 31 Jan 2025 04:46:09 GMT  
		Size: 3.8 MB (3789826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfee6029b833b262f6b8fe0147209d93c0e39393ceb93776ff055677218fd95d`  
		Last Modified: Fri, 31 Jan 2025 04:46:08 GMT  
		Size: 24.8 KB (24766 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.3` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:dc497481b9c796f4a26e3c82fecad41d90165fe6da1629b0f35940ee4363e005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120702842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d23abfda56556ae606214e1fc9eee51e0156f55c7b3c1fa63e4755ea5ab497c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1549ab3d8e534df8d96c792f2811628e2e2df295e9f3a0f7b600693d70ea4054`  
		Last Modified: Wed, 22 Jan 2025 18:30:54 GMT  
		Size: 17.7 MB (17651386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0adfe1116944f60bc9086d8430625fc17a62d6d3c33f38bebe372b09008b9e7`  
		Last Modified: Fri, 31 Jan 2025 04:51:32 GMT  
		Size: 46.8 MB (46769686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37654f19ec6d92e72c255e64a181b0f0438b4032e516977695b878aeb999248`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a978d624bef09843b3a9bd929f94a3d7b958919206064439abe8869992b8120c`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0333ef06de8c79f090ece86e015d0fdf5a1ea3bb8f55ac5a351d71cf9a1f48c`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae8eee43a0b144a5152c7e29e56d2eaea341bc2804b53047b900efd04343a47`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 1.1 MB (1089900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86903258effb23d771e5cfd71350c9948e4f30942cc1d15e804fcbe71bb7ee4c`  
		Last Modified: Fri, 31 Jan 2025 06:31:22 GMT  
		Size: 20.7 MB (20738582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408708c03d628c27719f2736f4439f49452f30107211ca7a2346ff661f216de4`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.3` - unknown; unknown

```console
$ docker pull zookeeper@sha256:163f0dbd4aec276441ce404db504a2399a41a5573f8d3bfd3309001eb015ce14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3818760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cb24a3ba3f15cd65ccacd881bb6a9ed7311b37e8ae812e2f2732ed6f32e298`

```dockerfile
```

-	Layers:
	-	`sha256:b09d7351d95570310b99a82892a6ea185a9bc452669a6d70570c49a81b91766a`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 3.8 MB (3794087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc62e1e9bc60f7411befb81e713df1c1e04c619c4fcf0c214f5d70f4fdd6d9b`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 24.7 KB (24673 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.3` - linux; s390x

```console
$ docker pull zookeeper@sha256:43700ef351003c66ded8b4b5fbb590a0f354640e47c422fdb0a88f8604cd95d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109943849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9504a9b2eb126ddfea724393dba83486c9d8d621c421c60fcc63a02c44215561`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce8df2d77e2997c97b30184cdfa23846196d4e5dfd005da96d8f36dcbc641a`  
		Last Modified: Wed, 22 Jan 2025 21:43:35 GMT  
		Size: 16.1 MB (16142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269211f1ea045e884f1175d77556df415d3093969647d5f33b870d33c557999`  
		Last Modified: Fri, 31 Jan 2025 01:43:28 GMT  
		Size: 43.9 MB (43949613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469f3a85ca4aad23caca93275437a25893f78888c8e35dcf3b777dfeec31c5e`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b248eed509cdcce48e80c1834adc9f5fb2a6d150447ac1b88ef4c81f5801ce`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6260fe841bd8ff183feb4f3b23be356af2587159a25957dce20b13c0486558e`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937294ed5c2b876156e6dd80cf376217fabd65bb3998c49c322b5a5c38fe8a5`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.1 MB (1106992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549988002ba8e52ba256a8f9d80b6bf108a1d30c7ddfd6e2b0fbba95329d3997`  
		Last Modified: Fri, 31 Jan 2025 03:06:00 GMT  
		Size: 20.7 MB (20738595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c181f6a200c29666bf284727fd36c83cc195e4256c6191833945198a7d621cd4`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.3` - unknown; unknown

```console
$ docker pull zookeeper@sha256:2f1f3fcb6282f645dab37295581e0cb96eb0abe6ca05c0b73901575b11b47877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66e1f839d5d0dfe7e3b0545284aa2343dc2bf4afe5298181c171bfe8133ae0e`

```dockerfile
```

-	Layers:
	-	`sha256:bd390fe31e5b1e6fbf3a8f394df26d0adaa6533984929212d60a0167fa92f9f3`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 3.8 MB (3791722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfae3079dd604603e30212b6ac374e782d770a95bb60ad1f5ad32b1678b1771f`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 24.6 KB (24619 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9.3-jre-17`

```console
$ docker pull zookeeper@sha256:f307fbf52d25609d47e3ac7704152577b0a002133aa212743e89908b567c35cf
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

### `zookeeper:3.9.3-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:aa6ec3db1a0960092086d220d02d0186c77c71172319dce506e27556ed1edde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114510925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6bd4b9a4138c3e5e8ee511ea6f5345852ce6a634c87f98ba7b2a9eef72009e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e0eb3ffb6314e0f9d31875847014be83d559907650166922294849a90067c`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d82f79248ff8f2c414866300c27772194c01d7f0bcca8d562e81b32985168`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 1.1 MB (1144074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d042f58baf6e8fcbfdc60b3d8769eeab68730d2a3418ced0999d5d87624c382`  
		Last Modified: Fri, 31 Jan 2025 02:17:25 GMT  
		Size: 20.7 MB (20738551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67463b93523af12e3e99fe23651b019a2613ace59f0088c1cc73958d2d6c2c3a`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.3-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:846a88c4b16b98554834c23c1de123935cb5ac57f3ff52b0923ca13758a5e5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49b42309840c1a36aafd63cc339bcbdc7ef61728433d93c9ee868cbad2ef371`

```dockerfile
```

-	Layers:
	-	`sha256:f33967c4fd801614c92bef87c91a60d9c95715b70734393b17d674a33942457f`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 3.8 MB (3788256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25abaa992310182c1eb48c410d83c9650c10da9240b5ab9039dedc02a7f5fe36`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.3-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:e8fef66f98939710ee60c784ac359e96a325fde422e7e6f7e064b09bff42e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111700833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb02eaf6d705617dd2538aa6b9e05b801b352b5d3fa77c1e0009bd88eab3943`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0973fbeb41c9a280ddd2a5231976081b3e144f214b1f8e797cab794b099c2e`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbefce51f5c275db2eae4e5a9891c31ca59fe9263dc1b26a6332ee0a5deaeb1c`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.1 MB (1073319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04182fd92029cf704a610af0d38ece6c62fa932d646e0fbbb4d0a7eb3ce60fe`  
		Last Modified: Fri, 31 Jan 2025 04:46:10 GMT  
		Size: 20.7 MB (20738605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b0a2d27c017a1159e2807e8e34b6b68dfd2960934e64373e40b153739fca34`  
		Last Modified: Fri, 31 Jan 2025 04:46:09 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.3-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:5169832127f3f1aa04eadab7e35568b638da0c8622f72d4e8d3ab2e8be7b1067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3814592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210328231554dc9443310a4bce02e52e2a65f9aab63298949688d65e7adc5488`

```dockerfile
```

-	Layers:
	-	`sha256:174064e8530e42e1c6989654c2b2592886517e0baad4fa14b2a4aa382f915b1c`  
		Last Modified: Fri, 31 Jan 2025 04:46:09 GMT  
		Size: 3.8 MB (3789826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfee6029b833b262f6b8fe0147209d93c0e39393ceb93776ff055677218fd95d`  
		Last Modified: Fri, 31 Jan 2025 04:46:08 GMT  
		Size: 24.8 KB (24766 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.3-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:dc497481b9c796f4a26e3c82fecad41d90165fe6da1629b0f35940ee4363e005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120702842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d23abfda56556ae606214e1fc9eee51e0156f55c7b3c1fa63e4755ea5ab497c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1549ab3d8e534df8d96c792f2811628e2e2df295e9f3a0f7b600693d70ea4054`  
		Last Modified: Wed, 22 Jan 2025 18:30:54 GMT  
		Size: 17.7 MB (17651386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0adfe1116944f60bc9086d8430625fc17a62d6d3c33f38bebe372b09008b9e7`  
		Last Modified: Fri, 31 Jan 2025 04:51:32 GMT  
		Size: 46.8 MB (46769686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37654f19ec6d92e72c255e64a181b0f0438b4032e516977695b878aeb999248`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a978d624bef09843b3a9bd929f94a3d7b958919206064439abe8869992b8120c`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0333ef06de8c79f090ece86e015d0fdf5a1ea3bb8f55ac5a351d71cf9a1f48c`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae8eee43a0b144a5152c7e29e56d2eaea341bc2804b53047b900efd04343a47`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 1.1 MB (1089900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86903258effb23d771e5cfd71350c9948e4f30942cc1d15e804fcbe71bb7ee4c`  
		Last Modified: Fri, 31 Jan 2025 06:31:22 GMT  
		Size: 20.7 MB (20738582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408708c03d628c27719f2736f4439f49452f30107211ca7a2346ff661f216de4`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.3-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:163f0dbd4aec276441ce404db504a2399a41a5573f8d3bfd3309001eb015ce14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3818760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cb24a3ba3f15cd65ccacd881bb6a9ed7311b37e8ae812e2f2732ed6f32e298`

```dockerfile
```

-	Layers:
	-	`sha256:b09d7351d95570310b99a82892a6ea185a9bc452669a6d70570c49a81b91766a`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 3.8 MB (3794087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc62e1e9bc60f7411befb81e713df1c1e04c619c4fcf0c214f5d70f4fdd6d9b`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 24.7 KB (24673 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.3-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:43700ef351003c66ded8b4b5fbb590a0f354640e47c422fdb0a88f8604cd95d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109943849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9504a9b2eb126ddfea724393dba83486c9d8d621c421c60fcc63a02c44215561`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce8df2d77e2997c97b30184cdfa23846196d4e5dfd005da96d8f36dcbc641a`  
		Last Modified: Wed, 22 Jan 2025 21:43:35 GMT  
		Size: 16.1 MB (16142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269211f1ea045e884f1175d77556df415d3093969647d5f33b870d33c557999`  
		Last Modified: Fri, 31 Jan 2025 01:43:28 GMT  
		Size: 43.9 MB (43949613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469f3a85ca4aad23caca93275437a25893f78888c8e35dcf3b777dfeec31c5e`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b248eed509cdcce48e80c1834adc9f5fb2a6d150447ac1b88ef4c81f5801ce`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6260fe841bd8ff183feb4f3b23be356af2587159a25957dce20b13c0486558e`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937294ed5c2b876156e6dd80cf376217fabd65bb3998c49c322b5a5c38fe8a5`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.1 MB (1106992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549988002ba8e52ba256a8f9d80b6bf108a1d30c7ddfd6e2b0fbba95329d3997`  
		Last Modified: Fri, 31 Jan 2025 03:06:00 GMT  
		Size: 20.7 MB (20738595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c181f6a200c29666bf284727fd36c83cc195e4256c6191833945198a7d621cd4`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.3-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:2f1f3fcb6282f645dab37295581e0cb96eb0abe6ca05c0b73901575b11b47877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66e1f839d5d0dfe7e3b0545284aa2343dc2bf4afe5298181c171bfe8133ae0e`

```dockerfile
```

-	Layers:
	-	`sha256:bd390fe31e5b1e6fbf3a8f394df26d0adaa6533984929212d60a0167fa92f9f3`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 3.8 MB (3791722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfae3079dd604603e30212b6ac374e782d770a95bb60ad1f5ad32b1678b1771f`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 24.6 KB (24619 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:f307fbf52d25609d47e3ac7704152577b0a002133aa212743e89908b567c35cf
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
$ docker pull zookeeper@sha256:aa6ec3db1a0960092086d220d02d0186c77c71172319dce506e27556ed1edde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114510925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6bd4b9a4138c3e5e8ee511ea6f5345852ce6a634c87f98ba7b2a9eef72009e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e0eb3ffb6314e0f9d31875847014be83d559907650166922294849a90067c`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d82f79248ff8f2c414866300c27772194c01d7f0bcca8d562e81b32985168`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 1.1 MB (1144074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d042f58baf6e8fcbfdc60b3d8769eeab68730d2a3418ced0999d5d87624c382`  
		Last Modified: Fri, 31 Jan 2025 02:17:25 GMT  
		Size: 20.7 MB (20738551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67463b93523af12e3e99fe23651b019a2613ace59f0088c1cc73958d2d6c2c3a`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:846a88c4b16b98554834c23c1de123935cb5ac57f3ff52b0923ca13758a5e5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49b42309840c1a36aafd63cc339bcbdc7ef61728433d93c9ee868cbad2ef371`

```dockerfile
```

-	Layers:
	-	`sha256:f33967c4fd801614c92bef87c91a60d9c95715b70734393b17d674a33942457f`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 3.8 MB (3788256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25abaa992310182c1eb48c410d83c9650c10da9240b5ab9039dedc02a7f5fe36`  
		Last Modified: Fri, 31 Jan 2025 02:17:24 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:e8fef66f98939710ee60c784ac359e96a325fde422e7e6f7e064b09bff42e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111700833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb02eaf6d705617dd2538aa6b9e05b801b352b5d3fa77c1e0009bd88eab3943`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0973fbeb41c9a280ddd2a5231976081b3e144f214b1f8e797cab794b099c2e`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbefce51f5c275db2eae4e5a9891c31ca59fe9263dc1b26a6332ee0a5deaeb1c`  
		Last Modified: Fri, 31 Jan 2025 04:45:48 GMT  
		Size: 1.1 MB (1073319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04182fd92029cf704a610af0d38ece6c62fa932d646e0fbbb4d0a7eb3ce60fe`  
		Last Modified: Fri, 31 Jan 2025 04:46:10 GMT  
		Size: 20.7 MB (20738605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b0a2d27c017a1159e2807e8e34b6b68dfd2960934e64373e40b153739fca34`  
		Last Modified: Fri, 31 Jan 2025 04:46:09 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:5169832127f3f1aa04eadab7e35568b638da0c8622f72d4e8d3ab2e8be7b1067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3814592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210328231554dc9443310a4bce02e52e2a65f9aab63298949688d65e7adc5488`

```dockerfile
```

-	Layers:
	-	`sha256:174064e8530e42e1c6989654c2b2592886517e0baad4fa14b2a4aa382f915b1c`  
		Last Modified: Fri, 31 Jan 2025 04:46:09 GMT  
		Size: 3.8 MB (3789826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfee6029b833b262f6b8fe0147209d93c0e39393ceb93776ff055677218fd95d`  
		Last Modified: Fri, 31 Jan 2025 04:46:08 GMT  
		Size: 24.8 KB (24766 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:dc497481b9c796f4a26e3c82fecad41d90165fe6da1629b0f35940ee4363e005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120702842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d23abfda56556ae606214e1fc9eee51e0156f55c7b3c1fa63e4755ea5ab497c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1549ab3d8e534df8d96c792f2811628e2e2df295e9f3a0f7b600693d70ea4054`  
		Last Modified: Wed, 22 Jan 2025 18:30:54 GMT  
		Size: 17.7 MB (17651386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0adfe1116944f60bc9086d8430625fc17a62d6d3c33f38bebe372b09008b9e7`  
		Last Modified: Fri, 31 Jan 2025 04:51:32 GMT  
		Size: 46.8 MB (46769686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37654f19ec6d92e72c255e64a181b0f0438b4032e516977695b878aeb999248`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a978d624bef09843b3a9bd929f94a3d7b958919206064439abe8869992b8120c`  
		Last Modified: Fri, 31 Jan 2025 04:51:30 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0333ef06de8c79f090ece86e015d0fdf5a1ea3bb8f55ac5a351d71cf9a1f48c`  
		Last Modified: Fri, 31 Jan 2025 06:30:45 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae8eee43a0b144a5152c7e29e56d2eaea341bc2804b53047b900efd04343a47`  
		Last Modified: Fri, 31 Jan 2025 06:30:46 GMT  
		Size: 1.1 MB (1089900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86903258effb23d771e5cfd71350c9948e4f30942cc1d15e804fcbe71bb7ee4c`  
		Last Modified: Fri, 31 Jan 2025 06:31:22 GMT  
		Size: 20.7 MB (20738582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408708c03d628c27719f2736f4439f49452f30107211ca7a2346ff661f216de4`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:163f0dbd4aec276441ce404db504a2399a41a5573f8d3bfd3309001eb015ce14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3818760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cb24a3ba3f15cd65ccacd881bb6a9ed7311b37e8ae812e2f2732ed6f32e298`

```dockerfile
```

-	Layers:
	-	`sha256:b09d7351d95570310b99a82892a6ea185a9bc452669a6d70570c49a81b91766a`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 3.8 MB (3794087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc62e1e9bc60f7411befb81e713df1c1e04c619c4fcf0c214f5d70f4fdd6d9b`  
		Last Modified: Fri, 31 Jan 2025 06:31:21 GMT  
		Size: 24.7 KB (24673 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; s390x

```console
$ docker pull zookeeper@sha256:43700ef351003c66ded8b4b5fbb590a0f354640e47c422fdb0a88f8604cd95d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109943849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9504a9b2eb126ddfea724393dba83486c9d8d621c421c60fcc63a02c44215561`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 10:14:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Mon, 28 Oct 2024 10:14:47 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.3
# Mon, 28 Oct 2024 10:14:47 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.3 DISTRO_NAME=apache-zookeeper-3.9.3-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
WORKDIR /apache-zookeeper-3.9.3-bin
# Mon, 28 Oct 2024 10:14:47 GMT
VOLUME [/data /datalog /logs]
# Mon, 28 Oct 2024 10:14:47 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Mon, 28 Oct 2024 10:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.3-bin/bin ZOOCFGDIR=/conf
# Mon, 28 Oct 2024 10:14:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 28 Oct 2024 10:14:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 28 Oct 2024 10:14:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce8df2d77e2997c97b30184cdfa23846196d4e5dfd005da96d8f36dcbc641a`  
		Last Modified: Wed, 22 Jan 2025 21:43:35 GMT  
		Size: 16.1 MB (16142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269211f1ea045e884f1175d77556df415d3093969647d5f33b870d33c557999`  
		Last Modified: Fri, 31 Jan 2025 01:43:28 GMT  
		Size: 43.9 MB (43949613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469f3a85ca4aad23caca93275437a25893f78888c8e35dcf3b777dfeec31c5e`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b248eed509cdcce48e80c1834adc9f5fb2a6d150447ac1b88ef4c81f5801ce`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6260fe841bd8ff183feb4f3b23be356af2587159a25957dce20b13c0486558e`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937294ed5c2b876156e6dd80cf376217fabd65bb3998c49c322b5a5c38fe8a5`  
		Last Modified: Fri, 31 Jan 2025 03:00:42 GMT  
		Size: 1.1 MB (1106992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549988002ba8e52ba256a8f9d80b6bf108a1d30c7ddfd6e2b0fbba95329d3997`  
		Last Modified: Fri, 31 Jan 2025 03:06:00 GMT  
		Size: 20.7 MB (20738595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c181f6a200c29666bf284727fd36c83cc195e4256c6191833945198a7d621cd4`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:2f1f3fcb6282f645dab37295581e0cb96eb0abe6ca05c0b73901575b11b47877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66e1f839d5d0dfe7e3b0545284aa2343dc2bf4afe5298181c171bfe8133ae0e`

```dockerfile
```

-	Layers:
	-	`sha256:bd390fe31e5b1e6fbf3a8f394df26d0adaa6533984929212d60a0167fa92f9f3`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 3.8 MB (3791722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfae3079dd604603e30212b6ac374e782d770a95bb60ad1f5ad32b1678b1771f`  
		Last Modified: Fri, 31 Jan 2025 03:05:59 GMT  
		Size: 24.6 KB (24619 bytes)  
		MIME: application/vnd.in-toto+json
