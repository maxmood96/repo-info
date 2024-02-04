## `solr:9-slim`

```console
$ docker pull solr@sha256:359960e66ed928535f8f020fec9b725c6447a736b755341393034ce84362b464
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
$ docker pull solr@sha256:1b9966368a3269de83ebced9f9cde16d610a59be2d1827247e2f776b1771a73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160804479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef30eca27bb75a1ae7978aab1b5a9229aa49d7fc4e031ffaf1e160e1a3f7dd93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 18:38:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 18:38:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 18:38:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 18:38:04 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 18:38:04 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 18:38:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_VERSION=9.4.1
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_DIST=-slim
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.version=9.4.1
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 25 Jan 2024 18:38:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
VOLUME [/var/solr]
# Thu, 25 Jan 2024 18:38:04 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 25 Jan 2024 18:38:04 GMT
WORKDIR /opt/solr
# Thu, 25 Jan 2024 18:38:04 GMT
USER 8983
# Thu, 25 Jan 2024 18:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jan 2024 18:38:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26611c45681a8966387aee7b2e1494405e20bc5a46dc5da0af9228c45f8e8ec4`  
		Last Modified: Fri, 02 Feb 2024 07:50:10 GMT  
		Size: 17.5 MB (17458288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7657bba016afbc9b5b668492429479081862469157560f39c722fca733c6a4e7`  
		Last Modified: Fri, 02 Feb 2024 07:50:54 GMT  
		Size: 47.2 MB (47163193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c532b683186e5e796b6523fee32e214bd7eeda453b630d2322010697be91e8`  
		Last Modified: Fri, 02 Feb 2024 07:50:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e11da758202f5d3e080b1205b5f37c11a0ca72e8d428ba219b7d9d99befe18`  
		Last Modified: Fri, 02 Feb 2024 07:50:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a58f1fde4f9e04eba4c17a12da3457525d243c71fdb22a9115a38b4e89959b2`  
		Last Modified: Fri, 02 Feb 2024 08:55:17 GMT  
		Size: 64.1 MB (64128293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6b1715de5a01022dcda54b32fa8cc7d7ba0aec80268cc86a232617b87a931b`  
		Last Modified: Fri, 02 Feb 2024 08:55:16 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64316e9573e00364197fb091ecc91498894d9a17ca8205669dd29ada62f349d8`  
		Last Modified: Fri, 02 Feb 2024 08:55:16 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afc8cc3da7c4d5b00c895d8f340de2d0d1958a5b7dc3903cf52d31fd49e45`  
		Last Modified: Fri, 02 Feb 2024 08:55:17 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150c5636e4d6c8083872d0db36904adc259450779b74a43706cdf512060741d6`  
		Last Modified: Fri, 02 Feb 2024 08:55:17 GMT  
		Size: 1.6 MB (1590734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:d4710c823c48227efadc60b0b3278686f7eda94aad0b7ba0951663ce72acb13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3366666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b699f74671f15bdb5f665ce7718372ea322d1b2809915f5649fc592ac85462b`

```dockerfile
```

-	Layers:
	-	`sha256:52cba39cc63dcf5c137c4c2440a5205771b1c1fb5e439867db100a2d73608c5a`  
		Last Modified: Fri, 02 Feb 2024 08:55:16 GMT  
		Size: 3.3 MB (3331799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077ae226d55a722adf5635a61645c5228148a9d1fe5d0749312255105e0a93a0`  
		Last Modified: Fri, 02 Feb 2024 08:55:15 GMT  
		Size: 34.9 KB (34867 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:2195ad211c499f75441702b2ffc019f44103eab97c5dd9bea2ea699c86156488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155476006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddc2032d71632ce0a6df9162e20119db581c2db3a6a22b95505f283c5a58c1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:53 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:00 GMT
ADD file:4ba96538a312573f561a65d64c11d4fdcdd435be02139f66ef9f44c4fd9507cd in / 
# Thu, 25 Jan 2024 17:57:00 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 18:38:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 18:38:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 18:38:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 18:38:04 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 18:38:04 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 18:38:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_VERSION=9.4.1
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_DIST=-slim
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.version=9.4.1
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 25 Jan 2024 18:38:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
VOLUME [/var/solr]
# Thu, 25 Jan 2024 18:38:04 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 25 Jan 2024 18:38:04 GMT
WORKDIR /opt/solr
# Thu, 25 Jan 2024 18:38:04 GMT
USER 8983
# Thu, 25 Jan 2024 18:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jan 2024 18:38:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:708d435a5d58f83439fc15ec09677faf51737e48d41a910750f0f6e9ef7285fe`  
		Last Modified: Fri, 26 Jan 2024 09:13:01 GMT  
		Size: 27.5 MB (27526382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c06b8a18876a77d3871437218031ef7718974677f2d62467e5cf313b116f80`  
		Last Modified: Thu, 01 Feb 2024 23:48:30 GMT  
		Size: 17.6 MB (17590415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d94f3c174e0bc77129c707ebadfb80513995148b69ccae6e9b28cb6af8dda7`  
		Last Modified: Thu, 01 Feb 2024 23:49:16 GMT  
		Size: 44.8 MB (44798812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9f28238346c21ae64d39651a3503334e14ef8d30f18b8e50f2cb9f10a847cd`  
		Last Modified: Thu, 01 Feb 2024 23:49:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b870cb35aeae4f07490ae358ce0a559e8cd3806e639dd5f67346e67994b241d4`  
		Last Modified: Thu, 01 Feb 2024 23:49:08 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380eebcff6077363489065bcabcdcbc7caba57a682659c42a1225aebf2976603`  
		Last Modified: Sun, 04 Feb 2024 00:44:44 GMT  
		Size: 64.1 MB (64128519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1404f3b41b678302707aa9134912bc36c41e714938b5ee58970266a38b8558`  
		Last Modified: Sun, 04 Feb 2024 00:44:42 GMT  
		Size: 4.2 KB (4201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4692469d5f5c7e7facdf2244db52692f99cdbe2f83d9133b43a8faae48563f7f`  
		Last Modified: Sun, 04 Feb 2024 00:44:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d6b499d44f79bf5f0d6148e225be353b9c2ffa33b1e0e137a17267102785b4`  
		Last Modified: Sun, 04 Feb 2024 00:44:42 GMT  
		Size: 10.7 KB (10673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4921c511059dabbef78a90d2abd82581dc1bec850a0ea8161e269c87aa9831a6`  
		Last Modified: Sun, 04 Feb 2024 00:44:43 GMT  
		Size: 1.4 MB (1415866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:9f1f6adf6fd8f3a04f8ef492a721e4d76412655321fe9dfe3d4a2a2bf7688599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eded369726c8c55256e37afd92db446a7a5c5e24ef7d8a0890d5aa7a6440f7f8`

```dockerfile
```

-	Layers:
	-	`sha256:cc8585436731b26229e106cd971e28ecf9d672b9ced751d7d7ec5ce2ab99a344`  
		Last Modified: Sun, 04 Feb 2024 00:44:42 GMT  
		Size: 3.3 MB (3266531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f2749024705686173713f052013f09bf210f29fa0eca9c3f735f7bcb6b3f524`  
		Last Modified: Sun, 04 Feb 2024 00:44:42 GMT  
		Size: 34.2 KB (34172 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:bca4ac60f8b78d3c646f9935f5a924353a54c81cc5d64cdef9d216125ee4275a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159493451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1593e3dc5b5eee23fbae854c3a2c31b002f4d28479809ae1f18b83d78b1086`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 18:38:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 18:38:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 18:38:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 18:38:04 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 18:38:04 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 18:38:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_VERSION=9.4.1
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_DIST=-slim
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.version=9.4.1
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 25 Jan 2024 18:38:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
VOLUME [/var/solr]
# Thu, 25 Jan 2024 18:38:04 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 25 Jan 2024 18:38:04 GMT
WORKDIR /opt/solr
# Thu, 25 Jan 2024 18:38:04 GMT
USER 8983
# Thu, 25 Jan 2024 18:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jan 2024 18:38:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d031894e4c0411af099ca88f2f4707adffb7144d8d3dc5d40457cededf240b5`  
		Last Modified: Fri, 02 Feb 2024 02:16:39 GMT  
		Size: 18.9 MB (18860666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0007a9ef9bab7b317a14a0d8594647e9c47755fcb79f9fa388e560fab31690`  
		Last Modified: Fri, 02 Feb 2024 02:17:22 GMT  
		Size: 46.6 MB (46639311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917c6cc534cfc01e73da456384906c210ffa86f1df265b8ee7255561e2a7c5fa`  
		Last Modified: Fri, 02 Feb 2024 02:17:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7a0f038262842ffcfdab428e9f3a7a1d0dc2e49da53bdde76335cbc0c02b48`  
		Last Modified: Fri, 02 Feb 2024 02:17:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46983b060b81e6639aabd1f48a20117bf96f2669a793e0a144b6b36f29a3d0d5`  
		Last Modified: Sat, 03 Feb 2024 09:42:43 GMT  
		Size: 64.1 MB (64128283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cd3088b408e82205daf152d40db8ec154fedba75b809f7ecae5870d87f5f77`  
		Last Modified: Sat, 03 Feb 2024 09:42:41 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e9ea1025f0f303c9443ff37a7320f3cc7e327ca14d3ce347a6dbfa4cdf816a`  
		Last Modified: Sat, 03 Feb 2024 09:42:41 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5729ab3a83410bdc2fb89f0a659d0f0fdd7a3cc28b67998092f1736863972f75`  
		Last Modified: Sat, 03 Feb 2024 09:42:41 GMT  
		Size: 10.7 KB (10673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f055a2d5ad04fe727e9dfb4dc325b2d460b35c33bf355219665cb6e8927d7a`  
		Last Modified: Sat, 03 Feb 2024 09:42:42 GMT  
		Size: 1.4 MB (1448968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:cb6ebd046e7f5dd191b4d2ecf3dc739f81fe69aa3ddec0c3ed30188e29a26eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3452365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f17221d22bc714f5543f7fe1b0193485229fcdba688b3ab8a2656f9a1a05fd9`

```dockerfile
```

-	Layers:
	-	`sha256:92c82d4febef9b8a8093b02963ea4e2ac547c4a7f3b024a7048d283aa6033018`  
		Last Modified: Sat, 03 Feb 2024 09:42:41 GMT  
		Size: 3.4 MB (3418306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5090ae2182d467a61018959d7d750cc4d4c7fa798917df1c50f5359e308edafb`  
		Last Modified: Sat, 03 Feb 2024 09:42:40 GMT  
		Size: 34.1 KB (34059 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:d5a7ce8f9b863b87e28e47280f9b23929023f576b99eced10bc8fafa45c6f50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167140594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc713db973fc8e8ff23cd1d16852da5151da68a7d9fb3a5cf4fcdd8cf4d91ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 18:38:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 18:38:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 18:38:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 18:38:04 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 25 Jan 2024 18:38:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 18:38:04 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 18:38:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_VERSION=9.4.1
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_DIST=-slim
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.version=9.4.1
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 25 Jan 2024 18:38:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
VOLUME [/var/solr]
# Thu, 25 Jan 2024 18:38:04 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 25 Jan 2024 18:38:04 GMT
WORKDIR /opt/solr
# Thu, 25 Jan 2024 18:38:04 GMT
USER 8983
# Thu, 25 Jan 2024 18:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jan 2024 18:38:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18e38d90dcfc4a5c7e7603c42709446092d81fa7db3d02bf1b3268ec7f2b33`  
		Last Modified: Fri, 02 Feb 2024 02:49:52 GMT  
		Size: 18.7 MB (18726284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca810e9b2aea7e8e34d5a49650956717c294cb08a1f4694bfb6f2dff3df04e05`  
		Last Modified: Fri, 02 Feb 2024 02:50:42 GMT  
		Size: 47.0 MB (47012525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156813484546a6535bd6a6b1b6d8ddf7f7512ed16513fc6d1704f17c1dba347d`  
		Last Modified: Fri, 02 Feb 2024 02:50:34 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f6c8758a6656575e6625bae130379131cefe92e137c79648b0ae07a09ac094`  
		Last Modified: Fri, 02 Feb 2024 02:50:34 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764420e729a37ea5808fd4170468184e14faf62aca5bea91dd6d251afe622f93`  
		Last Modified: Fri, 02 Feb 2024 21:28:03 GMT  
		Size: 64.1 MB (64128981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3558686764cf5003f96df39956de9ed450578e6c6890b4c7963b66dde54c5324`  
		Last Modified: Fri, 02 Feb 2024 21:28:00 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3670343ccad9a405600ff50a5065854c679a03092fec453fb53a5ce158ebfb32`  
		Last Modified: Fri, 02 Feb 2024 21:28:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18613d10afe32c26dc1143b25a997127fc3a72730fbe7dd1bdd5294220ba355b`  
		Last Modified: Fri, 02 Feb 2024 21:28:00 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9c918b8938d10ebd285fdec649016a664de1ccf362248f0742fe2a6bd7456e`  
		Last Modified: Fri, 02 Feb 2024 21:28:01 GMT  
		Size: 1.6 MB (1597532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:e0bbb01b101b8ea3ab0859b0d3b7fd629ba6678082966b71a25de6aa84e8c3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3395496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d17043b3c2233e2ca1f2139101e40adcda2eb1230ee4387a904e63ea6bd2c2a`

```dockerfile
```

-	Layers:
	-	`sha256:62ace198536397ee7c6b23a0a83cda33a24e536915af88eb2acf63cb327efa6c`  
		Last Modified: Fri, 02 Feb 2024 21:28:00 GMT  
		Size: 3.4 MB (3361400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4717eeddbeaff274e5d578fdd6ab50d6af7c57262be810856dced01a676f2b`  
		Last Modified: Fri, 02 Feb 2024 21:28:00 GMT  
		Size: 34.1 KB (34096 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:f1b998f20d7a0bc665378b390048c62b262b81b411b12d841f0a9e578242ac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155363727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3875f04b05a9d0a5a6713f3cce8c80b66ad30308086d11d4289b9c4d3e1d01a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

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
# Thu, 25 Jan 2024 18:38:04 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 18:38:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_VERSION=9.4.1
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_DIST=-slim
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B
# Thu, 25 Jan 2024 18:38:04 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.version=9.4.1
# Thu, 25 Jan 2024 18:38:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 25 Jan 2024 18:38:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
# ARGS: SOLR_VERSION=9.4.1 SOLR_DIST=-slim SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 25 Jan 2024 18:38:04 GMT
VOLUME [/var/solr]
# Thu, 25 Jan 2024 18:38:04 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 25 Jan 2024 18:38:04 GMT
WORKDIR /opt/solr
# Thu, 25 Jan 2024 18:38:04 GMT
USER 8983
# Thu, 25 Jan 2024 18:38:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jan 2024 18:38:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:9767f83c892c3413514216ee1180f4118e77f689d61466a79134bd214cf66520`  
		Last Modified: Wed, 17 Jan 2024 10:37:33 GMT  
		Size: 28.7 MB (28654354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40326ebc998b6c443a60efe299eea2a45c3f06018d04e989c62c792f2a235e0`  
		Last Modified: Wed, 17 Jan 2024 11:06:48 GMT  
		Size: 17.3 MB (17261225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25aa4940c8e6163e83480ea07f1ef23cb9ca2d1bd9e1441944a480cfdf0be320`  
		Last Modified: Thu, 25 Jan 2024 17:45:44 GMT  
		Size: 43.8 MB (43765978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57545d865aac97eb6016d5fdc9de37ff1f0e14218481bab1399dc3fa12026295`  
		Last Modified: Thu, 25 Jan 2024 17:45:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6708fc52fa273f05e4a85c593248bb4a068a84c7d8268db84e19590fdc83be`  
		Last Modified: Thu, 25 Jan 2024 22:37:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a6b9eed483ec7647f87337f123417f669a632e62fa0802c18a7e08e8c3882b`  
		Last Modified: Tue, 30 Jan 2024 02:56:03 GMT  
		Size: 64.1 MB (64128511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec716da854e026768e03b7e02b9fc172406c97f2f6144a4c8cac54d0606c928a`  
		Last Modified: Tue, 30 Jan 2024 02:56:02 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc75fa0de857199e3ca484e8f757f4d8fa9c772b5fd4bfaa1bf61cb06c0c29e0`  
		Last Modified: Tue, 30 Jan 2024 02:56:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925eb963bf3bab87ff635f663b99c7afbec69217059e0577328f5f8e9a82d6f4`  
		Last Modified: Tue, 30 Jan 2024 02:56:02 GMT  
		Size: 10.7 KB (10674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232a8d62fad5cc1d951d6bedf34fd0a845d64b7f807b5bf19790ae19c86e360b`  
		Last Modified: Tue, 30 Jan 2024 02:56:03 GMT  
		Size: 1.5 MB (1537538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:a91cf2cf00c55c5d083b57e47eabdc0347a53089806ebbb4eaedd231605d0212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3304898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fca151a86ffe18678d89c14073ea651279ca7e494f29af2908aeb8e026cd8f`

```dockerfile
```

-	Layers:
	-	`sha256:99774988df427db5783025cf404fdc8b3e692a27735df000ae0412c3c7d7d6ea`  
		Last Modified: Tue, 30 Jan 2024 02:56:02 GMT  
		Size: 3.3 MB (3270848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddee4d69aaa0258f49a4205e44476bffab897201529393d6527bb179e17be611`  
		Last Modified: Tue, 30 Jan 2024 02:56:02 GMT  
		Size: 34.0 KB (34050 bytes)  
		MIME: application/vnd.in-toto+json
