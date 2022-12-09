## `solr:latest`

```console
$ docker pull solr@sha256:971cd7a5c682390f8b1541ef74a8fd64d56c6a36e5c0849f6b48210a47b16fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:latest` - linux; amd64

```console
$ docker pull solr@sha256:d5c8885ad08bdf697a220eb76eccb8ee30d7e214a1460c3bc2f4ca78157a3c87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (331010337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af7db715550f7123188bbaae06df44589a870738c40b83beb05a41877fb5f44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:45:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:45:22 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Fri, 09 Dec 2022 01:46:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='34d6414710db27cd7760fe369135f3b9927ccc81410280606613166d4106d60a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        armhf|arm)          ESUM='9e0d1745139fe502f22df1e261d2ed1ad807085dd75a8b333d481289b579870d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='51dd491505bd2e096676b9dc8ecaf196d78993215af16c0f9dfddfe3dbc0205b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eeb1e92b8267e7e015908f3e3b80e48f418b37a2b4491f65290bc5d25e5daf93';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='11326464a14b63e6328d1d2088a23fb559c0e36b3f380e4c1f8dcbe160a8b95e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Dec 2022 01:46:26 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 09 Dec 2022 07:28:53 GMT
ARG SOLR_VERSION=9.1.0
# Fri, 09 Dec 2022 07:28:53 GMT
ARG SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926
# Fri, 09 Dec 2022 07:28:53 GMT
ARG SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C
# Fri, 09 Dec 2022 07:28:53 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 09 Dec 2022 07:28:53 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 09 Dec 2022 07:28:53 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 07:28:53 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 07:28:53 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 07:29:13 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Fri, 09 Dec 2022 07:29:14 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 09 Dec 2022 07:29:14 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 09 Dec 2022 07:29:14 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 09 Dec 2022 07:29:14 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 09 Dec 2022 07:29:14 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 09 Dec 2022 07:29:14 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 09 Dec 2022 07:29:14 GMT
LABEL org.opencontainers.image.version=9.1.0
# Fri, 09 Dec 2022 07:29:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 09 Dec 2022 07:29:14 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 09 Dec 2022 07:29:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 09 Dec 2022 07:29:16 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 09 Dec 2022 07:29:16 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 09 Dec 2022 07:29:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 09 Dec 2022 07:29:24 GMT
VOLUME [/var/solr]
# Fri, 09 Dec 2022 07:29:25 GMT
EXPOSE 8983
# Fri, 09 Dec 2022 07:29:25 GMT
WORKDIR /opt/solr
# Fri, 09 Dec 2022 07:29:25 GMT
USER 8983
# Fri, 09 Dec 2022 07:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Dec 2022 07:29:25 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b0873b98ac8f32b151346adbb3bebb71422b7f4d491cef4fe8fa08d19bf076`  
		Last Modified: Fri, 09 Dec 2022 01:52:23 GMT  
		Size: 20.1 MB (20086897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26a502e2cfaa51a64df04eae97cd6f2f2d99ca4fbcd4419f6bc9aed960e9882`  
		Last Modified: Fri, 09 Dec 2022 01:53:22 GMT  
		Size: 47.0 MB (46956274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459bdc265a8a62e4ecc0b7303d8268d09e98cab20931a8dec69443564d9f72db`  
		Last Modified: Fri, 09 Dec 2022 01:53:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e948057caabfd8aa4d74d44e694f29c77b1a10c86e637a14468c96e3ce8aefc1`  
		Last Modified: Fri, 09 Dec 2022 07:31:27 GMT  
		Size: 233.8 MB (233795838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915dc5fe0a70a39b8d1ff9d9c9e0a43993630a194d72361c9ec444ace9ccff08`  
		Last Modified: Fri, 09 Dec 2022 07:31:16 GMT  
		Size: 4.3 KB (4293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9d55286d4d59a130911e982e07763f2ca725c88fa068c49ec1d6b448f721d0`  
		Last Modified: Fri, 09 Dec 2022 07:31:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2670baf13166be97597194c0f9e23c5007a2d2462e65629265cb3f6d97282d4`  
		Last Modified: Fri, 09 Dec 2022 07:31:16 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8f2125142b7ca8fb95e26b9ee1126523b7ec8d2c819c76be8d2fc10ddbc484`  
		Last Modified: Fri, 09 Dec 2022 07:31:16 GMT  
		Size: 1.6 MB (1581691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm variant v7

```console
$ docker pull solr@sha256:1080b73f60fb34bf56b570fea9ecc38cdbf3fa5095869dcbac6c64010aa2f7e7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323240245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459dbdd10385bc3f544b41f6c9accc602813c7c2c478185506bb56789c0757c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Dec 2022 01:36:16 GMT
ADD file:b21aa237ba47147762a1b92947251163795189df45212a32e07ea3438a186e03 in / 
# Fri, 09 Dec 2022 01:36:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:07:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:07:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:07:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:10:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:10:50 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Fri, 09 Dec 2022 03:12:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='34d6414710db27cd7760fe369135f3b9927ccc81410280606613166d4106d60a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        armhf|arm)          ESUM='9e0d1745139fe502f22df1e261d2ed1ad807085dd75a8b333d481289b579870d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='51dd491505bd2e096676b9dc8ecaf196d78993215af16c0f9dfddfe3dbc0205b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eeb1e92b8267e7e015908f3e3b80e48f418b37a2b4491f65290bc5d25e5daf93';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='11326464a14b63e6328d1d2088a23fb559c0e36b3f380e4c1f8dcbe160a8b95e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Dec 2022 03:12:19 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 09 Dec 2022 06:09:57 GMT
ARG SOLR_VERSION=9.1.0
# Fri, 09 Dec 2022 06:09:57 GMT
ARG SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926
# Fri, 09 Dec 2022 06:09:57 GMT
ARG SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C
# Fri, 09 Dec 2022 06:09:57 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 09 Dec 2022 06:09:58 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 09 Dec 2022 06:09:58 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 06:09:58 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 06:09:58 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 06:10:29 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Fri, 09 Dec 2022 06:10:31 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 09 Dec 2022 06:10:31 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 09 Dec 2022 06:10:31 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 09 Dec 2022 06:10:31 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 09 Dec 2022 06:10:31 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 09 Dec 2022 06:10:31 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 09 Dec 2022 06:10:31 GMT
LABEL org.opencontainers.image.version=9.1.0
# Fri, 09 Dec 2022 06:10:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 09 Dec 2022 06:10:32 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 09 Dec 2022 06:10:32 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 09 Dec 2022 06:10:33 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 09 Dec 2022 06:10:33 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 09 Dec 2022 06:10:41 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 09 Dec 2022 06:10:41 GMT
VOLUME [/var/solr]
# Fri, 09 Dec 2022 06:10:41 GMT
EXPOSE 8983
# Fri, 09 Dec 2022 06:10:41 GMT
WORKDIR /opt/solr
# Fri, 09 Dec 2022 06:10:42 GMT
USER 8983
# Fri, 09 Dec 2022 06:10:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:10:42 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:cfbc8b467b3eb89e7c394402566b2965c83f3103dafb141203e0020a8acd3774`  
		Last Modified: Fri, 09 Dec 2022 01:38:40 GMT  
		Size: 24.6 MB (24589003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c28baf7ed12652cd7f4e26e1feed9e86c3f06e9e323f65f77388748b92781c`  
		Last Modified: Fri, 09 Dec 2022 03:20:19 GMT  
		Size: 19.5 MB (19464848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91474906434c7a76ff0b33ab8f5ec5032282f2467769af66cd68dddda1deb439`  
		Last Modified: Fri, 09 Dec 2022 03:21:29 GMT  
		Size: 44.5 MB (44500857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd126692ffe353110c6008765c265e189ce2fe08a2e56eeff8307b63847e188a`  
		Last Modified: Fri, 09 Dec 2022 03:21:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae64f8b443748c9cf2578787b660cd33715404bad526fce4f4abe2b3a228c037`  
		Last Modified: Fri, 09 Dec 2022 06:13:25 GMT  
		Size: 233.3 MB (233275770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b943181886a948cec528dc96006b9c5558b8705b54214415749bd4bb56936725`  
		Last Modified: Fri, 09 Dec 2022 06:13:07 GMT  
		Size: 4.2 KB (4225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb13003ec379af251a841a80ea89ad2a8da2c4db6fe1b3c0f691f23fc399b68`  
		Last Modified: Fri, 09 Dec 2022 06:13:07 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142bd8ff7401fe62b6ea1cb23ec7d1e13fb9b648e9bd3647bddaddd5bc3057a9`  
		Last Modified: Fri, 09 Dec 2022 06:13:07 GMT  
		Size: 8.0 KB (7999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9af704c58d42616a9e0865774288b3881aadcbb435e5a760b6e0351c15a9cf`  
		Last Modified: Fri, 09 Dec 2022 06:13:07 GMT  
		Size: 1.4 MB (1397164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:69003a59f63367c3e14a3f7b135d9eafd06f0a1fb7681908ea48a30de08d89c4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329631576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5193ee9d041a46f0108aa65b0903e2a42f1ee6f935ab729701ada3bfec459`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:38:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:38:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:38:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:41:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:41:25 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Fri, 09 Dec 2022 03:42:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='34d6414710db27cd7760fe369135f3b9927ccc81410280606613166d4106d60a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        armhf|arm)          ESUM='9e0d1745139fe502f22df1e261d2ed1ad807085dd75a8b333d481289b579870d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='51dd491505bd2e096676b9dc8ecaf196d78993215af16c0f9dfddfe3dbc0205b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eeb1e92b8267e7e015908f3e3b80e48f418b37a2b4491f65290bc5d25e5daf93';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='11326464a14b63e6328d1d2088a23fb559c0e36b3f380e4c1f8dcbe160a8b95e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Dec 2022 03:42:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 09 Dec 2022 06:14:15 GMT
ARG SOLR_VERSION=9.1.0
# Fri, 09 Dec 2022 06:14:15 GMT
ARG SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926
# Fri, 09 Dec 2022 06:14:15 GMT
ARG SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C
# Fri, 09 Dec 2022 06:14:15 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 09 Dec 2022 06:14:15 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 09 Dec 2022 06:14:15 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 06:14:15 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 06:14:15 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 06:14:42 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Fri, 09 Dec 2022 06:14:43 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 09 Dec 2022 06:14:43 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 09 Dec 2022 06:14:43 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 09 Dec 2022 06:14:43 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 09 Dec 2022 06:14:43 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 09 Dec 2022 06:14:43 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 09 Dec 2022 06:14:44 GMT
LABEL org.opencontainers.image.version=9.1.0
# Fri, 09 Dec 2022 06:14:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 09 Dec 2022 06:14:44 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 09 Dec 2022 06:14:44 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 09 Dec 2022 06:14:45 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 09 Dec 2022 06:14:45 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 09 Dec 2022 06:14:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 09 Dec 2022 06:14:52 GMT
VOLUME [/var/solr]
# Fri, 09 Dec 2022 06:14:52 GMT
EXPOSE 8983
# Fri, 09 Dec 2022 06:14:52 GMT
WORKDIR /opt/solr
# Fri, 09 Dec 2022 06:14:52 GMT
USER 8983
# Fri, 09 Dec 2022 06:14:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Dec 2022 06:14:52 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e6255f1d9634acbb611b17bafa5b0ec522018281353d85d93ff022b2cb8d08`  
		Last Modified: Fri, 09 Dec 2022 03:47:43 GMT  
		Size: 20.8 MB (20800924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4842b9157e67c223ff52e2b83e26b56da496dbea6b46c4a119a83d6ffb43a395`  
		Last Modified: Fri, 09 Dec 2022 03:48:33 GMT  
		Size: 46.4 MB (46398703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9191c480152f838e668fbfc5e95c440cafa592f303f581ead9215e025a001938`  
		Last Modified: Fri, 09 Dec 2022 03:48:28 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df500fec8d83e913453f69ca584a4d71d5fd72dfca8a3df425b914f2b88f297`  
		Last Modified: Fri, 09 Dec 2022 06:16:52 GMT  
		Size: 233.8 MB (233783402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799c4d9aff24d07732c792547537232f1b249cb10f1fca69637496c0f314bec3`  
		Last Modified: Fri, 09 Dec 2022 06:16:42 GMT  
		Size: 4.3 KB (4329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc91a941c3b38ce63657fbedba30b718cd5c6008e15b5c2fd760198a247484e7`  
		Last Modified: Fri, 09 Dec 2022 06:16:42 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f150411feebd87506fbd7417c36305bb30bf92a62f8bdcf3e877b0b42dc68f`  
		Last Modified: Fri, 09 Dec 2022 06:16:42 GMT  
		Size: 8.1 KB (8086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17bae04155aa786a086657393842ce2ed74e64cc9a216af046eb93ce36f1dcb0`  
		Last Modified: Fri, 09 Dec 2022 06:16:43 GMT  
		Size: 1.4 MB (1442583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:ecad42541b22b0a0430bfffc34e1ccd93320912fbd99539be9db82153a948979
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338437026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73af5431460e34ffab83a6b3377998420e56aed414072fb9ca9c148d3aeae309`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:36 GMT
ADD file:ca32a106475146fa5bd0f3e4920ea64671b1054f57a1f33d4681fe170deda313 in / 
# Fri, 09 Dec 2022 01:27:37 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:38:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 02:38:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 02:38:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 02:44:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:44:10 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Fri, 09 Dec 2022 02:46:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='34d6414710db27cd7760fe369135f3b9927ccc81410280606613166d4106d60a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        armhf|arm)          ESUM='9e0d1745139fe502f22df1e261d2ed1ad807085dd75a8b333d481289b579870d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='51dd491505bd2e096676b9dc8ecaf196d78993215af16c0f9dfddfe3dbc0205b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eeb1e92b8267e7e015908f3e3b80e48f418b37a2b4491f65290bc5d25e5daf93';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='11326464a14b63e6328d1d2088a23fb559c0e36b3f380e4c1f8dcbe160a8b95e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Dec 2022 02:46:16 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 09 Dec 2022 08:24:40 GMT
ARG SOLR_VERSION=9.1.0
# Fri, 09 Dec 2022 08:24:41 GMT
ARG SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926
# Fri, 09 Dec 2022 08:24:41 GMT
ARG SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C
# Fri, 09 Dec 2022 08:24:41 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 09 Dec 2022 08:24:42 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 09 Dec 2022 08:24:42 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 08:24:43 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 08:24:43 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 08:25:53 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Fri, 09 Dec 2022 08:25:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 09 Dec 2022 08:25:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 09 Dec 2022 08:25:57 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 09 Dec 2022 08:25:57 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 09 Dec 2022 08:25:58 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 09 Dec 2022 08:25:58 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 09 Dec 2022 08:25:58 GMT
LABEL org.opencontainers.image.version=9.1.0
# Fri, 09 Dec 2022 08:25:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 09 Dec 2022 08:25:59 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 09 Dec 2022 08:26:00 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 09 Dec 2022 08:26:01 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 09 Dec 2022 08:26:02 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 09 Dec 2022 08:26:13 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 09 Dec 2022 08:26:13 GMT
VOLUME [/var/solr]
# Fri, 09 Dec 2022 08:26:13 GMT
EXPOSE 8983
# Fri, 09 Dec 2022 08:26:14 GMT
WORKDIR /opt/solr
# Fri, 09 Dec 2022 08:26:14 GMT
USER 8983
# Fri, 09 Dec 2022 08:26:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Dec 2022 08:26:15 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d198f08d15a240101119086908bf4c5035dc657d52bfe206ddeede273c6b84f3`  
		Last Modified: Fri, 09 Dec 2022 01:30:09 GMT  
		Size: 33.3 MB (33299473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab1a4382d1a389e1c47c6c872157649690433c49f575b7c4f6d972d3c3dee2b`  
		Last Modified: Fri, 09 Dec 2022 02:56:45 GMT  
		Size: 22.1 MB (22058308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e37dfc20c7b716ec76a67cc9562fe5c570c0427b7c35fe2b4a5a34eedf1f5d`  
		Last Modified: Fri, 09 Dec 2022 02:58:21 GMT  
		Size: 46.8 MB (46807779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b70daeda21e7acd16245586178a724193832701ca89805de6ddfa6c5e058a0`  
		Last Modified: Fri, 09 Dec 2022 02:58:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a53ab0ae4fbf312a3237e65b4a66ddbdb20b82024017ef254b96d781e4aa949`  
		Last Modified: Fri, 09 Dec 2022 08:30:28 GMT  
		Size: 234.7 MB (234654621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759070eef835545dca7ee13246edf8b40f0fb4930500dd7caa8ba686ce391c55`  
		Last Modified: Fri, 09 Dec 2022 08:30:07 GMT  
		Size: 4.3 KB (4296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f676f890531793529591a156cc1fe727e6dfdaf084faea0e64c6d3c6b3d06558`  
		Last Modified: Fri, 09 Dec 2022 08:30:07 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a915428380e9a1b2ef7782ad639807d3fd82c23cf141ce414ba60ea2d55f92`  
		Last Modified: Fri, 09 Dec 2022 08:30:07 GMT  
		Size: 8.1 KB (8087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca990d372e861c41668ad7e7490430dbbfbbe4b65868e9388c732863a8452054`  
		Last Modified: Fri, 09 Dec 2022 08:30:07 GMT  
		Size: 1.6 MB (1604085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:52ded801abec8070c12c3a119c863975c265cbe1d3feb13c484f4532680ff6f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325499813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddd12999e3866abee9d8cab53b0eb558cc2cacafa49d770c19ba9b0d49d713f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:40 GMT
ADD file:3d26982d2188d52ed2423587d3d2597c1f8ff614c19408d892cadc91d3743deb in / 
# Fri, 09 Dec 2022 01:52:43 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:11:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 02:11:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 02:11:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 02:15:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:15:59 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Fri, 09 Dec 2022 02:18:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='34d6414710db27cd7760fe369135f3b9927ccc81410280606613166d4106d60a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        armhf|arm)          ESUM='9e0d1745139fe502f22df1e261d2ed1ad807085dd75a8b333d481289b579870d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='51dd491505bd2e096676b9dc8ecaf196d78993215af16c0f9dfddfe3dbc0205b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eeb1e92b8267e7e015908f3e3b80e48f418b37a2b4491f65290bc5d25e5daf93';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='11326464a14b63e6328d1d2088a23fb559c0e36b3f380e4c1f8dcbe160a8b95e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Dec 2022 02:18:23 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 09 Dec 2022 04:20:44 GMT
ARG SOLR_VERSION=9.1.0
# Fri, 09 Dec 2022 04:20:44 GMT
ARG SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926
# Fri, 09 Dec 2022 04:20:45 GMT
ARG SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C
# Fri, 09 Dec 2022 04:20:45 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 09 Dec 2022 04:20:46 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 09 Dec 2022 04:20:46 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 04:20:47 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 04:20:47 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz
# Fri, 09 Dec 2022 04:21:23 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Fri, 09 Dec 2022 04:21:32 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 09 Dec 2022 04:21:32 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 09 Dec 2022 04:21:33 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 09 Dec 2022 04:21:33 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 09 Dec 2022 04:21:34 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 09 Dec 2022 04:21:34 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 09 Dec 2022 04:21:35 GMT
LABEL org.opencontainers.image.version=9.1.0
# Fri, 09 Dec 2022 04:21:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 09 Dec 2022 04:21:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 09 Dec 2022 04:21:37 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 09 Dec 2022 04:21:38 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 09 Dec 2022 04:21:39 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 09 Dec 2022 04:21:45 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.0/solr-9.1.0.tgz SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=16715fe50a74bc4906f655531523875e9e5d4a013aea22afff10a52dc6f05a8b62e079aee75cd9f2e250300e40071140c0a966cbd51af811a622f2f1f0b0c926 SOLR_VERSION=9.1.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 09 Dec 2022 04:21:46 GMT
VOLUME [/var/solr]
# Fri, 09 Dec 2022 04:21:46 GMT
EXPOSE 8983
# Fri, 09 Dec 2022 04:21:46 GMT
WORKDIR /opt/solr
# Fri, 09 Dec 2022 04:21:46 GMT
USER 8983
# Fri, 09 Dec 2022 04:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Dec 2022 04:21:47 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5d330d9ae4f68425a719ebb93a3911994ee56b1328cf256fc3c44a4050de22ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:57 GMT  
		Size: 27.0 MB (27016083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d57ebcbddf1c3cd78b6b6496f2fea9dc9a32bcce47843ed876abc3a51294ce2`  
		Last Modified: Fri, 09 Dec 2022 02:25:04 GMT  
		Size: 19.5 MB (19527858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7220fb304b6bd7a55bd7d77ae0b73a2eaa863d173da6530805d4adfc7306546d`  
		Last Modified: Fri, 09 Dec 2022 02:25:54 GMT  
		Size: 43.7 MB (43737314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fa149eb8250221c7b363042e36bfa16c25e5e35ced548326a6ad3a78c4063f`  
		Last Modified: Fri, 09 Dec 2022 02:25:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a008f63669257ca1413c080e815354edcc7c54d8074541feef6d85bd986bd639`  
		Last Modified: Fri, 09 Dec 2022 04:24:55 GMT  
		Size: 233.7 MB (233709564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831e81b781ff3a1010a30c85e10cdc368b92de0086de3fa9d9827cf9f530d893`  
		Last Modified: Fri, 09 Dec 2022 04:24:45 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef61e767d1dbeefa1b844ffd1ba2731a498f13f8576f4dbd715f0366aa9130ac`  
		Last Modified: Fri, 09 Dec 2022 04:24:45 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4750cc330e7a03513a3dad6422a3706f194afd5dadf8df9976352d74be6d2eba`  
		Last Modified: Fri, 09 Dec 2022 04:24:45 GMT  
		Size: 8.1 KB (8090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897c94b3261fe6d102ac58de912f97d2d18d979a43f3b07d59a9160283b1680`  
		Last Modified: Fri, 09 Dec 2022 04:24:46 GMT  
		Size: 1.5 MB (1496195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
