## `solr:slim`

```console
$ docker pull solr@sha256:abde2b73b127399e0341e1eaf7f326be6cc36f6eaf84c84b88b5acc1f68b1a80
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

### `solr:slim` - linux; amd64

```console
$ docker pull solr@sha256:b7602ad3dafed86325ae00028398d0323bfe1f5738f11bc2d01f731253457015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161006087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb4c41f0781090eb4e97652fd9802bf4c8a205ac296c4e9d0cbbcbb5dfc7e7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 13 Feb 2024 16:30:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=-slim
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f83aa5deb6ccbbbf16737e6f75185ba795df2bc26b41cc4e5d20242e889f61b`  
		Last Modified: Fri, 16 Feb 2024 02:49:49 GMT  
		Size: 64.3 MB (64327301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbd72e8814a5cb8bca5fc60cc0552dcd2af84b2360f5a4d79966fc7179ba433`  
		Last Modified: Fri, 16 Feb 2024 02:49:48 GMT  
		Size: 4.3 KB (4270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6c496648b252da616a24b3fb561299605193ead8131874ebe67641611cdd1`  
		Last Modified: Fri, 16 Feb 2024 02:49:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163beff9ff9bde414c09073c6695f4092b604f6a713438947191852402539e8a`  
		Last Modified: Fri, 16 Feb 2024 02:49:49 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01038b1b58bce30188183b1e10e0b5b42d48dea77850d2fef9947c0a6fb7ced0`  
		Last Modified: Fri, 16 Feb 2024 02:49:49 GMT  
		Size: 1.6 MB (1590785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:4329a9e81b4cb401c3767f4c31d04b9a556cc22db08180a33bff632a93847a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3369348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a57115d0ced52150f032c131f1d8e7437d05008568c2939b11f5c7babd9521`

```dockerfile
```

-	Layers:
	-	`sha256:eee26d1220ec0d29776a6d97ac3272d7ba979a529c058e2c2f74c815ed803ccc`  
		Last Modified: Fri, 16 Feb 2024 02:49:47 GMT  
		Size: 3.3 MB (3334482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530c0e9b0e13cdf9b8e80a96b49e7f6d8ff4cae592e58877a95c5e6a018604ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:47 GMT  
		Size: 34.9 KB (34866 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:6f6913dd41c500b30ff7530e6b040c56cd96a157f6a26b6b20303d4e01ae3971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155674986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fa6d89212053761a9fe32602615fa137098a676474be6862389a63a8fe41ba`
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
# Thu, 01 Feb 2024 23:40:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 23:40:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 23:40:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Feb 2024 23:43:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:43:49 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Thu, 01 Feb 2024 23:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 01 Feb 2024 23:44:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 01 Feb 2024 23:44:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 01 Feb 2024 23:44:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 12 Feb 2024 14:46:38 GMT
ARG SOLR_VERSION=9.5.0
# Mon, 12 Feb 2024 14:46:38 GMT
ARG SOLR_DIST=-slim
# Mon, 12 Feb 2024 14:46:38 GMT
ARG SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6
# Mon, 12 Feb 2024 14:46:38 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Mon, 12 Feb 2024 14:46:38 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 12 Feb 2024 14:46:38 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 12 Feb 2024 14:46:38 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 12 Feb 2024 14:46:38 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 12 Feb 2024 14:46:38 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 12 Feb 2024 14:46:38 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 12 Feb 2024 14:46:38 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 12 Feb 2024 14:46:38 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 12 Feb 2024 14:46:38 GMT
LABEL org.opencontainers.image.version=9.5.0
# Mon, 12 Feb 2024 14:46:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 12 Feb 2024 14:46:38 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 12 Feb 2024 14:46:38 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 12 Feb 2024 14:46:38 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 12 Feb 2024 14:46:38 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 12 Feb 2024 14:46:38 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 12 Feb 2024 14:46:38 GMT
VOLUME [/var/solr]
# Mon, 12 Feb 2024 14:46:38 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 12 Feb 2024 14:46:38 GMT
WORKDIR /opt/solr
# Mon, 12 Feb 2024 14:46:38 GMT
USER 8983
# Mon, 12 Feb 2024 14:46:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 14:46:38 GMT
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
	-	`sha256:ae55527c7f1d0c15e3698fc829ce1e71252b782cf8bcbd4fec7cd1ea5438cc02`  
		Last Modified: Wed, 14 Feb 2024 01:28:47 GMT  
		Size: 64.3 MB (64327398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6d75f5f485251f29bd769e4b57e88aa95362629025103e637fbd8dc983803c`  
		Last Modified: Wed, 14 Feb 2024 01:28:46 GMT  
		Size: 4.2 KB (4202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52c7fdcfb38f0ee9d1707debe7fd68b0c3384106aff92f191b7beb32faf5a0c`  
		Last Modified: Wed, 14 Feb 2024 01:28:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e506febbd185729ddd069981034ce61743f8bd08cd1a3ba7de9e02aa3b5d1c`  
		Last Modified: Wed, 14 Feb 2024 01:28:45 GMT  
		Size: 10.8 KB (10789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3238460b953b5df7077025810e27a481dce5064993d38a6ed5aa94d719ad80d`  
		Last Modified: Wed, 14 Feb 2024 01:28:47 GMT  
		Size: 1.4 MB (1415852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:6ed6aa318d9248a97911a699506afe00eb0492616df889c27234e2c019eb1399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330889f561e33420445329db7b01f226ae92f385a485792bd531c6cc9d2954bd`

```dockerfile
```

-	Layers:
	-	`sha256:07f9d01b99e6e3b604d29d9bc3e6a7e17f780ea5a2324f1dbee85e5588d29238`  
		Last Modified: Wed, 14 Feb 2024 01:28:45 GMT  
		Size: 3.3 MB (3266468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:642206b5f71b526982f909f4e0bd500939af29e3cdefa265348617549756a30a`  
		Last Modified: Wed, 14 Feb 2024 01:28:45 GMT  
		Size: 34.2 KB (34171 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:b26c6059c0d92b74f1eaf65d9e3487dc1ef7a760952f039806c8859b8d5b1a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159692868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9814c5547f6dca380b53039d2f43a977d8a63026b2146691f01e4d38efabbd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 13 Feb 2024 16:30:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=-slim
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bac6b544c281c39df6cde20776732e9b89dbfbbbb49870c60c9af5ef1df471`  
		Last Modified: Fri, 16 Feb 2024 04:55:46 GMT  
		Size: 18.9 MB (18860590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244992bb9e51f456f3e5c927182054789a275d47eba65099182705a8e1952dc2`  
		Last Modified: Fri, 16 Feb 2024 04:56:12 GMT  
		Size: 46.6 MB (46639325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e543faa97f71ea4edea5a6153e1b82e4e9143354356435ca0a085c427b9b07e`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b734e973751dd4636bc278f0ef5ee31fc8e10cc65a07ebd5ef57aa728870187`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df47c216f9c4c6fdc3bc60c0ef408ca44cbdb08563830aee8ecfee33c3e443ea`  
		Last Modified: Fri, 16 Feb 2024 14:18:26 GMT  
		Size: 64.3 MB (64327348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198487c63b8b0acf742bd4876c6857f3f532e197a506503e3e12a9b1c1cb8ed7`  
		Last Modified: Fri, 16 Feb 2024 14:18:24 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8599733f8827496eeb41008b699374e3b421a9fb561f192ef861ad1b1f6a12`  
		Last Modified: Fri, 16 Feb 2024 14:18:24 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbaac76beddbc50c6d843d80fc69536d41f8b58d2e776d9ebc54ba3eeccbeaa`  
		Last Modified: Fri, 16 Feb 2024 14:18:24 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9691d52b45e5672c76c5e6f0b480b45e99cc81a90414cf95af7b4fdc61e1cb`  
		Last Modified: Fri, 16 Feb 2024 14:18:25 GMT  
		Size: 1.4 MB (1449054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:7d9fd8efc46e7ee1d85355bfce8ff07ccf33db14eeb348c1fba5c2dfbb6f4373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3452307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a20033a17255292849393389a0bc18936bd8a1b7de830a90d60e5276a106be`

```dockerfile
```

-	Layers:
	-	`sha256:93395724f69accf5f84c713c3806661d35fb488a8178e4fb943b3fec80828989`  
		Last Modified: Fri, 16 Feb 2024 14:18:24 GMT  
		Size: 3.4 MB (3418247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7531f024b6c7d7b77c9f46bcf8b4c28466d717378a01f6dcb4ce3a72f797a7d`  
		Last Modified: Fri, 16 Feb 2024 14:18:24 GMT  
		Size: 34.1 KB (34060 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:35816c939e43742027c07fd51ffaad45b3d41d144e3c7cbdc97e0c6bcc17f04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167309161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465d6cc2f2bd928cb98b378d43ab3f384ba896acd0baa10a17f12ce416168582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 13 Feb 2024 16:30:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=-slim
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc402319b10feb1c6820fa2bc7cfba7869a3473e27191ab283db519e7e6da50`  
		Last Modified: Fri, 16 Feb 2024 03:08:21 GMT  
		Size: 18.7 MB (18726189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f9bec281d586fe857a730cd40136459428c7ccefda7ad98a1e0c5194e2d295`  
		Last Modified: Fri, 16 Feb 2024 03:08:53 GMT  
		Size: 47.0 MB (47012472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64d28cb5695f590c46c7d223348d7d58bfba0e23dec221f5343b0dca7a09bcb`  
		Last Modified: Fri, 16 Feb 2024 03:08:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aabc96be0541477c14b4c395f0cedb75eb6388609833afb6cb0da3a3b182c7`  
		Last Modified: Fri, 16 Feb 2024 03:08:45 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99e4ed0441bf9ea449ef1fa0a31b6042528fdce04141bf6fe6bb6830b74d49d`  
		Last Modified: Fri, 16 Feb 2024 09:41:07 GMT  
		Size: 64.3 MB (64327949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9214558ce636d5e56ca76d0a6e8e3135fc2141ba188bef1bc584ee1ec4759a7`  
		Last Modified: Fri, 16 Feb 2024 09:41:04 GMT  
		Size: 4.3 KB (4269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610ba2834ae025c871c87db306fc317c663a4713b70ccfd55b4cf3b84d28156f`  
		Last Modified: Fri, 16 Feb 2024 09:41:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3942eec062203ff44fc13fc6af81efab5f7c8c16f46ed0b0ef5cf828753f0335`  
		Last Modified: Fri, 16 Feb 2024 09:41:04 GMT  
		Size: 10.8 KB (10790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcd52adaa8fb62ea3eae10d8ddd8d8698a2e1176ebead8cb131954e712b6dd4`  
		Last Modified: Fri, 16 Feb 2024 09:41:06 GMT  
		Size: 1.6 MB (1597514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:a96e499d093e4bf403cdcf5ccb7886932b8ef4900361b4b835d8127e153ca660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3395436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bf11af65ac892c1225c515275f96b3634f1cac232b0348aeb061bc1fc4967b`

```dockerfile
```

-	Layers:
	-	`sha256:8c0bc27144bb99e816c8d5fbfc548b75b2796492aea3c54fc7ef80de63e40e3e`  
		Last Modified: Fri, 16 Feb 2024 09:41:05 GMT  
		Size: 3.4 MB (3361341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b951fd430c360a74454bb9ab3b0e703a5d29d69371de17215a76f43db40da8e`  
		Last Modified: Fri, 16 Feb 2024 09:41:04 GMT  
		Size: 34.1 KB (34095 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:90dba541a91b467c54518cf3ebe9ebd3f224ef7ddaabb3fe50f7c571dd34e9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155564164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7561ce2cd58e08ca46455d9052a50aaf48611f27875aa3541cc85100de6bfdfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 25 Jan 2024 18:07:14 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:07:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 18:07:16 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Thu, 25 Jan 2024 18:07:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:52:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 01:52:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 01:52:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:01:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:01:14 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 02 Feb 2024 02:05:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 02:05:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 02:05:25 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:05:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=-slim
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4d63bfd51bdce6fd8dfe83946feba0ea66b3823f4955c098602769d1933dfb1a`  
		Last Modified: Fri, 02 Feb 2024 00:42:52 GMT  
		Size: 28.7 MB (28655632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec92f300c69dd15c23ba2afafe2c0d431cee8fcae0a0a951bc7ea9d2864f204`  
		Last Modified: Fri, 02 Feb 2024 02:15:44 GMT  
		Size: 17.3 MB (17261495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1715c27a41db1f376e54036f4ac683eccafaa60dab557a8c5565b396bcb14a`  
		Last Modified: Fri, 02 Feb 2024 02:16:20 GMT  
		Size: 43.8 MB (43766001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5d40f49348dce3275dc8964d310061a5c44698ffdcb3190d77288d295ed1e6`  
		Last Modified: Fri, 02 Feb 2024 02:16:15 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546cf6b02cff72d9860940eb40153cbe7ebb26fe43e0b6fc4c2a4746c348e16a`  
		Last Modified: Fri, 02 Feb 2024 02:16:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6afa58f8acacdc2ab1ac40633b821a1621354b885c93c3ffff18c6652d46aa9`  
		Last Modified: Wed, 14 Feb 2024 04:48:04 GMT  
		Size: 64.3 MB (64327345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d0d2bbd280557ad5170ea1ac5ab44809a11040ec7797248843d854aef04330`  
		Last Modified: Wed, 14 Feb 2024 04:48:03 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee509bafdc48a4e27399814a44ca3735b0e59098a77b418c35c671bc70283d48`  
		Last Modified: Wed, 14 Feb 2024 04:48:03 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0110298705314cec2d802e0d9bbe8a46bd5c493f72886ce1ffca5e63a26afa97`  
		Last Modified: Wed, 14 Feb 2024 04:48:03 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81586fd03cd1d99dd705d8c1203881fd4348772f853108554228d32284583862`  
		Last Modified: Wed, 14 Feb 2024 04:48:04 GMT  
		Size: 1.5 MB (1537460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:e62f7fa017c34f424746fe7728560237754aedca2b2caa8e46b4f28cc4926141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3307577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f415cd45ee6fe82e9c2f78d597d6b45b099933082d4e175385a7ee4da8460da7`

```dockerfile
```

-	Layers:
	-	`sha256:6defebb49a3cd2f9f531b57576240e76d02aa2cb27a2c154e576cb2db9213ee7`  
		Last Modified: Wed, 14 Feb 2024 04:48:03 GMT  
		Size: 3.3 MB (3273527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d577ad8da9c1de5abb887001e14448cf4ee44b7c4eedfe6b2748e75a87f205b7`  
		Last Modified: Wed, 14 Feb 2024 04:48:03 GMT  
		Size: 34.0 KB (34050 bytes)  
		MIME: application/vnd.in-toto+json
