## `solr:9-slim`

```console
$ docker pull solr@sha256:6cf08770d89a5abca860ef7323ba6709bdcf448c10dce6e09c5e07e3b9ae81d2
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
$ docker pull solr@sha256:eecc6d39f5e2b6fe48711dab642db755718fa514f7c97683bf55c97dabcbde6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156914020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf654c50c8c0bacce00e608b6b7ddcec55627751c4f9369f905d6c975a472c6`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d807bcbe5808a8e8a324767f3c89c0e07d2dcf4297e24860ae4389ef654ed39`  
		Last Modified: Sat, 17 Aug 2024 02:05:39 GMT  
		Size: 64.7 MB (64716301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3516aa790edc115f5ba1702fcb8dc5a14c539a04d45c852c4473aa9c584b86c`  
		Last Modified: Sat, 17 Aug 2024 02:05:38 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858b9b0b271701c9fff77113376a9786f3aaec4a6f18b1542c55c7c2b7c2781a`  
		Last Modified: Sat, 17 Aug 2024 02:05:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af0f7fe0a4b9a306dc31066b86bfbd37346d650073ab7f981ea1e23776002d1`  
		Last Modified: Sat, 17 Aug 2024 02:05:38 GMT  
		Size: 10.8 KB (10780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5c8e07ed84cd783f6c90b909d9d62dfcabadd23c9c3b111d1cadd67a39f750`  
		Last Modified: Sat, 17 Aug 2024 02:05:39 GMT  
		Size: 1.6 MB (1588591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:9babdacf5900c31aa286a4ffd321711b0245195c260e71c7a9e2b24fc57dec7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22eb02585a3abb5101e3ec9bd21e46ad9049ce753cb3f67511667aaaa8da3e75`

```dockerfile
```

-	Layers:
	-	`sha256:24a96192e2d44994eb619f19da56d94f7ac55dd3db6b89c4a9c27a80d6da45c6`  
		Last Modified: Sat, 17 Aug 2024 02:05:38 GMT  
		Size: 3.7 MB (3704177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01ebc80680154be71ba10f7df39fca7d72144e30825ae6229f7c07d51d39bc7`  
		Last Modified: Sat, 17 Aug 2024 02:05:38 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:e2dc2064ac0c72a71cee99dd97212497674b559a5cdbae445865d7c5fe017c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154141786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daacc8ef125fc5ed20b87743a5008c7a3410be713621c1c59232ddf4d61b548b`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90878f7e89a6f2b87e312129cf3eff6784a22f286192ee2d2432b08d63e8ebb`  
		Last Modified: Tue, 23 Jul 2024 04:14:05 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761145506627687a263e6f14af3f9464c59c42e90d0ec4f13d07782c0a35d4f`  
		Last Modified: Tue, 23 Jul 2024 04:14:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74a5dab598e20dbd54b67ab0f46199482917445fb519d7ef5bdd661607c7f5`  
		Last Modified: Thu, 25 Jul 2024 17:46:20 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d228ddd8820c338a91d2a8cfc17344639dba3de8f19888fd3b19734eb2226345`  
		Last Modified: Thu, 25 Jul 2024 22:35:12 GMT  
		Size: 64.7 MB (64716521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f06e878f87ba69a02c3fd5728eb6a3d416d3becc93f37806eac4835ad145e1`  
		Last Modified: Thu, 25 Jul 2024 22:35:09 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d655d5ac948b41ab8e88c2ed6291461e2975f8f39192e4a61f72461e221525`  
		Last Modified: Thu, 25 Jul 2024 22:35:09 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45c9430c3027255a9f8866c3fc89d2200e0d959894a686d9acef779a64b39d9`  
		Last Modified: Thu, 25 Jul 2024 22:35:09 GMT  
		Size: 10.8 KB (10786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e842a173365e74890b322b37b18a4cc428ed80f3d3671da486051851a9f4cce5`  
		Last Modified: Thu, 25 Jul 2024 22:35:11 GMT  
		Size: 1.4 MB (1447443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:b1e19258c1cd8b6398febf06dbc4e611374efb42eb167a3948bc3cfa69ffe45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5653e57191ab005511c0ae03045599848fb51e314e505281f7f18a0d26f39b7a`

```dockerfile
```

-	Layers:
	-	`sha256:c01bec7c8c57507274bc3287a5be28b7cf0e4cfec543883f8b0892fe8dd5b4fe`  
		Last Modified: Thu, 25 Jul 2024 22:35:10 GMT  
		Size: 3.7 MB (3704466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153bf0d4dcc75443f937ca7d02a60fdc79bede1e0154fe12d4a555f90d9c57f6`  
		Last Modified: Thu, 25 Jul 2024 22:35:09 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:8552a9225d9b0c2f46e1bf3404f0763227be016938f602c23cd0cc600e3c96f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162748388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d38a8bef9cc65edc4df312c7264312e6977f621e820adbfbaf8648213611a6`
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:03d88e63af0e9c74b520244f1440e8b5e318223ed76ca89660474f005d8a79e9`  
		Last Modified: Sat, 17 Aug 2024 01:02:51 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8520a8175add6fda2f5f9015db077c2f535e32199654b378ed7de938f73bffbe`  
		Last Modified: Sat, 17 Aug 2024 05:34:30 GMT  
		Size: 64.7 MB (64716821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d944e9c6b28be5e9f18e4763dcd22fd8598e3761b889485f1040771cb49dbcdb`  
		Last Modified: Sat, 17 Aug 2024 05:34:27 GMT  
		Size: 4.3 KB (4275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb0f22dad701c1e92da42ad0415cf5d1b81987f29dd5be33f7498c358741b94`  
		Last Modified: Sat, 17 Aug 2024 05:34:27 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdb6e45c2fa8f4d205445b2be216963377b6e10fc704cdd42b4033996dec3c1`  
		Last Modified: Sat, 17 Aug 2024 05:34:27 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781d2574ed76196c46fc7aa77ad7fdefd109941a6e545b56ccf968ec6af1dd46`  
		Last Modified: Sat, 17 Aug 2024 05:34:29 GMT  
		Size: 1.6 MB (1595493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1252eae7a169ca0dc932b34cd6f43ac3b5cda9d38c944bbcb3b3b01c6340877c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c462a5aa74623fa6a1a96c82205587ecb60c3eefd366cfafa789df531b7ab6`

```dockerfile
```

-	Layers:
	-	`sha256:d41427b5403c5d6cc0cc23feb18cd6386617fb05c8d34dfbf4fa7199a94f1938`  
		Last Modified: Sat, 17 Aug 2024 05:34:28 GMT  
		Size: 3.7 MB (3708703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de59371c367091db87eb515c26f85b8815bba38c5c0b44036c016296d1ca6962`  
		Last Modified: Sat, 17 Aug 2024 05:34:27 GMT  
		Size: 34.2 KB (34156 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:8a9b4aaf5779fafeaf8e6dc2440729e7486262732fe34b6a72f02c64ddc1bb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151726926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382c0f9fa04cebcead30c118487d71b2a3221bb524977eebcbdfd734532d366a`
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd83ebef6aecf3000f28c0a8db89615d00e18d88c19f65d06ef72c8a32075409`  
		Last Modified: Sat, 17 Aug 2024 05:06:12 GMT  
		Size: 64.7 MB (64716501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfbbb23547bdb46e546fd0b66cfae0a422bbc2e10ee290f052e7b00bd5899bd`  
		Last Modified: Sat, 17 Aug 2024 05:06:11 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb02b8cc61cc4bca5a8233759e9fe6eb09826c13f39994fce43e3b2c271a0b6`  
		Last Modified: Sat, 17 Aug 2024 05:06:11 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e48f84ab1afa86bb300543ab51eb54c6db557984ab2a9fd942280b666ba84ba`  
		Last Modified: Sat, 17 Aug 2024 05:06:11 GMT  
		Size: 10.8 KB (10786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f44f7e331df1e2dfee23cda3983b0dfdbb03adc0f0f56873e95f8625496b18`  
		Last Modified: Sat, 17 Aug 2024 05:06:12 GMT  
		Size: 1.5 MB (1535241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:e89853a63333076900be6d1b5e8454cfca87af1ef16484c4d4f280fbb0f6d48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf17e8882b43667c083c3a5cdf4bb6adc67ead43e0647442479854edeef6079`

```dockerfile
```

-	Layers:
	-	`sha256:b2ccc9ef4ff80bc61c8d2fd8fed3b3286b8a41121ef449df3f672a837c89c7fc`  
		Last Modified: Sat, 17 Aug 2024 05:06:11 GMT  
		Size: 3.7 MB (3705298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6378bd04fa9cf811956aa9e61e4a7707c6c52c85cb297dc1cd3307a12c460bb`  
		Last Modified: Sat, 17 Aug 2024 05:06:11 GMT  
		Size: 34.1 KB (34109 bytes)  
		MIME: application/vnd.in-toto+json
