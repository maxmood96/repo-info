## `solr:slim`

```console
$ docker pull solr@sha256:d6ad246116a8272c7290745cae1156060a074f1bd718e8d82ece2b79e98af07b
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
$ docker pull solr@sha256:10be4cf79d5442fd100ee8d4db0a76a88872021967cd9c0daf2d68ab16f41ed2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159749033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0ddb9fbb9abaa2130276c57e075f307148a0cb31bbe26731d1bbd482d18d1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:39:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 15:39:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 15:39:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 15:40:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:40:43 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Wed, 16 Aug 2023 15:41:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42525ae2951a669803c75ba5987dc8333c664dae50c3e12174f736a506b4aa15';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='20fa06a86e1647f5997c511dd19e4d1c9839d2500f835973fc9b3c86b87030a0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1cf2cf7dca98c74860799b162b9f2eeaaf1ad1e78f5cb7479fe7bd1ccfea3227';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='4df17b19510864651c1d620baaf13766a448d43ee7848ea9ff69db10d26467b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='dddbb5f817a77445711528a414678806b00b83c92701fe595c50cdb207758ae9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 16 Aug 2023 15:41:14 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 16 Aug 2023 15:41:14 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 16 Aug 2023 15:41:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Aug 2023 16:12:27 GMT
ARG SOLR_VERSION=9.3.0
# Wed, 16 Aug 2023 16:13:16 GMT
ARG SOLR_DIST=-slim
# Wed, 16 Aug 2023 16:13:16 GMT
ARG SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076
# Wed, 16 Aug 2023 16:13:16 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 16 Aug 2023 16:13:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 16 Aug 2023 16:13:31 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Wed, 16 Aug 2023 16:13:31 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 16 Aug 2023 16:13:31 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 16 Aug 2023 16:13:31 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 16 Aug 2023 16:13:31 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 16 Aug 2023 16:13:31 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 16 Aug 2023 16:13:32 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 16 Aug 2023 16:13:32 GMT
LABEL org.opencontainers.image.version=9.3.0
# Wed, 16 Aug 2023 16:13:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 16 Aug 2023 16:13:32 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Wed, 16 Aug 2023 16:13:32 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Wed, 16 Aug 2023 16:13:33 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Wed, 16 Aug 2023 16:13:33 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Wed, 16 Aug 2023 16:13:38 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Wed, 16 Aug 2023 16:13:38 GMT
VOLUME [/var/solr]
# Wed, 16 Aug 2023 16:13:38 GMT
EXPOSE 8983
# Wed, 16 Aug 2023 16:13:38 GMT
WORKDIR /opt/solr
# Wed, 16 Aug 2023 16:13:38 GMT
USER 8983
# Wed, 16 Aug 2023 16:13:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Aug 2023 16:13:38 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5980221a1ce1b53ecf2261f165c9bf6a24b845a2418dcf3c7aaf2f3f9e43f2a`  
		Last Modified: Wed, 16 Aug 2023 15:44:40 GMT  
		Size: 17.5 MB (17456341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b561fbe0ad19bb4387a8077fcb3e59b56817c3eefdca5733ab0abca140bf7744`  
		Last Modified: Wed, 16 Aug 2023 15:45:11 GMT  
		Size: 47.2 MB (47209336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afff93b71681f55d805da2e602437bd8d33c94f4ae97c046e423328117a27201`  
		Last Modified: Wed, 16 Aug 2023 15:45:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203befd6870750935a31ccdd763b14737956c402a290ff8cb0694745aff457a6`  
		Last Modified: Wed, 16 Aug 2023 15:45:05 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ad2f59a0d3f28d73818168f7b770589228ce0a81d21e64224219349386a285`  
		Last Modified: Wed, 16 Aug 2023 16:16:36 GMT  
		Size: 62.8 MB (62800609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9eaf501fd9c3b7f4d01c28a6bcc3bd7a5ba13a2d0fcb9979b06a546aa964f4`  
		Last Modified: Wed, 16 Aug 2023 16:16:32 GMT  
		Size: 4.3 KB (4296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904b520e5301455d8b7619f413ddedd09f29a6171a59f8a405ce8458c720be13`  
		Last Modified: Wed, 16 Aug 2023 16:16:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c24b887cc6660056e0ae663fcfce7f180f5695e0995cf0935f1f0770cdb6c3`  
		Last Modified: Wed, 16 Aug 2023 16:16:32 GMT  
		Size: 10.6 KB (10642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45219c57b390bcc6f714649f286ff53b988ec40be762c615ccb2429719ce87b1`  
		Last Modified: Wed, 16 Aug 2023 16:16:33 GMT  
		Size: 1.8 MB (1828733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:fe141072b4d92e5949a32d43caa235886632b7fa7f4b43c9b17f2d33eef357ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153808168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c4cede475e75be782b8d748263ec2c987a64ad7f318f80fc225f2249922d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:19 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:24 GMT
ADD file:ca783750060711e8590ab362921bae8d7b02201c48fa3d2cb3fdf6aac045a793 in / 
# Fri, 04 Aug 2023 05:03:25 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 16:00:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 16:00:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 16:00:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 16:03:05 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 16:03:05 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Wed, 16 Aug 2023 16:03:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42525ae2951a669803c75ba5987dc8333c664dae50c3e12174f736a506b4aa15';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='20fa06a86e1647f5997c511dd19e4d1c9839d2500f835973fc9b3c86b87030a0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1cf2cf7dca98c74860799b162b9f2eeaaf1ad1e78f5cb7479fe7bd1ccfea3227';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='4df17b19510864651c1d620baaf13766a448d43ee7848ea9ff69db10d26467b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='dddbb5f817a77445711528a414678806b00b83c92701fe595c50cdb207758ae9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 16 Aug 2023 16:03:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 16 Aug 2023 16:03:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 16 Aug 2023 16:03:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 17 Aug 2023 03:43:52 GMT
ARG SOLR_VERSION=9.3.0
# Thu, 17 Aug 2023 03:44:49 GMT
ARG SOLR_DIST=-slim
# Thu, 17 Aug 2023 03:44:49 GMT
ARG SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076
# Thu, 17 Aug 2023 03:44:49 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 17 Aug 2023 03:44:49 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 17 Aug 2023 03:45:04 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Thu, 17 Aug 2023 03:45:04 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 17 Aug 2023 03:45:05 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 17 Aug 2023 03:45:05 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 17 Aug 2023 03:45:05 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 17 Aug 2023 03:45:05 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 17 Aug 2023 03:45:05 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 17 Aug 2023 03:45:05 GMT
LABEL org.opencontainers.image.version=9.3.0
# Thu, 17 Aug 2023 03:45:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Aug 2023 03:45:05 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 17 Aug 2023 03:45:06 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 17 Aug 2023 03:45:06 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 17 Aug 2023 03:45:07 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 17 Aug 2023 03:45:11 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 17 Aug 2023 03:45:11 GMT
VOLUME [/var/solr]
# Thu, 17 Aug 2023 03:45:11 GMT
EXPOSE 8983
# Thu, 17 Aug 2023 03:45:11 GMT
WORKDIR /opt/solr
# Thu, 17 Aug 2023 03:45:11 GMT
USER 8983
# Thu, 17 Aug 2023 03:45:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Aug 2023 03:45:11 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:24758824a30b6e1f6132a6b6740dec1fc5723821f0f2b5b6513379480e0f74f9`  
		Last Modified: Sat, 05 Aug 2023 02:03:56 GMT  
		Size: 27.0 MB (27029194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f663432c579bc80e7965d8823f3989eb1a39328a202e033ab7b4dd1478a0d1a`  
		Last Modified: Wed, 16 Aug 2023 16:05:37 GMT  
		Size: 17.6 MB (17587799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393261335571754504edb55f5b7cd6aafc8e3befaeed6b0fcc3538f0d483616`  
		Last Modified: Wed, 16 Aug 2023 16:06:11 GMT  
		Size: 44.7 MB (44718580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5ad0ae3fbf1ad6f9fdaa6708b83576ea25dbfe1af6ae22995ba2212ec31317`  
		Last Modified: Wed, 16 Aug 2023 16:06:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b803a287c5439bcaf1e18032e1c2ed8d25bdb808d28c45b9db6ae4231badf3e`  
		Last Modified: Wed, 16 Aug 2023 16:06:03 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fac6d6814092c490e74693ddedb71959c7f6ec6c121a26695dcc66925c3896c`  
		Last Modified: Thu, 17 Aug 2023 03:47:34 GMT  
		Size: 62.8 MB (62801779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2307729b02b53528aefbb62e5f922716557ef3efe497ae0f4888b8d64d680fcf`  
		Last Modified: Thu, 17 Aug 2023 03:47:29 GMT  
		Size: 4.2 KB (4227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8dc54e52610ff2d6a66e79c10d6b3ccf1b610130fb3b8a9b644ff330fd981a3`  
		Last Modified: Thu, 17 Aug 2023 03:47:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b3e932745e9d5ac5109175e82a9a958567255238b3ceed43b9999a76c5816f`  
		Last Modified: Thu, 17 Aug 2023 03:47:29 GMT  
		Size: 10.6 KB (10645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3353e8e663e74bcb52a3e3148907804e7a483e1bbeacc9578b8e749f289feb`  
		Last Modified: Thu, 17 Aug 2023 03:47:29 GMT  
		Size: 1.7 MB (1654829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:ebb758b5b0f7794588c88602bec0b84249315b01cc705223e6d615c469b0f5d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158418119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b51ab0555fb9c4e09a57737c195258855ed2732741717bb29458cbcd784be2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 14:23:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 14:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 14:23:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 14:24:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:24:46 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Wed, 16 Aug 2023 14:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42525ae2951a669803c75ba5987dc8333c664dae50c3e12174f736a506b4aa15';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='20fa06a86e1647f5997c511dd19e4d1c9839d2500f835973fc9b3c86b87030a0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1cf2cf7dca98c74860799b162b9f2eeaaf1ad1e78f5cb7479fe7bd1ccfea3227';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='4df17b19510864651c1d620baaf13766a448d43ee7848ea9ff69db10d26467b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='dddbb5f817a77445711528a414678806b00b83c92701fe595c50cdb207758ae9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 16 Aug 2023 14:25:13 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 16 Aug 2023 14:25:13 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 16 Aug 2023 14:25:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Aug 2023 17:01:47 GMT
ARG SOLR_VERSION=9.3.0
# Wed, 16 Aug 2023 17:02:35 GMT
ARG SOLR_DIST=-slim
# Wed, 16 Aug 2023 17:02:35 GMT
ARG SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076
# Wed, 16 Aug 2023 17:02:36 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 16 Aug 2023 17:02:36 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 16 Aug 2023 17:02:49 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Wed, 16 Aug 2023 17:02:49 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 16 Aug 2023 17:02:49 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 16 Aug 2023 17:02:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 16 Aug 2023 17:02:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 16 Aug 2023 17:02:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 16 Aug 2023 17:02:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 16 Aug 2023 17:02:50 GMT
LABEL org.opencontainers.image.version=9.3.0
# Wed, 16 Aug 2023 17:02:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 16 Aug 2023 17:02:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Wed, 16 Aug 2023 17:02:50 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Wed, 16 Aug 2023 17:02:51 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Wed, 16 Aug 2023 17:02:51 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Wed, 16 Aug 2023 17:02:55 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Wed, 16 Aug 2023 17:02:55 GMT
VOLUME [/var/solr]
# Wed, 16 Aug 2023 17:02:55 GMT
EXPOSE 8983
# Wed, 16 Aug 2023 17:02:55 GMT
WORKDIR /opt/solr
# Wed, 16 Aug 2023 17:02:55 GMT
USER 8983
# Wed, 16 Aug 2023 17:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Aug 2023 17:02:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c321f4fb81c9a8d9170f2e66e24c105f438bac179a8c09632ea442be47ef6a3`  
		Last Modified: Wed, 16 Aug 2023 14:28:14 GMT  
		Size: 18.9 MB (18858726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9542e4f75bdb646a8d5f5b389f20d47ae2371577ec45f710d2b56748f1e51d50`  
		Last Modified: Wed, 16 Aug 2023 14:28:48 GMT  
		Size: 46.7 MB (46660708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9dde614396293bfe385ba8f7cd36be55a08fc8dc9805f1f8adbf01b0c2ecb0`  
		Last Modified: Wed, 16 Aug 2023 14:28:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0b81052b20dad9e5678fe5204fc636da6378beecb2a2c704b776c7069f0534`  
		Last Modified: Wed, 16 Aug 2023 14:28:43 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7506f74e869b7bc5bd50ceaa97f1cf2181fb4d05cc6c2a4a6f862869a2174ddf`  
		Last Modified: Wed, 16 Aug 2023 17:04:47 GMT  
		Size: 62.8 MB (62801870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631088e7e2e5ba7ac85bb9ab6d111af6100aee03c32a6ec8b2bff02dfc0af402`  
		Last Modified: Wed, 16 Aug 2023 17:04:43 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5fdb7f7fd711679cb6a75c6e306cde470596de605211005a5edff31a0326e`  
		Last Modified: Wed, 16 Aug 2023 17:04:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69819ab4a9cf38eb088cf560d985acdfbdf63f08beed2a8732d9e0a2b2a0b304`  
		Last Modified: Wed, 16 Aug 2023 17:04:43 GMT  
		Size: 10.6 KB (10643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17649fcb9a6a89eecf44f5674c25a70665a767e12c6b566c984e7d576b5d4ab4`  
		Last Modified: Wed, 16 Aug 2023 17:04:44 GMT  
		Size: 1.7 MB (1688821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:d3d0eda6adc8d5d29740f2f2e9161a498ad66f07fe374be87a8449f8959b6dad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166148021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b89957696c59ac97ee2ab1631f31d21a47aeb56f2e4f207a720c83d5a1e0874`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
CMD ["/bin/bash"]
# Thu, 17 Aug 2023 07:21:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Aug 2023 07:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Aug 2023 07:21:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Aug 2023 07:24:20 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:24:21 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Thu, 17 Aug 2023 07:25:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42525ae2951a669803c75ba5987dc8333c664dae50c3e12174f736a506b4aa15';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='20fa06a86e1647f5997c511dd19e4d1c9839d2500f835973fc9b3c86b87030a0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1cf2cf7dca98c74860799b162b9f2eeaaf1ad1e78f5cb7479fe7bd1ccfea3227';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='4df17b19510864651c1d620baaf13766a448d43ee7848ea9ff69db10d26467b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='dddbb5f817a77445711528a414678806b00b83c92701fe595c50cdb207758ae9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 17 Aug 2023 07:25:07 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 17 Aug 2023 07:25:07 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 17 Aug 2023 07:25:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 17 Aug 2023 12:32:08 GMT
ARG SOLR_VERSION=9.3.0
# Thu, 17 Aug 2023 12:33:47 GMT
ARG SOLR_DIST=-slim
# Thu, 17 Aug 2023 12:33:48 GMT
ARG SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076
# Thu, 17 Aug 2023 12:33:48 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 17 Aug 2023 12:33:48 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 17 Aug 2023 12:34:41 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Thu, 17 Aug 2023 12:34:42 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 17 Aug 2023 12:34:43 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 17 Aug 2023 12:34:43 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 17 Aug 2023 12:34:43 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 17 Aug 2023 12:34:44 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 17 Aug 2023 12:34:44 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 17 Aug 2023 12:34:44 GMT
LABEL org.opencontainers.image.version=9.3.0
# Thu, 17 Aug 2023 12:34:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Aug 2023 12:34:45 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 17 Aug 2023 12:34:46 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 17 Aug 2023 12:34:47 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 17 Aug 2023 12:34:49 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 17 Aug 2023 12:34:58 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 17 Aug 2023 12:34:59 GMT
VOLUME [/var/solr]
# Thu, 17 Aug 2023 12:35:00 GMT
EXPOSE 8983
# Thu, 17 Aug 2023 12:35:00 GMT
WORKDIR /opt/solr
# Thu, 17 Aug 2023 12:35:01 GMT
USER 8983
# Thu, 17 Aug 2023 12:35:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Aug 2023 12:35:02 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:09f4821f68917c7929419fff8bc583c406640180ea7d58eea03a95e463b8fb21`  
		Last Modified: Wed, 16 Aug 2023 02:15:01 GMT  
		Size: 35.7 MB (35712693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ac4cfa89e33fa6fac1fbd37e22637c5be91e0cc3a38c83101cd6547c2bacb8`  
		Last Modified: Thu, 17 Aug 2023 07:28:57 GMT  
		Size: 18.7 MB (18729521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd3806de7d075ddfd9d4a5cd7870a91c56f74ea840a518abecaa4cd3ce6b23e`  
		Last Modified: Thu, 17 Aug 2023 07:29:45 GMT  
		Size: 47.1 MB (47053183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ac3ddc6956ecbb7f2a4c5d4f805abfbd675dd6a7408b6415970d5d51946358`  
		Last Modified: Thu, 17 Aug 2023 07:29:34 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebb2228461fb7ad7316ddb3b52f5a47ff6b63b68ae223efbb366be7074a3852`  
		Last Modified: Thu, 17 Aug 2023 07:29:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b8be6a4e7d6d0cf432606393727f8073f8dc17d8fb3cfb2e25064c2fefbe00`  
		Last Modified: Thu, 17 Aug 2023 12:37:53 GMT  
		Size: 62.8 MB (62801275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08578080d4f9082f4500524d96e4737dbfb1b3c81ac4eeac91384e6d4ef14bcb`  
		Last Modified: Thu, 17 Aug 2023 12:37:46 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ff04f64fba9ecedfd4084f2d7a0b8c99f78cc3367b5ad73ba5601c8be6e20b`  
		Last Modified: Thu, 17 Aug 2023 12:37:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d46db7ffb04d71728baa05ce5ca2f7752d53c30d29de07b6f8f110ad71744b`  
		Last Modified: Thu, 17 Aug 2023 12:37:47 GMT  
		Size: 10.6 KB (10646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dfde929a384a48fc5f31e38d3826f4d760045dee7af6d2be1e3dc257ce54aa`  
		Last Modified: Thu, 17 Aug 2023 12:37:47 GMT  
		Size: 1.8 MB (1835287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:94d7dcd4f7056de1c54966c1ef64ea67686dd6225a4e1d09caeab39047b4cdd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154352384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3a27d8c4fe24be77d6d1638ac08d01643199c7f957f4a712f944ca91758d51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:16 GMT
ADD file:d5b5687c046ca0689ccc4f42ddcc27543404ae2273aa12241e6636a2b3d675df in / 
# Fri, 04 Aug 2023 05:03:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 09:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 09:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 09:42:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 09:43:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 09:43:50 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Wed, 16 Aug 2023 09:44:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42525ae2951a669803c75ba5987dc8333c664dae50c3e12174f736a506b4aa15';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8_7.tar.gz';          ;;        armhf|arm)          ESUM='20fa06a86e1647f5997c511dd19e4d1c9839d2500f835973fc9b3c86b87030a0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.8_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1cf2cf7dca98c74860799b162b9f2eeaaf1ad1e78f5cb7479fe7bd1ccfea3227';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='4df17b19510864651c1d620baaf13766a448d43ee7848ea9ff69db10d26467b6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='dddbb5f817a77445711528a414678806b00b83c92701fe595c50cdb207758ae9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 16 Aug 2023 09:44:31 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 16 Aug 2023 09:44:31 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 16 Aug 2023 09:44:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Aug 2023 17:30:28 GMT
ARG SOLR_VERSION=9.3.0
# Wed, 16 Aug 2023 17:31:17 GMT
ARG SOLR_DIST=-slim
# Wed, 16 Aug 2023 17:31:17 GMT
ARG SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076
# Wed, 16 Aug 2023 17:31:17 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 16 Aug 2023 17:31:17 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 16 Aug 2023 17:31:28 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Wed, 16 Aug 2023 17:31:30 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 16 Aug 2023 17:31:30 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 16 Aug 2023 17:31:30 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 16 Aug 2023 17:31:30 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 16 Aug 2023 17:31:30 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 16 Aug 2023 17:31:30 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 16 Aug 2023 17:31:30 GMT
LABEL org.opencontainers.image.version=9.3.0
# Wed, 16 Aug 2023 17:31:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 16 Aug 2023 17:31:30 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Wed, 16 Aug 2023 17:31:31 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Wed, 16 Aug 2023 17:31:31 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Wed, 16 Aug 2023 17:31:32 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Wed, 16 Aug 2023 17:31:35 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=432306fa6db9d772df84d6acb3adab095783dda10e55280bfd443e197969271364d86f5c64d737ca6c6660bda81e13ffe404e34feb8447dff6ca0cd302ddd076 SOLR_VERSION=9.3.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Wed, 16 Aug 2023 17:31:35 GMT
VOLUME [/var/solr]
# Wed, 16 Aug 2023 17:31:35 GMT
EXPOSE 8983
# Wed, 16 Aug 2023 17:31:35 GMT
WORKDIR /opt/solr
# Wed, 16 Aug 2023 17:31:35 GMT
USER 8983
# Wed, 16 Aug 2023 17:31:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Aug 2023 17:31:36 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:de1d106061fc0332ca262e39ed7d2aa6384ae341a084b39449e21c742802df9c`  
		Last Modified: Wed, 16 Aug 2023 04:39:02 GMT  
		Size: 28.6 MB (28644373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6e1ec281083c29c180a6e84015040293719595066688a13d0c4aa5c93a2ae9`  
		Last Modified: Wed, 16 Aug 2023 09:46:06 GMT  
		Size: 17.3 MB (17255619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eded86201f3d5ae0eead12626e3cd5cae5dc53a1822a1299cd466280cbfebc5b`  
		Last Modified: Wed, 16 Aug 2023 09:46:31 GMT  
		Size: 43.9 MB (43859757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd06318d226713b0e31cc5a908af46258108ba2091540a3de14d00f028dfb86`  
		Last Modified: Wed, 16 Aug 2023 09:46:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc44e4a9d6d72fb52fdb47a991c3a5a0dc96cfa0b2153e958d9968a7a76c4f86`  
		Last Modified: Wed, 16 Aug 2023 09:46:25 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b5143d8b1777c44cb82f2fece906d68f9aaaa21d8f9802a011678e02921b6`  
		Last Modified: Wed, 16 Aug 2023 17:33:32 GMT  
		Size: 62.8 MB (62800818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754571812044f572566e5f26e3286241458e40dcfe8a612cd6c18a80b13c8551`  
		Last Modified: Wed, 16 Aug 2023 17:33:27 GMT  
		Size: 4.3 KB (4329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124b7e7087023da3a079acc0e54102316903125e5c8e07926729662ce912ffe3`  
		Last Modified: Wed, 16 Aug 2023 17:33:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c44a44f63167ef843ffea467ef1ec7f8e3f993ba27f24feafb0c7717f6f3707`  
		Last Modified: Wed, 16 Aug 2023 17:33:27 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707cb04823320dc25d66629c8bcc01abb4099d3580eef7d56d9a7d04052f1eb`  
		Last Modified: Wed, 16 Aug 2023 17:33:27 GMT  
		Size: 1.8 MB (1775724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
