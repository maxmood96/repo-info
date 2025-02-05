## `solr:latest`

```console
$ docker pull solr@sha256:26fd07b70eeec2c2235e2ea9b37ac63413b1fedc878a0e402fb722dc21c42af7
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

### `solr:latest` - linux; amd64

```console
$ docker pull solr@sha256:68874c14eba4b479f471fa80e1a25e6f16adc38082b58be2d2bef96ca6055009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.6 MB (480629795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961291dfa24333e3f1bd706c98b381aacd193fa7d8b4b1d8a3a25ac2de076a9b`
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
ARG SOLR_DIST=
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:f8fb06178f890220b10d51f0e296af68ca1d001b000d57c73b0b039ece40dc8f`  
		Last Modified: Tue, 04 Feb 2025 05:27:11 GMT  
		Size: 386.4 MB (386370359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a56f318d5e375f73e7421b38e590f028b60c683aa3756f62b4b46859c50e43`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b02a3ffc681de025570fbae99d20ba78684baf60bf76d5f927cc43ea264480`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b84691b20130259c87f0659342514cd2a8efc3d45e2e4cda3464582abe68bb`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 10.9 KB (10886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47eee3f773e6763635ccbc41a718da3eff9b7a1d8a3c6601b7cf91156a6ddb7`  
		Last Modified: Tue, 04 Feb 2025 05:27:05 GMT  
		Size: 1.6 MB (1617836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:94dfe77656189257d97461b3fc6ad89f3a177311b8f237625783dd2f803d5a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1144afa045fc7c5c4f00da574ffa31e3e230d707bfa6fa1525aa330e0bd618`

```dockerfile
```

-	Layers:
	-	`sha256:4604d1be9d56fe56ffa90d7ff77956f17b1a5fead2b56c782fb9e8fe2a51db14`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 4.3 MB (4346759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124448f3b90099baa9d40287b7d9fc14e9e4998199c80b94ed4901475d25d370`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:13f0424d319c137b50454e992b5025c4537de8fb9241a1d9acd3e4baf6d9c7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.7 MB (477737287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17568e9d2c91e538a78d7520ceffc408959a5a6b4f74ba8825896d9b1a8da66c`
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
ARG SOLR_DIST=
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:c05da0f21a3b473aa088b36e7308a38faeac98ab3894582ae1a69a095f137950`  
		Last Modified: Tue, 04 Feb 2025 22:07:59 GMT  
		Size: 386.4 MB (386370384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a3e221db5512a3faebc6f6eabc461e550b7af98f32d8961773b9ca8d7b6f4a`  
		Last Modified: Tue, 04 Feb 2025 22:07:51 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cd0d31f42ecc2873cfb10c94c38658248ee11a47b65393add7dc43ae1960b6`  
		Last Modified: Tue, 04 Feb 2025 22:07:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaeef40fc076faf275552b85686baf01c13c70d5bc420c0ee4ab420a468ba86`  
		Last Modified: Tue, 04 Feb 2025 22:07:51 GMT  
		Size: 10.9 KB (10888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a731d1f543a4d828ab92f5c3edb16eac640add29eaf175d768042f61e5c6e5`  
		Last Modified: Tue, 04 Feb 2025 22:07:52 GMT  
		Size: 1.5 MB (1474634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:54726dcb33f629a16c448d8d36bab21bc905a703f982ea87f4b84aadff74d282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f9fcdd79397bc36325625f4b1d52b69771cbf2d6d932ea08b650b44b263479`

```dockerfile
```

-	Layers:
	-	`sha256:eeda9f6287c7f8fdddf71200ef6dfa4b55f3142951af87a495d225a49d9c9d24`  
		Last Modified: Tue, 04 Feb 2025 22:07:51 GMT  
		Size: 4.3 MB (4346435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd296a17429e3736d0b8962cfcf0794f922e20a89cbac6c9ea2f5dc98c97fd3b`  
		Last Modified: Tue, 04 Feb 2025 22:07:51 GMT  
		Size: 34.5 KB (34498 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:b0e1a294b181797e020c3c69ab4f37b8228486350a921c57ccc846d271e6aca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.9 MB (486879057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c054b7a1e937d7aa2cf7d01366dd48e8dacf13d209131d1d5e5cac803ff7c7`
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
ARG SOLR_DIST=
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:23fbe5120dbaa32bb499d1759f7fa06b0a2e8848e99e464d6d2a8d169a7ac1b6`  
		Last Modified: Tue, 04 Feb 2025 19:29:09 GMT  
		Size: 386.4 MB (386370635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6273b893e9000388a8c5ece0618ba3666e29ae9d70209e336508b7f8a095d6`  
		Last Modified: Tue, 04 Feb 2025 19:28:41 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5c49567ed9f030ac967ba1d68177b9baeece74ef16d1a7a4a52c8ab41a80d1`  
		Last Modified: Tue, 04 Feb 2025 19:28:41 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7e32f2a9d8a4a5b7a92e9045d9d13b7986ccf5ef7dc40f118918633853d856`  
		Last Modified: Tue, 04 Feb 2025 19:28:41 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed3fbbf4acba826c1c82eea7190976c44baf7acdd0899c37d554d13398cbf4b`  
		Last Modified: Tue, 04 Feb 2025 19:28:43 GMT  
		Size: 1.6 MB (1630609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:7e868294081ed46c7b07b36266e2074dd221de19428eef12207c41cff1504b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4385053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e76a219d6c52ab0e8ed9df4d57f94c5dc20a8d62c6d4aeb04da0293797e3e7`

```dockerfile
```

-	Layers:
	-	`sha256:6a4748e91c3840ddf6ed08ef47b80df81686ce3f01a2252fe13fed30dd860d14`  
		Last Modified: Tue, 04 Feb 2025 19:28:42 GMT  
		Size: 4.4 MB (4350668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3486462c495dbf841468882b5bbab04dcaf11e3005120f0559de3164dc77e715`  
		Last Modified: Tue, 04 Feb 2025 19:28:41 GMT  
		Size: 34.4 KB (34385 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:627cedf1152dc499e4afe0e867d7f2548a0431a22019f3af121badb041f51e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.0 MB (476040389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edf04d9063d80e2c879dd1be3315d840726dbd40f489c1cd8629d1e42bc4118`
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
ARG SOLR_DIST=
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:72f784746e8bc6a2425a48dc40ef75444cea26dc2dc70e0461a1cdca7231ccd4`  
		Last Modified: Fri, 31 Jan 2025 02:34:19 GMT  
		Size: 386.4 MB (386370292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacc1a50febcd6469e606a1f8bb4e279c0afee229bc15dd6515bd855a909d4dd`  
		Last Modified: Fri, 31 Jan 2025 02:34:11 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfb953b1a52946961b952f20e33eea00c9fe85d68d7f60bf7dbadc78002ca88`  
		Last Modified: Fri, 31 Jan 2025 02:34:11 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51107e4ea761bdd1c3db3cf234c5056fe0f18a072b9193152f5107a343ff0622`  
		Last Modified: Fri, 31 Jan 2025 02:34:11 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3187896c44e9cbce32b6ae0afab6efe0e8b3836d24231f055bf0eb1dfa3ef83c`  
		Last Modified: Fri, 31 Jan 2025 02:34:12 GMT  
		Size: 1.6 MB (1559005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:ef2d790b677bdc364a5cf92acf2ae517c65fad6b76fef1731c9149bf9516ea40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4384566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8372c9dad754b46b04d580ca4df1bb3d5539c9fc891e3ca6cbb740b0c029599`

```dockerfile
```

-	Layers:
	-	`sha256:4caf63467a49888119bbf0ccf03ee8ed92c81cabc77e67132ddf7d0e512b303c`  
		Last Modified: Fri, 31 Jan 2025 02:34:10 GMT  
		Size: 4.4 MB (4350231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846888a6cad739db9286f8b5105c572f85aad4f4124469c918bc9faf45089ff8`  
		Last Modified: Fri, 31 Jan 2025 02:34:10 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json
