<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `zookeeper`

-	[`zookeeper:3.8`](#zookeeper38)
-	[`zookeeper:3.8-jre-17`](#zookeeper38-jre-17)
-	[`zookeeper:3.8.5`](#zookeeper385)
-	[`zookeeper:3.8.5-jre-17`](#zookeeper385-jre-17)
-	[`zookeeper:3.9`](#zookeeper39)
-	[`zookeeper:3.9-jre-17`](#zookeeper39-jre-17)
-	[`zookeeper:3.9.4`](#zookeeper394)
-	[`zookeeper:3.9.4-jre-17`](#zookeeper394-jre-17)
-	[`zookeeper:latest`](#zookeeperlatest)

## `zookeeper:3.8`

```console
$ docker pull zookeeper@sha256:e3c04fec791d18237539943460002db4e59b2e87b417c9bf91beb9a2ba0d4334
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
$ docker pull zookeeper@sha256:d0bba8360545dd0c49d0070814e4f22e14aa7171c31265d227bd5588ad424de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109220050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd16a532148796f87e6d1960f1b2e81184a5466f042ee70df319f3fb68a783a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 04 Feb 2026 18:05:09 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 04 Feb 2026 18:05:09 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 04 Feb 2026 18:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 04 Feb 2026 18:05:16 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 04 Feb 2026 18:05:16 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Wed, 04 Feb 2026 18:05:16 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:05:20 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:05:20 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:05:20 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:05:20 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:05:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:05:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:05:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:05:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770a7ccbf824857f9a328739d1ddfec21c04a1b7423007c0a74c8ab500e3675`  
		Last Modified: Thu, 15 Jan 2026 22:20:01 GMT  
		Size: 16.1 MB (16147435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5de6e8045fe0102a83fbca815f435fd81296a7937cdeb04409eeec845a3502`  
		Last Modified: Thu, 15 Jan 2026 22:20:02 GMT  
		Size: 47.1 MB (47055148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012e01f9d2afd797ecf20b406260375e0fe120b00a6401bba84a92fc3968f3`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4b65fc380fc87df9d7a19c5abf67e22e913f6f0b56b870b1ee5ca46f5cdf5`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1208c53df4b968be7689005aaef5970d46818e92381dd8514e46bc232a66b`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972eae95fec01d953f1186614dd684570c01a8640400ffd6e91092b97b8a6081`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 1.1 MB (1144566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73e905ef6db73a659708c2bf49312256a9c39ad9fcd4672b400f9123f79af38`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 15.3 MB (15331198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c551b1eb5135bcd7b81671012083f9451e20a4526ec7f285dc75f372ddd1189f`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:b2e767cf03a5bc9ff5ede937914bb75da1eb4a8fac6b1e89cc291c6b9c380ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf30c4b82b727fb746797a1b20be597c158068603487c3de6694c81a139f78a`

```dockerfile
```

-	Layers:
	-	`sha256:3eb9b554bdcc223f78ac9281cb7e2c8ee32d830216b9a56e55b595888351a815`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 4.0 MB (3959477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06849fc5948bdd2830966b24c01cfbd11b1808e4dfef909df6123ecd266d2d95`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 24.3 KB (24274 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:feae2755255c4bb50495288d7bd1ef60b30bd9433921b87cfc91379f39ef5495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493bbb891140fb02ba4409006abe80a487e2680e436769f0f70f9f59abd11bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:39:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:39:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:39:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:39:43 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Fri, 16 Jan 2026 01:39:43 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Fri, 16 Jan 2026 01:39:43 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Fri, 16 Jan 2026 01:39:50 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:39:50 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Fri, 16 Jan 2026 01:39:50 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:39:50 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:39:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:39:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:39:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:39:50 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fc3ef6de679ecac0a74cc044dd73825b9e6daa54ab0904bc8e9b9e898d5bdd`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 16.1 MB (16065656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d903927893f88ea36a0f1ae2165c1cbabff6244e11daf33512f44c12631acd`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 46.5 MB (46538233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05322d833bff6a327f4cb5734a53c8ecd0811c295b8d670e977218a9a12d8906`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef01e65ce9e940b87d06c11af62f1cff2016c991c02e0b659ac1826a2466cbd5`  
		Last Modified: Thu, 15 Jan 2026 22:19:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e55d5e30460f4201033cd053b375a4a5b41c0e14c869c633d75898a8e106739`  
		Last Modified: Fri, 16 Jan 2026 01:40:00 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6373485f2036be4e69c7974110adc3ab5db0e7569fdd583a9ecbb8cb5be70ee`  
		Last Modified: Fri, 16 Jan 2026 01:40:00 GMT  
		Size: 1.1 MB (1073575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6c6d21b9156536f02dfdc51bb1a129d27b909a1f7d5e698cb62b20a787dbf`  
		Last Modified: Fri, 16 Jan 2026 01:40:01 GMT  
		Size: 14.7 MB (14682888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2747fd3dab8cd3a4a817e229b92b2a893d51cadd08a7465fbd2e183e7a504c`  
		Last Modified: Fri, 16 Jan 2026 01:40:00 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:f4b9109f61acac87b56c50141156a3d49a556e027f4e34e4c709aa6ab32a307b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef225b8897b2dc03435d736d36d1f4ae3ff6bd8056a26d3a25431c59806d69`

```dockerfile
```

-	Layers:
	-	`sha256:21996cef7fa35014963fc7d89e1a5116da516e8a9d0f4767df25cecb2668672a`  
		Last Modified: Fri, 16 Jan 2026 01:40:00 GMT  
		Size: 4.0 MB (3959159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef9094f2cb0524edc8d9457376dc8a9bb5c5f8eb5710520382892634b5a8a443`  
		Last Modified: Fri, 16 Jan 2026 01:40:00 GMT  
		Size: 24.4 KB (24410 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:783ddfb6c6b7186027668105c7d32df535d5cbe559e868338724db9019a05b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115373818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff57b0b69ceca02b289ca298471de078fcbdeb20d0949f7d0b6075d1032e68b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 04 Feb 2026 18:04:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 04 Feb 2026 18:04:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 04 Feb 2026 18:04:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 04 Feb 2026 18:04:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 04 Feb 2026 18:04:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Wed, 04 Feb 2026 18:04:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:04:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:04:26 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:04:26 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:04:26 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:04:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:04:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:04:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:04:26 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:41 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ca264798509a08ea6ccee410a564b50a0eb5a42f1e58216b34a0c846751eb`  
		Last Modified: Thu, 15 Jan 2026 22:17:15 GMT  
		Size: 46.9 MB (46881201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae30e596f1d1d565a863521696c50833d9594367b6717a150b7660b7f6f7d9`  
		Last Modified: Thu, 15 Jan 2026 22:17:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a011aa1930859a4407f64ffbb4fddcba4751ca856311b708bf6236c1d809dea`  
		Last Modified: Thu, 15 Jan 2026 22:17:14 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65affe7af8d9e76c1b767be1d62eec504bbd7af88841a87c1f0341ec151720ae`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281a94a9388ae9d5318e9efe394b6b9d87ccac964d8992a061b7725f086766e7`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 1.1 MB (1090080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79c46142d7fe8cb5b5787b0573079692d51e9a5f331d602917e898411c66b57`  
		Last Modified: Wed, 04 Feb 2026 18:04:50 GMT  
		Size: 15.3 MB (15331337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f4d9d4e89ab14652ba4fcf1d9e056c4711729cdcffccf7555294ea4628cbdf`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:9278cb56863f59fbe0e3f7cfd504327d42b589749b90088eeefdcd17996af67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d302ab64b884257268c91f04e2da52801e1e0327ee4afb625f6ab37f122c1609`

```dockerfile
```

-	Layers:
	-	`sha256:a7d31bda6ad0bc3a005ba8a8130affc03d1cc0ae0dec3d357e49299834bfa06d`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 4.0 MB (3963580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5745aaa42a4794104ba4a1daffba0e3063e9d3fb7a70c19f5e60a5bad87b679`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 24.3 KB (24324 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8` - linux; s390x

```console
$ docker pull zookeeper@sha256:cd53368124fea9017409ce680e827dec6ebe45dfbb41df53fec8df31b08f617f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104623451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb27b0c8c8d868bf0dd41e9668c9444ec7189d730f0cae70791e268982cf6ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:49 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 15 Jan 2026 23:07:49 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 15 Jan 2026 23:07:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Thu, 15 Jan 2026 23:07:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:01:52 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:01:52 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:01:52 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:01:52 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:01:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:01:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:01:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:01:52 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:21 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23c205723170273b192d9e9d8b97c8f22f0d97ed549cebd30eb736b55476e21`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2059e56e4bc25d5f4b1c017b55a0664e3674869eed7702692d591c85c655688f`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.1 MB (1106856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47b40f9990641efdaf0c7415e83b92a28c5957539874044dcdd7c74d50cadc3`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 15.3 MB (15331334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30680f44e6339c9bf39f06e75083bb81b16132be4914f1893dd92c73ae91e3`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8cfa7e6ee11cee44e3b156218d3905a405ba292aefc1a276c271683d2b354457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15865c2c628c1fea46e9f6a5398e999272a166f9bc02c917e2673f5788037e`

```dockerfile
```

-	Layers:
	-	`sha256:24af95f386fe628438fd366e0cef16666786117c020711db4882a526b2acd92e`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 4.0 MB (3961067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c1b37381cf0acf4fee9cecc9a8c67b467e0d49a4f4867650534f8ce492739b`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 24.3 KB (24276 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8-jre-17`

```console
$ docker pull zookeeper@sha256:e3c04fec791d18237539943460002db4e59b2e87b417c9bf91beb9a2ba0d4334
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
$ docker pull zookeeper@sha256:d0bba8360545dd0c49d0070814e4f22e14aa7171c31265d227bd5588ad424de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109220050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd16a532148796f87e6d1960f1b2e81184a5466f042ee70df319f3fb68a783a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 04 Feb 2026 18:05:09 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 04 Feb 2026 18:05:09 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 04 Feb 2026 18:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 04 Feb 2026 18:05:16 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 04 Feb 2026 18:05:16 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Wed, 04 Feb 2026 18:05:16 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:05:20 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:05:20 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:05:20 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:05:20 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:05:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:05:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:05:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:05:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770a7ccbf824857f9a328739d1ddfec21c04a1b7423007c0a74c8ab500e3675`  
		Last Modified: Thu, 15 Jan 2026 22:20:01 GMT  
		Size: 16.1 MB (16147435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5de6e8045fe0102a83fbca815f435fd81296a7937cdeb04409eeec845a3502`  
		Last Modified: Thu, 15 Jan 2026 22:20:02 GMT  
		Size: 47.1 MB (47055148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012e01f9d2afd797ecf20b406260375e0fe120b00a6401bba84a92fc3968f3`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4b65fc380fc87df9d7a19c5abf67e22e913f6f0b56b870b1ee5ca46f5cdf5`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1208c53df4b968be7689005aaef5970d46818e92381dd8514e46bc232a66b`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972eae95fec01d953f1186614dd684570c01a8640400ffd6e91092b97b8a6081`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 1.1 MB (1144566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73e905ef6db73a659708c2bf49312256a9c39ad9fcd4672b400f9123f79af38`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 15.3 MB (15331198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c551b1eb5135bcd7b81671012083f9451e20a4526ec7f285dc75f372ddd1189f`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:b2e767cf03a5bc9ff5ede937914bb75da1eb4a8fac6b1e89cc291c6b9c380ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf30c4b82b727fb746797a1b20be597c158068603487c3de6694c81a139f78a`

```dockerfile
```

-	Layers:
	-	`sha256:3eb9b554bdcc223f78ac9281cb7e2c8ee32d830216b9a56e55b595888351a815`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 4.0 MB (3959477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06849fc5948bdd2830966b24c01cfbd11b1808e4dfef909df6123ecd266d2d95`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 24.3 KB (24274 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:feae2755255c4bb50495288d7bd1ef60b30bd9433921b87cfc91379f39ef5495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493bbb891140fb02ba4409006abe80a487e2680e436769f0f70f9f59abd11bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:39:36 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:39:36 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:39:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:39:43 GMT
ARG GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66
# Fri, 16 Jan 2026 01:39:43 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.4
# Fri, 16 Jan 2026 01:39:43 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.4-bin
# Fri, 16 Jan 2026 01:39:50 GMT
# ARGS: GPG_KEY=AF3D175EC05DB249738D01AC8D8C3C3ED0B02E66 SHORT_DISTRO_NAME=zookeeper-3.8.4 DISTRO_NAME=apache-zookeeper-3.8.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:39:50 GMT
WORKDIR /apache-zookeeper-3.8.4-bin
# Fri, 16 Jan 2026 01:39:50 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:39:50 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:39:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:39:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:39:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:39:50 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fc3ef6de679ecac0a74cc044dd73825b9e6daa54ab0904bc8e9b9e898d5bdd`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 16.1 MB (16065656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d903927893f88ea36a0f1ae2165c1cbabff6244e11daf33512f44c12631acd`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 46.5 MB (46538233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05322d833bff6a327f4cb5734a53c8ecd0811c295b8d670e977218a9a12d8906`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef01e65ce9e940b87d06c11af62f1cff2016c991c02e0b659ac1826a2466cbd5`  
		Last Modified: Thu, 15 Jan 2026 22:19:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e55d5e30460f4201033cd053b375a4a5b41c0e14c869c633d75898a8e106739`  
		Last Modified: Fri, 16 Jan 2026 01:40:00 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6373485f2036be4e69c7974110adc3ab5db0e7569fdd583a9ecbb8cb5be70ee`  
		Last Modified: Fri, 16 Jan 2026 01:40:00 GMT  
		Size: 1.1 MB (1073575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb6c6d21b9156536f02dfdc51bb1a129d27b909a1f7d5e698cb62b20a787dbf`  
		Last Modified: Fri, 16 Jan 2026 01:40:01 GMT  
		Size: 14.7 MB (14682888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2747fd3dab8cd3a4a817e229b92b2a893d51cadd08a7465fbd2e183e7a504c`  
		Last Modified: Fri, 16 Jan 2026 01:40:00 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:f4b9109f61acac87b56c50141156a3d49a556e027f4e34e4c709aa6ab32a307b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef225b8897b2dc03435d736d36d1f4ae3ff6bd8056a26d3a25431c59806d69`

```dockerfile
```

-	Layers:
	-	`sha256:21996cef7fa35014963fc7d89e1a5116da516e8a9d0f4767df25cecb2668672a`  
		Last Modified: Fri, 16 Jan 2026 01:40:00 GMT  
		Size: 4.0 MB (3959159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef9094f2cb0524edc8d9457376dc8a9bb5c5f8eb5710520382892634b5a8a443`  
		Last Modified: Fri, 16 Jan 2026 01:40:00 GMT  
		Size: 24.4 KB (24410 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:783ddfb6c6b7186027668105c7d32df535d5cbe559e868338724db9019a05b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115373818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff57b0b69ceca02b289ca298471de078fcbdeb20d0949f7d0b6075d1032e68b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 04 Feb 2026 18:04:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 04 Feb 2026 18:04:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 04 Feb 2026 18:04:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 04 Feb 2026 18:04:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 04 Feb 2026 18:04:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Wed, 04 Feb 2026 18:04:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:04:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:04:26 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:04:26 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:04:26 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:04:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:04:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:04:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:04:26 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:41 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ca264798509a08ea6ccee410a564b50a0eb5a42f1e58216b34a0c846751eb`  
		Last Modified: Thu, 15 Jan 2026 22:17:15 GMT  
		Size: 46.9 MB (46881201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae30e596f1d1d565a863521696c50833d9594367b6717a150b7660b7f6f7d9`  
		Last Modified: Thu, 15 Jan 2026 22:17:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a011aa1930859a4407f64ffbb4fddcba4751ca856311b708bf6236c1d809dea`  
		Last Modified: Thu, 15 Jan 2026 22:17:14 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65affe7af8d9e76c1b767be1d62eec504bbd7af88841a87c1f0341ec151720ae`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281a94a9388ae9d5318e9efe394b6b9d87ccac964d8992a061b7725f086766e7`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 1.1 MB (1090080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79c46142d7fe8cb5b5787b0573079692d51e9a5f331d602917e898411c66b57`  
		Last Modified: Wed, 04 Feb 2026 18:04:50 GMT  
		Size: 15.3 MB (15331337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f4d9d4e89ab14652ba4fcf1d9e056c4711729cdcffccf7555294ea4628cbdf`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:9278cb56863f59fbe0e3f7cfd504327d42b589749b90088eeefdcd17996af67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d302ab64b884257268c91f04e2da52801e1e0327ee4afb625f6ab37f122c1609`

```dockerfile
```

-	Layers:
	-	`sha256:a7d31bda6ad0bc3a005ba8a8130affc03d1cc0ae0dec3d357e49299834bfa06d`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 4.0 MB (3963580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5745aaa42a4794104ba4a1daffba0e3063e9d3fb7a70c19f5e60a5bad87b679`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 24.3 KB (24324 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:cd53368124fea9017409ce680e827dec6ebe45dfbb41df53fec8df31b08f617f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104623451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb27b0c8c8d868bf0dd41e9668c9444ec7189d730f0cae70791e268982cf6ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:49 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 15 Jan 2026 23:07:49 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 15 Jan 2026 23:07:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Thu, 15 Jan 2026 23:07:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:01:52 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:01:52 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:01:52 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:01:52 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:01:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:01:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:01:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:01:52 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:21 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23c205723170273b192d9e9d8b97c8f22f0d97ed549cebd30eb736b55476e21`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2059e56e4bc25d5f4b1c017b55a0664e3674869eed7702692d591c85c655688f`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.1 MB (1106856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47b40f9990641efdaf0c7415e83b92a28c5957539874044dcdd7c74d50cadc3`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 15.3 MB (15331334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30680f44e6339c9bf39f06e75083bb81b16132be4914f1893dd92c73ae91e3`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8cfa7e6ee11cee44e3b156218d3905a405ba292aefc1a276c271683d2b354457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15865c2c628c1fea46e9f6a5398e999272a166f9bc02c917e2673f5788037e`

```dockerfile
```

-	Layers:
	-	`sha256:24af95f386fe628438fd366e0cef16666786117c020711db4882a526b2acd92e`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 4.0 MB (3961067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c1b37381cf0acf4fee9cecc9a8c67b467e0d49a4f4867650534f8ce492739b`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 24.3 KB (24276 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8.5`

```console
$ docker pull zookeeper@sha256:4e5d1a601d29cfba36f03a97aca330663aa86217a8d59d9395dd284445406ef5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.8.5` - linux; amd64

```console
$ docker pull zookeeper@sha256:d0bba8360545dd0c49d0070814e4f22e14aa7171c31265d227bd5588ad424de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109220050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd16a532148796f87e6d1960f1b2e81184a5466f042ee70df319f3fb68a783a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 04 Feb 2026 18:05:09 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 04 Feb 2026 18:05:09 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 04 Feb 2026 18:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 04 Feb 2026 18:05:16 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 04 Feb 2026 18:05:16 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Wed, 04 Feb 2026 18:05:16 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:05:20 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:05:20 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:05:20 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:05:20 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:05:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:05:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:05:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:05:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770a7ccbf824857f9a328739d1ddfec21c04a1b7423007c0a74c8ab500e3675`  
		Last Modified: Thu, 15 Jan 2026 22:20:01 GMT  
		Size: 16.1 MB (16147435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5de6e8045fe0102a83fbca815f435fd81296a7937cdeb04409eeec845a3502`  
		Last Modified: Thu, 15 Jan 2026 22:20:02 GMT  
		Size: 47.1 MB (47055148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012e01f9d2afd797ecf20b406260375e0fe120b00a6401bba84a92fc3968f3`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4b65fc380fc87df9d7a19c5abf67e22e913f6f0b56b870b1ee5ca46f5cdf5`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1208c53df4b968be7689005aaef5970d46818e92381dd8514e46bc232a66b`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972eae95fec01d953f1186614dd684570c01a8640400ffd6e91092b97b8a6081`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 1.1 MB (1144566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73e905ef6db73a659708c2bf49312256a9c39ad9fcd4672b400f9123f79af38`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 15.3 MB (15331198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c551b1eb5135bcd7b81671012083f9451e20a4526ec7f285dc75f372ddd1189f`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.5` - unknown; unknown

```console
$ docker pull zookeeper@sha256:b2e767cf03a5bc9ff5ede937914bb75da1eb4a8fac6b1e89cc291c6b9c380ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf30c4b82b727fb746797a1b20be597c158068603487c3de6694c81a139f78a`

```dockerfile
```

-	Layers:
	-	`sha256:3eb9b554bdcc223f78ac9281cb7e2c8ee32d830216b9a56e55b595888351a815`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 4.0 MB (3959477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06849fc5948bdd2830966b24c01cfbd11b1808e4dfef909df6123ecd266d2d95`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 24.3 KB (24274 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.5` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:783ddfb6c6b7186027668105c7d32df535d5cbe559e868338724db9019a05b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115373818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff57b0b69ceca02b289ca298471de078fcbdeb20d0949f7d0b6075d1032e68b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 04 Feb 2026 18:04:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 04 Feb 2026 18:04:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 04 Feb 2026 18:04:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 04 Feb 2026 18:04:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 04 Feb 2026 18:04:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Wed, 04 Feb 2026 18:04:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:04:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:04:26 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:04:26 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:04:26 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:04:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:04:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:04:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:04:26 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:41 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ca264798509a08ea6ccee410a564b50a0eb5a42f1e58216b34a0c846751eb`  
		Last Modified: Thu, 15 Jan 2026 22:17:15 GMT  
		Size: 46.9 MB (46881201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae30e596f1d1d565a863521696c50833d9594367b6717a150b7660b7f6f7d9`  
		Last Modified: Thu, 15 Jan 2026 22:17:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a011aa1930859a4407f64ffbb4fddcba4751ca856311b708bf6236c1d809dea`  
		Last Modified: Thu, 15 Jan 2026 22:17:14 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65affe7af8d9e76c1b767be1d62eec504bbd7af88841a87c1f0341ec151720ae`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281a94a9388ae9d5318e9efe394b6b9d87ccac964d8992a061b7725f086766e7`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 1.1 MB (1090080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79c46142d7fe8cb5b5787b0573079692d51e9a5f331d602917e898411c66b57`  
		Last Modified: Wed, 04 Feb 2026 18:04:50 GMT  
		Size: 15.3 MB (15331337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f4d9d4e89ab14652ba4fcf1d9e056c4711729cdcffccf7555294ea4628cbdf`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.5` - unknown; unknown

```console
$ docker pull zookeeper@sha256:9278cb56863f59fbe0e3f7cfd504327d42b589749b90088eeefdcd17996af67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d302ab64b884257268c91f04e2da52801e1e0327ee4afb625f6ab37f122c1609`

```dockerfile
```

-	Layers:
	-	`sha256:a7d31bda6ad0bc3a005ba8a8130affc03d1cc0ae0dec3d357e49299834bfa06d`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 4.0 MB (3963580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5745aaa42a4794104ba4a1daffba0e3063e9d3fb7a70c19f5e60a5bad87b679`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 24.3 KB (24324 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.5` - linux; s390x

```console
$ docker pull zookeeper@sha256:cd53368124fea9017409ce680e827dec6ebe45dfbb41df53fec8df31b08f617f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104623451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb27b0c8c8d868bf0dd41e9668c9444ec7189d730f0cae70791e268982cf6ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:49 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 15 Jan 2026 23:07:49 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 15 Jan 2026 23:07:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Thu, 15 Jan 2026 23:07:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:01:52 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:01:52 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:01:52 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:01:52 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:01:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:01:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:01:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:01:52 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:21 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23c205723170273b192d9e9d8b97c8f22f0d97ed549cebd30eb736b55476e21`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2059e56e4bc25d5f4b1c017b55a0664e3674869eed7702692d591c85c655688f`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.1 MB (1106856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47b40f9990641efdaf0c7415e83b92a28c5957539874044dcdd7c74d50cadc3`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 15.3 MB (15331334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30680f44e6339c9bf39f06e75083bb81b16132be4914f1893dd92c73ae91e3`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.5` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8cfa7e6ee11cee44e3b156218d3905a405ba292aefc1a276c271683d2b354457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15865c2c628c1fea46e9f6a5398e999272a166f9bc02c917e2673f5788037e`

```dockerfile
```

-	Layers:
	-	`sha256:24af95f386fe628438fd366e0cef16666786117c020711db4882a526b2acd92e`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 4.0 MB (3961067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c1b37381cf0acf4fee9cecc9a8c67b467e0d49a4f4867650534f8ce492739b`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 24.3 KB (24276 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.8.5-jre-17`

```console
$ docker pull zookeeper@sha256:4e5d1a601d29cfba36f03a97aca330663aa86217a8d59d9395dd284445406ef5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `zookeeper:3.8.5-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:d0bba8360545dd0c49d0070814e4f22e14aa7171c31265d227bd5588ad424de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109220050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd16a532148796f87e6d1960f1b2e81184a5466f042ee70df319f3fb68a783a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 04 Feb 2026 18:05:09 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 04 Feb 2026 18:05:09 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 04 Feb 2026 18:05:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 04 Feb 2026 18:05:16 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 04 Feb 2026 18:05:16 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Wed, 04 Feb 2026 18:05:16 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:05:20 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:05:20 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:05:20 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:05:20 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:05:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:05:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:05:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:05:20 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770a7ccbf824857f9a328739d1ddfec21c04a1b7423007c0a74c8ab500e3675`  
		Last Modified: Thu, 15 Jan 2026 22:20:01 GMT  
		Size: 16.1 MB (16147435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5de6e8045fe0102a83fbca815f435fd81296a7937cdeb04409eeec845a3502`  
		Last Modified: Thu, 15 Jan 2026 22:20:02 GMT  
		Size: 47.1 MB (47055148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012e01f9d2afd797ecf20b406260375e0fe120b00a6401bba84a92fc3968f3`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4b65fc380fc87df9d7a19c5abf67e22e913f6f0b56b870b1ee5ca46f5cdf5`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1208c53df4b968be7689005aaef5970d46818e92381dd8514e46bc232a66b`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972eae95fec01d953f1186614dd684570c01a8640400ffd6e91092b97b8a6081`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 1.1 MB (1144566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73e905ef6db73a659708c2bf49312256a9c39ad9fcd4672b400f9123f79af38`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 15.3 MB (15331198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c551b1eb5135bcd7b81671012083f9451e20a4526ec7f285dc75f372ddd1189f`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.5-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:b2e767cf03a5bc9ff5ede937914bb75da1eb4a8fac6b1e89cc291c6b9c380ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf30c4b82b727fb746797a1b20be597c158068603487c3de6694c81a139f78a`

```dockerfile
```

-	Layers:
	-	`sha256:3eb9b554bdcc223f78ac9281cb7e2c8ee32d830216b9a56e55b595888351a815`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 4.0 MB (3959477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06849fc5948bdd2830966b24c01cfbd11b1808e4dfef909df6123ecd266d2d95`  
		Last Modified: Wed, 04 Feb 2026 18:05:29 GMT  
		Size: 24.3 KB (24274 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.5-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:783ddfb6c6b7186027668105c7d32df535d5cbe559e868338724db9019a05b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115373818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff57b0b69ceca02b289ca298471de078fcbdeb20d0949f7d0b6075d1032e68b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 04 Feb 2026 18:04:08 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Wed, 04 Feb 2026 18:04:08 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Wed, 04 Feb 2026 18:04:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Wed, 04 Feb 2026 18:04:19 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Wed, 04 Feb 2026 18:04:19 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Wed, 04 Feb 2026 18:04:19 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:04:25 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:04:26 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:04:26 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:04:26 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:04:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:04:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:04:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:04:26 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:41 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ca264798509a08ea6ccee410a564b50a0eb5a42f1e58216b34a0c846751eb`  
		Last Modified: Thu, 15 Jan 2026 22:17:15 GMT  
		Size: 46.9 MB (46881201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae30e596f1d1d565a863521696c50833d9594367b6717a150b7660b7f6f7d9`  
		Last Modified: Thu, 15 Jan 2026 22:17:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a011aa1930859a4407f64ffbb4fddcba4751ca856311b708bf6236c1d809dea`  
		Last Modified: Thu, 15 Jan 2026 22:17:14 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65affe7af8d9e76c1b767be1d62eec504bbd7af88841a87c1f0341ec151720ae`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281a94a9388ae9d5318e9efe394b6b9d87ccac964d8992a061b7725f086766e7`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 1.1 MB (1090080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79c46142d7fe8cb5b5787b0573079692d51e9a5f331d602917e898411c66b57`  
		Last Modified: Wed, 04 Feb 2026 18:04:50 GMT  
		Size: 15.3 MB (15331337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f4d9d4e89ab14652ba4fcf1d9e056c4711729cdcffccf7555294ea4628cbdf`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.5-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:9278cb56863f59fbe0e3f7cfd504327d42b589749b90088eeefdcd17996af67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d302ab64b884257268c91f04e2da52801e1e0327ee4afb625f6ab37f122c1609`

```dockerfile
```

-	Layers:
	-	`sha256:a7d31bda6ad0bc3a005ba8a8130affc03d1cc0ae0dec3d357e49299834bfa06d`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 4.0 MB (3963580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5745aaa42a4794104ba4a1daffba0e3063e9d3fb7a70c19f5e60a5bad87b679`  
		Last Modified: Wed, 04 Feb 2026 18:04:49 GMT  
		Size: 24.3 KB (24324 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.8.5-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:cd53368124fea9017409ce680e827dec6ebe45dfbb41df53fec8df31b08f617f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104623451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb27b0c8c8d868bf0dd41e9668c9444ec7189d730f0cae70791e268982cf6ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:49 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 15 Jan 2026 23:07:49 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 15 Jan 2026 23:07:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.8.5
# Thu, 15 Jan 2026 23:07:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:01:52 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.8.5 DISTRO_NAME=apache-zookeeper-3.8.5-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Wed, 04 Feb 2026 18:01:52 GMT
WORKDIR /apache-zookeeper-3.8.5-bin
# Wed, 04 Feb 2026 18:01:52 GMT
VOLUME [/data /datalog /logs]
# Wed, 04 Feb 2026 18:01:52 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Wed, 04 Feb 2026 18:01:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.8.5-bin/bin ZOOCFGDIR=/conf
# Wed, 04 Feb 2026 18:01:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 18:01:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:01:52 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:21 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23c205723170273b192d9e9d8b97c8f22f0d97ed549cebd30eb736b55476e21`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2059e56e4bc25d5f4b1c017b55a0664e3674869eed7702692d591c85c655688f`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.1 MB (1106856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47b40f9990641efdaf0c7415e83b92a28c5957539874044dcdd7c74d50cadc3`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 15.3 MB (15331334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30680f44e6339c9bf39f06e75083bb81b16132be4914f1893dd92c73ae91e3`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.8.5-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8cfa7e6ee11cee44e3b156218d3905a405ba292aefc1a276c271683d2b354457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15865c2c628c1fea46e9f6a5398e999272a166f9bc02c917e2673f5788037e`

```dockerfile
```

-	Layers:
	-	`sha256:24af95f386fe628438fd366e0cef16666786117c020711db4882a526b2acd92e`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 4.0 MB (3961067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c1b37381cf0acf4fee9cecc9a8c67b467e0d49a4f4867650534f8ce492739b`  
		Last Modified: Wed, 04 Feb 2026 18:02:15 GMT  
		Size: 24.3 KB (24276 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9`

```console
$ docker pull zookeeper@sha256:98be0d025355dd2f1659af615def34f04eabb233c80f4a9a1cc5ab121831c413
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
$ docker pull zookeeper@sha256:e6cf2fe59cbe9d1b123b89c12e7d77b2064d9aef706c2f8a0341e20a1deed59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115061259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d4f135060f54d999d66752b2f16dedac95bb3ae601ab6dc0b0ba7ad597ba5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:36:45 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:36:45 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:36:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:36:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 01:36:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 01:36:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:36:57 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:36:57 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:36:57 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:36:57 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:36:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:36:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:36:57 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770a7ccbf824857f9a328739d1ddfec21c04a1b7423007c0a74c8ab500e3675`  
		Last Modified: Thu, 15 Jan 2026 22:20:01 GMT  
		Size: 16.1 MB (16147435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5de6e8045fe0102a83fbca815f435fd81296a7937cdeb04409eeec845a3502`  
		Last Modified: Thu, 15 Jan 2026 22:20:02 GMT  
		Size: 47.1 MB (47055148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012e01f9d2afd797ecf20b406260375e0fe120b00a6401bba84a92fc3968f3`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4b65fc380fc87df9d7a19c5abf67e22e913f6f0b56b870b1ee5ca46f5cdf5`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf3585c2fe03c0bd80a26548aea6ff148e7ae3e1c55b6a4e4179108b2fde650`  
		Last Modified: Fri, 16 Jan 2026 01:37:08 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156c25d396090684c7dff189d5dcf34713c303e8b57b5ffa30787058bef508a4`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 1.1 MB (1144578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd284f44cee01947999fd0651e650587c33e37815cad785bd50814f7c11d7c9`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 21.2 MB (21172396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee53cde065518328e18b04bff47df92b26aab11e66ce24e6f7012439363f342a`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:961cbc52444e4b330ae1029480efdb6d933935980d347cd6a878e2a7d9b37d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcb583f37a4e3598675657a0d76ffc7b457944e5990a3c9a623566c0ff5cc7a`

```dockerfile
```

-	Layers:
	-	`sha256:9a4967b11cfcd4b7332331e969d31c677eb0f940fde6f38f5c30b05d4a62d0c6`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 4.0 MB (3966253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a2b116ce21e5d1cbbe805d0a9e709d2a8f710b0d177da7e59f6e03a3227428`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 24.6 KB (24580 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:fd8d7baa3599e8e64a0543459de97566c28f5374c234d606ddf650efda7649d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112238432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba2306c49665b350cf00111aff4b1ae741433ff5e145c4a7e550e0752b2cbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:40:22 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:40:22 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:40:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:40:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 01:40:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 01:40:31 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:40:34 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:40:34 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:40:34 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:40:34 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:40:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:40:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:40:34 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fc3ef6de679ecac0a74cc044dd73825b9e6daa54ab0904bc8e9b9e898d5bdd`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 16.1 MB (16065656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d903927893f88ea36a0f1ae2165c1cbabff6244e11daf33512f44c12631acd`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 46.5 MB (46538233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05322d833bff6a327f4cb5734a53c8ecd0811c295b8d670e977218a9a12d8906`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef01e65ce9e940b87d06c11af62f1cff2016c991c02e0b659ac1826a2466cbd5`  
		Last Modified: Thu, 15 Jan 2026 22:19:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8db862d46a77e2d6af87165369540bbb128353c39fd534ec1bc745786112a`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d24a3dce8810275ea0a98a9d4847c86f2c6efe26c1c24c2a172a64e3646886e`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 1.1 MB (1073564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ef855d439e2ba38f6a9c60b94ee97ffc400b9bb2fad1c85f761f3ee92fc3ad`  
		Last Modified: Fri, 16 Jan 2026 01:40:45 GMT  
		Size: 21.2 MB (21172438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5571b26e6eda3e58c809bb0472faedc92d284e37b9fcec3e3398ee12868a62`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7049f58e879fb52f615d2f81d20c0ffdef8fc5e8107d7e718dbf7ceeb87409d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1426a88958d7e690dd7c320f94204d0ba351b90887d9a0c5ca38de74b7defe42`

```dockerfile
```

-	Layers:
	-	`sha256:6fa98e02ebea1734a0c9f774c204620face5a266bb372d316b37a0ddf3546d67`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 4.0 MB (3965947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7b504e7afabdfdfe74bf318c5e53ac672e49bb47acfa791a849414ea68cb7e`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 24.7 KB (24726 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:0366b3c4391ca9627e353e49c1bac8d62bca65f9df68183ab590ebfcdf9381ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121214870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96de994674f485ed31b035d91d46523fd1f5c1e3a6528d38f860f31de46a9456`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:38:03 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 02:38:03 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 02:38:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 02:38:13 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 02:38:13 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 02:38:13 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 02:39:14 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 02:39:15 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 02:39:15 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 02:39:15 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 02:39:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 02:39:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 02:39:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 02:39:15 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:41 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ca264798509a08ea6ccee410a564b50a0eb5a42f1e58216b34a0c846751eb`  
		Last Modified: Thu, 15 Jan 2026 22:17:15 GMT  
		Size: 46.9 MB (46881201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae30e596f1d1d565a863521696c50833d9594367b6717a150b7660b7f6f7d9`  
		Last Modified: Thu, 15 Jan 2026 22:17:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a011aa1930859a4407f64ffbb4fddcba4751ca856311b708bf6236c1d809dea`  
		Last Modified: Thu, 15 Jan 2026 22:17:14 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf81a92636b3c38340de4646628998f5b1c22a7c602e27b1e888e99525516c32`  
		Last Modified: Fri, 16 Jan 2026 02:38:50 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7142f408493309927e8c69411ed672557055df16f6c06f5dd27b95ef40e336d`  
		Last Modified: Fri, 16 Jan 2026 02:38:50 GMT  
		Size: 1.1 MB (1090111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731431cd69c8ce2bf4f1c16887d0e070bf30d67764c3330552e6eeee8e7ae3cc`  
		Last Modified: Fri, 16 Jan 2026 02:39:48 GMT  
		Size: 21.2 MB (21172362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c2421f3ebbf0a5f025adf9737583775bbab31aad2a425a339c6a9bb3122030`  
		Last Modified: Fri, 16 Jan 2026 02:39:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4476e61e4b3e1e574a91f8f9aca521fe7253c97df9de1799b6d62dca2f5f3935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559477b417ee5258fe91ffba7b61754fedcd87c4df451e8e2059bb4f4052c27b`

```dockerfile
```

-	Layers:
	-	`sha256:e773ce6f5144b02013ce174de5074cc1155043ee616a1c25fbd513cee8fd61ad`  
		Last Modified: Fri, 16 Jan 2026 02:39:47 GMT  
		Size: 4.0 MB (3970362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1b0322bfe3c7f5eda18e5da0338a509542590cf275eff40982a1864c2f89b1`  
		Last Modified: Fri, 16 Jan 2026 02:39:47 GMT  
		Size: 24.6 KB (24633 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9` - linux; s390x

```console
$ docker pull zookeeper@sha256:4bd3e6bf1c0f9f94724ade94ed010d58faccbd1fc36be729edf2632720fe28b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110464056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d8e529b78d815667cfaa02e5fb4f9d6a0432d2f6afcf95bc552f9a53686324`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:49 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 15 Jan 2026 23:07:49 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 15 Jan 2026 23:07:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Thu, 15 Jan 2026 23:07:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Thu, 15 Jan 2026 23:07:56 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 15 Jan 2026 23:07:56 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Thu, 15 Jan 2026 23:07:56 GMT
VOLUME [/data /datalog /logs]
# Thu, 15 Jan 2026 23:07:56 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 15 Jan 2026 23:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Thu, 15 Jan 2026 23:07:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:56 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:21 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23c205723170273b192d9e9d8b97c8f22f0d97ed549cebd30eb736b55476e21`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2059e56e4bc25d5f4b1c017b55a0664e3674869eed7702692d591c85c655688f`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.1 MB (1106856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6cb1c6792da391a96027dcf3e8aea42df2b6189b93140b8154001bb4a099ad`  
		Last Modified: Thu, 15 Jan 2026 23:08:10 GMT  
		Size: 21.2 MB (21171940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ceee274217c7ff581906ffaee29e8b824a28859ec8cd009db21ac4cd142412`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8e4c7f8f3900631bf1c6fbc225c2577afda76186583bdf81917777d8e09f12f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bc47ebc4fa798087fdcc5986b2a5c0581789cc8e00e7570578c021a52b48d2`

```dockerfile
```

-	Layers:
	-	`sha256:6d57227768de9070e140e046f1cf208fdde8b5e080dbddb5cb51aff80ce46a08`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 4.0 MB (3967843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cb0a4c8a83b944ab976042d096bcde54e897b6d7ccb4c68917768c9f519224`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 24.6 KB (24579 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9-jre-17`

```console
$ docker pull zookeeper@sha256:98be0d025355dd2f1659af615def34f04eabb233c80f4a9a1cc5ab121831c413
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
$ docker pull zookeeper@sha256:e6cf2fe59cbe9d1b123b89c12e7d77b2064d9aef706c2f8a0341e20a1deed59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115061259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d4f135060f54d999d66752b2f16dedac95bb3ae601ab6dc0b0ba7ad597ba5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:36:45 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:36:45 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:36:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:36:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 01:36:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 01:36:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:36:57 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:36:57 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:36:57 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:36:57 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:36:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:36:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:36:57 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770a7ccbf824857f9a328739d1ddfec21c04a1b7423007c0a74c8ab500e3675`  
		Last Modified: Thu, 15 Jan 2026 22:20:01 GMT  
		Size: 16.1 MB (16147435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5de6e8045fe0102a83fbca815f435fd81296a7937cdeb04409eeec845a3502`  
		Last Modified: Thu, 15 Jan 2026 22:20:02 GMT  
		Size: 47.1 MB (47055148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012e01f9d2afd797ecf20b406260375e0fe120b00a6401bba84a92fc3968f3`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4b65fc380fc87df9d7a19c5abf67e22e913f6f0b56b870b1ee5ca46f5cdf5`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf3585c2fe03c0bd80a26548aea6ff148e7ae3e1c55b6a4e4179108b2fde650`  
		Last Modified: Fri, 16 Jan 2026 01:37:08 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156c25d396090684c7dff189d5dcf34713c303e8b57b5ffa30787058bef508a4`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 1.1 MB (1144578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd284f44cee01947999fd0651e650587c33e37815cad785bd50814f7c11d7c9`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 21.2 MB (21172396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee53cde065518328e18b04bff47df92b26aab11e66ce24e6f7012439363f342a`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:961cbc52444e4b330ae1029480efdb6d933935980d347cd6a878e2a7d9b37d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcb583f37a4e3598675657a0d76ffc7b457944e5990a3c9a623566c0ff5cc7a`

```dockerfile
```

-	Layers:
	-	`sha256:9a4967b11cfcd4b7332331e969d31c677eb0f940fde6f38f5c30b05d4a62d0c6`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 4.0 MB (3966253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a2b116ce21e5d1cbbe805d0a9e709d2a8f710b0d177da7e59f6e03a3227428`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 24.6 KB (24580 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:fd8d7baa3599e8e64a0543459de97566c28f5374c234d606ddf650efda7649d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112238432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba2306c49665b350cf00111aff4b1ae741433ff5e145c4a7e550e0752b2cbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:40:22 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:40:22 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:40:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:40:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 01:40:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 01:40:31 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:40:34 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:40:34 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:40:34 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:40:34 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:40:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:40:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:40:34 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fc3ef6de679ecac0a74cc044dd73825b9e6daa54ab0904bc8e9b9e898d5bdd`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 16.1 MB (16065656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d903927893f88ea36a0f1ae2165c1cbabff6244e11daf33512f44c12631acd`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 46.5 MB (46538233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05322d833bff6a327f4cb5734a53c8ecd0811c295b8d670e977218a9a12d8906`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef01e65ce9e940b87d06c11af62f1cff2016c991c02e0b659ac1826a2466cbd5`  
		Last Modified: Thu, 15 Jan 2026 22:19:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8db862d46a77e2d6af87165369540bbb128353c39fd534ec1bc745786112a`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d24a3dce8810275ea0a98a9d4847c86f2c6efe26c1c24c2a172a64e3646886e`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 1.1 MB (1073564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ef855d439e2ba38f6a9c60b94ee97ffc400b9bb2fad1c85f761f3ee92fc3ad`  
		Last Modified: Fri, 16 Jan 2026 01:40:45 GMT  
		Size: 21.2 MB (21172438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5571b26e6eda3e58c809bb0472faedc92d284e37b9fcec3e3398ee12868a62`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7049f58e879fb52f615d2f81d20c0ffdef8fc5e8107d7e718dbf7ceeb87409d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1426a88958d7e690dd7c320f94204d0ba351b90887d9a0c5ca38de74b7defe42`

```dockerfile
```

-	Layers:
	-	`sha256:6fa98e02ebea1734a0c9f774c204620face5a266bb372d316b37a0ddf3546d67`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 4.0 MB (3965947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7b504e7afabdfdfe74bf318c5e53ac672e49bb47acfa791a849414ea68cb7e`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 24.7 KB (24726 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:0366b3c4391ca9627e353e49c1bac8d62bca65f9df68183ab590ebfcdf9381ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121214870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96de994674f485ed31b035d91d46523fd1f5c1e3a6528d38f860f31de46a9456`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:38:03 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 02:38:03 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 02:38:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 02:38:13 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 02:38:13 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 02:38:13 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 02:39:14 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 02:39:15 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 02:39:15 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 02:39:15 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 02:39:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 02:39:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 02:39:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 02:39:15 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:41 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ca264798509a08ea6ccee410a564b50a0eb5a42f1e58216b34a0c846751eb`  
		Last Modified: Thu, 15 Jan 2026 22:17:15 GMT  
		Size: 46.9 MB (46881201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae30e596f1d1d565a863521696c50833d9594367b6717a150b7660b7f6f7d9`  
		Last Modified: Thu, 15 Jan 2026 22:17:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a011aa1930859a4407f64ffbb4fddcba4751ca856311b708bf6236c1d809dea`  
		Last Modified: Thu, 15 Jan 2026 22:17:14 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf81a92636b3c38340de4646628998f5b1c22a7c602e27b1e888e99525516c32`  
		Last Modified: Fri, 16 Jan 2026 02:38:50 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7142f408493309927e8c69411ed672557055df16f6c06f5dd27b95ef40e336d`  
		Last Modified: Fri, 16 Jan 2026 02:38:50 GMT  
		Size: 1.1 MB (1090111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731431cd69c8ce2bf4f1c16887d0e070bf30d67764c3330552e6eeee8e7ae3cc`  
		Last Modified: Fri, 16 Jan 2026 02:39:48 GMT  
		Size: 21.2 MB (21172362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c2421f3ebbf0a5f025adf9737583775bbab31aad2a425a339c6a9bb3122030`  
		Last Modified: Fri, 16 Jan 2026 02:39:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4476e61e4b3e1e574a91f8f9aca521fe7253c97df9de1799b6d62dca2f5f3935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559477b417ee5258fe91ffba7b61754fedcd87c4df451e8e2059bb4f4052c27b`

```dockerfile
```

-	Layers:
	-	`sha256:e773ce6f5144b02013ce174de5074cc1155043ee616a1c25fbd513cee8fd61ad`  
		Last Modified: Fri, 16 Jan 2026 02:39:47 GMT  
		Size: 4.0 MB (3970362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1b0322bfe3c7f5eda18e5da0338a509542590cf275eff40982a1864c2f89b1`  
		Last Modified: Fri, 16 Jan 2026 02:39:47 GMT  
		Size: 24.6 KB (24633 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:4bd3e6bf1c0f9f94724ade94ed010d58faccbd1fc36be729edf2632720fe28b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110464056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d8e529b78d815667cfaa02e5fb4f9d6a0432d2f6afcf95bc552f9a53686324`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:49 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 15 Jan 2026 23:07:49 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 15 Jan 2026 23:07:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Thu, 15 Jan 2026 23:07:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Thu, 15 Jan 2026 23:07:56 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 15 Jan 2026 23:07:56 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Thu, 15 Jan 2026 23:07:56 GMT
VOLUME [/data /datalog /logs]
# Thu, 15 Jan 2026 23:07:56 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 15 Jan 2026 23:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Thu, 15 Jan 2026 23:07:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:56 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:21 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23c205723170273b192d9e9d8b97c8f22f0d97ed549cebd30eb736b55476e21`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2059e56e4bc25d5f4b1c017b55a0664e3674869eed7702692d591c85c655688f`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.1 MB (1106856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6cb1c6792da391a96027dcf3e8aea42df2b6189b93140b8154001bb4a099ad`  
		Last Modified: Thu, 15 Jan 2026 23:08:10 GMT  
		Size: 21.2 MB (21171940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ceee274217c7ff581906ffaee29e8b824a28859ec8cd009db21ac4cd142412`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8e4c7f8f3900631bf1c6fbc225c2577afda76186583bdf81917777d8e09f12f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bc47ebc4fa798087fdcc5986b2a5c0581789cc8e00e7570578c021a52b48d2`

```dockerfile
```

-	Layers:
	-	`sha256:6d57227768de9070e140e046f1cf208fdde8b5e080dbddb5cb51aff80ce46a08`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 4.0 MB (3967843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cb0a4c8a83b944ab976042d096bcde54e897b6d7ccb4c68917768c9f519224`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 24.6 KB (24579 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9.4`

```console
$ docker pull zookeeper@sha256:98be0d025355dd2f1659af615def34f04eabb233c80f4a9a1cc5ab121831c413
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

### `zookeeper:3.9.4` - linux; amd64

```console
$ docker pull zookeeper@sha256:e6cf2fe59cbe9d1b123b89c12e7d77b2064d9aef706c2f8a0341e20a1deed59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115061259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d4f135060f54d999d66752b2f16dedac95bb3ae601ab6dc0b0ba7ad597ba5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:36:45 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:36:45 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:36:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:36:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 01:36:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 01:36:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:36:57 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:36:57 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:36:57 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:36:57 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:36:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:36:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:36:57 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770a7ccbf824857f9a328739d1ddfec21c04a1b7423007c0a74c8ab500e3675`  
		Last Modified: Thu, 15 Jan 2026 22:20:01 GMT  
		Size: 16.1 MB (16147435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5de6e8045fe0102a83fbca815f435fd81296a7937cdeb04409eeec845a3502`  
		Last Modified: Thu, 15 Jan 2026 22:20:02 GMT  
		Size: 47.1 MB (47055148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012e01f9d2afd797ecf20b406260375e0fe120b00a6401bba84a92fc3968f3`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4b65fc380fc87df9d7a19c5abf67e22e913f6f0b56b870b1ee5ca46f5cdf5`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf3585c2fe03c0bd80a26548aea6ff148e7ae3e1c55b6a4e4179108b2fde650`  
		Last Modified: Fri, 16 Jan 2026 01:37:08 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156c25d396090684c7dff189d5dcf34713c303e8b57b5ffa30787058bef508a4`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 1.1 MB (1144578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd284f44cee01947999fd0651e650587c33e37815cad785bd50814f7c11d7c9`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 21.2 MB (21172396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee53cde065518328e18b04bff47df92b26aab11e66ce24e6f7012439363f342a`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:961cbc52444e4b330ae1029480efdb6d933935980d347cd6a878e2a7d9b37d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcb583f37a4e3598675657a0d76ffc7b457944e5990a3c9a623566c0ff5cc7a`

```dockerfile
```

-	Layers:
	-	`sha256:9a4967b11cfcd4b7332331e969d31c677eb0f940fde6f38f5c30b05d4a62d0c6`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 4.0 MB (3966253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a2b116ce21e5d1cbbe805d0a9e709d2a8f710b0d177da7e59f6e03a3227428`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 24.6 KB (24580 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.4` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:fd8d7baa3599e8e64a0543459de97566c28f5374c234d606ddf650efda7649d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112238432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba2306c49665b350cf00111aff4b1ae741433ff5e145c4a7e550e0752b2cbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:40:22 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:40:22 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:40:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:40:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 01:40:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 01:40:31 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:40:34 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:40:34 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:40:34 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:40:34 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:40:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:40:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:40:34 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fc3ef6de679ecac0a74cc044dd73825b9e6daa54ab0904bc8e9b9e898d5bdd`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 16.1 MB (16065656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d903927893f88ea36a0f1ae2165c1cbabff6244e11daf33512f44c12631acd`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 46.5 MB (46538233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05322d833bff6a327f4cb5734a53c8ecd0811c295b8d670e977218a9a12d8906`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef01e65ce9e940b87d06c11af62f1cff2016c991c02e0b659ac1826a2466cbd5`  
		Last Modified: Thu, 15 Jan 2026 22:19:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8db862d46a77e2d6af87165369540bbb128353c39fd534ec1bc745786112a`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d24a3dce8810275ea0a98a9d4847c86f2c6efe26c1c24c2a172a64e3646886e`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 1.1 MB (1073564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ef855d439e2ba38f6a9c60b94ee97ffc400b9bb2fad1c85f761f3ee92fc3ad`  
		Last Modified: Fri, 16 Jan 2026 01:40:45 GMT  
		Size: 21.2 MB (21172438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5571b26e6eda3e58c809bb0472faedc92d284e37b9fcec3e3398ee12868a62`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7049f58e879fb52f615d2f81d20c0ffdef8fc5e8107d7e718dbf7ceeb87409d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1426a88958d7e690dd7c320f94204d0ba351b90887d9a0c5ca38de74b7defe42`

```dockerfile
```

-	Layers:
	-	`sha256:6fa98e02ebea1734a0c9f774c204620face5a266bb372d316b37a0ddf3546d67`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 4.0 MB (3965947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7b504e7afabdfdfe74bf318c5e53ac672e49bb47acfa791a849414ea68cb7e`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 24.7 KB (24726 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.4` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:0366b3c4391ca9627e353e49c1bac8d62bca65f9df68183ab590ebfcdf9381ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121214870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96de994674f485ed31b035d91d46523fd1f5c1e3a6528d38f860f31de46a9456`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:38:03 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 02:38:03 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 02:38:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 02:38:13 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 02:38:13 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 02:38:13 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 02:39:14 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 02:39:15 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 02:39:15 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 02:39:15 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 02:39:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 02:39:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 02:39:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 02:39:15 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:41 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ca264798509a08ea6ccee410a564b50a0eb5a42f1e58216b34a0c846751eb`  
		Last Modified: Thu, 15 Jan 2026 22:17:15 GMT  
		Size: 46.9 MB (46881201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae30e596f1d1d565a863521696c50833d9594367b6717a150b7660b7f6f7d9`  
		Last Modified: Thu, 15 Jan 2026 22:17:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a011aa1930859a4407f64ffbb4fddcba4751ca856311b708bf6236c1d809dea`  
		Last Modified: Thu, 15 Jan 2026 22:17:14 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf81a92636b3c38340de4646628998f5b1c22a7c602e27b1e888e99525516c32`  
		Last Modified: Fri, 16 Jan 2026 02:38:50 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7142f408493309927e8c69411ed672557055df16f6c06f5dd27b95ef40e336d`  
		Last Modified: Fri, 16 Jan 2026 02:38:50 GMT  
		Size: 1.1 MB (1090111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731431cd69c8ce2bf4f1c16887d0e070bf30d67764c3330552e6eeee8e7ae3cc`  
		Last Modified: Fri, 16 Jan 2026 02:39:48 GMT  
		Size: 21.2 MB (21172362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c2421f3ebbf0a5f025adf9737583775bbab31aad2a425a339c6a9bb3122030`  
		Last Modified: Fri, 16 Jan 2026 02:39:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4476e61e4b3e1e574a91f8f9aca521fe7253c97df9de1799b6d62dca2f5f3935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559477b417ee5258fe91ffba7b61754fedcd87c4df451e8e2059bb4f4052c27b`

```dockerfile
```

-	Layers:
	-	`sha256:e773ce6f5144b02013ce174de5074cc1155043ee616a1c25fbd513cee8fd61ad`  
		Last Modified: Fri, 16 Jan 2026 02:39:47 GMT  
		Size: 4.0 MB (3970362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1b0322bfe3c7f5eda18e5da0338a509542590cf275eff40982a1864c2f89b1`  
		Last Modified: Fri, 16 Jan 2026 02:39:47 GMT  
		Size: 24.6 KB (24633 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.4` - linux; s390x

```console
$ docker pull zookeeper@sha256:4bd3e6bf1c0f9f94724ade94ed010d58faccbd1fc36be729edf2632720fe28b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110464056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d8e529b78d815667cfaa02e5fb4f9d6a0432d2f6afcf95bc552f9a53686324`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:49 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 15 Jan 2026 23:07:49 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 15 Jan 2026 23:07:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Thu, 15 Jan 2026 23:07:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Thu, 15 Jan 2026 23:07:56 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 15 Jan 2026 23:07:56 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Thu, 15 Jan 2026 23:07:56 GMT
VOLUME [/data /datalog /logs]
# Thu, 15 Jan 2026 23:07:56 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 15 Jan 2026 23:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Thu, 15 Jan 2026 23:07:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:56 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:21 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23c205723170273b192d9e9d8b97c8f22f0d97ed549cebd30eb736b55476e21`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2059e56e4bc25d5f4b1c017b55a0664e3674869eed7702692d591c85c655688f`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.1 MB (1106856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6cb1c6792da391a96027dcf3e8aea42df2b6189b93140b8154001bb4a099ad`  
		Last Modified: Thu, 15 Jan 2026 23:08:10 GMT  
		Size: 21.2 MB (21171940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ceee274217c7ff581906ffaee29e8b824a28859ec8cd009db21ac4cd142412`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.4` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8e4c7f8f3900631bf1c6fbc225c2577afda76186583bdf81917777d8e09f12f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bc47ebc4fa798087fdcc5986b2a5c0581789cc8e00e7570578c021a52b48d2`

```dockerfile
```

-	Layers:
	-	`sha256:6d57227768de9070e140e046f1cf208fdde8b5e080dbddb5cb51aff80ce46a08`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 4.0 MB (3967843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cb0a4c8a83b944ab976042d096bcde54e897b6d7ccb4c68917768c9f519224`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 24.6 KB (24579 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:3.9.4-jre-17`

```console
$ docker pull zookeeper@sha256:98be0d025355dd2f1659af615def34f04eabb233c80f4a9a1cc5ab121831c413
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

### `zookeeper:3.9.4-jre-17` - linux; amd64

```console
$ docker pull zookeeper@sha256:e6cf2fe59cbe9d1b123b89c12e7d77b2064d9aef706c2f8a0341e20a1deed59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115061259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d4f135060f54d999d66752b2f16dedac95bb3ae601ab6dc0b0ba7ad597ba5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:36:45 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:36:45 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:36:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:36:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 01:36:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 01:36:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:36:57 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:36:57 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:36:57 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:36:57 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:36:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:36:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:36:57 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770a7ccbf824857f9a328739d1ddfec21c04a1b7423007c0a74c8ab500e3675`  
		Last Modified: Thu, 15 Jan 2026 22:20:01 GMT  
		Size: 16.1 MB (16147435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5de6e8045fe0102a83fbca815f435fd81296a7937cdeb04409eeec845a3502`  
		Last Modified: Thu, 15 Jan 2026 22:20:02 GMT  
		Size: 47.1 MB (47055148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012e01f9d2afd797ecf20b406260375e0fe120b00a6401bba84a92fc3968f3`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4b65fc380fc87df9d7a19c5abf67e22e913f6f0b56b870b1ee5ca46f5cdf5`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf3585c2fe03c0bd80a26548aea6ff148e7ae3e1c55b6a4e4179108b2fde650`  
		Last Modified: Fri, 16 Jan 2026 01:37:08 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156c25d396090684c7dff189d5dcf34713c303e8b57b5ffa30787058bef508a4`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 1.1 MB (1144578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd284f44cee01947999fd0651e650587c33e37815cad785bd50814f7c11d7c9`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 21.2 MB (21172396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee53cde065518328e18b04bff47df92b26aab11e66ce24e6f7012439363f342a`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:961cbc52444e4b330ae1029480efdb6d933935980d347cd6a878e2a7d9b37d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcb583f37a4e3598675657a0d76ffc7b457944e5990a3c9a623566c0ff5cc7a`

```dockerfile
```

-	Layers:
	-	`sha256:9a4967b11cfcd4b7332331e969d31c677eb0f940fde6f38f5c30b05d4a62d0c6`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 4.0 MB (3966253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a2b116ce21e5d1cbbe805d0a9e709d2a8f710b0d177da7e59f6e03a3227428`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 24.6 KB (24580 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.4-jre-17` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:fd8d7baa3599e8e64a0543459de97566c28f5374c234d606ddf650efda7649d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112238432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba2306c49665b350cf00111aff4b1ae741433ff5e145c4a7e550e0752b2cbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:40:22 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:40:22 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:40:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:40:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 01:40:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 01:40:31 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:40:34 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:40:34 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:40:34 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:40:34 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:40:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:40:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:40:34 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fc3ef6de679ecac0a74cc044dd73825b9e6daa54ab0904bc8e9b9e898d5bdd`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 16.1 MB (16065656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d903927893f88ea36a0f1ae2165c1cbabff6244e11daf33512f44c12631acd`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 46.5 MB (46538233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05322d833bff6a327f4cb5734a53c8ecd0811c295b8d670e977218a9a12d8906`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef01e65ce9e940b87d06c11af62f1cff2016c991c02e0b659ac1826a2466cbd5`  
		Last Modified: Thu, 15 Jan 2026 22:19:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8db862d46a77e2d6af87165369540bbb128353c39fd534ec1bc745786112a`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d24a3dce8810275ea0a98a9d4847c86f2c6efe26c1c24c2a172a64e3646886e`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 1.1 MB (1073564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ef855d439e2ba38f6a9c60b94ee97ffc400b9bb2fad1c85f761f3ee92fc3ad`  
		Last Modified: Fri, 16 Jan 2026 01:40:45 GMT  
		Size: 21.2 MB (21172438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5571b26e6eda3e58c809bb0472faedc92d284e37b9fcec3e3398ee12868a62`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7049f58e879fb52f615d2f81d20c0ffdef8fc5e8107d7e718dbf7ceeb87409d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1426a88958d7e690dd7c320f94204d0ba351b90887d9a0c5ca38de74b7defe42`

```dockerfile
```

-	Layers:
	-	`sha256:6fa98e02ebea1734a0c9f774c204620face5a266bb372d316b37a0ddf3546d67`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 4.0 MB (3965947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7b504e7afabdfdfe74bf318c5e53ac672e49bb47acfa791a849414ea68cb7e`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 24.7 KB (24726 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.4-jre-17` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:0366b3c4391ca9627e353e49c1bac8d62bca65f9df68183ab590ebfcdf9381ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121214870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96de994674f485ed31b035d91d46523fd1f5c1e3a6528d38f860f31de46a9456`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:38:03 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 02:38:03 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 02:38:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 02:38:13 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 02:38:13 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 02:38:13 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 02:39:14 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 02:39:15 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 02:39:15 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 02:39:15 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 02:39:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 02:39:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 02:39:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 02:39:15 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:41 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ca264798509a08ea6ccee410a564b50a0eb5a42f1e58216b34a0c846751eb`  
		Last Modified: Thu, 15 Jan 2026 22:17:15 GMT  
		Size: 46.9 MB (46881201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae30e596f1d1d565a863521696c50833d9594367b6717a150b7660b7f6f7d9`  
		Last Modified: Thu, 15 Jan 2026 22:17:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a011aa1930859a4407f64ffbb4fddcba4751ca856311b708bf6236c1d809dea`  
		Last Modified: Thu, 15 Jan 2026 22:17:14 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf81a92636b3c38340de4646628998f5b1c22a7c602e27b1e888e99525516c32`  
		Last Modified: Fri, 16 Jan 2026 02:38:50 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7142f408493309927e8c69411ed672557055df16f6c06f5dd27b95ef40e336d`  
		Last Modified: Fri, 16 Jan 2026 02:38:50 GMT  
		Size: 1.1 MB (1090111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731431cd69c8ce2bf4f1c16887d0e070bf30d67764c3330552e6eeee8e7ae3cc`  
		Last Modified: Fri, 16 Jan 2026 02:39:48 GMT  
		Size: 21.2 MB (21172362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c2421f3ebbf0a5f025adf9737583775bbab31aad2a425a339c6a9bb3122030`  
		Last Modified: Fri, 16 Jan 2026 02:39:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4476e61e4b3e1e574a91f8f9aca521fe7253c97df9de1799b6d62dca2f5f3935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559477b417ee5258fe91ffba7b61754fedcd87c4df451e8e2059bb4f4052c27b`

```dockerfile
```

-	Layers:
	-	`sha256:e773ce6f5144b02013ce174de5074cc1155043ee616a1c25fbd513cee8fd61ad`  
		Last Modified: Fri, 16 Jan 2026 02:39:47 GMT  
		Size: 4.0 MB (3970362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1b0322bfe3c7f5eda18e5da0338a509542590cf275eff40982a1864c2f89b1`  
		Last Modified: Fri, 16 Jan 2026 02:39:47 GMT  
		Size: 24.6 KB (24633 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:3.9.4-jre-17` - linux; s390x

```console
$ docker pull zookeeper@sha256:4bd3e6bf1c0f9f94724ade94ed010d58faccbd1fc36be729edf2632720fe28b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110464056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d8e529b78d815667cfaa02e5fb4f9d6a0432d2f6afcf95bc552f9a53686324`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:49 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 15 Jan 2026 23:07:49 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 15 Jan 2026 23:07:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Thu, 15 Jan 2026 23:07:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Thu, 15 Jan 2026 23:07:56 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 15 Jan 2026 23:07:56 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Thu, 15 Jan 2026 23:07:56 GMT
VOLUME [/data /datalog /logs]
# Thu, 15 Jan 2026 23:07:56 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 15 Jan 2026 23:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Thu, 15 Jan 2026 23:07:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:56 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:21 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23c205723170273b192d9e9d8b97c8f22f0d97ed549cebd30eb736b55476e21`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2059e56e4bc25d5f4b1c017b55a0664e3674869eed7702692d591c85c655688f`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.1 MB (1106856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6cb1c6792da391a96027dcf3e8aea42df2b6189b93140b8154001bb4a099ad`  
		Last Modified: Thu, 15 Jan 2026 23:08:10 GMT  
		Size: 21.2 MB (21171940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ceee274217c7ff581906ffaee29e8b824a28859ec8cd009db21ac4cd142412`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:3.9.4-jre-17` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8e4c7f8f3900631bf1c6fbc225c2577afda76186583bdf81917777d8e09f12f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bc47ebc4fa798087fdcc5986b2a5c0581789cc8e00e7570578c021a52b48d2`

```dockerfile
```

-	Layers:
	-	`sha256:6d57227768de9070e140e046f1cf208fdde8b5e080dbddb5cb51aff80ce46a08`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 4.0 MB (3967843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cb0a4c8a83b944ab976042d096bcde54e897b6d7ccb4c68917768c9f519224`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 24.6 KB (24579 bytes)  
		MIME: application/vnd.in-toto+json

## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:98be0d025355dd2f1659af615def34f04eabb233c80f4a9a1cc5ab121831c413
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
$ docker pull zookeeper@sha256:e6cf2fe59cbe9d1b123b89c12e7d77b2064d9aef706c2f8a0341e20a1deed59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115061259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d4f135060f54d999d66752b2f16dedac95bb3ae601ab6dc0b0ba7ad597ba5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:36:45 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:36:45 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:36:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:36:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 01:36:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 01:36:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:36:57 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:36:57 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:36:57 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:36:57 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:36:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:36:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:36:57 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770a7ccbf824857f9a328739d1ddfec21c04a1b7423007c0a74c8ab500e3675`  
		Last Modified: Thu, 15 Jan 2026 22:20:01 GMT  
		Size: 16.1 MB (16147435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5de6e8045fe0102a83fbca815f435fd81296a7937cdeb04409eeec845a3502`  
		Last Modified: Thu, 15 Jan 2026 22:20:02 GMT  
		Size: 47.1 MB (47055148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012e01f9d2afd797ecf20b406260375e0fe120b00a6401bba84a92fc3968f3`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4b65fc380fc87df9d7a19c5abf67e22e913f6f0b56b870b1ee5ca46f5cdf5`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf3585c2fe03c0bd80a26548aea6ff148e7ae3e1c55b6a4e4179108b2fde650`  
		Last Modified: Fri, 16 Jan 2026 01:37:08 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156c25d396090684c7dff189d5dcf34713c303e8b57b5ffa30787058bef508a4`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 1.1 MB (1144578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd284f44cee01947999fd0651e650587c33e37815cad785bd50814f7c11d7c9`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 21.2 MB (21172396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee53cde065518328e18b04bff47df92b26aab11e66ce24e6f7012439363f342a`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:961cbc52444e4b330ae1029480efdb6d933935980d347cd6a878e2a7d9b37d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcb583f37a4e3598675657a0d76ffc7b457944e5990a3c9a623566c0ff5cc7a`

```dockerfile
```

-	Layers:
	-	`sha256:9a4967b11cfcd4b7332331e969d31c677eb0f940fde6f38f5c30b05d4a62d0c6`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 4.0 MB (3966253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a2b116ce21e5d1cbbe805d0a9e709d2a8f710b0d177da7e59f6e03a3227428`  
		Last Modified: Fri, 16 Jan 2026 01:37:09 GMT  
		Size: 24.6 KB (24580 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; arm64 variant v8

```console
$ docker pull zookeeper@sha256:fd8d7baa3599e8e64a0543459de97566c28f5374c234d606ddf650efda7649d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112238432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba2306c49665b350cf00111aff4b1ae741433ff5e145c4a7e550e0752b2cbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 01:40:22 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 01:40:22 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 01:40:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 01:40:31 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 01:40:31 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 01:40:31 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:40:34 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 01:40:34 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 01:40:34 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 01:40:34 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 01:40:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 01:40:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 01:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 01:40:34 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fc3ef6de679ecac0a74cc044dd73825b9e6daa54ab0904bc8e9b9e898d5bdd`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 16.1 MB (16065656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d903927893f88ea36a0f1ae2165c1cbabff6244e11daf33512f44c12631acd`  
		Last Modified: Thu, 15 Jan 2026 22:20:06 GMT  
		Size: 46.5 MB (46538233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05322d833bff6a327f4cb5734a53c8ecd0811c295b8d670e977218a9a12d8906`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef01e65ce9e940b87d06c11af62f1cff2016c991c02e0b659ac1826a2466cbd5`  
		Last Modified: Thu, 15 Jan 2026 22:19:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8db862d46a77e2d6af87165369540bbb128353c39fd534ec1bc745786112a`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d24a3dce8810275ea0a98a9d4847c86f2c6efe26c1c24c2a172a64e3646886e`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 1.1 MB (1073564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ef855d439e2ba38f6a9c60b94ee97ffc400b9bb2fad1c85f761f3ee92fc3ad`  
		Last Modified: Fri, 16 Jan 2026 01:40:45 GMT  
		Size: 21.2 MB (21172438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5571b26e6eda3e58c809bb0472faedc92d284e37b9fcec3e3398ee12868a62`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:7049f58e879fb52f615d2f81d20c0ffdef8fc5e8107d7e718dbf7ceeb87409d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1426a88958d7e690dd7c320f94204d0ba351b90887d9a0c5ca38de74b7defe42`

```dockerfile
```

-	Layers:
	-	`sha256:6fa98e02ebea1734a0c9f774c204620face5a266bb372d316b37a0ddf3546d67`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 4.0 MB (3965947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7b504e7afabdfdfe74bf318c5e53ac672e49bb47acfa791a849414ea68cb7e`  
		Last Modified: Fri, 16 Jan 2026 01:40:44 GMT  
		Size: 24.7 KB (24726 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; ppc64le

```console
$ docker pull zookeeper@sha256:0366b3c4391ca9627e353e49c1bac8d62bca65f9df68183ab590ebfcdf9381ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121214870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96de994674f485ed31b035d91d46523fd1f5c1e3a6528d38f860f31de46a9456`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:38:03 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Fri, 16 Jan 2026 02:38:03 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 02:38:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Fri, 16 Jan 2026 02:38:13 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Fri, 16 Jan 2026 02:38:13 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Fri, 16 Jan 2026 02:38:13 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 02:39:14 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Fri, 16 Jan 2026 02:39:15 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Fri, 16 Jan 2026 02:39:15 GMT
VOLUME [/data /datalog /logs]
# Fri, 16 Jan 2026 02:39:15 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Fri, 16 Jan 2026 02:39:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Fri, 16 Jan 2026 02:39:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 16 Jan 2026 02:39:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 02:39:15 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:41 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ca264798509a08ea6ccee410a564b50a0eb5a42f1e58216b34a0c846751eb`  
		Last Modified: Thu, 15 Jan 2026 22:17:15 GMT  
		Size: 46.9 MB (46881201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae30e596f1d1d565a863521696c50833d9594367b6717a150b7660b7f6f7d9`  
		Last Modified: Thu, 15 Jan 2026 22:17:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a011aa1930859a4407f64ffbb4fddcba4751ca856311b708bf6236c1d809dea`  
		Last Modified: Thu, 15 Jan 2026 22:17:14 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf81a92636b3c38340de4646628998f5b1c22a7c602e27b1e888e99525516c32`  
		Last Modified: Fri, 16 Jan 2026 02:38:50 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7142f408493309927e8c69411ed672557055df16f6c06f5dd27b95ef40e336d`  
		Last Modified: Fri, 16 Jan 2026 02:38:50 GMT  
		Size: 1.1 MB (1090111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731431cd69c8ce2bf4f1c16887d0e070bf30d67764c3330552e6eeee8e7ae3cc`  
		Last Modified: Fri, 16 Jan 2026 02:39:48 GMT  
		Size: 21.2 MB (21172362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c2421f3ebbf0a5f025adf9737583775bbab31aad2a425a339c6a9bb3122030`  
		Last Modified: Fri, 16 Jan 2026 02:39:48 GMT  
		Size: 776.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:4476e61e4b3e1e574a91f8f9aca521fe7253c97df9de1799b6d62dca2f5f3935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559477b417ee5258fe91ffba7b61754fedcd87c4df451e8e2059bb4f4052c27b`

```dockerfile
```

-	Layers:
	-	`sha256:e773ce6f5144b02013ce174de5074cc1155043ee616a1c25fbd513cee8fd61ad`  
		Last Modified: Fri, 16 Jan 2026 02:39:47 GMT  
		Size: 4.0 MB (3970362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1b0322bfe3c7f5eda18e5da0338a509542590cf275eff40982a1864c2f89b1`  
		Last Modified: Fri, 16 Jan 2026 02:39:47 GMT  
		Size: 24.6 KB (24633 bytes)  
		MIME: application/vnd.in-toto+json

### `zookeeper:latest` - linux; s390x

```console
$ docker pull zookeeper@sha256:4bd3e6bf1c0f9f94724ade94ed010d58faccbd1fc36be729edf2632720fe28b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110464056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d8e529b78d815667cfaa02e5fb4f9d6a0432d2f6afcf95bc552f9a53686324`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:49 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Thu, 15 Jan 2026 23:07:49 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR" # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true # buildkit
# Thu, 15 Jan 2026 23:07:52 GMT
ARG GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA
# Thu, 15 Jan 2026 23:07:52 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.9.4
# Thu, 15 Jan 2026 23:07:52 GMT
ARG DISTRO_NAME=apache-zookeeper-3.9.4-bin
# Thu, 15 Jan 2026 23:07:56 GMT
# ARGS: GPG_KEY=3F7A1D16FA4217B1DC75E1C9FFE35B7F15DFA1BA SHORT_DISTRO_NAME=zookeeper-3.9.4 DISTRO_NAME=apache-zookeeper-3.9.4-bin
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver hkps://keyserver.pgp.com --recv-key "$GPG_KEY" ||     gpg --keyserver hkps://keyserver.ubuntu.com --recv-keys "$GPG_KEY" ||     gpg --keyserver hkps://pgp.mit.edu --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME" # buildkit
# Thu, 15 Jan 2026 23:07:56 GMT
WORKDIR /apache-zookeeper-3.9.4-bin
# Thu, 15 Jan 2026 23:07:56 GMT
VOLUME [/data /datalog /logs]
# Thu, 15 Jan 2026 23:07:56 GMT
EXPOSE map[2181/tcp:{} 2888/tcp:{} 3888/tcp:{} 8080/tcp:{}]
# Thu, 15 Jan 2026 23:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.9.4-bin/bin ZOOCFGDIR=/conf
# Thu, 15 Jan 2026 23:07:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:56 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:07 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:21 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23c205723170273b192d9e9d8b97c8f22f0d97ed549cebd30eb736b55476e21`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2059e56e4bc25d5f4b1c017b55a0664e3674869eed7702692d591c85c655688f`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 1.1 MB (1106856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6cb1c6792da391a96027dcf3e8aea42df2b6189b93140b8154001bb4a099ad`  
		Last Modified: Thu, 15 Jan 2026 23:08:10 GMT  
		Size: 21.2 MB (21171940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ceee274217c7ff581906ffaee29e8b824a28859ec8cd009db21ac4cd142412`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 775.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `zookeeper:latest` - unknown; unknown

```console
$ docker pull zookeeper@sha256:8e4c7f8f3900631bf1c6fbc225c2577afda76186583bdf81917777d8e09f12f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bc47ebc4fa798087fdcc5986b2a5c0581789cc8e00e7570578c021a52b48d2`

```dockerfile
```

-	Layers:
	-	`sha256:6d57227768de9070e140e046f1cf208fdde8b5e080dbddb5cb51aff80ce46a08`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 4.0 MB (3967843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cb0a4c8a83b944ab976042d096bcde54e897b6d7ccb4c68917768c9f519224`  
		Last Modified: Thu, 15 Jan 2026 23:08:09 GMT  
		Size: 24.6 KB (24579 bytes)  
		MIME: application/vnd.in-toto+json
