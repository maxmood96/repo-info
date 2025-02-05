## `solr:slim`

```console
$ docker pull solr@sha256:fd236ed14ace4718c99d007d7c0360307ecba380ac4927abdf91fbf105804f28
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

### `solr:slim` - linux; amd64

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

### `solr:slim` - unknown; unknown

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

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:444de29b44629b86e3b1d78043bac74da9c21a2f4c04b2a24022d369641b1696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156356308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4061bb8386907f6e4d2b9d0fbbdae9cb5d8bb4f687bb598a9a18cfefae20ab89`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a786ca393e9870b4f4cde075bbc383186091c0991daac29a65ca2c4a536246`  
		Last Modified: Tue, 04 Feb 2025 22:10:49 GMT  
		Size: 65.0 MB (64989494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265712ce6a5e23a10e63423ee38661610acf72b5648bfe70932e53c6fdd068ca`  
		Last Modified: Tue, 04 Feb 2025 22:10:47 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2371b1a7b8fad29450c641065cc5541dcba951d9cde0fa915eca357b57be1a7`  
		Last Modified: Tue, 04 Feb 2025 22:10:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0013cd967a5c9f6674543864d3f03a19f4b431d354f1c88cd39264a37e3cbcc`  
		Last Modified: Tue, 04 Feb 2025 22:10:47 GMT  
		Size: 10.8 KB (10800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b727d97cd83e253f07918e7975b24d5fbe0cd7564dc68d076855aff5c8816363`  
		Last Modified: Tue, 04 Feb 2025 22:10:49 GMT  
		Size: 1.5 MB (1474627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:74b4a020544c1eb93421daa0b2aeab200bc22ae139ef7eb89c7b180fe0f86422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991e3efc9bee0daf5d65889633129e259a7ed25d40cff467407b20cf85279ff8`

```dockerfile
```

-	Layers:
	-	`sha256:f2a336dc65726b4deda9177ee1b65f0184ff81df229e88e9978275375db6aeda`  
		Last Modified: Tue, 04 Feb 2025 22:10:48 GMT  
		Size: 3.8 MB (3796874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33fe31537f6929427de5cabbd60721bcf1cc5fdcecba02b468ff18bfbf4d97d0`  
		Last Modified: Tue, 04 Feb 2025 22:10:47 GMT  
		Size: 34.6 KB (34562 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

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

### `solr:slim` - unknown; unknown

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

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:fee91e6ca9b464b39ef51a5c801fe4d7313e9bae230ca3c74fb269e8f767e86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154649069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f167a7640db5e7c48dfd947e170100319fc4893a21eef04aaa90fc10293bbfb`
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
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
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
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c64c26afd0885ce3d2d456d35ff90e813c65ee4e2f59dd40604fa8b3e90414`  
		Last Modified: Tue, 04 Feb 2025 07:39:56 GMT  
		Size: 16.1 MB (16132604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853fc1b43db0179366c6c94346c45e817496299f9c2c952d16d743490530bc87`  
		Last Modified: Tue, 04 Feb 2025 21:11:39 GMT  
		Size: 43.9 MB (43949615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbbceb71f629d897b434579a4d4706d08c24a3585a1a912cca27bacc0e37206`  
		Last Modified: Tue, 04 Feb 2025 21:11:38 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6abbee1e90bc496a9f8c880c0cac746b97d79005c6424661138b5d09582440`  
		Last Modified: Tue, 04 Feb 2025 21:11:38 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b792540e1f32674678379596f37753d80b1ef46593707888e6a5403373e3b8f6`  
		Last Modified: Wed, 05 Feb 2025 08:56:00 GMT  
		Size: 65.0 MB (64989322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b5063cffe62d23cedc039fe7cc6dc75f04c819127200ed432a55a9ccf9e51`  
		Last Modified: Wed, 05 Feb 2025 08:55:58 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042681844c01828cce2f92ceae7549b38e751e1cd6c0237afe16c48974c0a916`  
		Last Modified: Wed, 05 Feb 2025 08:55:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c06c133eaa58243de55bd2fdd791f29b573b52fa4e733fa9174abd0a30a6d5`  
		Last Modified: Wed, 05 Feb 2025 08:55:58 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae776fb81ccfcceec01ef2db383867f5ac9366e0bfd52fda0d35e3e14f2a2d3c`  
		Last Modified: Wed, 05 Feb 2025 08:55:59 GMT  
		Size: 1.6 MB (1558805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:936c6eedb3c65ae472ace99ba49fe1a6dd234d1a189806fbf5467daf25f5c7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e379c124eebc0042701e6c3d9ddee16a2cc2834d20a0afc1359ea34ec957f8c8`

```dockerfile
```

-	Layers:
	-	`sha256:54dfcc6b1fdf3aef2ad974d655c19e7dec62334aa93959b8ff4ce72a9bff9962`  
		Last Modified: Wed, 05 Feb 2025 08:55:58 GMT  
		Size: 3.8 MB (3798794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23671c6aa4c7d418e5b80fa159000090c651d920d7ad08ab71d1214125d5fd6f`  
		Last Modified: Wed, 05 Feb 2025 08:55:58 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json
