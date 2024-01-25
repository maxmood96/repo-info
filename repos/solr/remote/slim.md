## `solr:slim`

```console
$ docker pull solr@sha256:82a2b6dd14714c7485aaf36e678ed699c0274ca43e098bc0c03b112ff766dec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:slim` - linux; amd64

```console
$ docker pull solr@sha256:d92413b3689706920cc152a8df3bc02a857dcdb20829857ac703c4482ccd0da2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161266486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafd9c4504328d2e17ccd17588b36c7a7c0b7bf6f3a8d3f9db9b683e026d022b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

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
# Wed, 17 Jan 2024 07:16:34 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Wed, 17 Jan 2024 07:17:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 07:17:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 07:17:07 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 07:17:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 19:40:46 GMT
ARG SOLR_VERSION=9.4.1
# Thu, 18 Jan 2024 19:41:20 GMT
ARG SOLR_DIST=-slim
# Thu, 18 Jan 2024 19:41:21 GMT
ARG SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657
# Thu, 18 Jan 2024 19:41:21 GMT
ARG SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B
# Thu, 18 Jan 2024 19:41:21 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 18 Jan 2024 19:41:32 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Thu, 18 Jan 2024 19:41:32 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 18 Jan 2024 19:41:32 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 18 Jan 2024 19:41:32 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 18 Jan 2024 19:41:33 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 18 Jan 2024 19:41:33 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 18 Jan 2024 19:41:33 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 18 Jan 2024 19:41:33 GMT
LABEL org.opencontainers.image.version=9.4.1
# Thu, 18 Jan 2024 19:41:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 18 Jan 2024 19:41:33 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 18 Jan 2024 19:41:34 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 18 Jan 2024 19:41:34 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 18 Jan 2024 19:41:35 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 18 Jan 2024 19:41:40 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 18 Jan 2024 19:41:40 GMT
VOLUME [/var/solr]
# Thu, 18 Jan 2024 19:41:40 GMT
EXPOSE 8983
# Thu, 18 Jan 2024 19:41:40 GMT
WORKDIR /opt/solr
# Thu, 18 Jan 2024 19:41:40 GMT
USER 8983
# Thu, 18 Jan 2024 19:41:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 19:41:40 GMT
CMD ["solr-foreground"]
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
	-	`sha256:ec70d9e863c2b918442abf26eb84b0afbc4a2c5dda1c34857c51955e26a803c3`  
		Last Modified: Wed, 17 Jan 2024 07:20:58 GMT  
		Size: 47.1 MB (47149289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680d0df58130ac2dc6ee238ad0275c9652892eda90a334fd3ce02eedf7147963`  
		Last Modified: Wed, 17 Jan 2024 07:20:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73eedc84985754d22cc59527bee6b3fc0a39558017abcf0fe7ae531123dc84e`  
		Last Modified: Wed, 17 Jan 2024 07:20:52 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d379ca67aacba138a27a1d9ef44ac9a7a0e4626969043c07e69045ef6282f3`  
		Last Modified: Thu, 18 Jan 2024 19:42:49 GMT  
		Size: 64.4 MB (64366845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a44360abcd54dee7e072f0bf8695db882fc7311328a06fbed4aa94bdbcc6c`  
		Last Modified: Thu, 18 Jan 2024 19:42:45 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea19e922dac19886d45e20a34049d4e02ddf36040f17e52a3481e42ea016dc3`  
		Last Modified: Thu, 18 Jan 2024 19:42:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cde273078a77d12b47f0dcc12583443fa68cb016099443ecf774023c4c529d`  
		Last Modified: Thu, 18 Jan 2024 19:42:45 GMT  
		Size: 10.7 KB (10744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abd8134f03de35e0f592c64bee268288a92894bb30a131a9326b42212d52886`  
		Last Modified: Thu, 18 Jan 2024 19:42:45 GMT  
		Size: 1.8 MB (1828938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:e9210dc6a1057d61337e68c07e8e6fdd4b7578f57d52826c286b0f71ece1da86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155955979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae95a9a5680397e790613d35ec0c5b34c767235f04ddfb697d403bf2b0e654e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 17:30:37 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:30:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:30:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:30:37 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:30:39 GMT
ADD file:7c2f93ce47dedf9ba449bf11d41e9930af9fa209725f5772dc09f8c8100b5626 in / 
# Thu, 11 Jan 2024 17:30:40 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 09:39:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:39:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 09:41:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 21:12:44 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 21:13:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 21:13:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 21:13:15 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 21:13:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 22:19:19 GMT
ARG SOLR_VERSION=9.4.1
# Wed, 24 Jan 2024 22:20:17 GMT
ARG SOLR_DIST=-slim
# Wed, 24 Jan 2024 22:20:17 GMT
ARG SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657
# Wed, 24 Jan 2024 22:20:17 GMT
ARG SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B
# Wed, 24 Jan 2024 22:20:17 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 24 Jan 2024 22:20:34 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Wed, 24 Jan 2024 22:20:34 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 24 Jan 2024 22:20:34 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 24 Jan 2024 22:20:34 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 24 Jan 2024 22:20:34 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 24 Jan 2024 22:20:35 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 24 Jan 2024 22:20:35 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 24 Jan 2024 22:20:35 GMT
LABEL org.opencontainers.image.version=9.4.1
# Wed, 24 Jan 2024 22:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 24 Jan 2024 22:20:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 24 Jan 2024 22:20:36 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Wed, 24 Jan 2024 22:20:36 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Wed, 24 Jan 2024 22:20:37 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Wed, 24 Jan 2024 22:20:41 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Wed, 24 Jan 2024 22:20:41 GMT
VOLUME [/var/solr]
# Wed, 24 Jan 2024 22:20:42 GMT
EXPOSE 8983
# Wed, 24 Jan 2024 22:20:42 GMT
WORKDIR /opt/solr
# Wed, 24 Jan 2024 22:20:42 GMT
USER 8983
# Wed, 24 Jan 2024 22:20:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2024 22:20:42 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:cea537175db3d13760d71d7a8baa0a5e82491345696d2da089429926cceccffe`  
		Last Modified: Fri, 12 Jan 2024 04:33:34 GMT  
		Size: 27.5 MB (27525460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d718e61980ad7fa6f989d43c4a8b6ee393bd6940e24b4ac30785daa28ddee20c`  
		Last Modified: Wed, 17 Jan 2024 09:44:51 GMT  
		Size: 17.6 MB (17592266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d68fd9be6aacf61019be2b797efb80026c6076ce9d027ecac109b0c641dbab`  
		Last Modified: Wed, 24 Jan 2024 21:17:40 GMT  
		Size: 44.8 MB (44798877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdaf7aef7a909cfaa3e14398442b39d365f10a8922fb153ba9dda9a928d9f7ed`  
		Last Modified: Wed, 24 Jan 2024 21:17:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab583f74e69484d909d7627ef9a55ff9d94a729e7d85c623ec5fe1bf0a9b946`  
		Last Modified: Wed, 24 Jan 2024 21:17:32 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2edffa4578b863ab1975e98b3b5360e291aefe89348b1250ea012c20c21aee`  
		Last Modified: Wed, 24 Jan 2024 22:27:46 GMT  
		Size: 64.4 MB (64368197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a89412bbb4163297da0296293d04c50b5767fa252c600edcfc64c5b576ecf1d`  
		Last Modified: Wed, 24 Jan 2024 22:27:41 GMT  
		Size: 4.2 KB (4226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c7adb598993d9bad32bdd76a9b8aa274ed52f3e9f8bcd3c08be52d09a9a594`  
		Last Modified: Wed, 24 Jan 2024 22:27:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194eb5308e6e83094b990bcf0956f7859139369654c62d0363b1a8c8983afbfc`  
		Last Modified: Wed, 24 Jan 2024 22:27:41 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa75babe5893ea6231152478a1def3c994e5d668c28e10289e3261ce6c7112b`  
		Last Modified: Wed, 24 Jan 2024 22:27:41 GMT  
		Size: 1.7 MB (1655109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:403f719092525e41ad1d65657fced8e228c1866348e9d38bead68a16f314d809
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159954612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a716fb1db1348bfdc55934f96dd5001ebddcf7fb4660040f9ff2cd4fc853c47a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

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
# Wed, 17 Jan 2024 06:59:06 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Wed, 17 Jan 2024 06:59:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 06:59:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 06:59:33 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 06:59:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 19:40:55 GMT
ARG SOLR_VERSION=9.4.1
# Thu, 18 Jan 2024 19:41:29 GMT
ARG SOLR_DIST=-slim
# Thu, 18 Jan 2024 19:41:29 GMT
ARG SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657
# Thu, 18 Jan 2024 19:41:29 GMT
ARG SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B
# Thu, 18 Jan 2024 19:41:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 18 Jan 2024 19:41:39 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Thu, 18 Jan 2024 19:41:39 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 18 Jan 2024 19:41:39 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 18 Jan 2024 19:41:39 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 18 Jan 2024 19:41:39 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 18 Jan 2024 19:41:39 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 18 Jan 2024 19:41:40 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 18 Jan 2024 19:41:40 GMT
LABEL org.opencontainers.image.version=9.4.1
# Thu, 18 Jan 2024 19:41:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 18 Jan 2024 19:41:40 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 18 Jan 2024 19:41:40 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 18 Jan 2024 19:41:41 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 18 Jan 2024 19:41:41 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 18 Jan 2024 19:41:45 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 18 Jan 2024 19:41:45 GMT
VOLUME [/var/solr]
# Thu, 18 Jan 2024 19:41:45 GMT
EXPOSE 8983
# Thu, 18 Jan 2024 19:41:45 GMT
WORKDIR /opt/solr
# Thu, 18 Jan 2024 19:41:45 GMT
USER 8983
# Thu, 18 Jan 2024 19:41:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 19:41:46 GMT
CMD ["solr-foreground"]
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
	-	`sha256:b40ddacc22778a98794779fd2342df132ad4c2fb4cbfc8863316d31fd435b197`  
		Last Modified: Wed, 17 Jan 2024 07:02:40 GMT  
		Size: 46.6 MB (46624031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aa70867b319793d597ac109e4ab08a1640a03419c64b02fc2a0f83d3fab963`  
		Last Modified: Wed, 17 Jan 2024 07:02:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cb574f7d99aeb3b3f52602da29bf978d23b304f4233a2ea5587d6ae88cbd66`  
		Last Modified: Wed, 17 Jan 2024 07:02:34 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670c4dd84d12ef38a383b82cc2b7f59626e9dd7b0e7211aa5d2c327462e2f55d`  
		Last Modified: Thu, 18 Jan 2024 19:42:43 GMT  
		Size: 64.4 MB (64366923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f175c78ecfb73850ac3028cdf3c92679714e599e2e52b5aaf50345bc87cb982a`  
		Last Modified: Thu, 18 Jan 2024 19:42:40 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43169c609d7cfa70575ea3d3b515f7185d344f8dc40ede08d2b059531430025`  
		Last Modified: Thu, 18 Jan 2024 19:42:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c7be846e3a67ee5313802484238862fd1b210f72a8eab700f5ea383da3f44b`  
		Last Modified: Thu, 18 Jan 2024 19:42:40 GMT  
		Size: 10.7 KB (10744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc174c526f283278c44b30dd046c9ed4decc3c85e21e07fd63a77b21f874e13a`  
		Last Modified: Thu, 18 Jan 2024 19:42:40 GMT  
		Size: 1.7 MB (1687755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:cace78c19e1084e0030b616f3c2bb30c135747492e8c8840ba1e45a6bb363c3e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167614707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3bca9faba4fd4e831d9a8c4318dffc338c5dafb7a97b2a177e41efab8c62db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

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
# Wed, 24 Jan 2024 20:43:06 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:43:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 22:59:46 GMT
ARG SOLR_VERSION=9.4.1
# Wed, 24 Jan 2024 23:01:26 GMT
ARG SOLR_DIST=-slim
# Wed, 24 Jan 2024 23:01:27 GMT
ARG SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657
# Wed, 24 Jan 2024 23:01:27 GMT
ARG SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B
# Wed, 24 Jan 2024 23:01:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 24 Jan 2024 23:01:55 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Wed, 24 Jan 2024 23:01:57 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 24 Jan 2024 23:01:57 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 24 Jan 2024 23:01:58 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 24 Jan 2024 23:01:58 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 24 Jan 2024 23:01:59 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 24 Jan 2024 23:01:59 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 24 Jan 2024 23:02:00 GMT
LABEL org.opencontainers.image.version=9.4.1
# Wed, 24 Jan 2024 23:02:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 24 Jan 2024 23:02:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 24 Jan 2024 23:02:02 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Wed, 24 Jan 2024 23:02:04 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Wed, 24 Jan 2024 23:02:06 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Wed, 24 Jan 2024 23:02:14 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Wed, 24 Jan 2024 23:02:15 GMT
VOLUME [/var/solr]
# Wed, 24 Jan 2024 23:02:15 GMT
EXPOSE 8983
# Wed, 24 Jan 2024 23:02:16 GMT
WORKDIR /opt/solr
# Wed, 24 Jan 2024 23:02:16 GMT
USER 8983
# Wed, 24 Jan 2024 23:02:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2024 23:02:17 GMT
CMD ["solr-foreground"]
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
	-	`sha256:ec8a1405ffb5fb4df646925939e10a1fcc1a6ab68bf2488db8428a0fd9009954`  
		Last Modified: Wed, 24 Jan 2024 20:54:53 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f53887dbf12b0df25209685f062b318740ca20a1d490dcd8cc01f3b723bd7c`  
		Last Modified: Wed, 24 Jan 2024 23:11:03 GMT  
		Size: 64.4 MB (64367461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef9eab145374d67d9537bce13cd97181784cf51f2dd63b30b4cce722667da69`  
		Last Modified: Wed, 24 Jan 2024 23:10:59 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfc721d911657caa33c0731a54609e71b830892306d0dfd534e2511bf2d226b`  
		Last Modified: Wed, 24 Jan 2024 23:10:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c7b72bcd3e7ff667ee4416810369b79788296b069227b617d7e460fcdb4091`  
		Last Modified: Wed, 24 Jan 2024 23:10:59 GMT  
		Size: 10.8 KB (10751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bedbde08e7d5bc51c53f1484858847b1124c5ae8752f8e6edd9bfdd4f71103e`  
		Last Modified: Wed, 24 Jan 2024 23:11:00 GMT  
		Size: 1.8 MB (1835519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:77e494cf43bf5754f5f908417eef4d82f9ebc2bfbbc8a895dd9092ba04308fda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155829007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70833c065d92ebd9f17254e5702362a8d156e0dd145fc311b941598423023f40`
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
# Wed, 17 Jan 2024 10:54:39 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Wed, 17 Jan 2024 10:58:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 10:58:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 10:58:51 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 10:58:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 21:12:24 GMT
ARG SOLR_VERSION=9.4.1
# Thu, 18 Jan 2024 21:14:36 GMT
ARG SOLR_DIST=-slim
# Thu, 18 Jan 2024 21:14:36 GMT
ARG SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657
# Thu, 18 Jan 2024 21:14:36 GMT
ARG SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B
# Thu, 18 Jan 2024 21:14:36 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 18 Jan 2024 21:14:49 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Thu, 18 Jan 2024 21:14:51 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 18 Jan 2024 21:14:51 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 18 Jan 2024 21:14:51 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 18 Jan 2024 21:14:51 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 18 Jan 2024 21:14:51 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 18 Jan 2024 21:14:51 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 18 Jan 2024 21:14:51 GMT
LABEL org.opencontainers.image.version=9.4.1
# Thu, 18 Jan 2024 21:14:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 18 Jan 2024 21:14:52 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 18 Jan 2024 21:14:52 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 18 Jan 2024 21:14:53 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 18 Jan 2024 21:14:53 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 18 Jan 2024 21:14:56 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=515EA995ED1DD799FA1422E5CA7514D8385D790B SOLR_SHA512=5f93e83f04842aabdbb1122638d7bdf7e89c09b1a90ef6944fc5605258d6a48f60f3ea84c56b4c8044554bf4c2a54283775128aa0cb047fcf8e9a2e8f6fc2657 SOLR_VERSION=9.4.1
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 18 Jan 2024 21:14:57 GMT
VOLUME [/var/solr]
# Thu, 18 Jan 2024 21:14:57 GMT
EXPOSE 8983
# Thu, 18 Jan 2024 21:14:57 GMT
WORKDIR /opt/solr
# Thu, 18 Jan 2024 21:14:57 GMT
USER 8983
# Thu, 18 Jan 2024 21:14:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 21:14:57 GMT
CMD ["solr-foreground"]
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
	-	`sha256:3a9b6905169bad57d93be899f601e37644cea1bdcf6a72801406404b1423af37`  
		Last Modified: Wed, 17 Jan 2024 11:07:43 GMT  
		Size: 43.8 MB (43754375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9899f305d4b4dc2039ffbeac0b15470a0a35f9ed7f52c95aa6df577462a8a4b1`  
		Last Modified: Wed, 17 Jan 2024 11:07:37 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bb972c6e6feef0460d2075f6bfdbca9dd1ca1ef5db70f10f69d0aed99bc13c`  
		Last Modified: Wed, 17 Jan 2024 11:07:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6fd10beab942d0b150d2ace2b497356afe08ff6f4d2b8f342295b86011778b`  
		Last Modified: Thu, 18 Jan 2024 21:26:00 GMT  
		Size: 64.4 MB (64367060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f698642c7d828ebe4385824f60faa382f2f8d68c34ee1b3da4b79887215f4fb2`  
		Last Modified: Thu, 18 Jan 2024 21:25:57 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6ce8cf144c10267903489146e6c62ca5637644afd6c99d202f5341fd318974`  
		Last Modified: Thu, 18 Jan 2024 21:25:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db07900b4f9835da1ab46670ce80b7109d09bd5b2140d3988259d61e2ab78e42`  
		Last Modified: Thu, 18 Jan 2024 21:25:57 GMT  
		Size: 10.7 KB (10748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3c0f5257923c8f3e0aa72a620445ff6b88a00e4d2f94c43ef7cdbde460d33c`  
		Last Modified: Thu, 18 Jan 2024 21:25:57 GMT  
		Size: 1.8 MB (1775795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
