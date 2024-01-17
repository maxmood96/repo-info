## `solr:latest`

```console
$ docker pull solr@sha256:c5486069406fae1041e0e711f8fdca4934e7720d45407e012c0b2a6224b5c21b
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
$ docker pull solr@sha256:4e9b6794895f1f6685a61d587b63e2f0caa2b6f9a5a2c0e67613d4f160d9540d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.6 MB (376604087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7335f3162d5e87bb49d15fb9d9046e68c3aac0f0e78788c5b5f840fb18b27c7`
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
# Wed, 17 Jan 2024 16:40:46 GMT
ARG SOLR_VERSION=9.4.0
# Wed, 17 Jan 2024 16:40:46 GMT
ARG SOLR_DIST=
# Wed, 17 Jan 2024 16:40:46 GMT
ARG SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5
# Wed, 17 Jan 2024 16:40:46 GMT
ARG SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E
# Wed, 17 Jan 2024 16:40:46 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 17 Jan 2024 16:41:20 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Wed, 17 Jan 2024 16:41:21 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 17 Jan 2024 16:41:21 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 17 Jan 2024 16:41:21 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 17 Jan 2024 16:41:21 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 17 Jan 2024 16:41:21 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 17 Jan 2024 16:41:21 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 17 Jan 2024 16:41:21 GMT
LABEL org.opencontainers.image.version=9.4.0
# Wed, 17 Jan 2024 16:41:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 17 Jan 2024 16:41:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 17 Jan 2024 16:41:22 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Wed, 17 Jan 2024 16:41:23 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Wed, 17 Jan 2024 16:41:23 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Wed, 17 Jan 2024 16:41:31 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Jan 2024 16:41:31 GMT
VOLUME [/var/solr]
# Wed, 17 Jan 2024 16:41:31 GMT
EXPOSE 8983
# Wed, 17 Jan 2024 16:41:32 GMT
WORKDIR /opt/solr
# Wed, 17 Jan 2024 16:41:32 GMT
USER 8983
# Wed, 17 Jan 2024 16:41:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 16:41:32 GMT
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
	-	`sha256:c4a535407f887499b622f76874b8b85efd24ddc4b0a0ac9f4c2c2f2fbfa18eb0`  
		Last Modified: Wed, 17 Jan 2024 16:48:38 GMT  
		Size: 279.7 MB (279704296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be777ab2706ce3a2629b315d8236ceb1dda704f07f2f6954aec1a0c72d8719c5`  
		Last Modified: Wed, 17 Jan 2024 16:48:26 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea3c23d6fa43e439a23122fac8602c9097909a9024f5b7108c0eb233e0f9869`  
		Last Modified: Wed, 17 Jan 2024 16:48:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6445e9114942e5980e30ae7de417f0bb25dc21937dd8bd5c5c0670c69f989077`  
		Last Modified: Wed, 17 Jan 2024 16:48:26 GMT  
		Size: 10.8 KB (10847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe145567c183a2cde15d111d88777af1ecfa7b28330fe9b97e47eceb84ff3339`  
		Last Modified: Wed, 17 Jan 2024 16:48:27 GMT  
		Size: 1.8 MB (1828991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm variant v7

```console
$ docker pull solr@sha256:ba506645cba3249ffd164eb1b8c7f29468e0f883be6c61457f81e6bf27599c2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.3 MB (371281681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6af480667900fb57203562ddfc12ce033ac7b8a2f3603f91ded6840ff057c46`
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
# Wed, 17 Jan 2024 09:41:53 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Wed, 17 Jan 2024 09:42:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 09:42:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 09:42:32 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 09:42:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Jan 2024 11:38:18 GMT
ARG SOLR_VERSION=9.4.0
# Wed, 17 Jan 2024 11:38:19 GMT
ARG SOLR_DIST=
# Wed, 17 Jan 2024 11:38:19 GMT
ARG SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5
# Wed, 17 Jan 2024 11:38:19 GMT
ARG SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E
# Wed, 17 Jan 2024 11:38:19 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 17 Jan 2024 11:39:19 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Wed, 17 Jan 2024 11:39:21 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 17 Jan 2024 11:39:21 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 17 Jan 2024 11:39:22 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 17 Jan 2024 11:39:22 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 17 Jan 2024 11:39:22 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 17 Jan 2024 11:39:22 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 17 Jan 2024 11:39:23 GMT
LABEL org.opencontainers.image.version=9.4.0
# Wed, 17 Jan 2024 11:39:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 17 Jan 2024 11:39:23 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 17 Jan 2024 11:39:26 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Wed, 17 Jan 2024 11:39:28 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Wed, 17 Jan 2024 11:39:30 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Wed, 17 Jan 2024 11:39:42 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Jan 2024 11:39:42 GMT
VOLUME [/var/solr]
# Wed, 17 Jan 2024 11:39:43 GMT
EXPOSE 8983
# Wed, 17 Jan 2024 11:39:43 GMT
WORKDIR /opt/solr
# Wed, 17 Jan 2024 11:39:44 GMT
USER 8983
# Wed, 17 Jan 2024 11:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 11:39:44 GMT
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
	-	`sha256:c6ee69922ab4277b4963ad889f16970d3babdca44711949d7c14975da390fff5`  
		Last Modified: Wed, 17 Jan 2024 09:45:24 GMT  
		Size: 44.8 MB (44787083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670be13a1da7573f737bd1068f3e94f8548eee127fc98f85fa13ef3d34641e52`  
		Last Modified: Wed, 17 Jan 2024 09:45:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acba2a35d2a216f6590167f78175ee24f0b6ab0ec87e3200d9c7a17f10d08572`  
		Last Modified: Wed, 17 Jan 2024 09:45:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee1d86f6452c7bc890e6b08e5ceae18deceed25873b56b7d2bd327e60784e93`  
		Last Modified: Wed, 17 Jan 2024 11:49:13 GMT  
		Size: 279.7 MB (279705474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3471d13e5dcd9ee5646658d8b310406eda2bc074385dad8ad0a676621083b849`  
		Last Modified: Wed, 17 Jan 2024 11:48:50 GMT  
		Size: 4.2 KB (4220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8237a04ba569c9dc348be9888016ff9c555e9a056f81a23648151250b71e746`  
		Last Modified: Wed, 17 Jan 2024 11:48:50 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8205652bd54098b6f2621cdcd158729d96d26e4ada2575c8af23174ac1f9b0e`  
		Last Modified: Wed, 17 Jan 2024 11:48:50 GMT  
		Size: 10.9 KB (10864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b134f56f0af5ee1ceaa7cc7f1355fe6f6cacf85d52e3895f70a0e0694026f9da`  
		Last Modified: Wed, 17 Jan 2024 11:48:50 GMT  
		Size: 1.7 MB (1655203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:fbb40ba32b4092aa7e81f49b66dea2628b66950121853ac6792674ee82ce75b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.3 MB (375292247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfc0b405e748d6fab80fc1efc36c91515c12b3858e884a18abae7d46facb6d2`
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
# Wed, 17 Jan 2024 11:38:18 GMT
ARG SOLR_VERSION=9.4.0
# Wed, 17 Jan 2024 11:38:18 GMT
ARG SOLR_DIST=
# Wed, 17 Jan 2024 11:38:18 GMT
ARG SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5
# Wed, 17 Jan 2024 11:38:18 GMT
ARG SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E
# Wed, 17 Jan 2024 11:38:18 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 17 Jan 2024 11:38:45 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Wed, 17 Jan 2024 11:38:47 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 17 Jan 2024 11:38:47 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 17 Jan 2024 11:38:47 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 17 Jan 2024 11:38:47 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 17 Jan 2024 11:38:47 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 17 Jan 2024 11:38:47 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 17 Jan 2024 11:38:47 GMT
LABEL org.opencontainers.image.version=9.4.0
# Wed, 17 Jan 2024 11:38:47 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 17 Jan 2024 11:38:47 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 17 Jan 2024 11:38:48 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Wed, 17 Jan 2024 11:38:48 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Wed, 17 Jan 2024 11:38:49 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Wed, 17 Jan 2024 11:38:55 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Jan 2024 11:38:55 GMT
VOLUME [/var/solr]
# Wed, 17 Jan 2024 11:38:55 GMT
EXPOSE 8983
# Wed, 17 Jan 2024 11:38:55 GMT
WORKDIR /opt/solr
# Wed, 17 Jan 2024 11:38:55 GMT
USER 8983
# Wed, 17 Jan 2024 11:38:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 11:38:56 GMT
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
	-	`sha256:ad8bf53a7ea1ac702715def59a088856f72bd147d168dbbf99b8d9cbd2106e23`  
		Last Modified: Wed, 17 Jan 2024 11:44:26 GMT  
		Size: 279.7 MB (279704431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc49b6c8e21a5a1e554f72e8a66f3531bac7a8326e06192de9d920d63bc5bbe5`  
		Last Modified: Wed, 17 Jan 2024 11:44:16 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a1150de81952ffd58ae581450d51dd17fc7b53678ffe2e95915b96ecab6412`  
		Last Modified: Wed, 17 Jan 2024 11:44:16 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d302644d638a3d7bbf3cf6a3e57d24e797ff62abc72d209a802644e631ec44`  
		Last Modified: Wed, 17 Jan 2024 11:44:16 GMT  
		Size: 10.9 KB (10852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2f8deeebb32d97feade61d5dcb3c24bfd1e80d8dabca922e6802cb2d3949df`  
		Last Modified: Wed, 17 Jan 2024 11:44:16 GMT  
		Size: 1.7 MB (1687778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:97bd055a4d8b1837c17b838553415ea1aa343867ee2119f70913abb9b491e872
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382939081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a177580bfe77e1c2a4fe621718d341a62c973e09dcd4b418b80882b8c28ff275`
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
# Wed, 17 Jan 2024 07:33:28 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Wed, 17 Jan 2024 07:34:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 07:34:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 07:34:33 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 07:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Jan 2024 09:34:27 GMT
ARG SOLR_VERSION=9.4.0
# Wed, 17 Jan 2024 09:34:27 GMT
ARG SOLR_DIST=
# Wed, 17 Jan 2024 09:34:27 GMT
ARG SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5
# Wed, 17 Jan 2024 09:34:28 GMT
ARG SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E
# Wed, 17 Jan 2024 09:34:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 17 Jan 2024 09:35:14 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Wed, 17 Jan 2024 09:35:17 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 17 Jan 2024 09:35:18 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 17 Jan 2024 09:35:18 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 17 Jan 2024 09:35:18 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 17 Jan 2024 09:35:19 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 17 Jan 2024 09:35:19 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 17 Jan 2024 09:35:20 GMT
LABEL org.opencontainers.image.version=9.4.0
# Wed, 17 Jan 2024 09:35:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 17 Jan 2024 09:35:21 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 17 Jan 2024 09:35:22 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Wed, 17 Jan 2024 09:35:23 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Wed, 17 Jan 2024 09:35:24 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Wed, 17 Jan 2024 09:35:34 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Jan 2024 09:35:35 GMT
VOLUME [/var/solr]
# Wed, 17 Jan 2024 09:35:35 GMT
EXPOSE 8983
# Wed, 17 Jan 2024 09:35:35 GMT
WORKDIR /opt/solr
# Wed, 17 Jan 2024 09:35:35 GMT
USER 8983
# Wed, 17 Jan 2024 09:35:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:35:36 GMT
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
	-	`sha256:f241a20dbdb68ed5978b41eca3f937e1bb57bf13c98cba61759e0a2b2a086039`  
		Last Modified: Wed, 17 Jan 2024 07:38:37 GMT  
		Size: 47.0 MB (46999731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4cda891a1f47a002ac4f53ad8b0c6a27560c234eca077ea5f961835e5cdc8f9`  
		Last Modified: Wed, 17 Jan 2024 07:38:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087f381ba62669e9a868b7a354cb1cc13677a566407ffa21e4d794d8654129e5`  
		Last Modified: Wed, 17 Jan 2024 07:38:29 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a7423364bb91a08329263a3cbedd9839684cf6cc327acea69bb98383bc5146`  
		Last Modified: Wed, 17 Jan 2024 09:48:40 GMT  
		Size: 279.7 MB (279704800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8635d19340c42a21a9df00962c2e9949df04c6d0db137ec01848736673e561`  
		Last Modified: Wed, 17 Jan 2024 09:48:27 GMT  
		Size: 4.3 KB (4293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169ed0763a8f51abcdb738db7c860502efa8599fa2351132305ec999e80c8f39`  
		Last Modified: Wed, 17 Jan 2024 09:48:27 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8233e79471dcdba98960b374fe2ed516b4e26cafcc65893594879ee1e7325931`  
		Last Modified: Wed, 17 Jan 2024 09:48:27 GMT  
		Size: 10.8 KB (10848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5636160631f3a35266ef56c2b107e15152cc3020dd6bad625484efbc31a0ad4`  
		Last Modified: Wed, 17 Jan 2024 09:48:27 GMT  
		Size: 1.8 MB (1835496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:3616161fc83f37fa5825bdf46c4414db879a77cca29ca0f435872ec255c950b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.2 MB (371166718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733c345c38654d09cc90297e346bedcdc3df4681369a84e2a7e76d62ecac1ea4`
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
# Wed, 17 Jan 2024 16:35:03 GMT
ARG SOLR_VERSION=9.4.0
# Wed, 17 Jan 2024 16:35:03 GMT
ARG SOLR_DIST=
# Wed, 17 Jan 2024 16:35:03 GMT
ARG SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5
# Wed, 17 Jan 2024 16:35:03 GMT
ARG SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E
# Wed, 17 Jan 2024 16:35:04 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 17 Jan 2024 16:35:39 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Wed, 17 Jan 2024 16:35:44 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 17 Jan 2024 16:35:45 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 17 Jan 2024 16:35:45 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 17 Jan 2024 16:35:45 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 17 Jan 2024 16:35:45 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 17 Jan 2024 16:35:45 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 17 Jan 2024 16:35:45 GMT
LABEL org.opencontainers.image.version=9.4.0
# Wed, 17 Jan 2024 16:35:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 17 Jan 2024 16:35:45 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 17 Jan 2024 16:35:46 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Wed, 17 Jan 2024 16:35:46 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Wed, 17 Jan 2024 16:35:47 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Wed, 17 Jan 2024 16:35:53 GMT
# ARGS: SOLR_DIST= SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=7147caaec5290049b721f9a4e8b0c09b1775315fc4aa790fa7a88a783a45a61815b3532a938731fd583e91195492c4176f3c87d0438216dab26a07a4da51c1f5 SOLR_VERSION=9.4.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Jan 2024 16:35:53 GMT
VOLUME [/var/solr]
# Wed, 17 Jan 2024 16:35:53 GMT
EXPOSE 8983
# Wed, 17 Jan 2024 16:35:53 GMT
WORKDIR /opt/solr
# Wed, 17 Jan 2024 16:35:53 GMT
USER 8983
# Wed, 17 Jan 2024 16:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 16:35:53 GMT
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
	-	`sha256:01e62dcaf3b80a961f9b251cf411c7cf93017eb7e64e9f0a363a658eae286fed`  
		Last Modified: Wed, 17 Jan 2024 16:51:19 GMT  
		Size: 279.7 MB (279704652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcda5641b04dfd4481ae4e398181863fb735d3bd9204358606a2a96ee850937`  
		Last Modified: Wed, 17 Jan 2024 16:51:07 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97b4124231762a547d80f3044e83a5bb1aa2fe95fc71859fd7f96cb3d26cfd3`  
		Last Modified: Wed, 17 Jan 2024 16:51:07 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5f3bf0a758f15d205cf65a91f7cc31a36e6e57ea8471e6d01f48fbb0c1f381`  
		Last Modified: Wed, 17 Jan 2024 16:51:07 GMT  
		Size: 10.8 KB (10850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc3dd367afc90576e9098c4a212a17902bbb38a8d7d922f9f088755f8465380`  
		Last Modified: Wed, 17 Jan 2024 16:51:07 GMT  
		Size: 1.8 MB (1775817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
