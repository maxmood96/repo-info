## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:fc17a45b74b4330fe2a02c1f0f1790696cc097695a967a32a203875814d44c17
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
$ docker pull zookeeper@sha256:a7ae4b813af9fd4d8724d426533caf62d7dd07941db9b464e6c22666111a3912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117113742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ff1dee87efc0ff8b4e39b66bc991af57703e5079d6fd8ee2ae4a8a35480a3d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:22:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:22:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:22:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:22:57 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Mar 2026 01:23:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:23:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:23:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:23:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:02 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Tue, 17 Mar 2026 02:55:02 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Tue, 17 Mar 2026 02:55:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:55:10 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Tue, 17 Mar 2026 02:55:10 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Tue, 17 Mar 2026 02:55:10 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Tue, 17 Mar 2026 02:55:14 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Tue, 17 Mar 2026 02:55:14 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Tue, 17 Mar 2026 02:55:14 GMT
VOLUME [/data /datalog /logs]
# Tue, 17 Mar 2026 02:55:14 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Tue, 17 Mar 2026 02:55:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Tue, 17 Mar 2026 02:55:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:55:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:55:14 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c560279ecc84545235e5cebad6aaf2aa6e27fc9fea2aa195c2da94486e9fbb5`  
		Last Modified: Tue, 17 Mar 2026 01:23:12 GMT  
		Size: 16.1 MB (16149326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8c11b487b051022d0f8ec435cd416f8f37a9aab106942fdb9c681a95a8ae56`  
		Last Modified: Tue, 17 Mar 2026 01:23:13 GMT  
		Size: 47.4 MB (47434776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c765fe3dad74deb6f0667017a0c70fbb5c396f434f177ec7abd91a4cd6d65829`  
		Last Modified: Tue, 17 Mar 2026 01:23:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d8a5e252c3ea2af7215da38a6d6fd08150cddaaea6c61d1c3b7b8fd423852b`  
		Last Modified: Tue, 17 Mar 2026 01:23:11 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7a0e0a8150876cfc60bca3f8919a660ad1fa59b406788e6d5704dff8e5251b`  
		Last Modified: Tue, 17 Mar 2026 02:55:25 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079854ace67a7de907cb92b768e0d254a7a24286e718ea843b139b5fa48cf2df`  
		Last Modified: Tue, 17 Mar 2026 02:55:25 GMT  
		Size: 1.1 MB (1144533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435b8af7c17950a4e27c9340fe5e74dd43285c41dd070e50fe8b6f5f1139250`  
		Last Modified: Tue, 17 Mar 2026 02:55:25 GMT  
		Size: 22.8 MB (22841547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55df36fe27c9eea7372143977b4624afd6a905044feae3681870f754e42682c7`  
		Last Modified: Tue, 17 Mar 2026 02:55:25 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:cd4cc86fa253e5a8e299548a48b8eed1cfb84526e171438eff93f8346c73a194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84c2d0eadb584626765d860f6e3ddd73893ae6f3b977dae86acf25b0d5ff088`

```dockerfile
```

-	Layers:
	-	`sha256:4b67cbfdc4ccf900159ee2f11e5f33f1b614b1c37ac755a377af68f6f640197a`  
		Last Modified: Tue, 17 Mar 2026 02:55:25 GMT  
		Size: 4.0 MB (3985509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37790c27d028dd6b791c12c15743b24d097d5173b886d40a8d6d21827b4aa690`  
		Last Modified: Tue, 17 Mar 2026 02:55:25 GMT  
		Size: 24.6 KB (24576 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:2f0ea623fe18f35659af82e9bd22f40eabc2e70100da8cab0e67a370dd03b650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114304773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898317cd1529b70dc74b5f01ad19a3b6f428a81dbbd01fe2387abdc25752b8d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:24:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:24:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:24:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:24:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:24:17 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Mar 2026 01:24:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:24:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:24:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:24:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Tue, 17 Mar 2026 02:59:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Tue, 17 Mar 2026 02:59:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:59:17 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Tue, 17 Mar 2026 02:59:17 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Tue, 17 Mar 2026 02:59:17 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Tue, 17 Mar 2026 02:59:21 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Tue, 17 Mar 2026 02:59:21 GMT
VOLUME [/data /datalog /logs]
# Tue, 17 Mar 2026 02:59:21 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Tue, 17 Mar 2026 02:59:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Tue, 17 Mar 2026 02:59:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:59:21 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962ff3a9e44a298002491adeb36eb584ccda2eae305116b890be005bdf028a32`  
		Last Modified: Tue, 17 Mar 2026 01:24:33 GMT  
		Size: 16.1 MB (16073508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf62962d30fa85f0a393ba2b88ed7030994f0dfde9bc76acf07fa1dce073d76b`  
		Last Modified: Tue, 17 Mar 2026 01:24:34 GMT  
		Size: 46.9 MB (46922068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6e05267fe05fe7df77eab3eb141f795abbf8d140204208e4033a35938d2e7e`  
		Last Modified: Tue, 17 Mar 2026 01:24:33 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df8a52c9bf0e659b5cec871191dfa0627d2e050ca28c43669e4d98d61cf0734`  
		Last Modified: Tue, 17 Mar 2026 01:24:33 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609b9ddb0a54885de7089d917869a4c5fd2f7d24d287391baab147db4557e7e6`  
		Last Modified: Tue, 17 Mar 2026 02:59:32 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b187b51e395381cb593dda9377f9804f52b616de6cb39859b91427c492dc8dcd`  
		Last Modified: Tue, 17 Mar 2026 02:59:32 GMT  
		Size: 1.1 MB (1073589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261aff12355ab4e032696f64b90623a1624c74713cce10301dfd26a76af3d0eb`  
		Last Modified: Tue, 17 Mar 2026 02:59:32 GMT  
		Size: 22.8 MB (22841541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8c50b31f1ce441e4ed203e782640f29a51002f2425042f352e8299067b988b`  
		Last Modified: Tue, 17 Mar 2026 02:59:32 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:ce628502b8109b2ef75dce4d4c4fb4404f7287e200caab11328caa8901a2d6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ad40580fb6e3f7bc33d81bd7af8a3032d03a8240d84df4ef95cae0880d8ec7`

```dockerfile
```

-	Layers:
	-	`sha256:e469bab38d61675b6fd5eee34acd1dc421642a88dc54a105a738394ede2bab3d`  
		Last Modified: Tue, 17 Mar 2026 02:59:32 GMT  
		Size: 4.0 MB (3985203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b728d7d141d6ed129d983c2d8a168f0d98592c1016728aa2ceacdb283eba1d3d`  
		Last Modified: Tue, 17 Mar 2026 02:59:32 GMT  
		Size: 24.7 KB (24723 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:3693f5d7a361fdc59ac55b9c05358a5a30489bfff7d94e9021f3a5b8572fc156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123343820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9141840bc39fb34a26872862efc53d9a0d80eba8238886437fc57ee41bc4d47c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:28:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 08:28:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:28:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:28:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:28:22 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Mar 2026 08:34:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 08:34:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 08:34:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 08:34:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 18:00:11 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Tue, 17 Mar 2026 18:00:11 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Tue, 17 Mar 2026 18:00:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:00:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Tue, 17 Mar 2026 18:00:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Tue, 17 Mar 2026 18:00:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Tue, 17 Mar 2026 18:01:27 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Tue, 17 Mar 2026 18:01:28 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Tue, 17 Mar 2026 18:01:28 GMT
VOLUME [/data /datalog /logs]
# Tue, 17 Mar 2026 18:01:28 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Tue, 17 Mar 2026 18:01:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Tue, 17 Mar 2026 18:01:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 18:01:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:01:28 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfccd4bd959ddb60fe973d79544b531c56c792667c929465975638cd29ad37`  
		Last Modified: Tue, 17 Mar 2026 08:28:58 GMT  
		Size: 17.6 MB (17622291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8134fae8753fed6c545cb387b4eaddde7465baab7cb082d8e58a7884ae07a6`  
		Last Modified: Tue, 17 Mar 2026 08:35:15 GMT  
		Size: 47.3 MB (47331392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a50798c3d3c71253b348d7cd1c587e5ee2f032f4701caab985320306411cb7`  
		Last Modified: Tue, 17 Mar 2026 08:35:13 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebc145cbf015b8221169c6ba862f2e438d8cb79bdce73991c34827260748695`  
		Last Modified: Tue, 17 Mar 2026 08:35:13 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c1c69e3f31830ad4177e43791aac0ff464f6e4854910c0d0185e1f9ab0719e`  
		Last Modified: Tue, 17 Mar 2026 18:00:53 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5955c202e6225da87ffee7566dd0a471e85fe55e39932c1889a340ca56c9d108`  
		Last Modified: Tue, 17 Mar 2026 18:00:53 GMT  
		Size: 1.1 MB (1090032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889c057934d8fa82bfb2fb32767d837362b79382b329c4eaef555724db3ed8a5`  
		Last Modified: Tue, 17 Mar 2026 18:01:48 GMT  
		Size: 22.8 MB (22841615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28a4b3d0810bfe72ecd3ea5c6374445e72909dd3034ee8d0ac72eefdfc4e265`  
		Last Modified: Tue, 17 Mar 2026 18:01:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:09b817801d0abe5b120cfa8f3ea347b8eca28c8e5e6eae9634c676f00d1e03e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf41203e537bb7b48750ad59876fcee3c19e48c236354de33cc30c69a01aecaf`

```dockerfile
```

-	Layers:
	-	`sha256:9480e07f96b27ddd949078de7d005ab846974417dd312bc1de957db5d55decbd`  
		Last Modified: Tue, 17 Mar 2026 18:01:48 GMT  
		Size: 4.0 MB (3989618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6c2db3ed48a46526b87a2d1a6893879dae90b6041b00998d8e34b3927f2f19`  
		Last Modified: Tue, 17 Mar 2026 18:01:47 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; s390x

```console
$ docker pull zookeeper@sha256:f0b549b36d0d4cc5950e6fb657785e9693dedd7179af83dfb2a4eef1819423df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112519820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23536cc0d775df16cce070740288d380a0320c19986d7c065d2047e90a7f7e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:19:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:19:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:19:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 02:19:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:51 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Mar 2026 02:21:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 02:21:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 02:21:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:21:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 11:18:48 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Tue, 17 Mar 2026 11:18:48 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Tue, 17 Mar 2026 11:19:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Tue, 17 Mar 2026 11:19:05 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Tue, 17 Mar 2026 11:19:05 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.5
# Tue, 17 Mar 2026 11:19:05 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.5-bin
# Tue, 17 Mar 2026 11:19:12 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.5 DISTRO_NAME=apache-zookeeper-3.9.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Tue, 17 Mar 2026 11:19:15 GMT
WORKDIR /apache-zookeeper-3.9.5-bin
# Tue, 17 Mar 2026 11:19:15 GMT
VOLUME [/data /datalog /logs]
# Tue, 17 Mar 2026 11:19:15 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Tue, 17 Mar 2026 11:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.5-bin/bin ZOOCFGDIR=/conf
# Tue, 17 Mar 2026 11:19:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 11:19:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 11:19:17 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88da8e1771e21f8f53e977dc8e3688ba1e8ee9215e482ff9901af82b8b916511`  
		Last Modified: Tue, 17 Mar 2026 02:20:20 GMT  
		Size: 16.1 MB (16149396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4099338edb7877b0f05f51c969e3bdcf969e9c5eefbf771c7a2329edfdd947`  
		Last Modified: Tue, 17 Mar 2026 02:22:11 GMT  
		Size: 44.4 MB (44409609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57452725a7fd2abf8a2db3c82673ca44723d9d9d35860586382473b9548915b`  
		Last Modified: Tue, 17 Mar 2026 02:22:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283bf769566a70f9548438d08b808ab456b95d37518ea67dc5b00a507b660f7a`  
		Last Modified: Tue, 17 Mar 2026 02:22:10 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf1ce6171610d3e6d7ea8d26f886736ba843a20b1c00d98107e140d70d175a6`  
		Last Modified: Tue, 17 Mar 2026 11:19:55 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693fe777eb3e3d3a9616d683501c73a6e4128f74a6d1b2cc5c904d5e8061f365`  
		Last Modified: Tue, 17 Mar 2026 11:19:55 GMT  
		Size: 1.1 MB (1107063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40501d5bdcc8320a5b89859620a6ebc9936cf04972d30b2285d08d2b85939e1`  
		Last Modified: Tue, 17 Mar 2026 11:19:57 GMT  
		Size: 22.8 MB (22841597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12c02bcccdb5b111110e4c6c6cebc0307173f108a7c6638211922fcb1328e6a`  
		Last Modified: Tue, 17 Mar 2026 11:19:55 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:3e2ac0567fbe2cb0be857e74bfd5aa5353358e5c5b01364eac331b7e8564523e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166395f4bdafbf55d59356e70840ebfc455831760d4c34ed71d306f137e5710d`

```dockerfile
```

-	Layers:
	-	`sha256:c93f5df39c5854ef897618045f081936e896809f2dc345bb9c1afb2a50cee21d`  
		Last Modified: Tue, 17 Mar 2026 11:19:56 GMT  
		Size: 4.0 MB (3987099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffeef32674fba1b0bebf2b5ead3abeb0feac077d146f747ab0db682575e08210`  
		Last Modified: Tue, 17 Mar 2026 11:19:54 GMT  
		Size: 24.6 KB (24576 bytes)  
		MIME: application/vnd.in-toto+json
