## `solr:9-slim`

```console
$ docker pull solr@sha256:85a532976af89eee31a3a01f8dffda29bbfbafc5341fa5dd86d500ffd7ecf60a
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

### `solr:9-slim` - linux; amd64

```console
$ docker pull solr@sha256:7dbd6ed92e88d79a634396dc30d59be6f2fe3174569e2fb18aca88359d035355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157020359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5412a7e01df33e8b71a80a3ebe2df7f1fdea6fa3f7983799407b59a04cbddb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5161e45ecd8d096f978edcb483c5ed70580526e02a1f8155653ca1c6c192f097`  
		Last Modified: Fri, 23 Aug 2024 19:27:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6628cf8054ba74852eab4e741f8bb0ac4aa9f91189a708d47db58b93b55a58a1`  
		Last Modified: Mon, 09 Sep 2024 19:13:22 GMT  
		Size: 64.8 MB (64822352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4613b45416bb32d2ee7f475f9ddd16b8954e4f7f99dc37e78f7056a63b3a0daf`  
		Last Modified: Mon, 09 Sep 2024 19:13:20 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f41a14339ea52552e4dea8695c31eb0d427976861cc5052c28941c747c7d9`  
		Last Modified: Mon, 09 Sep 2024 19:13:20 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15379b89c34d67698a86d011b43ccf757b273b3ebbeece39c341a6ce4802e6bc`  
		Last Modified: Mon, 09 Sep 2024 19:13:20 GMT  
		Size: 10.8 KB (10783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c47b3a303cbdf7ccc24f9d279e53d7fe8af2a507d98e23a21f1e32c9172c8bb`  
		Last Modified: Mon, 09 Sep 2024 19:13:22 GMT  
		Size: 1.6 MB (1588633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:7d09e63c15e977b1b8c4807c09ad0858d9a58d42cdb03f3ddc6fdbfd1a7123da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec415a7b112d3453b567edfb042081ed7747132ba302e10613a1a8e16a40725`

```dockerfile
```

-	Layers:
	-	`sha256:5821dcf56c71f4ab8a9c7f2cf5fb865f9f37f767ee20a649bb4d309247fdfd32`  
		Last Modified: Mon, 09 Sep 2024 19:13:21 GMT  
		Size: 3.7 MB (3706729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af43d592605686f3e0a3b268d8b0c49665609fda4acb1ae9c84dec1b7d72838c`  
		Last Modified: Mon, 09 Sep 2024 19:13:20 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:f15c86f231ad2fbf7b30d7c9f0c206d6b94a1b06d101b0b9a9e2fe6243475e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154138306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29b902c99566affaba9bc0a509ad60a73190c54834495b43f4dad5858548cdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 29 May 2024 20:45:28 GMT
ARG RELEASE
# Wed, 29 May 2024 20:45:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 29 May 2024 20:45:28 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=-slim
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 20:45:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
VOLUME [/var/solr]
# Wed, 29 May 2024 20:45:28 GMT
EXPOSE map[8983/tcp:{}]
# Wed, 29 May 2024 20:45:28 GMT
WORKDIR /opt/solr
# Wed, 29 May 2024 20:45:28 GMT
USER 8983
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaccc9f07c9a604bcc09b1f72d88fddec7cb0ab55847ecbbde2d95d7ce3f5d52`  
		Last Modified: Fri, 23 Aug 2024 22:55:57 GMT  
		Size: 64.7 MB (64716512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7694406d8ba0436b0c5a6acced2f0c63ba54fd0204b6ce70aa7789270cf5fcbd`  
		Last Modified: Fri, 23 Aug 2024 22:55:55 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00a5d43b91df2a8e3b0fc145fe5bfce9a01b3397f3fc9221039bfcf459e458`  
		Last Modified: Fri, 23 Aug 2024 22:55:55 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7974108d9eb90783102bb6581205db1ac783514b8ca935079eaec4eaf7cf28`  
		Last Modified: Fri, 23 Aug 2024 22:55:55 GMT  
		Size: 10.8 KB (10780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d55c9152b2d46781827a43cdd884cf79ae9c6b878a9c6e6dcec82d378a81c3`  
		Last Modified: Fri, 23 Aug 2024 22:55:56 GMT  
		Size: 1.4 MB (1447492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:ff17d50c3fe6cd69012ba3ed7f3b4d81b79af41cc7a76cbfe4f1f8b043a4b582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db56de4e996416e5e5823448f232ff3bb7ab3598c49b2bf141548e83223fafcc`

```dockerfile
```

-	Layers:
	-	`sha256:7e77c2af3761e2f426c8e862ac983a49b394e571ea2112b50c774ec8394d23b2`  
		Last Modified: Fri, 23 Aug 2024 22:55:55 GMT  
		Size: 3.7 MB (3704470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99990e77c827bbe555381df28e805253e9fbf5c519f9cd5c1811ae2d1b10090`  
		Last Modified: Fri, 23 Aug 2024 22:55:54 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:c51273abd36330bad85142f5de76f7b7bfefa275f71e332d629e8ca5a0e9058a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162748703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b9c8afa5f4d15de15b38400f5619ea9cce46528a1acc3eb682923976f228dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 29 May 2024 20:45:28 GMT
ARG RELEASE
# Wed, 29 May 2024 20:45:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 29 May 2024 20:45:28 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=-slim
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 20:45:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
VOLUME [/var/solr]
# Wed, 29 May 2024 20:45:28 GMT
EXPOSE map[8983/tcp:{}]
# Wed, 29 May 2024 20:45:28 GMT
WORKDIR /opt/solr
# Wed, 29 May 2024 20:45:28 GMT
USER 8983
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdf38f664ed28bcdf7c6283707b320f9cdd22314bee0b43f5abc9e21972523`  
		Last Modified: Fri, 23 Aug 2024 20:46:21 GMT  
		Size: 64.7 MB (64716876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd8e3959e72e1abf2ea41e3b7506141563a0ec81703a98491280daf09cfe771`  
		Last Modified: Fri, 23 Aug 2024 20:46:18 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ab287fa348cbe7ed429e56f8d976cd61ca21e4fc734d125cd222eccea4661d`  
		Last Modified: Fri, 23 Aug 2024 20:46:18 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da804580d4767846eb76997256a4349fdce2ea6b946b6c8b137eb016f52169`  
		Last Modified: Fri, 23 Aug 2024 20:46:18 GMT  
		Size: 10.8 KB (10786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7f0f4aa653767232d524b8369e0b942605f807e2aa667bb51e9f266c0f4ff8`  
		Last Modified: Fri, 23 Aug 2024 20:46:19 GMT  
		Size: 1.6 MB (1595512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1fcbd4b33c11b15e24f9649054c50a4818a4d584e9aaf03e845c5a93f8c2b6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3bcf254546adb0ab4b6d07fce5d172fe22ff140a2a7e02d4d7f1679e6ba5d7`

```dockerfile
```

-	Layers:
	-	`sha256:d9c48ced867cff6f992b060eb5dc98cc378fa87fc7d93b8e61742a7967146c0d`  
		Last Modified: Fri, 23 Aug 2024 20:46:18 GMT  
		Size: 3.7 MB (3708703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da1774d8dd9a504ff6c3790d49975b57f818510c941c8e3d7f3e8a92440e2bd6`  
		Last Modified: Fri, 23 Aug 2024 20:46:18 GMT  
		Size: 34.2 KB (34156 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:cf774165360b1f0d083f29a492e662afd8f589642ec6c8c01171b3847b5f91d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151727351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf3ed1a16736d4dc63e3ac968cee04efa5a47d33d54102b60fdc1209386fa12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 29 May 2024 20:45:28 GMT
ARG RELEASE
# Wed, 29 May 2024 20:45:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 29 May 2024 20:45:28 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=-slim
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 20:45:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
VOLUME [/var/solr]
# Wed, 29 May 2024 20:45:28 GMT
EXPOSE map[8983/tcp:{}]
# Wed, 29 May 2024 20:45:28 GMT
WORKDIR /opt/solr
# Wed, 29 May 2024 20:45:28 GMT
USER 8983
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436b27d7c7e10a663ee6272640668b780b0fc626cf34c50e8fbae3c0488723b1`  
		Last Modified: Fri, 23 Aug 2024 19:47:54 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f94de5119feec695668ce135ee3ede18f789fc9303efc7e0afdd351282f4ddd`  
		Last Modified: Sat, 24 Aug 2024 00:16:42 GMT  
		Size: 64.7 MB (64716592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36d556f8fe8d49ca7ddc6d051782d369b36b957a593faeea8a695a8b2cae41a`  
		Last Modified: Sat, 24 Aug 2024 00:16:36 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf2ad98d817b16043ff35262bfba59b9bcf566dc4e8e1be4bd06d544b7731d`  
		Last Modified: Sat, 24 Aug 2024 00:16:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad42c66d7c4a068bac6f4d9e41c7856cbf15c5d650576a2466d8a0e39d33b455`  
		Last Modified: Sat, 24 Aug 2024 00:16:36 GMT  
		Size: 10.8 KB (10789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beda7c181626a676bfd272062cdbb6bd8f6a54387a7e1ee5f90114cc15f3112f`  
		Last Modified: Sat, 24 Aug 2024 00:16:37 GMT  
		Size: 1.5 MB (1535328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:e95e3f0f0e578cf685d7a37393db4feeeeef707cc0ea36bba9cd7e27e3c7ff92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb31b6e9a16cd1ae3a49dc6ff605a58b543096b74daec75c425d8d38b07c4ab3`

```dockerfile
```

-	Layers:
	-	`sha256:6ebf8297bfaf9b2ef5468cc4550cf70b32b2554645b95481eb4b9c0112095bce`  
		Last Modified: Sat, 24 Aug 2024 00:16:36 GMT  
		Size: 3.7 MB (3705298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:659f568e8cc97eecaeb8878ba13d30b260d895af429cfcabaa6506ab5795254b`  
		Last Modified: Sat, 24 Aug 2024 00:16:36 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json
