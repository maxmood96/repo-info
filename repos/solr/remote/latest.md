## `solr:latest`

```console
$ docker pull solr@sha256:05332e172bd3335eb36f2477e22cecae99f1f8e3b1bc4d1c148cb5373f1abaae
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
$ docker pull solr@sha256:49280abe390c5b3fee5e56983ff27577ca6278a29ee599ebbb28425160b70e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.6 MB (480646492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edd1739a4b1b109bd095d0d8ab17279989722a902673f4a999ad4a77318b863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 11 Mar 2025 21:10:22 GMT
ARG RELEASE
# Tue, 11 Mar 2025 21:10:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 11 Mar 2025 21:10:22 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["/bin/bash"]
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 11 Mar 2025 21:10:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 21:10:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_VERSION=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DIST=
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 Mar 2025 21:10:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
VOLUME [/var/solr]
# Tue, 11 Mar 2025 21:10:22 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 11 Mar 2025 21:10:22 GMT
WORKDIR /opt/solr
# Tue, 11 Mar 2025 21:10:22 GMT
USER 8983
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97781601768cddddc35e23ddf38633ea2e4a0a4ae0a8f59f11856fffbd8a3bad`  
		Last Modified: Wed, 23 Apr 2025 16:31:54 GMT  
		Size: 16.1 MB (16146029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa68485484727aa6d5321f078fb21840fd2a8bdd598f4f8a3e1672a95317733e`  
		Last Modified: Wed, 23 Apr 2025 16:31:56 GMT  
		Size: 47.0 MB (46958421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e85f04a42eb69d25f9b02e9a1c46559467f5274b45bb338cd0809534deef05e`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0137fea4bef4dc4ff919d973a8ae36f29edacba15f7b5129ebe177983d665fe0`  
		Last Modified: Wed, 23 Apr 2025 16:31:53 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa7b313ad9d309100ff5fef2216a7c7ac73cb1d21d583b97788bd667fa5ec97`  
		Last Modified: Wed, 23 Apr 2025 17:13:54 GMT  
		Size: 386.4 MB (386373890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9af466ec734d0cabe76a773fe8d5561f4d37f4d2f079a89bcdf0464f8efaf7`  
		Last Modified: Wed, 23 Apr 2025 17:13:44 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0553957a43d0a1cfdb8cc5812b96dd7cf5a1131dead32ccfd15f3f0d1edb39`  
		Last Modified: Wed, 23 Apr 2025 17:13:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5028478f6b05df65011ea6f0cfb5c3fe9eaab065eb28385bd6045550368d719e`  
		Last Modified: Wed, 23 Apr 2025 17:13:44 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f1a2f976f8752e8852c7d289f9266afa5591c7296a3875487d3912f431f9bc`  
		Last Modified: Wed, 23 Apr 2025 17:13:46 GMT  
		Size: 1.6 MB (1617944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:c6a50eff3d8e88e01e5cfd2c5f0160adbb7e7d41a56e0fa2a2518da2a574e238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1877f32851f79a9292ac45fe5dedcc77e1487cd269b0b92c5318a0c1c606f965`

```dockerfile
```

-	Layers:
	-	`sha256:ff89a626122de0ae5eb19042b04d0a44654140ab0cd6a43c435a02117a9abd35`  
		Last Modified: Wed, 23 Apr 2025 17:13:45 GMT  
		Size: 4.3 MB (4348549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b412f3edd28596f76d1fb53e07a2a701f56aa7636cc59d695f699db34f8e458`  
		Last Modified: Wed, 23 Apr 2025 17:13:44 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:a9735fb0f55472fa9ee6ac26e07689100ef7d8750286cf9148410764104e2cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.8 MB (477754619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326e639cc4eeaf0552ed71a0d619286d410127893425e373fa56899b97d221c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 11 Mar 2025 21:10:22 GMT
ARG RELEASE
# Tue, 11 Mar 2025 21:10:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 11 Mar 2025 21:10:22 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["/bin/bash"]
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 11 Mar 2025 21:10:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 21:10:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_VERSION=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DIST=
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 Mar 2025 21:10:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
VOLUME [/var/solr]
# Tue, 11 Mar 2025 21:10:22 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 11 Mar 2025 21:10:22 GMT
WORKDIR /opt/solr
# Tue, 11 Mar 2025 21:10:22 GMT
USER 8983
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d988c284109adb0ee08f6d6a95a152f6e364456e1a4853bb6c3ebc58c40f099`  
		Last Modified: Wed, 09 Apr 2025 06:58:01 GMT  
		Size: 16.1 MB (16059566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac488a8321ea959588c227573cf8a20259cc8fde212361febce0a1b0c814dbef`  
		Last Modified: Wed, 23 Apr 2025 16:38:17 GMT  
		Size: 46.5 MB (46474324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1af5cf872e078be1505c0565767eed13113730ec78326847e626469b0b8c663`  
		Last Modified: Wed, 23 Apr 2025 16:38:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88f83d0cfd9bd69d840192dccb1b340da7121b21b5d2c5d41ad894714765f2`  
		Last Modified: Wed, 23 Apr 2025 16:38:15 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29e0ed22c8fe825a12b78a6eab8a57088d0deee6c1856d0f7dd4cd35dbf3d52`  
		Last Modified: Wed, 23 Apr 2025 18:16:11 GMT  
		Size: 386.4 MB (386373874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750bae8a266e9f69ee9a9d931ee1491d7ce4ba2548c92ee81439c0969efc37da`  
		Last Modified: Wed, 23 Apr 2025 18:15:45 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b3c56cee29493e739720f60e1b70d8ccd151b0b4f8c3a550f93f916920a32b`  
		Last Modified: Wed, 23 Apr 2025 18:15:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf7c2835846a907c12606f0e6e39224f6894e7a09adb85ffc112b170f99a071`  
		Last Modified: Wed, 23 Apr 2025 18:15:45 GMT  
		Size: 10.9 KB (10889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118648237fb4767e8c96eaeb3f21b63b7487bdfbf912e5e6e74ea08ac42b34a5`  
		Last Modified: Wed, 23 Apr 2025 18:15:47 GMT  
		Size: 1.5 MB (1474744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:e60d59fdf47d23ff70c612949ab5156bfffed728503ea0e98ea6368da7c5b265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0ce0fe3dce0202b376866d2a59915d6bd559b3653d98811359d83aa99b8017`

```dockerfile
```

-	Layers:
	-	`sha256:e9b495f9115631f71641ab4f4a0b663f3d9a674342c4c8e990155a3c0ae24d99`  
		Last Modified: Wed, 23 Apr 2025 18:15:46 GMT  
		Size: 4.3 MB (4348225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d41263a20cdc041ed2b3476edd2da0a614bbf2576e43c98afc5c76901507e96`  
		Last Modified: Wed, 23 Apr 2025 18:15:50 GMT  
		Size: 34.5 KB (34499 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:348d1c884887856c3170991aadd3110a0964dadfaa2a6ccffd003c308f8f90b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.9 MB (486853204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cf22480516741bbe491e49e1ac453f45afeea7b493c479f231456d3707fc75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 11 Mar 2025 21:10:22 GMT
ARG RELEASE
# Tue, 11 Mar 2025 21:10:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 11 Mar 2025 21:10:22 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["/bin/bash"]
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 11 Mar 2025 21:10:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 21:10:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_VERSION=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DIST=
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 Mar 2025 21:10:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
VOLUME [/var/solr]
# Tue, 11 Mar 2025 21:10:22 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 11 Mar 2025 21:10:22 GMT
WORKDIR /opt/solr
# Tue, 11 Mar 2025 21:10:22 GMT
USER 8983
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c38ec2b4ee36ca93f19596eb065a396e648e65a58e52db4e0886be5ded596`  
		Last Modified: Wed, 09 Apr 2025 04:35:13 GMT  
		Size: 17.6 MB (17617815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3400d5f2e38520c6487762c909ae0af92dd3ef636453c243c27e5b531e5aef`  
		Last Modified: Wed, 23 Apr 2025 16:46:41 GMT  
		Size: 46.8 MB (46769848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69913fe4465cbe95c02bbc2b0d2b5e177748b9b473e31e65f9b26da73727e4e`  
		Last Modified: Wed, 23 Apr 2025 16:46:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d3c21455a5d9e113244f43286c051f57e04caff2e5fc4b16462b0d8e7b4783`  
		Last Modified: Wed, 23 Apr 2025 16:46:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b854e9452f4a9c414ec172e925a2027a29299612f3077de3492baa36520b35`  
		Last Modified: Wed, 23 Apr 2025 17:45:39 GMT  
		Size: 386.4 MB (386374107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adb7f1fc61dc00cfce550bdff9df88d17186aa7cba94e1bde26b7cd7a0d09f7`  
		Last Modified: Wed, 23 Apr 2025 17:45:15 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bff39f5cba5435b847b7eaf1d290cc02d313c2e6dcb339db4db6d529590dc41`  
		Last Modified: Wed, 23 Apr 2025 17:45:15 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f27feb42164f4e8a4976ad33e7cf5ec93fa844304d97dd05484bf21d142e4`  
		Last Modified: Wed, 23 Apr 2025 17:45:15 GMT  
		Size: 10.9 KB (10897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7be292e5a7ad96224ce9e80715acd945490c3ccb9a06cdb2cf5cd92106d241`  
		Last Modified: Wed, 23 Apr 2025 17:45:17 GMT  
		Size: 1.6 MB (1630884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:f955f6af711311fd682a01bd9ef15732f36331c198840a403bf6a7168fc8fe52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4386845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bc49e0e1ac4122e57e3489d26e3b2442954f9eb79aef36ffd072710ca251f7`

```dockerfile
```

-	Layers:
	-	`sha256:625406fc84a44806e5750d58aa5dca7d8e8dffb7695117ad7fc16dcce446adcd`  
		Last Modified: Wed, 23 Apr 2025 17:45:15 GMT  
		Size: 4.4 MB (4352458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77906ebf9609d7dbc06ba0e5e893ec8710474592a21039b61f1055550e84a061`  
		Last Modified: Wed, 23 Apr 2025 17:45:15 GMT  
		Size: 34.4 KB (34387 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:050b76720501815d494d1ba59df49877dea5e962a66c6e6cdde75191937c3151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.1 MB (476054952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbf91fd595643521df5d659b78bf7874eb9a73a82955a2fffbf919eec341d27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 11 Mar 2025 21:10:22 GMT
ARG RELEASE
# Tue, 11 Mar 2025 21:10:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 11 Mar 2025 21:10:22 GMT
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["/bin/bash"]
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 11 Mar 2025 21:10:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 21:10:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_VERSION=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DIST=
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 Mar 2025 21:10:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
VOLUME [/var/solr]
# Tue, 11 Mar 2025 21:10:22 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 11 Mar 2025 21:10:22 GMT
WORKDIR /opt/solr
# Tue, 11 Mar 2025 21:10:22 GMT
USER 8983
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:25cf79adc8d2979d397edb23d9d8f0127bc0edfd1addfa501b8a0cc74338576b`  
		Last Modified: Mon, 07 Apr 2025 08:26:58 GMT  
		Size: 28.0 MB (28000118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ffac1a60b6cb80417a2deaa826c5568b388878415c01490d46c373b76b9af`  
		Last Modified: Wed, 09 Apr 2025 04:16:19 GMT  
		Size: 16.1 MB (16143553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4519af0c38240cf5ea7eabd190f4bb907c7286d25ddf361b362469def9b4cf05`  
		Last Modified: Wed, 23 Apr 2025 16:41:17 GMT  
		Size: 44.0 MB (43960934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c191115a908862638fb921185212d5a25c45f899ea7ebf5d5d7de623e202bf`  
		Last Modified: Wed, 23 Apr 2025 16:41:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c9d1ab01c219fdc662993dc0f57d42d26989e7e8a709570b2e15dee5128f40`  
		Last Modified: Wed, 23 Apr 2025 16:41:16 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb5b713439f1017370a1ac0ab2c27f07422d86fa18c20c4979c270482cdf5ed`  
		Last Modified: Wed, 23 Apr 2025 17:31:39 GMT  
		Size: 386.4 MB (386373521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cb01771ea7cffabdd4baa0114bccc25a1dabc3e1d74167a37f83685b3bdd88`  
		Last Modified: Wed, 23 Apr 2025 17:31:33 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7798acc7aa75fc3247ef2e58daa2acbea6a0d8c66332f27faf914d154b927cf9`  
		Last Modified: Wed, 23 Apr 2025 17:31:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8e05b5f1f3b8b633107d12c91955af9d09e58b2bc137c1d6dfca5408d4275e`  
		Last Modified: Wed, 23 Apr 2025 17:31:33 GMT  
		Size: 10.9 KB (10892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000038d0c14eea615d9af217b251810b5aa880a69917ac186892caeb1c8bbc99`  
		Last Modified: Wed, 23 Apr 2025 17:31:34 GMT  
		Size: 1.6 MB (1558947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:6c8fa8f287e48c5a2bc254b6c3823e3a9332c758e2931de79342ff5fad0979ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab590057968037e2cc2b521fbb352f4d4a2c95943adcea5eba2f68ffcde08181`

```dockerfile
```

-	Layers:
	-	`sha256:f19c51dc651534c32f89e5ee6646c7fe1d657169de3f13573a038676e2db577b`  
		Last Modified: Wed, 23 Apr 2025 17:31:33 GMT  
		Size: 4.4 MB (4350145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da55ea4a77a400c4fa976dd0eb21fcf43d3b9a149f5554e8d16a3a252730c55b`  
		Last Modified: Wed, 23 Apr 2025 17:31:33 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json
