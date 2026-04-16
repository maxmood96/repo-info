<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `zookeeper`

-	[`zookeeper:3.8`](#zookeeper38)
-	[`zookeeper:3.8-jre-17`](#zookeeper38-jre-17)
-	[`zookeeper:3.8.6`](#zookeeper386)
-	[`zookeeper:3.8.6-jre-17`](#zookeeper386-jre-17)
-	[`zookeeper:3.9`](#zookeeper39)
-	[`zookeeper:3.9-jre-17`](#zookeeper39-jre-17)
-	[`zookeeper:3.9.5`](#zookeeper395)
-	[`zookeeper:3.9.5-jre-17`](#zookeeper395-jre-17)
-	[`zookeeper:latest`](#zookeeperlatest)

## `zookeeper:3.8`

```console
$ docker pull zookeeper@sha256:ee87b2e71915c5224cc808c38781f7579e248dbfec7eb51b9c9d1bb1ef218844
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
$ docker pull zookeeper@sha256:748e6c13ac9d5e52a00ed92f6974a9b6a0f34293eb6063743012d8970f63b2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110942448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085f806d6df9b4bbf8f6df2d7a6ae43b6b2343429187d2793e8c8f4012103e16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:34 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 21:59:34 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 21:59:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:59:41 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 21:59:41 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Wed, 15 Apr 2026 21:59:41 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 21:59:46 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 21:59:46 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 21:59:46 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 21:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 21:59:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:59:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f3568ba76ea6d97e9c2c393f0a402371cba409856a0ef86d9bf4821182a7d7`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 47.4 MB (47434807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b777945cb531796e3b41d7173704f3fdc2d7011ca46c9a27a4237eb04af664`  
		Last Modified: Wed, 15 Apr 2026 20:33:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007562ed65e8aa941dbb159078fc35e51f2378385997d673ff39b4d6b6d0c97`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a64adf91b4dafcb8c7f1da0360d8afbe712180d3f614f82dd63d33d8aa7756`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33efda4ce2c95c7590f2d2326abc49a99c7ea9645f088bc2124e07df51a288c3`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 1.1 MB (1144553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074f758fd8811e6e533cf3bc063e361c7dad4f42b1d33872ae144905116d503`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 16.5 MB (16470696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42957319b38fb15f9a7b02a66918cf239914efe1a3441423cd95526b32ec935e`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:20e7d52fcaa3a82e8d0b2fa52216882cd26c8eba9eb052ea05607ad0ce2858fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d99a59a4e8905a903243207caaa81b6d1bd266508a8f3ed431dc9070458d2e5`

```dockerfile
```

-	Layers:
	-	`sha256:15a70727d1ef72abf76c57bdba46b990f99b50ab7e3ef5b40732659d42feff02`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 4.0 MB (3978733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7374c8496d8a28c69128688434cfddf86e712410e4d924ce50c8ecf6353555c`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 24.3 KB (24272 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:173d345277d40f88af34a730123a892ebac1942c2c5ae271fa7b7695e06b2a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108152941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14c6f5cc2aa601f13a6c583ae8d62a400f5aa945450cc363143f590a3e6a8e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:38 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 22:11:38 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 22:11:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:11:46 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 22:11:46 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Wed, 15 Apr 2026 22:11:46 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 22:11:50 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 22:11:50 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 22:11:50 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 22:11:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 22:11:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:50 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98330033bf657ef38c4def539642b9558b298a9b15192b97392d09c1639d97`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 16.1 MB (16075224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936158611fedc7b5b979e813ae30ae867716cacdd0feae8ce49cfe3f8180eca5`  
		Last Modified: Wed, 15 Apr 2026 20:34:26 GMT  
		Size: 46.9 MB (46922027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db291c6cfd32c40bdd43b4647fbce29caf2d1115fd8c41859c06cbd8c3f3bd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e8b1b8a651c9f479d408d0b0d092c2b17d3f06923781ee09a0704899f0686`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe0f2305abfd3c686942254721db6764a3ee652917b2c3a2c05370d9cf990bf`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310aca1041bb199114fa10767be424517b691da8cf1df7cd3ad4eecdbadde4fb`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 1.1 MB (1073680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc17b121a704f5f21b1fc40f6fd33c7d55a6be84573c559c68d3a5e00324ec4`  
		Last Modified: Wed, 15 Apr 2026 22:12:02 GMT  
		Size: 16.5 MB (16470428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fdc20441dd70c6cd3f8faaaafed4329413c80a83ec531de9038981aecfc21a`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bcdcb0b07e3b139d7391596a14eadc993e5899368ed0f406ab752b8d8af1582b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eeaf76b5a5c75f4d4c0f6da4f72c385cd0b4fd8ba752db9d6282eaf2a614734`

```dockerfile
```

-	Layers:
	-	`sha256:60ad0b6a2b3b6f33bc0d3319e1ca22eefdfdf5d3d8b1abe419d6a70c202e17f8`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 4.0 MB (3978415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bec71c2e7f43ffa8827e76694e2731e460d3c8700ba2881852baf09ce5bdd3b`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 24.4 KB (24407 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:3429ec98079a048dc7662b25f5dcade7235993b8334355987d94f3757608ded8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117169170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a6c41ee50807c843719b413361451f06313f5983983421432d98d9ee76df87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 21:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:19:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 02:26:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 02:26:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Thu, 16 Apr 2026 02:26:17 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 02:26:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 02:26:25 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 02:26:25 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 02:26:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 02:26:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:25 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1be39ccce666bd30c5be03c8d81050c9ca7700ec279467e4c63973a13926f3`  
		Last Modified: Wed, 15 Apr 2026 21:20:27 GMT  
		Size: 47.3 MB (47331380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69109c2036e1b5cc92e8265d9d08ba987b3e05b754d1122c09349c8585b8498`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67097945e74c5c06dbc1104e2850f6e16a79862c4a8f6dfd35c9a76f82e5ed93`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b253b33e4ddb53fd66bccd92f5695f7f86fe517dac3869afaf462122a2df2`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be4341530f5750c21db1358fb8f3eafd8c7fb9c1168b3f7f20a32e576cee5b4`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 1.1 MB (1090094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a47d12a75d070a32a6f546d3e52ba39ca3929bc249d57d44d62f8174864c049`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 16.5 MB (16470719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb8a7211ccdd7feefe6cf6273245d15c98e96be6fa1fb6e5515c2972b05808b`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:c18985dce7dc468be530dd4603d7353c479d67fd76c164ed6932a686650e2862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0490477b101cc78a41faa533cd4505bb109896f9f9882ebcfaa0560bda82aca`

```dockerfile
```

-	Layers:
	-	`sha256:c803fa6471c0f4edd0fff49e14a1fcb95bac5360abb9e0ef333ee25ef070f20c`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 4.0 MB (3982836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d9d47e1b3d383e06ce562b995b7193c33f7866e443d88106f4c459184ae9f6`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 24.3 KB (24321 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; s390x

```console
$ docker pull zookeeper@sha256:66b20392e238d44cfe6d108e9a8acb07ce819d04618921f6b50a13306327939a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106345430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a0917fa6a9c860073fb174308f2108f64e3d08afe81da5b51dfaff8ced17e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 00:32:51 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 00:32:51 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 00:32:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 00:32:55 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 00:32:55 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Thu, 16 Apr 2026 00:32:55 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 00:34:04 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 00:34:05 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 00:34:05 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 00:34:05 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 00:34:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 00:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 00:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:34:05 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd7f09d29853aeb978fa00c6a174063d2db0ceaef7ccc882bb2c9860c7f11c`  
		Last Modified: Wed, 15 Apr 2026 20:45:05 GMT  
		Size: 16.2 MB (16150512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51bc10b538bf35e7f17be627dc7d61e6e37baeff43c2f218814cc0c3d1ca3d`  
		Last Modified: Wed, 15 Apr 2026 20:45:48 GMT  
		Size: 44.4 MB (44409749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c359110d1bcbaa06c849c55581bb7a8236f6488fad8fa7cc3c2670108cb1c`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82cf8d2de7f90f113d0d7ee205b7e94eb4802062569f557ee778aacdc2e8069`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406943eb89b493b71c1593f0ffa3295556fca614b74cfd306017023507615e`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b7addb15b02f03bf9d46135e2179e278c2d8f74dc8994020541469e76ee1ef`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 1.1 MB (1107109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8853f290d01062b9cacddfdc14130b1ac427f57a3af366dd174ee38f912e4cc9`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 16.5 MB (16470719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1544d3658a6570c719d98abb86aac6535d1f723ef19929aa17dcbb00bb6532a8`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8b016af8e0074a70df0e659e9a4112a21d793fdceb6d25e0baf44fc42b5a4e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c500944b5ff669ec3422ba464ccee1491fd65c8575ca49e74ca6079837cf8`

```dockerfile
```

-	Layers:
	-	`sha256:970a454b2a95805990980030d0a4f53b9dff8463289d92fd7b5f49fcf0bf8ca2`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 4.0 MB (3980323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df05d0d1a8ae846316002d211affe0cc0058e139d4465b033d7fbefb81e842ec`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 24.3 KB (24272 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8-jre-17`

```console
$ docker pull zookeeper@sha256:ee87b2e71915c5224cc808c38781f7579e248dbfec7eb51b9c9d1bb1ef218844
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
$ docker pull zookeeper@sha256:748e6c13ac9d5e52a00ed92f6974a9b6a0f34293eb6063743012d8970f63b2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110942448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085f806d6df9b4bbf8f6df2d7a6ae43b6b2343429187d2793e8c8f4012103e16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:34 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 21:59:34 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 21:59:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:59:41 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 21:59:41 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Wed, 15 Apr 2026 21:59:41 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 21:59:46 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 21:59:46 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 21:59:46 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 21:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 21:59:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:59:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f3568ba76ea6d97e9c2c393f0a402371cba409856a0ef86d9bf4821182a7d7`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 47.4 MB (47434807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b777945cb531796e3b41d7173704f3fdc2d7011ca46c9a27a4237eb04af664`  
		Last Modified: Wed, 15 Apr 2026 20:33:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007562ed65e8aa941dbb159078fc35e51f2378385997d673ff39b4d6b6d0c97`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a64adf91b4dafcb8c7f1da0360d8afbe712180d3f614f82dd63d33d8aa7756`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33efda4ce2c95c7590f2d2326abc49a99c7ea9645f088bc2124e07df51a288c3`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 1.1 MB (1144553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074f758fd8811e6e533cf3bc063e361c7dad4f42b1d33872ae144905116d503`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 16.5 MB (16470696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42957319b38fb15f9a7b02a66918cf239914efe1a3441423cd95526b32ec935e`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:20e7d52fcaa3a82e8d0b2fa52216882cd26c8eba9eb052ea05607ad0ce2858fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d99a59a4e8905a903243207caaa81b6d1bd266508a8f3ed431dc9070458d2e5`

```dockerfile
```

-	Layers:
	-	`sha256:15a70727d1ef72abf76c57bdba46b990f99b50ab7e3ef5b40732659d42feff02`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 4.0 MB (3978733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7374c8496d8a28c69128688434cfddf86e712410e4d924ce50c8ecf6353555c`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 24.3 KB (24272 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:173d345277d40f88af34a730123a892ebac1942c2c5ae271fa7b7695e06b2a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108152941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14c6f5cc2aa601f13a6c583ae8d62a400f5aa945450cc363143f590a3e6a8e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:38 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 22:11:38 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 22:11:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:11:46 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 22:11:46 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Wed, 15 Apr 2026 22:11:46 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 22:11:50 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 22:11:50 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 22:11:50 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 22:11:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 22:11:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:50 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98330033bf657ef38c4def539642b9558b298a9b15192b97392d09c1639d97`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 16.1 MB (16075224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936158611fedc7b5b979e813ae30ae867716cacdd0feae8ce49cfe3f8180eca5`  
		Last Modified: Wed, 15 Apr 2026 20:34:26 GMT  
		Size: 46.9 MB (46922027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db291c6cfd32c40bdd43b4647fbce29caf2d1115fd8c41859c06cbd8c3f3bd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e8b1b8a651c9f479d408d0b0d092c2b17d3f06923781ee09a0704899f0686`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe0f2305abfd3c686942254721db6764a3ee652917b2c3a2c05370d9cf990bf`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310aca1041bb199114fa10767be424517b691da8cf1df7cd3ad4eecdbadde4fb`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 1.1 MB (1073680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc17b121a704f5f21b1fc40f6fd33c7d55a6be84573c559c68d3a5e00324ec4`  
		Last Modified: Wed, 15 Apr 2026 22:12:02 GMT  
		Size: 16.5 MB (16470428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fdc20441dd70c6cd3f8faaaafed4329413c80a83ec531de9038981aecfc21a`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bcdcb0b07e3b139d7391596a14eadc993e5899368ed0f406ab752b8d8af1582b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eeaf76b5a5c75f4d4c0f6da4f72c385cd0b4fd8ba752db9d6282eaf2a614734`

```dockerfile
```

-	Layers:
	-	`sha256:60ad0b6a2b3b6f33bc0d3319e1ca22eefdfdf5d3d8b1abe419d6a70c202e17f8`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 4.0 MB (3978415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bec71c2e7f43ffa8827e76694e2731e460d3c8700ba2881852baf09ce5bdd3b`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 24.4 KB (24407 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:3429ec98079a048dc7662b25f5dcade7235993b8334355987d94f3757608ded8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117169170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a6c41ee50807c843719b413361451f06313f5983983421432d98d9ee76df87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 21:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:19:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 02:26:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 02:26:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Thu, 16 Apr 2026 02:26:17 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 02:26:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 02:26:25 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 02:26:25 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 02:26:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 02:26:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:25 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1be39ccce666bd30c5be03c8d81050c9ca7700ec279467e4c63973a13926f3`  
		Last Modified: Wed, 15 Apr 2026 21:20:27 GMT  
		Size: 47.3 MB (47331380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69109c2036e1b5cc92e8265d9d08ba987b3e05b754d1122c09349c8585b8498`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67097945e74c5c06dbc1104e2850f6e16a79862c4a8f6dfd35c9a76f82e5ed93`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b253b33e4ddb53fd66bccd92f5695f7f86fe517dac3869afaf462122a2df2`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be4341530f5750c21db1358fb8f3eafd8c7fb9c1168b3f7f20a32e576cee5b4`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 1.1 MB (1090094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a47d12a75d070a32a6f546d3e52ba39ca3929bc249d57d44d62f8174864c049`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 16.5 MB (16470719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb8a7211ccdd7feefe6cf6273245d15c98e96be6fa1fb6e5515c2972b05808b`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:c18985dce7dc468be530dd4603d7353c479d67fd76c164ed6932a686650e2862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0490477b101cc78a41faa533cd4505bb109896f9f9882ebcfaa0560bda82aca`

```dockerfile
```

-	Layers:
	-	`sha256:c803fa6471c0f4edd0fff49e14a1fcb95bac5360abb9e0ef333ee25ef070f20c`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 4.0 MB (3982836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d9d47e1b3d383e06ce562b995b7193c33f7866e443d88106f4c459184ae9f6`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 24.3 KB (24321 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:66b20392e238d44cfe6d108e9a8acb07ce819d04618921f6b50a13306327939a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106345430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a0917fa6a9c860073fb174308f2108f64e3d08afe81da5b51dfaff8ced17e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 00:32:51 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 00:32:51 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 00:32:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 00:32:55 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 00:32:55 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Thu, 16 Apr 2026 00:32:55 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 00:34:04 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 00:34:05 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 00:34:05 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 00:34:05 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 00:34:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 00:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 00:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:34:05 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd7f09d29853aeb978fa00c6a174063d2db0ceaef7ccc882bb2c9860c7f11c`  
		Last Modified: Wed, 15 Apr 2026 20:45:05 GMT  
		Size: 16.2 MB (16150512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51bc10b538bf35e7f17be627dc7d61e6e37baeff43c2f218814cc0c3d1ca3d`  
		Last Modified: Wed, 15 Apr 2026 20:45:48 GMT  
		Size: 44.4 MB (44409749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c359110d1bcbaa06c849c55581bb7a8236f6488fad8fa7cc3c2670108cb1c`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82cf8d2de7f90f113d0d7ee205b7e94eb4802062569f557ee778aacdc2e8069`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406943eb89b493b71c1593f0ffa3295556fca614b74cfd306017023507615e`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b7addb15b02f03bf9d46135e2179e278c2d8f74dc8994020541469e76ee1ef`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 1.1 MB (1107109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8853f290d01062b9cacddfdc14130b1ac427f57a3af366dd174ee38f912e4cc9`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 16.5 MB (16470719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1544d3658a6570c719d98abb86aac6535d1f723ef19929aa17dcbb00bb6532a8`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8b016af8e0074a70df0e659e9a4112a21d793fdceb6d25e0baf44fc42b5a4e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c500944b5ff669ec3422ba464ccee1491fd65c8575ca49e74ca6079837cf8`

```dockerfile
```

-	Layers:
	-	`sha256:970a454b2a95805990980030d0a4f53b9dff8463289d92fd7b5f49fcf0bf8ca2`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 4.0 MB (3980323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df05d0d1a8ae846316002d211affe0cc0058e139d4465b033d7fbefb81e842ec`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 24.3 KB (24272 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8.6`

```console
$ docker pull zookeeper@sha256:ee87b2e71915c5224cc808c38781f7579e248dbfec7eb51b9c9d1bb1ef218844
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

### `zookeeper:3.8.6` - linux; amd64

```console
$ docker pull zookeeper@sha256:748e6c13ac9d5e52a00ed92f6974a9b6a0f34293eb6063743012d8970f63b2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110942448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085f806d6df9b4bbf8f6df2d7a6ae43b6b2343429187d2793e8c8f4012103e16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:34 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 21:59:34 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 21:59:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:59:41 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 21:59:41 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Wed, 15 Apr 2026 21:59:41 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 21:59:46 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 21:59:46 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 21:59:46 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 21:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 21:59:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:59:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f3568ba76ea6d97e9c2c393f0a402371cba409856a0ef86d9bf4821182a7d7`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 47.4 MB (47434807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b777945cb531796e3b41d7173704f3fdc2d7011ca46c9a27a4237eb04af664`  
		Last Modified: Wed, 15 Apr 2026 20:33:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007562ed65e8aa941dbb159078fc35e51f2378385997d673ff39b4d6b6d0c97`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a64adf91b4dafcb8c7f1da0360d8afbe712180d3f614f82dd63d33d8aa7756`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33efda4ce2c95c7590f2d2326abc49a99c7ea9645f088bc2124e07df51a288c3`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 1.1 MB (1144553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074f758fd8811e6e533cf3bc063e361c7dad4f42b1d33872ae144905116d503`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 16.5 MB (16470696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42957319b38fb15f9a7b02a66918cf239914efe1a3441423cd95526b32ec935e`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.6` - unknown; unknown

```console
$ docker pull zookeeper@sha256:20e7d52fcaa3a82e8d0b2fa52216882cd26c8eba9eb052ea05607ad0ce2858fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d99a59a4e8905a903243207caaa81b6d1bd266508a8f3ed431dc9070458d2e5`

```dockerfile
```

-	Layers:
	-	`sha256:15a70727d1ef72abf76c57bdba46b990f99b50ab7e3ef5b40732659d42feff02`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 4.0 MB (3978733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7374c8496d8a28c69128688434cfddf86e712410e4d924ce50c8ecf6353555c`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 24.3 KB (24272 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.6` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:173d345277d40f88af34a730123a892ebac1942c2c5ae271fa7b7695e06b2a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108152941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14c6f5cc2aa601f13a6c583ae8d62a400f5aa945450cc363143f590a3e6a8e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:38 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 22:11:38 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 22:11:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:11:46 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 22:11:46 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Wed, 15 Apr 2026 22:11:46 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 22:11:50 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 22:11:50 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 22:11:50 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 22:11:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 22:11:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:50 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98330033bf657ef38c4def539642b9558b298a9b15192b97392d09c1639d97`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 16.1 MB (16075224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936158611fedc7b5b979e813ae30ae867716cacdd0feae8ce49cfe3f8180eca5`  
		Last Modified: Wed, 15 Apr 2026 20:34:26 GMT  
		Size: 46.9 MB (46922027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db291c6cfd32c40bdd43b4647fbce29caf2d1115fd8c41859c06cbd8c3f3bd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e8b1b8a651c9f479d408d0b0d092c2b17d3f06923781ee09a0704899f0686`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe0f2305abfd3c686942254721db6764a3ee652917b2c3a2c05370d9cf990bf`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310aca1041bb199114fa10767be424517b691da8cf1df7cd3ad4eecdbadde4fb`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 1.1 MB (1073680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc17b121a704f5f21b1fc40f6fd33c7d55a6be84573c559c68d3a5e00324ec4`  
		Last Modified: Wed, 15 Apr 2026 22:12:02 GMT  
		Size: 16.5 MB (16470428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fdc20441dd70c6cd3f8faaaafed4329413c80a83ec531de9038981aecfc21a`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.6` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bcdcb0b07e3b139d7391596a14eadc993e5899368ed0f406ab752b8d8af1582b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eeaf76b5a5c75f4d4c0f6da4f72c385cd0b4fd8ba752db9d6282eaf2a614734`

```dockerfile
```

-	Layers:
	-	`sha256:60ad0b6a2b3b6f33bc0d3319e1ca22eefdfdf5d3d8b1abe419d6a70c202e17f8`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 4.0 MB (3978415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bec71c2e7f43ffa8827e76694e2731e460d3c8700ba2881852baf09ce5bdd3b`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 24.4 KB (24407 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.6` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:3429ec98079a048dc7662b25f5dcade7235993b8334355987d94f3757608ded8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117169170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a6c41ee50807c843719b413361451f06313f5983983421432d98d9ee76df87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 21:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:19:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 02:26:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 02:26:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Thu, 16 Apr 2026 02:26:17 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 02:26:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 02:26:25 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 02:26:25 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 02:26:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 02:26:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:25 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1be39ccce666bd30c5be03c8d81050c9ca7700ec279467e4c63973a13926f3`  
		Last Modified: Wed, 15 Apr 2026 21:20:27 GMT  
		Size: 47.3 MB (47331380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69109c2036e1b5cc92e8265d9d08ba987b3e05b754d1122c09349c8585b8498`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67097945e74c5c06dbc1104e2850f6e16a79862c4a8f6dfd35c9a76f82e5ed93`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b253b33e4ddb53fd66bccd92f5695f7f86fe517dac3869afaf462122a2df2`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be4341530f5750c21db1358fb8f3eafd8c7fb9c1168b3f7f20a32e576cee5b4`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 1.1 MB (1090094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a47d12a75d070a32a6f546d3e52ba39ca3929bc249d57d44d62f8174864c049`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 16.5 MB (16470719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb8a7211ccdd7feefe6cf6273245d15c98e96be6fa1fb6e5515c2972b05808b`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.6` - unknown; unknown

```console
$ docker pull zookeeper@sha256:c18985dce7dc468be530dd4603d7353c479d67fd76c164ed6932a686650e2862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0490477b101cc78a41faa533cd4505bb109896f9f9882ebcfaa0560bda82aca`

```dockerfile
```

-	Layers:
	-	`sha256:c803fa6471c0f4edd0fff49e14a1fcb95bac5360abb9e0ef333ee25ef070f20c`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 4.0 MB (3982836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d9d47e1b3d383e06ce562b995b7193c33f7866e443d88106f4c459184ae9f6`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 24.3 KB (24321 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.6` - linux; s390x

```console
$ docker pull zookeeper@sha256:66b20392e238d44cfe6d108e9a8acb07ce819d04618921f6b50a13306327939a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106345430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a0917fa6a9c860073fb174308f2108f64e3d08afe81da5b51dfaff8ced17e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 00:32:51 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 00:32:51 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 00:32:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 00:32:55 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 00:32:55 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Thu, 16 Apr 2026 00:32:55 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 00:34:04 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 00:34:05 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 00:34:05 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 00:34:05 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 00:34:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 00:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 00:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:34:05 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd7f09d29853aeb978fa00c6a174063d2db0ceaef7ccc882bb2c9860c7f11c`  
		Last Modified: Wed, 15 Apr 2026 20:45:05 GMT  
		Size: 16.2 MB (16150512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51bc10b538bf35e7f17be627dc7d61e6e37baeff43c2f218814cc0c3d1ca3d`  
		Last Modified: Wed, 15 Apr 2026 20:45:48 GMT  
		Size: 44.4 MB (44409749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c359110d1bcbaa06c849c55581bb7a8236f6488fad8fa7cc3c2670108cb1c`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82cf8d2de7f90f113d0d7ee205b7e94eb4802062569f557ee778aacdc2e8069`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406943eb89b493b71c1593f0ffa3295556fca614b74cfd306017023507615e`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b7addb15b02f03bf9d46135e2179e278c2d8f74dc8994020541469e76ee1ef`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 1.1 MB (1107109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8853f290d01062b9cacddfdc14130b1ac427f57a3af366dd174ee38f912e4cc9`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 16.5 MB (16470719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1544d3658a6570c719d98abb86aac6535d1f723ef19929aa17dcbb00bb6532a8`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.6` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8b016af8e0074a70df0e659e9a4112a21d793fdceb6d25e0baf44fc42b5a4e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c500944b5ff669ec3422ba464ccee1491fd65c8575ca49e74ca6079837cf8`

```dockerfile
```

-	Layers:
	-	`sha256:970a454b2a95805990980030d0a4f53b9dff8463289d92fd7b5f49fcf0bf8ca2`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 4.0 MB (3980323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df05d0d1a8ae846316002d211affe0cc0058e139d4465b033d7fbefb81e842ec`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 24.3 KB (24272 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8.6-jre-17`

```console
$ docker pull zookeeper@sha256:ee87b2e71915c5224cc808c38781f7579e248dbfec7eb51b9c9d1bb1ef218844
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

### `zookeeper:3.8.6-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:748e6c13ac9d5e52a00ed92f6974a9b6a0f34293eb6063743012d8970f63b2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110942448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085f806d6df9b4bbf8f6df2d7a6ae43b6b2343429187d2793e8c8f4012103e16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:34 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 21:59:34 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 21:59:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:59:41 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 21:59:41 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Wed, 15 Apr 2026 21:59:41 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 21:59:46 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 21:59:46 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 21:59:46 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 21:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 21:59:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:59:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:47 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f3568ba76ea6d97e9c2c393f0a402371cba409856a0ef86d9bf4821182a7d7`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 47.4 MB (47434807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b777945cb531796e3b41d7173704f3fdc2d7011ca46c9a27a4237eb04af664`  
		Last Modified: Wed, 15 Apr 2026 20:33:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007562ed65e8aa941dbb159078fc35e51f2378385997d673ff39b4d6b6d0c97`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a64adf91b4dafcb8c7f1da0360d8afbe712180d3f614f82dd63d33d8aa7756`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33efda4ce2c95c7590f2d2326abc49a99c7ea9645f088bc2124e07df51a288c3`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 1.1 MB (1144553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074f758fd8811e6e533cf3bc063e361c7dad4f42b1d33872ae144905116d503`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 16.5 MB (16470696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42957319b38fb15f9a7b02a66918cf239914efe1a3441423cd95526b32ec935e`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.6-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:20e7d52fcaa3a82e8d0b2fa52216882cd26c8eba9eb052ea05607ad0ce2858fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d99a59a4e8905a903243207caaa81b6d1bd266508a8f3ed431dc9070458d2e5`

```dockerfile
```

-	Layers:
	-	`sha256:15a70727d1ef72abf76c57bdba46b990f99b50ab7e3ef5b40732659d42feff02`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 4.0 MB (3978733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7374c8496d8a28c69128688434cfddf86e712410e4d924ce50c8ecf6353555c`  
		Last Modified: Wed, 15 Apr 2026 21:59:55 GMT  
		Size: 24.3 KB (24272 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.6-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:173d345277d40f88af34a730123a892ebac1942c2c5ae271fa7b7695e06b2a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108152941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14c6f5cc2aa601f13a6c583ae8d62a400f5aa945450cc363143f590a3e6a8e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:38 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 22:11:38 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 22:11:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:11:46 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 22:11:46 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Wed, 15 Apr 2026 22:11:46 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 22:11:50 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Wed, 15 Apr 2026 22:11:50 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 22:11:50 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 22:11:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 22:11:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:50 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98330033bf657ef38c4def539642b9558b298a9b15192b97392d09c1639d97`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 16.1 MB (16075224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936158611fedc7b5b979e813ae30ae867716cacdd0feae8ce49cfe3f8180eca5`  
		Last Modified: Wed, 15 Apr 2026 20:34:26 GMT  
		Size: 46.9 MB (46922027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db291c6cfd32c40bdd43b4647fbce29caf2d1115fd8c41859c06cbd8c3f3bd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e8b1b8a651c9f479d408d0b0d092c2b17d3f06923781ee09a0704899f0686`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe0f2305abfd3c686942254721db6764a3ee652917b2c3a2c05370d9cf990bf`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310aca1041bb199114fa10767be424517b691da8cf1df7cd3ad4eecdbadde4fb`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 1.1 MB (1073680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc17b121a704f5f21b1fc40f6fd33c7d55a6be84573c559c68d3a5e00324ec4`  
		Last Modified: Wed, 15 Apr 2026 22:12:02 GMT  
		Size: 16.5 MB (16470428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fdc20441dd70c6cd3f8faaaafed4329413c80a83ec531de9038981aecfc21a`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.6-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:bcdcb0b07e3b139d7391596a14eadc993e5899368ed0f406ab752b8d8af1582b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eeaf76b5a5c75f4d4c0f6da4f72c385cd0b4fd8ba752db9d6282eaf2a614734`

```dockerfile
```

-	Layers:
	-	`sha256:60ad0b6a2b3b6f33bc0d3319e1ca22eefdfdf5d3d8b1abe419d6a70c202e17f8`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 4.0 MB (3978415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bec71c2e7f43ffa8827e76694e2731e460d3c8700ba2881852baf09ce5bdd3b`  
		Last Modified: Wed, 15 Apr 2026 22:12:01 GMT  
		Size: 24.4 KB (24407 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.6-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:3429ec98079a048dc7662b25f5dcade7235993b8334355987d94f3757608ded8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117169170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a6c41ee50807c843719b413361451f06313f5983983421432d98d9ee76df87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 21:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:19:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 02:26:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 02:26:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Thu, 16 Apr 2026 02:26:17 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 02:26:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 02:26:25 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 02:26:25 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 02:26:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 02:26:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:25 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1be39ccce666bd30c5be03c8d81050c9ca7700ec279467e4c63973a13926f3`  
		Last Modified: Wed, 15 Apr 2026 21:20:27 GMT  
		Size: 47.3 MB (47331380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69109c2036e1b5cc92e8265d9d08ba987b3e05b754d1122c09349c8585b8498`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67097945e74c5c06dbc1104e2850f6e16a79862c4a8f6dfd35c9a76f82e5ed93`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b253b33e4ddb53fd66bccd92f5695f7f86fe517dac3869afaf462122a2df2`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be4341530f5750c21db1358fb8f3eafd8c7fb9c1168b3f7f20a32e576cee5b4`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 1.1 MB (1090094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a47d12a75d070a32a6f546d3e52ba39ca3929bc249d57d44d62f8174864c049`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 16.5 MB (16470719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb8a7211ccdd7feefe6cf6273245d15c98e96be6fa1fb6e5515c2972b05808b`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 773.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.6-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:c18985dce7dc468be530dd4603d7353c479d67fd76c164ed6932a686650e2862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0490477b101cc78a41faa533cd4505bb109896f9f9882ebcfaa0560bda82aca`

```dockerfile
```

-	Layers:
	-	`sha256:c803fa6471c0f4edd0fff49e14a1fcb95bac5360abb9e0ef333ee25ef070f20c`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 4.0 MB (3982836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d9d47e1b3d383e06ce562b995b7193c33f7866e443d88106f4c459184ae9f6`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 24.3 KB (24321 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.6-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:66b20392e238d44cfe6d108e9a8acb07ce819d04618921f6b50a13306327939a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106345430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a0917fa6a9c860073fb174308f2108f64e3d08afe81da5b51dfaff8ced17e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 00:32:51 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 00:32:51 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 00:32:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 00:32:55 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 00:32:55 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.6
# Thu, 16 Apr 2026 00:32:55 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 00:34:04 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.6 DISTRO_NAME=apache-zookeeper-3.8.6-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 00:34:05 GMT
WORKDIR /apache-zookeeper-3.8.6-bin
# Thu, 16 Apr 2026 00:34:05 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 00:34:05 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 00:34:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.6-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 00:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 00:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:34:05 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd7f09d29853aeb978fa00c6a174063d2db0ceaef7ccc882bb2c9860c7f11c`  
		Last Modified: Wed, 15 Apr 2026 20:45:05 GMT  
		Size: 16.2 MB (16150512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51bc10b538bf35e7f17be627dc7d61e6e37baeff43c2f218814cc0c3d1ca3d`  
		Last Modified: Wed, 15 Apr 2026 20:45:48 GMT  
		Size: 44.4 MB (44409749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c359110d1bcbaa06c849c55581bb7a8236f6488fad8fa7cc3c2670108cb1c`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82cf8d2de7f90f113d0d7ee205b7e94eb4802062569f557ee778aacdc2e8069`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406943eb89b493b71c1593f0ffa3295556fca614b74cfd306017023507615e`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b7addb15b02f03bf9d46135e2179e278c2d8f74dc8994020541469e76ee1ef`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 1.1 MB (1107109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8853f290d01062b9cacddfdc14130b1ac427f57a3af366dd174ee38f912e4cc9`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 16.5 MB (16470719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1544d3658a6570c719d98abb86aac6535d1f723ef19929aa17dcbb00bb6532a8`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.6-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8b016af8e0074a70df0e659e9a4112a21d793fdceb6d25e0baf44fc42b5a4e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c500944b5ff669ec3422ba464ccee1491fd65c8575ca49e74ca6079837cf8`

```dockerfile
```

-	Layers:
	-	`sha256:970a454b2a95805990980030d0a4f53b9dff8463289d92fd7b5f49fcf0bf8ca2`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 4.0 MB (3980323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df05d0d1a8ae846316002d211affe0cc0058e139d4465b033d7fbefb81e842ec`  
		Last Modified: Thu, 16 Apr 2026 00:34:20 GMT  
		Size: 24.3 KB (24272 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9`

```console
$ docker pull zookeeper@sha256:0598e33ed585128313125f9c36cce6c164f0f21224e4bb75ca5c30b34655a13e
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
$ docker pull zookeeper@sha256:c8eb8e81f40b52a790b03ff5012dadd0ea2254bb94d45056dff2299b96d620f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117313378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b6567a57b971f5eede1d9ea752c7c25ba50128405c0cf77cde1a329afbc159`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:38 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 21:59:38 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 21:59:46 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Wed, 15 Apr 2026 21:59:46 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 21:59:50 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 21:59:50 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 21:59:50 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 21:59:50 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 21:59:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 21:59:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:59:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:50 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f3568ba76ea6d97e9c2c393f0a402371cba409856a0ef86d9bf4821182a7d7`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 47.4 MB (47434807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b777945cb531796e3b41d7173704f3fdc2d7011ca46c9a27a4237eb04af664`  
		Last Modified: Wed, 15 Apr 2026 20:33:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007562ed65e8aa941dbb159078fc35e51f2378385997d673ff39b4d6b6d0c97`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87a276eede96b082c7728d745f0a25d0f246458eaa1d419411fb048403f247`  
		Last Modified: Wed, 15 Apr 2026 22:00:00 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8758592b33ad5f822bf7c9d3db4151dca19abc9d62b236bee7a00af1f997e134`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 1.1 MB (1144597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e5f47f2313da96413d86c72226f81aca7142af02c29b83c25b5f623c61b271`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 22.8 MB (22841573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cd26cd0a20cd3d9333cae4599d1ecedfd7953b55d07a60bf38e6bcaca71aed`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:14d74daa7f1b2027f333a415cb1ebd8e9d80d55af1765677787acab605bf52ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4797b5b482c04e0e7b7407f3d080d3be2efc616346a1f87467f4df5bfee80c`

```dockerfile
```

-	Layers:
	-	`sha256:c2fa99cc07e2b2541d04a7d8038ce019ea421d9c0e0ce8c4e0d413dd1abf00fd`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 4.0 MB (3985509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457584590002f8713dced8b62d3732fd99ec64fffad173f73d3dd1f5800be2b0`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:c7c88d57fd28e04ac3ba4873493b00b1ced2cba639b36177a63dc37c99beca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114524080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc0dd184cb687124574b5e33cce18557387ff2b74943a9829241b5adc408539`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 22:11:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 22:11:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:11:56 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 22:11:56 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Wed, 15 Apr 2026 22:11:56 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 22:12:00 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 22:12:00 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 22:12:00 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 22:12:00 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 22:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 22:12:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:12:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:12:00 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98330033bf657ef38c4def539642b9558b298a9b15192b97392d09c1639d97`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 16.1 MB (16075224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936158611fedc7b5b979e813ae30ae867716cacdd0feae8ce49cfe3f8180eca5`  
		Last Modified: Wed, 15 Apr 2026 20:34:26 GMT  
		Size: 46.9 MB (46922027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db291c6cfd32c40bdd43b4647fbce29caf2d1115fd8c41859c06cbd8c3f3bd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e8b1b8a651c9f479d408d0b0d092c2b17d3f06923781ee09a0704899f0686`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0218ea9a27847c898c805d7e7c7fa85faf7334450d11ca9525559be91595d304`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c98375e424e65476743a816606f9270eb94aa50f105f09fe961678098247d5`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 1.1 MB (1073695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ec46bd5475c47364454444b10c5f23793a1e2b122fed2176154737aeee2d8`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 22.8 MB (22841551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a928c4252683c4240d0b5b18fc9d99afa856a48c0472571b013618ede75c474`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7fcc0b7086789c0797ad8a31cfab4982269034f5d4c50ff2c182ed6e465554a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f58334a441fa88020960af088f397007b1e2987bc0376095394858ccb1b789`

```dockerfile
```

-	Layers:
	-	`sha256:1ecc5caf1bbb05a8b1d167e2ab7281dc5bc8c95b575aba25a1c5d765be7b6cd7`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 4.0 MB (3985203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ac535077ee83b008d2ae66f822834641a91cf2e029dfd01e52da60fac1d5be4`  
		Last Modified: Wed, 15 Apr 2026 22:12:11 GMT  
		Size: 24.7 KB (24722 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:83eaea1cbaa61e8a0a2e7df9484fbce491e29cfcecfc3b720ef665225cc7c7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123540045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c1b4a8352a46ada62a6869534a7de7be6c909a9560168fd877129e9d7b97d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 21:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:19:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 02:26:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 02:26:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Thu, 16 Apr 2026 02:26:17 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 02:26:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 02:26:25 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 02:26:25 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 02:26:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 02:26:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:25 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1be39ccce666bd30c5be03c8d81050c9ca7700ec279467e4c63973a13926f3`  
		Last Modified: Wed, 15 Apr 2026 21:20:27 GMT  
		Size: 47.3 MB (47331380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69109c2036e1b5cc92e8265d9d08ba987b3e05b754d1122c09349c8585b8498`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67097945e74c5c06dbc1104e2850f6e16a79862c4a8f6dfd35c9a76f82e5ed93`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b253b33e4ddb53fd66bccd92f5695f7f86fe517dac3869afaf462122a2df2`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be4341530f5750c21db1358fb8f3eafd8c7fb9c1168b3f7f20a32e576cee5b4`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 1.1 MB (1090094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf2644f46e37ca9a34d97d0ab850ae62847c566ff10236343b30012a8035fa9`  
		Last Modified: Thu, 16 Apr 2026 02:26:48 GMT  
		Size: 22.8 MB (22841591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e2f535b7a28cdc24d50f1ab47011840e037ee4b973e956c215ab0fbdec3914`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7b7a9fb4fe12aa5d4a221e6fdc0f99485e861361e64d708290929e8a2bc5465d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a5458ee572ef1327adc370f75c0476be1dace3186c3abc6b346a36c6c799b3`

```dockerfile
```

-	Layers:
	-	`sha256:6ab573aba859d148274c5319af69429e273641ad8199d460c5a4bc9d1d33c054`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 4.0 MB (3989618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6173b096db84dd8667b9170905c40112e06375c2394a7305c867c5403abd1e81`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; s390x

```console
$ docker pull zookeeper@sha256:12c47b955d41a4a717423e4b0421cab72a8b915ce9eeac0a42d198f05af931ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112716241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979915f02fc2e25f99492cd1f7289c540d4b6c9a2e9c325181ff4925d689ed70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 00:33:24 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 00:33:24 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 00:33:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 00:33:28 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 00:33:28 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Thu, 16 Apr 2026 00:33:28 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 00:33:31 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 00:33:31 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 00:33:31 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 00:33:31 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 00:33:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 00:33:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 00:33:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:33:31 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd7f09d29853aeb978fa00c6a174063d2db0ceaef7ccc882bb2c9860c7f11c`  
		Last Modified: Wed, 15 Apr 2026 20:45:05 GMT  
		Size: 16.2 MB (16150512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51bc10b538bf35e7f17be627dc7d61e6e37baeff43c2f218814cc0c3d1ca3d`  
		Last Modified: Wed, 15 Apr 2026 20:45:48 GMT  
		Size: 44.4 MB (44409749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c359110d1bcbaa06c849c55581bb7a8236f6488fad8fa7cc3c2670108cb1c`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82cf8d2de7f90f113d0d7ee205b7e94eb4802062569f557ee778aacdc2e8069`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60374274574ecccf54877ac2826243aecae6c4a640bbf0f66d2ba85ea8c58d9e`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a6fbab791518f22e56a8a735f3c65926a2933886a3a4d6d8888b8b9c0f029`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 1.1 MB (1107064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a507bde4a7e395f695d0513a46896eafc7696e31735eb06b630eb7c62da5280d`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 22.8 MB (22841575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49d351b3ca9f641ee349e0798c36f1e261e421769125ffbb2fc8a562fad1589`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:cc5e9e37969f71efcb76e2f849cb20eae8c699889a0db884ce6da00caf856c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc518c9a5593ea7f019bbcb5a1e5d2dca4b4b1c45f9154374739a4a47f92f2a`

```dockerfile
```

-	Layers:
	-	`sha256:4db664b197a59d70df91738154ddaa50d989786f7a3b66c3bf3cb6eb0a6e8522`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 4.0 MB (3987099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb3148f66996e8197b78f81007a48c67095f9c5275989351768ab69a9ccec21`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9-jre-17`

```console
$ docker pull zookeeper@sha256:0598e33ed585128313125f9c36cce6c164f0f21224e4bb75ca5c30b34655a13e
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
$ docker pull zookeeper@sha256:c8eb8e81f40b52a790b03ff5012dadd0ea2254bb94d45056dff2299b96d620f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117313378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b6567a57b971f5eede1d9ea752c7c25ba50128405c0cf77cde1a329afbc159`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:38 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 21:59:38 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 21:59:46 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Wed, 15 Apr 2026 21:59:46 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 21:59:50 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 21:59:50 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 21:59:50 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 21:59:50 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 21:59:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 21:59:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:59:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:50 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f3568ba76ea6d97e9c2c393f0a402371cba409856a0ef86d9bf4821182a7d7`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 47.4 MB (47434807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b777945cb531796e3b41d7173704f3fdc2d7011ca46c9a27a4237eb04af664`  
		Last Modified: Wed, 15 Apr 2026 20:33:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007562ed65e8aa941dbb159078fc35e51f2378385997d673ff39b4d6b6d0c97`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87a276eede96b082c7728d745f0a25d0f246458eaa1d419411fb048403f247`  
		Last Modified: Wed, 15 Apr 2026 22:00:00 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8758592b33ad5f822bf7c9d3db4151dca19abc9d62b236bee7a00af1f997e134`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 1.1 MB (1144597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e5f47f2313da96413d86c72226f81aca7142af02c29b83c25b5f623c61b271`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 22.8 MB (22841573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cd26cd0a20cd3d9333cae4599d1ecedfd7953b55d07a60bf38e6bcaca71aed`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:14d74daa7f1b2027f333a415cb1ebd8e9d80d55af1765677787acab605bf52ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4797b5b482c04e0e7b7407f3d080d3be2efc616346a1f87467f4df5bfee80c`

```dockerfile
```

-	Layers:
	-	`sha256:c2fa99cc07e2b2541d04a7d8038ce019ea421d9c0e0ce8c4e0d413dd1abf00fd`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 4.0 MB (3985509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457584590002f8713dced8b62d3732fd99ec64fffad173f73d3dd1f5800be2b0`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:c7c88d57fd28e04ac3ba4873493b00b1ced2cba639b36177a63dc37c99beca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114524080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc0dd184cb687124574b5e33cce18557387ff2b74943a9829241b5adc408539`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 22:11:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 22:11:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:11:56 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 22:11:56 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Wed, 15 Apr 2026 22:11:56 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 22:12:00 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 22:12:00 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 22:12:00 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 22:12:00 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 22:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 22:12:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:12:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:12:00 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98330033bf657ef38c4def539642b9558b298a9b15192b97392d09c1639d97`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 16.1 MB (16075224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936158611fedc7b5b979e813ae30ae867716cacdd0feae8ce49cfe3f8180eca5`  
		Last Modified: Wed, 15 Apr 2026 20:34:26 GMT  
		Size: 46.9 MB (46922027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db291c6cfd32c40bdd43b4647fbce29caf2d1115fd8c41859c06cbd8c3f3bd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e8b1b8a651c9f479d408d0b0d092c2b17d3f06923781ee09a0704899f0686`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0218ea9a27847c898c805d7e7c7fa85faf7334450d11ca9525559be91595d304`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c98375e424e65476743a816606f9270eb94aa50f105f09fe961678098247d5`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 1.1 MB (1073695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ec46bd5475c47364454444b10c5f23793a1e2b122fed2176154737aeee2d8`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 22.8 MB (22841551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a928c4252683c4240d0b5b18fc9d99afa856a48c0472571b013618ede75c474`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7fcc0b7086789c0797ad8a31cfab4982269034f5d4c50ff2c182ed6e465554a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f58334a441fa88020960af088f397007b1e2987bc0376095394858ccb1b789`

```dockerfile
```

-	Layers:
	-	`sha256:1ecc5caf1bbb05a8b1d167e2ab7281dc5bc8c95b575aba25a1c5d765be7b6cd7`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 4.0 MB (3985203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ac535077ee83b008d2ae66f822834641a91cf2e029dfd01e52da60fac1d5be4`  
		Last Modified: Wed, 15 Apr 2026 22:12:11 GMT  
		Size: 24.7 KB (24722 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:83eaea1cbaa61e8a0a2e7df9484fbce491e29cfcecfc3b720ef665225cc7c7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123540045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c1b4a8352a46ada62a6869534a7de7be6c909a9560168fd877129e9d7b97d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 21:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:19:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 02:26:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 02:26:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Thu, 16 Apr 2026 02:26:17 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 02:26:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 02:26:25 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 02:26:25 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 02:26:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 02:26:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:25 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1be39ccce666bd30c5be03c8d81050c9ca7700ec279467e4c63973a13926f3`  
		Last Modified: Wed, 15 Apr 2026 21:20:27 GMT  
		Size: 47.3 MB (47331380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69109c2036e1b5cc92e8265d9d08ba987b3e05b754d1122c09349c8585b8498`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67097945e74c5c06dbc1104e2850f6e16a79862c4a8f6dfd35c9a76f82e5ed93`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b253b33e4ddb53fd66bccd92f5695f7f86fe517dac3869afaf462122a2df2`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be4341530f5750c21db1358fb8f3eafd8c7fb9c1168b3f7f20a32e576cee5b4`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 1.1 MB (1090094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf2644f46e37ca9a34d97d0ab850ae62847c566ff10236343b30012a8035fa9`  
		Last Modified: Thu, 16 Apr 2026 02:26:48 GMT  
		Size: 22.8 MB (22841591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e2f535b7a28cdc24d50f1ab47011840e037ee4b973e956c215ab0fbdec3914`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7b7a9fb4fe12aa5d4a221e6fdc0f99485e861361e64d708290929e8a2bc5465d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a5458ee572ef1327adc370f75c0476be1dace3186c3abc6b346a36c6c799b3`

```dockerfile
```

-	Layers:
	-	`sha256:6ab573aba859d148274c5319af69429e273641ad8199d460c5a4bc9d1d33c054`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 4.0 MB (3989618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6173b096db84dd8667b9170905c40112e06375c2394a7305c867c5403abd1e81`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:12c47b955d41a4a717423e4b0421cab72a8b915ce9eeac0a42d198f05af931ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112716241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979915f02fc2e25f99492cd1f7289c540d4b6c9a2e9c325181ff4925d689ed70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 00:33:24 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 00:33:24 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 00:33:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 00:33:28 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 00:33:28 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Thu, 16 Apr 2026 00:33:28 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 00:33:31 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 00:33:31 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 00:33:31 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 00:33:31 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 00:33:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 00:33:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 00:33:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:33:31 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd7f09d29853aeb978fa00c6a174063d2db0ceaef7ccc882bb2c9860c7f11c`  
		Last Modified: Wed, 15 Apr 2026 20:45:05 GMT  
		Size: 16.2 MB (16150512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51bc10b538bf35e7f17be627dc7d61e6e37baeff43c2f218814cc0c3d1ca3d`  
		Last Modified: Wed, 15 Apr 2026 20:45:48 GMT  
		Size: 44.4 MB (44409749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c359110d1bcbaa06c849c55581bb7a8236f6488fad8fa7cc3c2670108cb1c`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82cf8d2de7f90f113d0d7ee205b7e94eb4802062569f557ee778aacdc2e8069`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60374274574ecccf54877ac2826243aecae6c4a640bbf0f66d2ba85ea8c58d9e`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a6fbab791518f22e56a8a735f3c65926a2933886a3a4d6d8888b8b9c0f029`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 1.1 MB (1107064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a507bde4a7e395f695d0513a46896eafc7696e31735eb06b630eb7c62da5280d`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 22.8 MB (22841575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49d351b3ca9f641ee349e0798c36f1e261e421769125ffbb2fc8a562fad1589`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:cc5e9e37969f71efcb76e2f849cb20eae8c699889a0db884ce6da00caf856c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc518c9a5593ea7f019bbcb5a1e5d2dca4b4b1c45f9154374739a4a47f92f2a`

```dockerfile
```

-	Layers:
	-	`sha256:4db664b197a59d70df91738154ddaa50d989786f7a3b66c3bf3cb6eb0a6e8522`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 4.0 MB (3987099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb3148f66996e8197b78f81007a48c67095f9c5275989351768ab69a9ccec21`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9.5`

```console
$ docker pull zookeeper@sha256:0598e33ed585128313125f9c36cce6c164f0f21224e4bb75ca5c30b34655a13e
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

### `zookeeper:3.9.5` - linux; amd64

```console
$ docker pull zookeeper@sha256:c8eb8e81f40b52a790b03ff5012dadd0ea2254bb94d45056dff2299b96d620f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117313378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b6567a57b971f5eede1d9ea752c7c25ba50128405c0cf77cde1a329afbc159`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:38 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 21:59:38 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 21:59:46 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Wed, 15 Apr 2026 21:59:46 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 21:59:50 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 21:59:50 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 21:59:50 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 21:59:50 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 21:59:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 21:59:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:59:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:50 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f3568ba76ea6d97e9c2c393f0a402371cba409856a0ef86d9bf4821182a7d7`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 47.4 MB (47434807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b777945cb531796e3b41d7173704f3fdc2d7011ca46c9a27a4237eb04af664`  
		Last Modified: Wed, 15 Apr 2026 20:33:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007562ed65e8aa941dbb159078fc35e51f2378385997d673ff39b4d6b6d0c97`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87a276eede96b082c7728d745f0a25d0f246458eaa1d419411fb048403f247`  
		Last Modified: Wed, 15 Apr 2026 22:00:00 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8758592b33ad5f822bf7c9d3db4151dca19abc9d62b236bee7a00af1f997e134`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 1.1 MB (1144597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e5f47f2313da96413d86c72226f81aca7142af02c29b83c25b5f623c61b271`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 22.8 MB (22841573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cd26cd0a20cd3d9333cae4599d1ecedfd7953b55d07a60bf38e6bcaca71aed`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.5` - unknown; unknown

```console
$ docker pull zookeeper@sha256:14d74daa7f1b2027f333a415cb1ebd8e9d80d55af1765677787acab605bf52ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4797b5b482c04e0e7b7407f3d080d3be2efc616346a1f87467f4df5bfee80c`

```dockerfile
```

-	Layers:
	-	`sha256:c2fa99cc07e2b2541d04a7d8038ce019ea421d9c0e0ce8c4e0d413dd1abf00fd`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 4.0 MB (3985509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457584590002f8713dced8b62d3732fd99ec64fffad173f73d3dd1f5800be2b0`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.5` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:c7c88d57fd28e04ac3ba4873493b00b1ced2cba639b36177a63dc37c99beca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114524080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc0dd184cb687124574b5e33cce18557387ff2b74943a9829241b5adc408539`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 22:11:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 22:11:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:11:56 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 22:11:56 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Wed, 15 Apr 2026 22:11:56 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 22:12:00 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 22:12:00 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 22:12:00 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 22:12:00 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 22:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 22:12:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:12:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:12:00 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98330033bf657ef38c4def539642b9558b298a9b15192b97392d09c1639d97`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 16.1 MB (16075224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936158611fedc7b5b979e813ae30ae867716cacdd0feae8ce49cfe3f8180eca5`  
		Last Modified: Wed, 15 Apr 2026 20:34:26 GMT  
		Size: 46.9 MB (46922027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db291c6cfd32c40bdd43b4647fbce29caf2d1115fd8c41859c06cbd8c3f3bd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e8b1b8a651c9f479d408d0b0d092c2b17d3f06923781ee09a0704899f0686`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0218ea9a27847c898c805d7e7c7fa85faf7334450d11ca9525559be91595d304`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c98375e424e65476743a816606f9270eb94aa50f105f09fe961678098247d5`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 1.1 MB (1073695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ec46bd5475c47364454444b10c5f23793a1e2b122fed2176154737aeee2d8`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 22.8 MB (22841551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a928c4252683c4240d0b5b18fc9d99afa856a48c0472571b013618ede75c474`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.5` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7fcc0b7086789c0797ad8a31cfab4982269034f5d4c50ff2c182ed6e465554a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f58334a441fa88020960af088f397007b1e2987bc0376095394858ccb1b789`

```dockerfile
```

-	Layers:
	-	`sha256:1ecc5caf1bbb05a8b1d167e2ab7281dc5bc8c95b575aba25a1c5d765be7b6cd7`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 4.0 MB (3985203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ac535077ee83b008d2ae66f822834641a91cf2e029dfd01e52da60fac1d5be4`  
		Last Modified: Wed, 15 Apr 2026 22:12:11 GMT  
		Size: 24.7 KB (24722 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.5` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:83eaea1cbaa61e8a0a2e7df9484fbce491e29cfcecfc3b720ef665225cc7c7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123540045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c1b4a8352a46ada62a6869534a7de7be6c909a9560168fd877129e9d7b97d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 21:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:19:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 02:26:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 02:26:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Thu, 16 Apr 2026 02:26:17 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 02:26:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 02:26:25 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 02:26:25 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 02:26:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 02:26:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:25 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1be39ccce666bd30c5be03c8d81050c9ca7700ec279467e4c63973a13926f3`  
		Last Modified: Wed, 15 Apr 2026 21:20:27 GMT  
		Size: 47.3 MB (47331380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69109c2036e1b5cc92e8265d9d08ba987b3e05b754d1122c09349c8585b8498`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67097945e74c5c06dbc1104e2850f6e16a79862c4a8f6dfd35c9a76f82e5ed93`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b253b33e4ddb53fd66bccd92f5695f7f86fe517dac3869afaf462122a2df2`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be4341530f5750c21db1358fb8f3eafd8c7fb9c1168b3f7f20a32e576cee5b4`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 1.1 MB (1090094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf2644f46e37ca9a34d97d0ab850ae62847c566ff10236343b30012a8035fa9`  
		Last Modified: Thu, 16 Apr 2026 02:26:48 GMT  
		Size: 22.8 MB (22841591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e2f535b7a28cdc24d50f1ab47011840e037ee4b973e956c215ab0fbdec3914`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.5` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7b7a9fb4fe12aa5d4a221e6fdc0f99485e861361e64d708290929e8a2bc5465d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a5458ee572ef1327adc370f75c0476be1dace3186c3abc6b346a36c6c799b3`

```dockerfile
```

-	Layers:
	-	`sha256:6ab573aba859d148274c5319af69429e273641ad8199d460c5a4bc9d1d33c054`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 4.0 MB (3989618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6173b096db84dd8667b9170905c40112e06375c2394a7305c867c5403abd1e81`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.5` - linux; s390x

```console
$ docker pull zookeeper@sha256:12c47b955d41a4a717423e4b0421cab72a8b915ce9eeac0a42d198f05af931ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112716241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979915f02fc2e25f99492cd1f7289c540d4b6c9a2e9c325181ff4925d689ed70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 00:33:24 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 00:33:24 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 00:33:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 00:33:28 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 00:33:28 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Thu, 16 Apr 2026 00:33:28 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 00:33:31 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 00:33:31 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 00:33:31 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 00:33:31 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 00:33:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 00:33:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 00:33:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:33:31 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd7f09d29853aeb978fa00c6a174063d2db0ceaef7ccc882bb2c9860c7f11c`  
		Last Modified: Wed, 15 Apr 2026 20:45:05 GMT  
		Size: 16.2 MB (16150512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51bc10b538bf35e7f17be627dc7d61e6e37baeff43c2f218814cc0c3d1ca3d`  
		Last Modified: Wed, 15 Apr 2026 20:45:48 GMT  
		Size: 44.4 MB (44409749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c359110d1bcbaa06c849c55581bb7a8236f6488fad8fa7cc3c2670108cb1c`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82cf8d2de7f90f113d0d7ee205b7e94eb4802062569f557ee778aacdc2e8069`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60374274574ecccf54877ac2826243aecae6c4a640bbf0f66d2ba85ea8c58d9e`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a6fbab791518f22e56a8a735f3c65926a2933886a3a4d6d8888b8b9c0f029`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 1.1 MB (1107064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a507bde4a7e395f695d0513a46896eafc7696e31735eb06b630eb7c62da5280d`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 22.8 MB (22841575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49d351b3ca9f641ee349e0798c36f1e261e421769125ffbb2fc8a562fad1589`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.5` - unknown; unknown

```console
$ docker pull zookeeper@sha256:cc5e9e37969f71efcb76e2f849cb20eae8c699889a0db884ce6da00caf856c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc518c9a5593ea7f019bbcb5a1e5d2dca4b4b1c45f9154374739a4a47f92f2a`

```dockerfile
```

-	Layers:
	-	`sha256:4db664b197a59d70df91738154ddaa50d989786f7a3b66c3bf3cb6eb0a6e8522`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 4.0 MB (3987099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb3148f66996e8197b78f81007a48c67095f9c5275989351768ab69a9ccec21`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9.5-jre-17`

```console
$ docker pull zookeeper@sha256:0598e33ed585128313125f9c36cce6c164f0f21224e4bb75ca5c30b34655a13e
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

### `zookeeper:3.9.5-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:c8eb8e81f40b52a790b03ff5012dadd0ea2254bb94d45056dff2299b96d620f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117313378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b6567a57b971f5eede1d9ea752c7c25ba50128405c0cf77cde1a329afbc159`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:38 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 21:59:38 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 21:59:46 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Wed, 15 Apr 2026 21:59:46 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 21:59:50 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 21:59:50 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 21:59:50 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 21:59:50 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 21:59:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 21:59:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:59:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:50 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f3568ba76ea6d97e9c2c393f0a402371cba409856a0ef86d9bf4821182a7d7`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 47.4 MB (47434807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b777945cb531796e3b41d7173704f3fdc2d7011ca46c9a27a4237eb04af664`  
		Last Modified: Wed, 15 Apr 2026 20:33:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007562ed65e8aa941dbb159078fc35e51f2378385997d673ff39b4d6b6d0c97`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87a276eede96b082c7728d745f0a25d0f246458eaa1d419411fb048403f247`  
		Last Modified: Wed, 15 Apr 2026 22:00:00 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8758592b33ad5f822bf7c9d3db4151dca19abc9d62b236bee7a00af1f997e134`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 1.1 MB (1144597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e5f47f2313da96413d86c72226f81aca7142af02c29b83c25b5f623c61b271`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 22.8 MB (22841573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cd26cd0a20cd3d9333cae4599d1ecedfd7953b55d07a60bf38e6bcaca71aed`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.5-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:14d74daa7f1b2027f333a415cb1ebd8e9d80d55af1765677787acab605bf52ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4797b5b482c04e0e7b7407f3d080d3be2efc616346a1f87467f4df5bfee80c`

```dockerfile
```

-	Layers:
	-	`sha256:c2fa99cc07e2b2541d04a7d8038ce019ea421d9c0e0ce8c4e0d413dd1abf00fd`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 4.0 MB (3985509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457584590002f8713dced8b62d3732fd99ec64fffad173f73d3dd1f5800be2b0`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.5-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:c7c88d57fd28e04ac3ba4873493b00b1ced2cba639b36177a63dc37c99beca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114524080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc0dd184cb687124574b5e33cce18557387ff2b74943a9829241b5adc408539`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 22:11:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 22:11:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:11:56 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 22:11:56 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Wed, 15 Apr 2026 22:11:56 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 22:12:00 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 22:12:00 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 22:12:00 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 22:12:00 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 22:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 22:12:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:12:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:12:00 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98330033bf657ef38c4def539642b9558b298a9b15192b97392d09c1639d97`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 16.1 MB (16075224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936158611fedc7b5b979e813ae30ae867716cacdd0feae8ce49cfe3f8180eca5`  
		Last Modified: Wed, 15 Apr 2026 20:34:26 GMT  
		Size: 46.9 MB (46922027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db291c6cfd32c40bdd43b4647fbce29caf2d1115fd8c41859c06cbd8c3f3bd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e8b1b8a651c9f479d408d0b0d092c2b17d3f06923781ee09a0704899f0686`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0218ea9a27847c898c805d7e7c7fa85faf7334450d11ca9525559be91595d304`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c98375e424e65476743a816606f9270eb94aa50f105f09fe961678098247d5`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 1.1 MB (1073695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ec46bd5475c47364454444b10c5f23793a1e2b122fed2176154737aeee2d8`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 22.8 MB (22841551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a928c4252683c4240d0b5b18fc9d99afa856a48c0472571b013618ede75c474`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.5-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7fcc0b7086789c0797ad8a31cfab4982269034f5d4c50ff2c182ed6e465554a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f58334a441fa88020960af088f397007b1e2987bc0376095394858ccb1b789`

```dockerfile
```

-	Layers:
	-	`sha256:1ecc5caf1bbb05a8b1d167e2ab7281dc5bc8c95b575aba25a1c5d765be7b6cd7`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 4.0 MB (3985203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ac535077ee83b008d2ae66f822834641a91cf2e029dfd01e52da60fac1d5be4`  
		Last Modified: Wed, 15 Apr 2026 22:12:11 GMT  
		Size: 24.7 KB (24722 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.5-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:83eaea1cbaa61e8a0a2e7df9484fbce491e29cfcecfc3b720ef665225cc7c7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123540045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c1b4a8352a46ada62a6869534a7de7be6c909a9560168fd877129e9d7b97d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 21:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:19:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 02:26:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 02:26:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Thu, 16 Apr 2026 02:26:17 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 02:26:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 02:26:25 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 02:26:25 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 02:26:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 02:26:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:25 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1be39ccce666bd30c5be03c8d81050c9ca7700ec279467e4c63973a13926f3`  
		Last Modified: Wed, 15 Apr 2026 21:20:27 GMT  
		Size: 47.3 MB (47331380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69109c2036e1b5cc92e8265d9d08ba987b3e05b754d1122c09349c8585b8498`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67097945e74c5c06dbc1104e2850f6e16a79862c4a8f6dfd35c9a76f82e5ed93`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b253b33e4ddb53fd66bccd92f5695f7f86fe517dac3869afaf462122a2df2`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be4341530f5750c21db1358fb8f3eafd8c7fb9c1168b3f7f20a32e576cee5b4`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 1.1 MB (1090094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf2644f46e37ca9a34d97d0ab850ae62847c566ff10236343b30012a8035fa9`  
		Last Modified: Thu, 16 Apr 2026 02:26:48 GMT  
		Size: 22.8 MB (22841591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e2f535b7a28cdc24d50f1ab47011840e037ee4b973e956c215ab0fbdec3914`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.5-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7b7a9fb4fe12aa5d4a221e6fdc0f99485e861361e64d708290929e8a2bc5465d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a5458ee572ef1327adc370f75c0476be1dace3186c3abc6b346a36c6c799b3`

```dockerfile
```

-	Layers:
	-	`sha256:6ab573aba859d148274c5319af69429e273641ad8199d460c5a4bc9d1d33c054`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 4.0 MB (3989618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6173b096db84dd8667b9170905c40112e06375c2394a7305c867c5403abd1e81`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.5-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:12c47b955d41a4a717423e4b0421cab72a8b915ce9eeac0a42d198f05af931ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112716241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979915f02fc2e25f99492cd1f7289c540d4b6c9a2e9c325181ff4925d689ed70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 00:33:24 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 00:33:24 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 00:33:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 00:33:28 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 00:33:28 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Thu, 16 Apr 2026 00:33:28 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 00:33:31 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 00:33:31 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 00:33:31 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 00:33:31 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 00:33:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 00:33:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 00:33:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:33:31 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd7f09d29853aeb978fa00c6a174063d2db0ceaef7ccc882bb2c9860c7f11c`  
		Last Modified: Wed, 15 Apr 2026 20:45:05 GMT  
		Size: 16.2 MB (16150512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51bc10b538bf35e7f17be627dc7d61e6e37baeff43c2f218814cc0c3d1ca3d`  
		Last Modified: Wed, 15 Apr 2026 20:45:48 GMT  
		Size: 44.4 MB (44409749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c359110d1bcbaa06c849c55581bb7a8236f6488fad8fa7cc3c2670108cb1c`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82cf8d2de7f90f113d0d7ee205b7e94eb4802062569f557ee778aacdc2e8069`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60374274574ecccf54877ac2826243aecae6c4a640bbf0f66d2ba85ea8c58d9e`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a6fbab791518f22e56a8a735f3c65926a2933886a3a4d6d8888b8b9c0f029`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 1.1 MB (1107064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a507bde4a7e395f695d0513a46896eafc7696e31735eb06b630eb7c62da5280d`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 22.8 MB (22841575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49d351b3ca9f641ee349e0798c36f1e261e421769125ffbb2fc8a562fad1589`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.5-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:cc5e9e37969f71efcb76e2f849cb20eae8c699889a0db884ce6da00caf856c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc518c9a5593ea7f019bbcb5a1e5d2dca4b4b1c45f9154374739a4a47f92f2a`

```dockerfile
```

-	Layers:
	-	`sha256:4db664b197a59d70df91738154ddaa50d989786f7a3b66c3bf3cb6eb0a6e8522`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 4.0 MB (3987099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb3148f66996e8197b78f81007a48c67095f9c5275989351768ab69a9ccec21`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:0598e33ed585128313125f9c36cce6c164f0f21224e4bb75ca5c30b34655a13e
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
$ docker pull zookeeper@sha256:c8eb8e81f40b52a790b03ff5012dadd0ea2254bb94d45056dff2299b96d620f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117313378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b6567a57b971f5eede1d9ea752c7c25ba50128405c0cf77cde1a329afbc159`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:13 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:38 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 21:59:38 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 21:59:46 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Wed, 15 Apr 2026 21:59:46 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 21:59:50 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 21:59:50 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 21:59:50 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 21:59:50 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 21:59:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 21:59:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:59:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:59:50 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8f7509ae1b30e54ce560974758f550dcf122f90197a5ef95486959a756060`  
		Last Modified: Wed, 15 Apr 2026 20:33:36 GMT  
		Size: 16.2 MB (16150856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f3568ba76ea6d97e9c2c393f0a402371cba409856a0ef86d9bf4821182a7d7`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 47.4 MB (47434807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b777945cb531796e3b41d7173704f3fdc2d7011ca46c9a27a4237eb04af664`  
		Last Modified: Wed, 15 Apr 2026 20:33:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007562ed65e8aa941dbb159078fc35e51f2378385997d673ff39b4d6b6d0c97`  
		Last Modified: Wed, 15 Apr 2026 20:34:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87a276eede96b082c7728d745f0a25d0f246458eaa1d419411fb048403f247`  
		Last Modified: Wed, 15 Apr 2026 22:00:00 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8758592b33ad5f822bf7c9d3db4151dca19abc9d62b236bee7a00af1f997e134`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 1.1 MB (1144597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e5f47f2313da96413d86c72226f81aca7142af02c29b83c25b5f623c61b271`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 22.8 MB (22841573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cd26cd0a20cd3d9333cae4599d1ecedfd7953b55d07a60bf38e6bcaca71aed`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:14d74daa7f1b2027f333a415cb1ebd8e9d80d55af1765677787acab605bf52ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4797b5b482c04e0e7b7407f3d080d3be2efc616346a1f87467f4df5bfee80c`

```dockerfile
```

-	Layers:
	-	`sha256:c2fa99cc07e2b2541d04a7d8038ce019ea421d9c0e0ce8c4e0d413dd1abf00fd`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 4.0 MB (3985509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457584590002f8713dced8b62d3732fd99ec64fffad173f73d3dd1f5800be2b0`  
		Last Modified: Wed, 15 Apr 2026 22:00:01 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:c7c88d57fd28e04ac3ba4873493b00b1ced2cba639b36177a63dc37c99beca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114524080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc0dd184cb687124574b5e33cce18557387ff2b74943a9829241b5adc408539`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:47 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 15 Apr 2026 22:11:47 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 15 Apr 2026 22:11:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:11:56 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 15 Apr 2026 22:11:56 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Wed, 15 Apr 2026 22:11:56 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 22:12:00 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 15 Apr 2026 22:12:00 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Wed, 15 Apr 2026 22:12:00 GMT
VOLUME [/data /datalog /logs]
# Wed, 15 Apr 2026 22:12:00 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 15 Apr 2026 22:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Wed, 15 Apr 2026 22:12:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:12:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:12:00 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98330033bf657ef38c4def539642b9558b298a9b15192b97392d09c1639d97`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 16.1 MB (16075224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936158611fedc7b5b979e813ae30ae867716cacdd0feae8ce49cfe3f8180eca5`  
		Last Modified: Wed, 15 Apr 2026 20:34:26 GMT  
		Size: 46.9 MB (46922027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db291c6cfd32c40bdd43b4647fbce29caf2d1115fd8c41859c06cbd8c3f3bd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e8b1b8a651c9f479d408d0b0d092c2b17d3f06923781ee09a0704899f0686`  
		Last Modified: Wed, 15 Apr 2026 20:34:24 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0218ea9a27847c898c805d7e7c7fa85faf7334450d11ca9525559be91595d304`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c98375e424e65476743a816606f9270eb94aa50f105f09fe961678098247d5`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 1.1 MB (1073695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ec46bd5475c47364454444b10c5f23793a1e2b122fed2176154737aeee2d8`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 22.8 MB (22841551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a928c4252683c4240d0b5b18fc9d99afa856a48c0472571b013618ede75c474`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7fcc0b7086789c0797ad8a31cfab4982269034f5d4c50ff2c182ed6e465554a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f58334a441fa88020960af088f397007b1e2987bc0376095394858ccb1b789`

```dockerfile
```

-	Layers:
	-	`sha256:1ecc5caf1bbb05a8b1d167e2ab7281dc5bc8c95b575aba25a1c5d765be7b6cd7`  
		Last Modified: Wed, 15 Apr 2026 22:12:12 GMT  
		Size: 4.0 MB (3985203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ac535077ee83b008d2ae66f822834641a91cf2e029dfd01e52da60fac1d5be4`  
		Last Modified: Wed, 15 Apr 2026 22:12:11 GMT  
		Size: 24.7 KB (24722 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:83eaea1cbaa61e8a0a2e7df9484fbce491e29cfcecfc3b720ef665225cc7c7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123540045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c1b4a8352a46ada62a6869534a7de7be6c909a9560168fd877129e9d7b97d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 21:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:19:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:19:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 02:26:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 02:26:17 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 02:26:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Thu, 16 Apr 2026 02:26:17 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 02:26:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 02:26:25 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 02:26:25 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 02:26:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 02:26:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 02:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 02:26:25 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1be39ccce666bd30c5be03c8d81050c9ca7700ec279467e4c63973a13926f3`  
		Last Modified: Wed, 15 Apr 2026 21:20:27 GMT  
		Size: 47.3 MB (47331380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69109c2036e1b5cc92e8265d9d08ba987b3e05b754d1122c09349c8585b8498`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67097945e74c5c06dbc1104e2850f6e16a79862c4a8f6dfd35c9a76f82e5ed93`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b253b33e4ddb53fd66bccd92f5695f7f86fe517dac3869afaf462122a2df2`  
		Last Modified: Thu, 16 Apr 2026 02:26:46 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be4341530f5750c21db1358fb8f3eafd8c7fb9c1168b3f7f20a32e576cee5b4`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 1.1 MB (1090094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf2644f46e37ca9a34d97d0ab850ae62847c566ff10236343b30012a8035fa9`  
		Last Modified: Thu, 16 Apr 2026 02:26:48 GMT  
		Size: 22.8 MB (22841591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e2f535b7a28cdc24d50f1ab47011840e037ee4b973e956c215ab0fbdec3914`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7b7a9fb4fe12aa5d4a221e6fdc0f99485e861361e64d708290929e8a2bc5465d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a5458ee572ef1327adc370f75c0476be1dace3186c3abc6b346a36c6c799b3`

```dockerfile
```

-	Layers:
	-	`sha256:6ab573aba859d148274c5319af69429e273641ad8199d460c5a4bc9d1d33c054`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 4.0 MB (3989618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6173b096db84dd8667b9170905c40112e06375c2394a7305c867c5403abd1e81`  
		Last Modified: Thu, 16 Apr 2026 02:26:47 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; s390x

```console
$ docker pull zookeeper@sha256:12c47b955d41a4a717423e4b0421cab72a8b915ce9eeac0a42d198f05af931ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112716241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979915f02fc2e25f99492cd1f7289c540d4b6c9a2e9c325181ff4925d689ed70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:44 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 00:33:24 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 16 Apr 2026 00:33:24 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 16 Apr 2026 00:33:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 16 Apr 2026 00:33:28 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 16 Apr 2026 00:33:28 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Thu, 16 Apr 2026 00:33:28 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 00:33:31 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 16 Apr 2026 00:33:31 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Thu, 16 Apr 2026 00:33:31 GMT
VOLUME [/data /datalog /logs]
# Thu, 16 Apr 2026 00:33:31 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 16 Apr 2026 00:33:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Thu, 16 Apr 2026 00:33:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 00:33:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:33:31 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd7f09d29853aeb978fa00c6a174063d2db0ceaef7ccc882bb2c9860c7f11c`  
		Last Modified: Wed, 15 Apr 2026 20:45:05 GMT  
		Size: 16.2 MB (16150512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51bc10b538bf35e7f17be627dc7d61e6e37baeff43c2f218814cc0c3d1ca3d`  
		Last Modified: Wed, 15 Apr 2026 20:45:48 GMT  
		Size: 44.4 MB (44409749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c359110d1bcbaa06c849c55581bb7a8236f6488fad8fa7cc3c2670108cb1c`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82cf8d2de7f90f113d0d7ee205b7e94eb4802062569f557ee778aacdc2e8069`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60374274574ecccf54877ac2826243aecae6c4a640bbf0f66d2ba85ea8c58d9e`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a6fbab791518f22e56a8a735f3c65926a2933886a3a4d6d8888b8b9c0f029`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 1.1 MB (1107064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a507bde4a7e395f695d0513a46896eafc7696e31735eb06b630eb7c62da5280d`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 22.8 MB (22841575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49d351b3ca9f641ee349e0798c36f1e261e421769125ffbb2fc8a562fad1589`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:cc5e9e37969f71efcb76e2f849cb20eae8c699889a0db884ce6da00caf856c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc518c9a5593ea7f019bbcb5a1e5d2dca4b4b1c45f9154374739a4a47f92f2a`

```dockerfile
```

-	Layers:
	-	`sha256:4db664b197a59d70df91738154ddaa50d989786f7a3b66c3bf3cb6eb0a6e8522`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 4.0 MB (3987099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deb3148f66996e8197b78f81007a48c67095f9c5275989351768ab69a9ccec21`  
		Last Modified: Thu, 16 Apr 2026 00:33:45 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json
