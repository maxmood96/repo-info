## `solr:9-slim`

```console
$ docker pull solr@sha256:c570af7edf806a6c765c87dbc8058b09285580d3c6afa81f89130b3974dff230
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
$ docker pull solr@sha256:efd34f9e077612511f9d412435732caf639e5a081e31872f671f715ed4d2a54f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159248760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305028581781e7418a1fb799add432a97f539667c86b4a147bb72ccf4f651bea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 21 Jan 2025 19:07:29 GMT
ARG RELEASE
# Tue, 21 Jan 2025 19:07:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Jan 2025 19:07:29 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Tue, 21 Jan 2025 19:07:29 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Jan 2025 19:07:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:07:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_VERSION=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DIST=-slim
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.version=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 Jan 2025 19:07:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
VOLUME [/var/solr]
# Tue, 21 Jan 2025 19:07:29 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 21 Jan 2025 19:07:29 GMT
WORKDIR /opt/solr
# Tue, 21 Jan 2025 19:07:29 GMT
USER 8983
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce09a4bbc7f04167438eedf58d01d25ea16e93e102a7bb626de9977b766255`  
		Last Modified: Tue, 04 Feb 2025 05:26:12 GMT  
		Size: 65.0 MB (64989432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4897826cdc96b36a7ad356864285e7ae6503ff542a7fe25b17e1af217553410`  
		Last Modified: Tue, 04 Feb 2025 05:26:12 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae888a7bd1b98ff25c066df0d5384816b7e35788e5922960346452e44b588d11`  
		Last Modified: Tue, 04 Feb 2025 05:26:11 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a8d4c746b3cb23f30e138cb0bb8481bbffe09008f27211f869ad48687578f2`  
		Last Modified: Tue, 04 Feb 2025 05:26:12 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05163ba22259c4886b9407804f12a3f407fb90abfb3358b2d2c88a98bb900540`  
		Last Modified: Tue, 04 Feb 2025 05:26:12 GMT  
		Size: 1.6 MB (1617805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:e016555a4bfeda11b569ded518b040ca37a5a6475d349ecbabe83390e9bc0d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa4751f733283bef38a5e155665a81d7da78e350e688c60071f4e1292e54c85`

```dockerfile
```

-	Layers:
	-	`sha256:f82907ab2b2cc68a514ee985f0e1939d5f43d9f6ac3ba48e5482dc477e37ab9d`  
		Last Modified: Tue, 04 Feb 2025 05:26:12 GMT  
		Size: 3.8 MB (3797198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:231999daa25f2fc23f03452ff0b3cd65dd24ccd9ea994f28cf15e21c0f253fdf`  
		Last Modified: Tue, 04 Feb 2025 05:26:12 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:3e10022fd14c69874326ce914e80caf929ffe17bc7641ae3dca96d7bb62bc704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156365384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae1bf8b40de0d5be08336d7a3210bd8c5099817add3796d87889c4bb148d101`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Jan 2025 19:07:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:07:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_VERSION=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DIST=-slim
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.version=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 Jan 2025 19:07:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
VOLUME [/var/solr]
# Tue, 21 Jan 2025 19:07:29 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 21 Jan 2025 19:07:29 GMT
WORKDIR /opt/solr
# Tue, 21 Jan 2025 19:07:29 GMT
USER 8983
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9247ea11654ceac03d03b0cc555e72beb2bb64ccdacb11a7f8274e013422f679`  
		Last Modified: Fri, 31 Jan 2025 03:41:21 GMT  
		Size: 65.0 MB (64989263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f55dcf6a62877d8e8bc9875fc4f862176cf72b19aaa785803611c21dae582b0`  
		Last Modified: Fri, 31 Jan 2025 03:41:19 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fc8eee516b2851a13fb04a580c242da9c9f5648aa03d02441b52e4d208f92a`  
		Last Modified: Fri, 31 Jan 2025 03:41:19 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922c2ad0aee9cb5f5aee02c0ecffaaf54ab07fb66d5c117fa9fb158a5fa70710`  
		Last Modified: Fri, 31 Jan 2025 03:41:19 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddffb787c8ef5ce30fee6c75cc0223fa4cfbd4fb2955de1eb8bbf6c12fa028bf`  
		Last Modified: Fri, 31 Jan 2025 03:41:21 GMT  
		Size: 1.5 MB (1474456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:7a85acfee5b303d2850a981aeee697c95278ff765392517b6b161078b8f5981e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60772ce694bb1bd56f123b65b83e194bfc79e09f9baf2287ba12c91479987f8d`

```dockerfile
```

-	Layers:
	-	`sha256:a219b680cd66266ec2c74e1682dfe8896769d7bcc3f1d6ddfdf6e74d4dce3c92`  
		Last Modified: Fri, 31 Jan 2025 03:41:20 GMT  
		Size: 3.8 MB (3798750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90fabdadbb1e7c924ccc79264169eee1521cb15cfbadbca1a226c4b715f77fe`  
		Last Modified: Fri, 31 Jan 2025 03:41:19 GMT  
		Size: 34.6 KB (34562 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:fb767a819218f442f2c1fd85d7c9b2ca1dbad70ba9cfa60bcc232f6e026837be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165498167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448656c80e77d1dd85cbe72e6fb11584fc2b8211064a2152005d566af383dda4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 21 Jan 2025 19:07:29 GMT
ARG RELEASE
# Tue, 21 Jan 2025 19:07:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Jan 2025 19:07:29 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Tue, 21 Jan 2025 19:07:29 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Jan 2025 19:07:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:07:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_VERSION=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DIST=-slim
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.version=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 Jan 2025 19:07:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
VOLUME [/var/solr]
# Tue, 21 Jan 2025 19:07:29 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 21 Jan 2025 19:07:29 GMT
WORKDIR /opt/solr
# Tue, 21 Jan 2025 19:07:29 GMT
USER 8983
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71de2d980599cbec4dab5c3bd7274078312e68d7cc81171b5d8bda1a98eb2403`  
		Last Modified: Tue, 04 Feb 2025 07:32:10 GMT  
		Size: 17.6 MB (17642335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30b6dc9603fa30cfaeaf94b4f0afc490673bc37614634f344ef2172f29afa74`  
		Last Modified: Tue, 04 Feb 2025 07:44:12 GMT  
		Size: 46.8 MB (46769698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c04307e9c18ff1b510c546e4467455954ff8ab916e0e48044941ce74965ac83`  
		Last Modified: Tue, 04 Feb 2025 07:44:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640f96035063c914d8c6861a46f9131b45dc5967d86d34cb927cfa5c131d7750`  
		Last Modified: Tue, 04 Feb 2025 07:44:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df64cc1fe0b2b84788aab7921563d47083cf630f0e769c607455cbae2ef32c25`  
		Last Modified: Tue, 04 Feb 2025 19:30:38 GMT  
		Size: 65.0 MB (64989773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44e2bff1268d702ece57d3b23faebe9215539761f80015d0a042496a3e0e2c9`  
		Last Modified: Tue, 04 Feb 2025 19:30:36 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a3392c59094d80e433b45f48b36f63b3d45c006c8ebbbc0344b22871def323`  
		Last Modified: Tue, 04 Feb 2025 19:30:36 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ceb6c68e4fd3339c6f58cf08431bf21ba4e3366dcf2d34226fa39874627ffe3`  
		Last Modified: Tue, 04 Feb 2025 19:30:36 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826e66e6fd3f5a4607689f8289cf310a902e712377ac477bc82ee3c9ec6f4636`  
		Last Modified: Tue, 04 Feb 2025 19:30:37 GMT  
		Size: 1.6 MB (1630659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:af77427d47788f578cf39478c6e8cb5be884421a2470c420598b5ffa3dbc851d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117d060b338cc76f4f7567973d660d8b0b955bc6bd9258b7e2c538368d043290`

```dockerfile
```

-	Layers:
	-	`sha256:d149dca9111e9a2d5b120526853771f81e1d2abfd2ab3131872d46ec31708b9f`  
		Last Modified: Tue, 04 Feb 2025 19:30:36 GMT  
		Size: 3.8 MB (3801107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e073f908ce5d41c0081d2d84866d0a4fd1964b3ba70e348c96c75645ad30559`  
		Last Modified: Tue, 04 Feb 2025 19:30:36 GMT  
		Size: 34.5 KB (34450 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:16c9892cb872f063a0b59fe94cf700c581c7324a5feb08a49259bebf10aac30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154659487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414aed004b50f21b19488f92f77101eb2b2fd67898167904f8373cafc759ed51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Jan 2025 19:07:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:07:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_VERSION=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DIST=-slim
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.version=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 Jan 2025 19:07:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST=-slim SOLR_SHA512=ba30ce2933fee3a7e13fb71d24c78860e45d11b36197eac95c7b8aa1faa1cfbf4d1bbf32e6d43c9a660f92e33c1e063db9b12fa5bbd3b023e01bb3f1d793f299 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
VOLUME [/var/solr]
# Tue, 21 Jan 2025 19:07:29 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 21 Jan 2025 19:07:29 GMT
WORKDIR /opt/solr
# Tue, 21 Jan 2025 19:07:29 GMT
USER 8983
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce8df2d77e2997c97b30184cdfa23846196d4e5dfd005da96d8f36dcbc641a`  
		Last Modified: Wed, 22 Jan 2025 21:43:35 GMT  
		Size: 16.1 MB (16142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269211f1ea045e884f1175d77556df415d3093969647d5f33b870d33c557999`  
		Last Modified: Fri, 31 Jan 2025 01:43:28 GMT  
		Size: 43.9 MB (43949613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469f3a85ca4aad23caca93275437a25893f78888c8e35dcf3b777dfeec31c5e`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b248eed509cdcce48e80c1834adc9f5fb2a6d150447ac1b88ef4c81f5801ce`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d946980e62ecd005aa80e041dfc96b23be6b25a979f6e847300d87e033e20e`  
		Last Modified: Fri, 31 Jan 2025 02:35:27 GMT  
		Size: 65.0 MB (64989471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f311bdbab5ce06fc0483b0ac11de32231b58009a24957892925ad535963648`  
		Last Modified: Fri, 31 Jan 2025 02:35:26 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f97093a0c49f8984f2bf95367169bb6f11fc45f6965762345d30fab694af6fb`  
		Last Modified: Fri, 31 Jan 2025 02:35:26 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27de959374ddc5a05c0671cbf91d200a652bc08160152d9c54fa7203e9abd77`  
		Last Modified: Fri, 31 Jan 2025 02:35:26 GMT  
		Size: 10.8 KB (10808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5000c643040bcc46b1ca3008d10b50ba62adddc3e8037e5808829c1bce1f92c`  
		Last Modified: Fri, 31 Jan 2025 02:35:27 GMT  
		Size: 1.6 MB (1559000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:8eabb6722852a6b6a4ce5da7806e132bdbba7a3e755e8b5d4c2d36529cd28b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37817c620c800ec3139d411f3ee133c734068ccdeaa8990aa6af364c72f3b53`

```dockerfile
```

-	Layers:
	-	`sha256:ae336bf36dc9f7b4405b7460693836178fdc25ee625210a06bb1ca6140b8c7bf`  
		Last Modified: Fri, 31 Jan 2025 02:35:26 GMT  
		Size: 3.8 MB (3800670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b22adb1083708001aeecae12d040933c94a2ec2868fbd10cea763983cb59eb9`  
		Last Modified: Fri, 31 Jan 2025 02:35:25 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json
