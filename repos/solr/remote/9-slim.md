## `solr:9-slim`

```console
$ docker pull solr@sha256:7bcb15f1b63ec63113594a4dafdfe931d42ff7b964fd4ee91d8180d5195f36ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `solr:9-slim` - linux; amd64

```console
$ docker pull solr@sha256:95480c37254b3401ac002b8696816a11bc6030f9fdfc07ca08b10bbbb5f5d2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156921707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2690981516028da8743a9abf3e8fe1a32a4c6cec79355054585f63fa04c292a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_VERSION=9.6.0
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DIST=-slim
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.version=9.6.0
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Apr 2024 18:14:55 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
VOLUME [/var/solr]
# Sat, 27 Apr 2024 18:14:55 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 27 Apr 2024 18:14:55 GMT
WORKDIR /opt/solr
# Sat, 27 Apr 2024 18:14:55 GMT
USER 8983
# Sat, 27 Apr 2024 18:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7c5a42f2fad87126e0a61b4605e0b8b0b8100485fbffb0fa0e14e87400873`  
		Last Modified: Thu, 25 Apr 2024 22:13:22 GMT  
		Size: 12.9 MB (12905143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7fcad56b7f8a33a6681a9ae067f80cc8ad2a08502172c8dda569c1338752bc`  
		Last Modified: Thu, 25 Apr 2024 22:16:38 GMT  
		Size: 47.3 MB (47256188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75513697e6ba945551856344dc1f1c94b25b9b98458dd13e8f1a25811e2424cc`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e30da527722230ddaac2aa5e9ae62f333caa596c7853ae2b516c06d2d6f321f`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a14e01495f1b688faf84b902dab05640b9d7468884a43b5b426f3f82d5f2f`  
		Last Modified: Tue, 30 Apr 2024 17:50:03 GMT  
		Size: 64.7 MB (64715902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f3adab263f0af8849e392bae1cb10ff1592305d0dff84bb42c39db7c9d8d59`  
		Last Modified: Tue, 30 Apr 2024 17:50:01 GMT  
		Size: 4.3 KB (4269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3a156a07fe2d6184684d789e9209c5b3f55ea9295cb50335b14999eb438a13`  
		Last Modified: Tue, 30 Apr 2024 17:50:01 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ae31268d650853fda280c58fcd1893f349b969b2ad07d4cda3d0804aab740`  
		Last Modified: Tue, 30 Apr 2024 17:50:01 GMT  
		Size: 10.8 KB (10779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f413b5bff9ef4f01f8deb685ce2a59ebe00077d545d2787fa6a3aa63c18be6`  
		Last Modified: Tue, 30 Apr 2024 17:50:02 GMT  
		Size: 1.6 MB (1588558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:306cce5071760fe6c497bed44f767e1f8c552ab5c68c7e9b08b867d6c57f4f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef19780939ee7d36fbda9693d342214f0f591f14238338367647972f99b97cf`

```dockerfile
```

-	Layers:
	-	`sha256:0fe36c84f8be67fce5a1d2225e6dd99b5d5163d47fb586f9d2756c2f227860af`  
		Last Modified: Tue, 30 Apr 2024 17:50:01 GMT  
		Size: 3.7 MB (3657605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ecb7c0b462dfa9b46205a658bb3143588e0e01af56c0488653b175c2250cae4`  
		Last Modified: Tue, 30 Apr 2024 17:50:01 GMT  
		Size: 34.9 KB (34870 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:2beae48ffbc8bb715aa7026ac64f6996c9a25b9f6ac03a110dad28130422d820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151089961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a5396e221435de90434851d69bb3e683b4d90ff911b2a98640d50cbdaa7e59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 17 Apr 2024 18:29:44 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:29:46 GMT
ADD file:511fd2f076c60f46f9185a7e8c176585251f3eec5c08d6b4cb8efdb0a9bb53fb in / 
# Wed, 17 Apr 2024 18:29:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_VERSION=9.6.0
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DIST=-slim
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.version=9.6.0
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Apr 2024 18:14:55 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
VOLUME [/var/solr]
# Sat, 27 Apr 2024 18:14:55 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 27 Apr 2024 18:14:55 GMT
WORKDIR /opt/solr
# Sat, 27 Apr 2024 18:14:55 GMT
USER 8983
# Sat, 27 Apr 2024 18:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:071d1faceffed6640d770a55f271b5d135ce2ffc51ec5653810e9f20e5c4c5fd`  
		Last Modified: Thu, 18 Apr 2024 01:33:02 GMT  
		Size: 27.5 MB (27534148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002cecbb9c98fb3389e41e26f05485fc9e85f910cff583a691fbb102ee905a42`  
		Last Modified: Thu, 25 Apr 2024 20:32:45 GMT  
		Size: 12.5 MB (12492638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f6e0163838b603fff5bd2b859818d2d4d95b42e5a473d9aeb55caae0dd9294`  
		Last Modified: Thu, 25 Apr 2024 20:35:54 GMT  
		Size: 44.9 MB (44917119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce20dd53ab5e75776355fb45f6ef2d2608f516124b855ad4991912ef1853286`  
		Last Modified: Thu, 25 Apr 2024 20:35:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c43bb76d1f4547b0f77e71254784d3235488fff0d81419914a76540c4179e2`  
		Last Modified: Thu, 25 Apr 2024 20:35:47 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921be9c76e0031f55cfe81b01a385e83c63d5efe08e1f4d7adf7ca6ac93c1fd9`  
		Last Modified: Tue, 30 Apr 2024 18:06:40 GMT  
		Size: 64.7 MB (64716173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e99db607073197f108b63ea9cb6213f0cd91320da924db4a44041152977fbe`  
		Last Modified: Tue, 30 Apr 2024 18:06:37 GMT  
		Size: 4.2 KB (4203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ffbf9a4cd9af543704819359800cdd76849df1dbf2c7c8d8c14ec06a96b974`  
		Last Modified: Tue, 30 Apr 2024 18:06:37 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26535b240a01c948fe1d1e5852975bfc4ff261d6a304cd5c6864b71825bbd8ec`  
		Last Modified: Tue, 30 Apr 2024 18:06:37 GMT  
		Size: 10.8 KB (10776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5a71f8b664584652278658a89726c82a47b64f0e2123592a5c7112ed4410a9`  
		Last Modified: Tue, 30 Apr 2024 18:06:39 GMT  
		Size: 1.4 MB (1413766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:8c41a07f9900b746cf2047d6c419f9fb265b8405fb07af11d1800b40af5b2e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3693158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179bb86e653e5a55f41f6c1d57e703f6969243141ea35369414dad2facece2bf`

```dockerfile
```

-	Layers:
	-	`sha256:bb9c44f945fd78e7d417a9db9ed0b21a8e2889be65c8ea0b07ce425c2c4624b1`  
		Last Modified: Tue, 30 Apr 2024 18:06:37 GMT  
		Size: 3.7 MB (3658982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c31b3ce9efa00322e601868d7ae0ca16ad0a22640ea95af1eda9d1b6f4a99e`  
		Last Modified: Tue, 30 Apr 2024 18:06:37 GMT  
		Size: 34.2 KB (34176 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:04201f1bdfc5ded52925cafc4161a73c8dee8eff19fcc28650a5804c57704c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154143828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3bca509c23dab9aaacefb79685cb5223d801b973fcf49e086e465df0075d0f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_VERSION=9.6.0
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DIST=-slim
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.version=9.6.0
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Apr 2024 18:14:55 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
VOLUME [/var/solr]
# Sat, 27 Apr 2024 18:14:55 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 27 Apr 2024 18:14:55 GMT
WORKDIR /opt/solr
# Sat, 27 Apr 2024 18:14:55 GMT
USER 8983
# Sat, 27 Apr 2024 18:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f037ef0398100188bd636ef3da1525cc5cc7f04347a802ecc28ba3240408631`  
		Last Modified: Thu, 25 Apr 2024 21:59:12 GMT  
		Size: 12.8 MB (12846901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a9d01cdbea836fa98a88c869097ca339c17dd29480bc1c936f937840fbde4d`  
		Last Modified: Thu, 25 Apr 2024 22:02:15 GMT  
		Size: 46.7 MB (46716123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e659b60df2e1030cfa0f2df9583f9aab145276e83a37490b983bbcfa9322fde3`  
		Last Modified: Thu, 25 Apr 2024 22:02:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f320f164b70019d3de719bb4a4b380f596330be1d584f5d935f80a4344b5b48`  
		Last Modified: Thu, 25 Apr 2024 22:02:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e753d2e53c93de2594e27b552a0248f513495624c530f01c85d5af3892278f39`  
		Last Modified: Tue, 30 Apr 2024 18:32:32 GMT  
		Size: 64.7 MB (64716154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6205346dc5391cb4621e4703351e887aac5c99bd9961ed3cd6c0fe32b84ec45`  
		Last Modified: Tue, 30 Apr 2024 18:32:30 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e28abb1c77a161977129506f6bcf7fd7728a9d181902ceff78831adb1f0c114`  
		Last Modified: Tue, 30 Apr 2024 18:32:30 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec73048edbd1920d01d903e2ad213621af17423a9c7fc6a13a002e119b28741`  
		Last Modified: Tue, 30 Apr 2024 18:32:30 GMT  
		Size: 10.8 KB (10778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86739035b8b1a1de363f43dbe41c1c22043723209e8ec7b831e98497c9f76875`  
		Last Modified: Tue, 30 Apr 2024 18:32:31 GMT  
		Size: 1.4 MB (1447422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:f0597c04bf19c16cb416470ff0294573a82127f1468b0a115e191a9cdb82d0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971e8f55d6a7d2e475f995545705b6e2c45c15dd7c177b8824ffe1fe35136ae9`

```dockerfile
```

-	Layers:
	-	`sha256:bcc17f1cf98ba25002a8f16aa7749ae140e3b564eac62d6891ee36990d26f40f`  
		Last Modified: Tue, 30 Apr 2024 18:32:30 GMT  
		Size: 3.7 MB (3657853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6ab96d5495c50a2310fd88a2fc343b5ff7ebf4dd7d909779c5952fbd1169c5`  
		Last Modified: Tue, 30 Apr 2024 18:32:30 GMT  
		Size: 34.1 KB (34064 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:6b6bbbdf6ca25e9963113a9e574756d8c4185cc90f6b9ac1490b0dcb22992aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162772645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20a3dd330f865dfc70d01acd396fc13871e08529c5b0450f5527d5222d45f72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 17 Apr 2024 17:51:23 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:51:27 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Wed, 17 Apr 2024 17:51:27 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_VERSION=9.6.0
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DIST=-slim
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.version=9.6.0
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Apr 2024 18:14:55 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
VOLUME [/var/solr]
# Sat, 27 Apr 2024 18:14:55 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 27 Apr 2024 18:14:55 GMT
WORKDIR /opt/solr
# Sat, 27 Apr 2024 18:14:55 GMT
USER 8983
# Sat, 27 Apr 2024 18:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a9466735f8829921e05503ca4d4d92bb6f06facd77aa4b2feb86645d7c27b1ba`  
		Last Modified: Thu, 25 Apr 2024 20:35:05 GMT  
		Size: 35.6 MB (35588305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0de467fd0448940d36a45afa474251ce2e8bd6e8f60ef7eb65adb86c07161a`  
		Last Modified: Thu, 25 Apr 2024 20:52:58 GMT  
		Size: 13.8 MB (13767010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139c1ea4e64d0b726f7d19518870f27a28d6bc36f6ac3db66d8eb91060a294de`  
		Last Modified: Thu, 25 Apr 2024 20:56:22 GMT  
		Size: 47.1 MB (47088915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8b1496c6d2c3bf4eee8880414a7a0f10b22fecc23b08012e3d6e7580bd8ac5`  
		Last Modified: Thu, 25 Apr 2024 20:56:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016cbc90916d690e8bd5221d91fa763a9df5fed03fdf320b50d50025a43d31ef`  
		Last Modified: Thu, 25 Apr 2024 20:56:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2146ee99bd4a403d023d4ef7fd8a4363eff70cff905db9300fe2b53c502064d4`  
		Last Modified: Tue, 30 Apr 2024 18:08:43 GMT  
		Size: 64.7 MB (64716572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773045df9ba0e1da88ef018685f92b5b49e08d0a8ba53916413b30869648e76`  
		Last Modified: Tue, 30 Apr 2024 18:08:41 GMT  
		Size: 4.3 KB (4281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a66ac5b87635f2ac59b7243a739e24c73559ab2487dcc36b2009962065d596c`  
		Last Modified: Tue, 30 Apr 2024 18:08:41 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246dbd1d48c35d975e7868d6568b72bf62297a4af5b9a2a70b82e7fa536f78c`  
		Last Modified: Tue, 30 Apr 2024 18:08:41 GMT  
		Size: 10.8 KB (10783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec8fd190ead737aa290e981d91cb27fc0dd13e37ac6bccbbefbf955fe9b554e`  
		Last Modified: Tue, 30 Apr 2024 18:08:43 GMT  
		Size: 1.6 MB (1595638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:9ccf5f357011b04edd903c4cda9f5cf4cf47e91b7c4d399f6421f41a7a2e4663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e85a77a90403e32c898f672674bb070285eea66b2925835eca11e0987cdb545`

```dockerfile
```

-	Layers:
	-	`sha256:53ecde03db26ddb7c7be7d6188a6757eae9b627e6654ac3ce847e367b7eed6ef`  
		Last Modified: Tue, 30 Apr 2024 18:08:41 GMT  
		Size: 3.7 MB (3662131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9eba067685ca0e68872fb31e66a1d16f582a0a37f81fa0763434cf6c6b2f098`  
		Last Modified: Tue, 30 Apr 2024 18:08:41 GMT  
		Size: 34.1 KB (34100 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:9a72540c39120181b2e4941f5a59c88ce53f7b413ac117563eb76bb06b406dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151722729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e04b78bf8608a864aceeb0a8fac2311f44a2c5ae8aa47051682b41d9a49c4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 17 Apr 2024 18:42:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:42:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:42:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:42:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:42:34 GMT
ADD file:f721f8e69988c4a423ddfb143b1001213ba52ffe029e8623c2f62e210d611fbc in / 
# Wed, 17 Apr 2024 18:42:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_VERSION=9.6.0
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DIST=-slim
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.version=9.6.0
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Apr 2024 18:14:55 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=9.6.0 SOLR_DIST=-slim SOLR_SHA512=deb3585aa25edbcb919109c8388bbc8c1efb136880628ccd1b057daaf6bab1e9ebcd7189465f28db35ae6990ed5bf2127cc95a18b6b4da6abfa33b10d5e5cc37 SOLR_KEYS=1CF0DAD1470504C4EA95C697140BC45803B03F7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
VOLUME [/var/solr]
# Sat, 27 Apr 2024 18:14:55 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 27 Apr 2024 18:14:55 GMT
WORKDIR /opt/solr
# Sat, 27 Apr 2024 18:14:55 GMT
USER 8983
# Sat, 27 Apr 2024 18:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a9e3c76851ed4cb17ff69f864b6230094c69b50fc344074f5cccf18cabee6dbf`  
		Last Modified: Thu, 25 Apr 2024 20:58:17 GMT  
		Size: 28.6 MB (28637471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256964579a885020253dbe5c22f56c46052445d333305990618830cec3421a61`  
		Last Modified: Thu, 25 Apr 2024 21:19:46 GMT  
		Size: 13.0 MB (12986661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed742935159ae2c8d2eb3c9f9c197cd910b010bd4da24fa3b3742f4d490ab32a`  
		Last Modified: Thu, 25 Apr 2024 21:21:38 GMT  
		Size: 43.8 MB (43830966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb485526c73c1b0a7f4587028c9115bb0d739697e08a0ecee6641e11aca6ac9`  
		Last Modified: Thu, 25 Apr 2024 21:21:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c371f0304c7553249d1955cd601fbf909fbe857da6c62e96f58b2ea42297afaf`  
		Last Modified: Thu, 25 Apr 2024 21:21:32 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b8c17e787411a1acd4e96456b80d350c23535efdba40032aee2213d6afd070`  
		Last Modified: Tue, 30 Apr 2024 18:06:36 GMT  
		Size: 64.7 MB (64716192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0865a1d8b5426f8c846951450c4cb2959e97c2117f99cc8f489baa32e233743`  
		Last Modified: Tue, 30 Apr 2024 18:06:34 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8580bb3bcd85c5bf2651e8da3a608230db968cac6627549fe76bc7538dab312`  
		Last Modified: Tue, 30 Apr 2024 18:06:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a848b9bdd72150e763ae0abfa9a8e4fe9f7a6000a886eeb878250f11593605b1`  
		Last Modified: Tue, 30 Apr 2024 18:06:34 GMT  
		Size: 10.8 KB (10776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3211236c8f7332d8c82ea5772eda8d511dd73748f99f2a814317303c412dd92d`  
		Last Modified: Tue, 30 Apr 2024 18:06:35 GMT  
		Size: 1.5 MB (1535219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:26fe96e151c49c045ffdc83a8a2b8d4626b710c306e39ae1e2a7bf688ffa1d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c7940bb930fde906bcebb6ffee742e3e2483de88718f7c6fe360d92dfb4ed0`

```dockerfile
```

-	Layers:
	-	`sha256:e57144889e7d690cd516aa1fba7f0ad32ef66cdd314be0ba24cd8a0df7dc47a9`  
		Last Modified: Tue, 30 Apr 2024 18:06:34 GMT  
		Size: 3.7 MB (3658869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:552eab2fdbe4d4b901b82324c1106de02649bab78dc51c1bb0c7b6464e7ef2d1`  
		Last Modified: Tue, 30 Apr 2024 18:06:34 GMT  
		Size: 34.1 KB (34054 bytes)  
		MIME: application/vnd.in-toto+json
