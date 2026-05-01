## `solr:slim`

```console
$ docker pull solr@sha256:914878e08f7896eaa8b02504e4fe8962d09991906f3a3432560c33152c7e4a7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `solr:slim` - linux; amd64

```console
$ docker pull solr@sha256:d565ebb7b8271fcaac04bdc6ac0e59ee9b7ca907d714081b4d27a53c3934a15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187069950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac29ad4c5bc87da4da56ec576c21ec6dff922b84a5de99d7c896680caf4a158`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:29:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:29:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:29:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:29:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:29:33 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:29:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:29:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:50:27 GMT
ARG SOLR_VERSION=10.0.0
# Thu, 30 Apr 2026 23:50:27 GMT
ARG SOLR_DIST=-slim
# Thu, 30 Apr 2026 23:50:27 GMT
ARG SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1
# Thu, 30 Apr 2026 23:50:27 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Thu, 30 Apr 2026 23:50:27 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 30 Apr 2026 23:50:27 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 30 Apr 2026 23:50:27 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 30 Apr 2026 23:50:27 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 30 Apr 2026 23:50:27 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 30 Apr 2026 23:50:27 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 30 Apr 2026 23:50:27 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 30 Apr 2026 23:50:27 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 30 Apr 2026 23:50:27 GMT
LABEL org.opencontainers.image.version=10.0.0
# Thu, 30 Apr 2026 23:50:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 Apr 2026 23:50:27 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_HOST_BIND=0.0.0.0 SOLR_ZOOKEEPER_EMBEDDED_HOST=0.0.0.0
# Thu, 30 Apr 2026 23:50:27 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 30 Apr 2026 23:50:27 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 30 Apr 2026 23:50:27 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr; # buildkit
# Thu, 30 Apr 2026 23:50:35 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install curl acl lsof procps wget netcat-openbsd gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 30 Apr 2026 23:50:35 GMT
VOLUME [/var/solr]
# Thu, 30 Apr 2026 23:50:35 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 30 Apr 2026 23:50:35 GMT
WORKDIR /opt/solr
# Thu, 30 Apr 2026 23:50:35 GMT
USER 8983
# Thu, 30 Apr 2026 23:50:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:50:35 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191a1bea837eca9a44b1c34ab4dd5a859fb2c2f0730259b2a733a608ea883bd6`  
		Last Modified: Thu, 30 Apr 2026 23:30:05 GMT  
		Size: 11.5 MB (11479095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe21702fcd1c69c16d0bd83f87aff92266d210ea37d3d040493acf85ac4a62`  
		Last Modified: Thu, 30 Apr 2026 23:30:07 GMT  
		Size: 63.0 MB (63042478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c999e71703cb09c68bab49067fa8d026dc8370282f6135990ac69b0ccb16b37`  
		Last Modified: Thu, 30 Apr 2026 23:30:05 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec46807d01851ae1441d270d9fc716c8d62a38953b0fefc8e05ec355f6f97de`  
		Last Modified: Thu, 30 Apr 2026 23:50:48 GMT  
		Size: 79.0 MB (79044268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8574e6fad3a0b4dc0768f81f0b4c669d2d1f7079e76335d3eecec58034ff68`  
		Last Modified: Thu, 30 Apr 2026 23:50:46 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e1bfbc3bae38f8d0b13181f19efd07bab79695cc1b25f728c8ca1348105030`  
		Last Modified: Thu, 30 Apr 2026 23:50:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6707bf166aa053d33c53ab488e646421deaaeaa245a4f34e3d4a8311b267ce0`  
		Last Modified: Thu, 30 Apr 2026 23:50:46 GMT  
		Size: 10.3 KB (10300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc1a16bf5e712556f0a8e4ff19480134c2f0768ba65ae62cbc45fba1a55f576`  
		Last Modified: Thu, 30 Apr 2026 23:50:47 GMT  
		Size: 3.8 MB (3757115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:b64ef0938ad883c1bdcad0cee6e87c2cb5c9505cd27b09846c32b9fb7c84736e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3481570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dd802e71dd20bda1c09ab3dbcbc93ba85b9b803499225d89a552fff033a265`

```dockerfile
```

-	Layers:
	-	`sha256:0cf84007d501d0534ceae801d6af099d2dff9c671c4a8760b1904f36fc07a9d0`  
		Last Modified: Thu, 30 Apr 2026 23:50:46 GMT  
		Size: 3.4 MB (3447881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85f62d6f470afb4f78efcc86e5e0323c3a14f1c120214c1e8ec6c06ac837cf8c`  
		Last Modified: Thu, 30 Apr 2026 23:50:46 GMT  
		Size: 33.7 KB (33689 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:80fc81ed0a096591b01d7c51f942662df9c817e8a13ee37461d06ab00a7263c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185001875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8672b39c7b720291884fd725e2824a8266c2eff45098fc788930b56f38b4be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:29:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:29:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:29:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:29:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:29:38 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:30:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:30:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:30:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:30:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:49:54 GMT
ARG SOLR_VERSION=10.0.0
# Thu, 30 Apr 2026 23:49:54 GMT
ARG SOLR_DIST=-slim
# Thu, 30 Apr 2026 23:49:54 GMT
ARG SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1
# Thu, 30 Apr 2026 23:49:54 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Thu, 30 Apr 2026 23:49:54 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 30 Apr 2026 23:49:54 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 30 Apr 2026 23:49:54 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 30 Apr 2026 23:49:54 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 30 Apr 2026 23:49:54 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 30 Apr 2026 23:49:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 30 Apr 2026 23:49:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 30 Apr 2026 23:49:54 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 30 Apr 2026 23:49:54 GMT
LABEL org.opencontainers.image.version=10.0.0
# Thu, 30 Apr 2026 23:49:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 Apr 2026 23:49:54 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_HOST_BIND=0.0.0.0 SOLR_ZOOKEEPER_EMBEDDED_HOST=0.0.0.0
# Thu, 30 Apr 2026 23:49:54 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 30 Apr 2026 23:49:54 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 30 Apr 2026 23:49:54 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr; # buildkit
# Thu, 30 Apr 2026 23:50:04 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install curl acl lsof procps wget netcat-openbsd gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 30 Apr 2026 23:50:04 GMT
VOLUME [/var/solr]
# Thu, 30 Apr 2026 23:50:04 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 30 Apr 2026 23:50:04 GMT
WORKDIR /opt/solr
# Thu, 30 Apr 2026 23:50:04 GMT
USER 8983
# Thu, 30 Apr 2026 23:50:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:50:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b502206b1d693f9f65c15a390ab1af25442fef8155a462be7ff05ca7d3e8c7`  
		Last Modified: Thu, 30 Apr 2026 23:30:19 GMT  
		Size: 11.5 MB (11474371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575f27cf1d92903883bac4bec927051337774783b6eaeb93ccc0fbd2a6449c9a`  
		Last Modified: Thu, 30 Apr 2026 23:30:20 GMT  
		Size: 61.9 MB (61943078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd4dab533194e1c28ff921fa8c55c5e3a28c8fe780c0aad21a1b08ddbb34cf4`  
		Last Modified: Thu, 30 Apr 2026 23:30:18 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c4395bcff462f00b48d4dbace36021f9a632daf35353fe62e26d09c9abe584`  
		Last Modified: Thu, 30 Apr 2026 23:50:18 GMT  
		Size: 79.0 MB (79046067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca362bf2aca92e8274a1810733e04079e774a1c55d6562c2f5e0a4eaef93de31`  
		Last Modified: Thu, 30 Apr 2026 23:50:16 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cdd8950165c765c51ef421c1bc735986e15430b7137293e5643da00b29410f`  
		Last Modified: Thu, 30 Apr 2026 23:50:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da73efe78e24fc48b0cdd8f3df56197468236e147fcd1fca82717965271f1003`  
		Last Modified: Thu, 30 Apr 2026 23:50:16 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bc2f1affadeda3783663040bb6f361bf2bd6ffe55867df773bf99cff21d64a`  
		Last Modified: Thu, 30 Apr 2026 23:50:17 GMT  
		Size: 3.6 MB (3648553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:66442b0aaa42598c63c62c6d5a62cbd23963fdac8e0fc6525a62966e8e1ed682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3482200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0277774e95add4523c9b27061eb7f318e96789eeced85fdee29a0dbfe5d2ac`

```dockerfile
```

-	Layers:
	-	`sha256:30f3035cb09bc587bf9aa2a7d5a89b685de92da176b96fa1d809c6c407b8346a`  
		Last Modified: Thu, 30 Apr 2026 23:50:16 GMT  
		Size: 3.4 MB (3448347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6eefa09ec4db7fa0e3c182636457ed54e1775d237fc91db366636b0b1d6b064`  
		Last Modified: Thu, 30 Apr 2026 23:50:16 GMT  
		Size: 33.9 KB (33853 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:08e7394c1d3cdac40fc7b5c18688d81ed489413fe9990da2061c3b1dc023ad93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192201172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eb0da885494214d8a57aba8020d2316e81a59db8bb4c24726431801adfcd52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:27:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:27:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:27:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:27:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:27:31 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:29:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:29:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:29:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:29:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:59:31 GMT
ARG SOLR_VERSION=10.0.0
# Thu, 30 Apr 2026 23:59:31 GMT
ARG SOLR_DIST=-slim
# Thu, 30 Apr 2026 23:59:31 GMT
ARG SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1
# Thu, 30 Apr 2026 23:59:31 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Thu, 30 Apr 2026 23:59:31 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 30 Apr 2026 23:59:31 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 30 Apr 2026 23:59:31 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 30 Apr 2026 23:59:31 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 30 Apr 2026 23:59:31 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 30 Apr 2026 23:59:31 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 30 Apr 2026 23:59:31 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 30 Apr 2026 23:59:31 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 30 Apr 2026 23:59:31 GMT
LABEL org.opencontainers.image.version=10.0.0
# Thu, 30 Apr 2026 23:59:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 Apr 2026 23:59:31 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_HOST_BIND=0.0.0.0 SOLR_ZOOKEEPER_EMBEDDED_HOST=0.0.0.0
# Thu, 30 Apr 2026 23:59:32 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 30 Apr 2026 23:59:32 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 30 Apr 2026 23:59:33 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr; # buildkit
# Fri, 01 May 2026 00:00:16 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install curl acl lsof procps wget netcat-openbsd gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 01 May 2026 00:00:16 GMT
VOLUME [/var/solr]
# Fri, 01 May 2026 00:00:16 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 01 May 2026 00:00:18 GMT
WORKDIR /opt/solr
# Fri, 01 May 2026 00:00:18 GMT
USER 8983
# Fri, 01 May 2026 00:00:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 00:00:18 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11468cd83b98e641dde5c21c5e1938721c488b185fde118f5fffd875549e49ac`  
		Last Modified: Thu, 30 Apr 2026 23:30:21 GMT  
		Size: 12.0 MB (12046030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcaae897d5871bd31d9ab8e475ad91141d12f3017fc8f8459836dccb8eb2cee`  
		Last Modified: Thu, 30 Apr 2026 23:30:23 GMT  
		Size: 62.4 MB (62443184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc449840d8a6873ea12af42d72b0a72a6eeef0397398f02439b6533c3705c51`  
		Last Modified: Thu, 30 Apr 2026 23:30:21 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778c7bf06104eeff7c86cc5cf1b5c2342f5329f447e292c25b3e9d165251ecef`  
		Last Modified: Fri, 01 May 2026 00:01:00 GMT  
		Size: 79.1 MB (79113717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de24c4f1fa7a32bb4e3f581e0de476d8afe1da91643d4b4a6d87c6e6533c4c08`  
		Last Modified: Fri, 01 May 2026 00:00:57 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4149df4dec11cc84b4860218639e1bbb5af2024700d62b510d2f04692c3c8e88`  
		Last Modified: Fri, 01 May 2026 00:00:57 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72614c1008d1c0b4cdc426f2dd087df52b6aa1ea8ebb5f448c91353dbc32072`  
		Last Modified: Fri, 01 May 2026 00:01:03 GMT  
		Size: 10.3 KB (10308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a290c3b2193527e4d542044d5fbd929a9993866afc0ff8c7820a99059e651f4a`  
		Last Modified: Fri, 01 May 2026 00:01:00 GMT  
		Size: 4.3 MB (4270040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:39395cc255490d004d8347f9115cc898ea70627eec5a348b4946595e80ffde54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d34dda2733e9bad5b7e6315b9f033f66f9de8410ad6870876711be250f811f`

```dockerfile
```

-	Layers:
	-	`sha256:ebee64e75b7c3c42f0cca3779eaadd124a0b2bdf5bede62f6aee8e298f70f50e`  
		Last Modified: Fri, 01 May 2026 00:00:57 GMT  
		Size: 3.5 MB (3451314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:924af98cb92f366fa5958ed4e0cd9175a91584593bda164b27041c46bb470ab1`  
		Last Modified: Fri, 01 May 2026 00:00:56 GMT  
		Size: 33.7 KB (33741 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; riscv64

```console
$ docker pull solr@sha256:00c23a9d295f1bedc267be09d54803e9f455c38c04c57d20425eb17bef0b8919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187056775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3100cbb0aefc276913ec1805eec038d42eab6a10ca4bb637144bbcae7158ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:24:05 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:24:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:24:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 09:24:43 GMT
ADD file:a9a4679e3df2846468311b83a8f6ab86f5a205bab966d3f236c9f30151010c5b in / 
# Fri, 10 Apr 2026 09:24:47 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 17:16:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 17:16:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 17:16:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Apr 2026 17:16:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 17:16:29 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:49:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:49:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:49:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:49:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 May 2026 00:42:00 GMT
ARG SOLR_VERSION=10.0.0
# Fri, 01 May 2026 00:42:00 GMT
ARG SOLR_DIST=-slim
# Fri, 01 May 2026 00:42:00 GMT
ARG SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1
# Fri, 01 May 2026 00:42:00 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Fri, 01 May 2026 00:42:00 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 01 May 2026 00:42:00 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.version=10.0.0
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 01 May 2026 00:42:00 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_HOST_BIND=0.0.0.0 SOLR_ZOOKEEPER_EMBEDDED_HOST=0.0.0.0
# Fri, 01 May 2026 00:42:01 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 01 May 2026 00:42:01 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 01 May 2026 00:42:02 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr; # buildkit
# Fri, 01 May 2026 00:42:54 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install curl acl lsof procps wget netcat-openbsd gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 01 May 2026 00:42:54 GMT
VOLUME [/var/solr]
# Fri, 01 May 2026 00:42:54 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 01 May 2026 00:42:54 GMT
WORKDIR /opt/solr
# Fri, 01 May 2026 00:42:54 GMT
USER 8983
# Fri, 01 May 2026 00:42:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 00:42:54 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb1da3a1b0530db8bac4f80d6d7cf1cab174ba1fdb49b966e841ec211df17d0`  
		Last Modified: Thu, 16 Apr 2026 17:21:23 GMT  
		Size: 11.6 MB (11570962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40941cf16e4717c40e5532cf516bb886886846120960f18c87affbe922325b4e`  
		Last Modified: Thu, 30 Apr 2026 23:52:33 GMT  
		Size: 61.7 MB (61693654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614352beef2c40d720b7a1387b3a660d056f4e7578072704da8135acd2507070`  
		Last Modified: Thu, 30 Apr 2026 23:52:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a32acaa0c958dd35c41fc929f97715d724c7b774c338fadf79adea2341a238f`  
		Last Modified: Fri, 01 May 2026 00:45:51 GMT  
		Size: 79.1 MB (79059662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c1e3aa794edab81bb50eb594d17eb5ade7d6496c3ebc0fc5a006864296a72b`  
		Last Modified: Fri, 01 May 2026 00:45:38 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a84217abb97ae3c82e4cc4e4b224daee86fcc12766b8544268c4baf6131621`  
		Last Modified: Fri, 01 May 2026 00:45:38 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42865751b78261e36a3111ab399b126b0cdda6723015a3d03332839304dc8165`  
		Last Modified: Fri, 01 May 2026 00:45:39 GMT  
		Size: 10.3 KB (10317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea4e6000daf030a8f3906598a073d4c30ec58f9f0a5cca09398f12e73a79fc1`  
		Last Modified: Fri, 01 May 2026 00:45:41 GMT  
		Size: 3.8 MB (3753138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:8c315e710a658aedf232886642e39bb0267a6cd3c5b90311128f3d5318340e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3473687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19fff30edf6206a3bae156dec463eb0cac96f4ec0a01006300bc78ee3fc650d`

```dockerfile
```

-	Layers:
	-	`sha256:2b69029512db8161265e11687c7ec7be15f14a15d520d186d5a58fc0b410dc5f`  
		Last Modified: Fri, 01 May 2026 00:45:39 GMT  
		Size: 3.4 MB (3439946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5adaa68da26cc006ef4df9cfd06b61b571a24d02d0dfe6b17bd356d1c2ff2968`  
		Last Modified: Fri, 01 May 2026 00:45:38 GMT  
		Size: 33.7 KB (33741 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:39e4a91352c2e1f6933a7d567dd8ae20acadfcc2d0424344e48a167e22cd28d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185084632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe3bd7eff7e3fee10e8b6ebdde0277151dd1054479a239869f46004be480686`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:25:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:25:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:25:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:25:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:25:40 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:25:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:25:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:25:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:25:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:47:22 GMT
ARG SOLR_VERSION=10.0.0
# Thu, 30 Apr 2026 23:47:22 GMT
ARG SOLR_DIST=-slim
# Thu, 30 Apr 2026 23:47:22 GMT
ARG SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1
# Thu, 30 Apr 2026 23:47:22 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Thu, 30 Apr 2026 23:47:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 30 Apr 2026 23:47:22 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 30 Apr 2026 23:47:22 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 30 Apr 2026 23:47:22 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 30 Apr 2026 23:47:22 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 30 Apr 2026 23:47:22 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 30 Apr 2026 23:47:22 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 30 Apr 2026 23:47:22 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 30 Apr 2026 23:47:22 GMT
LABEL org.opencontainers.image.version=10.0.0
# Thu, 30 Apr 2026 23:47:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 Apr 2026 23:47:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_HOST_BIND=0.0.0.0 SOLR_ZOOKEEPER_EMBEDDED_HOST=0.0.0.0
# Thu, 30 Apr 2026 23:47:23 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 30 Apr 2026 23:47:23 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 30 Apr 2026 23:47:23 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr; # buildkit
# Thu, 30 Apr 2026 23:47:31 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install curl acl lsof procps wget netcat-openbsd gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 30 Apr 2026 23:47:31 GMT
VOLUME [/var/solr]
# Thu, 30 Apr 2026 23:47:31 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 30 Apr 2026 23:47:31 GMT
WORKDIR /opt/solr
# Thu, 30 Apr 2026 23:47:31 GMT
USER 8983
# Thu, 30 Apr 2026 23:47:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:47:31 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e83b9b6edbfd65a81ce2bb644e5ddcfbe6b86f7a2f84acc79561254e03fa78`  
		Last Modified: Thu, 30 Apr 2026 23:26:12 GMT  
		Size: 11.8 MB (11757245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0530f96093e62e331b5a7ce5cc7e8c1d41cb0637ab419ceaab0fd2535d3548`  
		Last Modified: Thu, 30 Apr 2026 23:26:13 GMT  
		Size: 60.5 MB (60531717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8cb8f6d8622017f7f74b8413fcef7d39bf1df0473dfe77822b73e57c464c7`  
		Last Modified: Thu, 30 Apr 2026 23:26:11 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64512c010e272068d07ac6b6109e8c43c9dbe94aec615232475eedebba232f96`  
		Last Modified: Thu, 30 Apr 2026 23:47:51 GMT  
		Size: 79.1 MB (79069753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68230ff77ebc95aec5c5202d90c7f6c2e4e9762346e83b331e3239aa77186339`  
		Last Modified: Thu, 30 Apr 2026 23:47:49 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934587ced9519f204712400e3fd83e2b68664b5aafc4acc4bf2b11a1def274c6`  
		Last Modified: Thu, 30 Apr 2026 23:47:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c40d47aee7040c2b59f92e7e1fd6e189506a5412537be5e1628c14d0098efb`  
		Last Modified: Thu, 30 Apr 2026 23:47:49 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fb52686e951b4c0a8cf15bee6067fd458b801cf65dff9095ef069f33e4a999`  
		Last Modified: Thu, 30 Apr 2026 23:47:50 GMT  
		Size: 3.8 MB (3799749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:eec1dfc19db2201f8b75518a814a8b10d8c6948cf61e661585790a54e401a06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3483151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd5e4d21d9036b86a9ae2ff9e8b0ccb9a221cbcfcaa104e3ce6c4dc612685de`

```dockerfile
```

-	Layers:
	-	`sha256:b8ad14a69f7221891d42dee4450de16996f25b0872b2f8be351e53a7a0f21f2c`  
		Last Modified: Thu, 30 Apr 2026 23:47:49 GMT  
		Size: 3.4 MB (3449462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6fe19be86d563ff2bd1907a4f465bef2c11b5e7029fece8263dba708308b6aa`  
		Last Modified: Thu, 30 Apr 2026 23:47:49 GMT  
		Size: 33.7 KB (33689 bytes)  
		MIME: application/vnd.in-toto+json
