## `solr:slim`

```console
$ docker pull solr@sha256:113a4b5f96fd941e2e22dbfc1ddf31bf70ad7777b68b169e02fb5528880e13f4
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
$ docker pull solr@sha256:a49a9ce1ce38d852cd4dd327ddcd7894fa96c0af7971227165083d17572078dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159267425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929b78929b3a8d240270e7565ade638bb4eb545a3c8ac18e0601822f2f758359`
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
ARG SOLR_DIST=-slim
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:15406bbb13ba0a5508806e2edb8c51bc8a7249de1b953a3b3c3379ab506e377b`  
		Last Modified: Wed, 23 Apr 2025 17:12:54 GMT  
		Size: 65.0 MB (64994907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7881bdb3e129139937c371b0d65ececeabf1ccaa385b1f3a71f8a493544bf052`  
		Last Modified: Wed, 23 Apr 2025 17:12:53 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee30ae17b0b0eb87f349ab17fb2cab328a70732a714ed039c9416f05b4232202`  
		Last Modified: Wed, 23 Apr 2025 17:12:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6908d79e03dab820fe66055dfb32fe88d799680dd5cc532ef4a6d29f342b36b2`  
		Last Modified: Wed, 23 Apr 2025 17:12:53 GMT  
		Size: 10.8 KB (10806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eac8c7dca17fd2b76ca159c89ba16155e5846d32ccfc9dd59d198b1144e5a9a`  
		Last Modified: Wed, 23 Apr 2025 17:12:54 GMT  
		Size: 1.6 MB (1617941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:b06f6edbff7270afe4a5dbe6d8d8fabb131e334bc8ac8b34cab8223b6c0d96d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefec73ac914ca90c51cbb09a412d85eeb1ca0c45639b4bde56acb00fd5fbdc6`

```dockerfile
```

-	Layers:
	-	`sha256:4031e125cbc8634171571b743af9493b08632ddc6655e556c86caba7eb28a010`  
		Last Modified: Wed, 23 Apr 2025 17:12:53 GMT  
		Size: 3.8 MB (3798988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be303c1133d1c1b11f263da18614804415a1a092b9f86e27b2044b760d26db8`  
		Last Modified: Wed, 23 Apr 2025 17:12:53 GMT  
		Size: 34.4 KB (34397 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:8ce28a8df262de78a02356f3ae97be89ee1f043d730e0c5282e97a6f5084f1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156375739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699b29afd7ed91e1827deb51a366a4a0ceb10171f254c7dd6dbdf3661f0c41e7`
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
ARG SOLR_DIST=-slim
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:5dbfefdfa62ba5663b0e87f734c165581341187e2436644d08db61c5e42899b5`  
		Last Modified: Wed, 23 Apr 2025 18:16:49 GMT  
		Size: 65.0 MB (64995012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d7afeee3f6d3dc547658a2d2d3e134aa5b7f71f9ec4d905e130caa92174041`  
		Last Modified: Wed, 23 Apr 2025 18:16:47 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145491909b56003e7bb5a347ea5ca1b02f61640958fe2577902e4d8f0f6c4ff8`  
		Last Modified: Wed, 23 Apr 2025 18:16:47 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df5381a602c690b68dd1ce0279eeabc225c50b3cbfd7f81a46a3003b487919`  
		Last Modified: Wed, 23 Apr 2025 18:16:47 GMT  
		Size: 10.8 KB (10812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2cd1da39eaff42d816f508b2b7a23574aa9712e548df095641963644ff546e`  
		Last Modified: Wed, 23 Apr 2025 18:16:48 GMT  
		Size: 1.5 MB (1474798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:9bb4dd5d0d296a4076965f8343bfe260f33a8fdb93e4602b9afb8a999bfbc2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76d75b104178ddb957bb151fc2890a74964cc92b415d21befcfa9c91688c2da`

```dockerfile
```

-	Layers:
	-	`sha256:e2104d64d5429cdc56c3ae60d1f8461432022920dd99e0ebaf9610055b086495`  
		Last Modified: Wed, 23 Apr 2025 18:16:47 GMT  
		Size: 3.8 MB (3798664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad20f712996f9127bc8afaab6d5b29776b12e851b90eefe0bbb5c7108e02097`  
		Last Modified: Wed, 23 Apr 2025 18:16:47 GMT  
		Size: 34.6 KB (34562 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:622b3a6beb126a25c3650516db58ef09b966f6d8c4ad4b749ee47d5b7a0b9fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165474161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e912163353392a40295899e9c2f2a7084e874aceaf9bfee6135705d418e5ed04`
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
ARG SOLR_DIST=-slim
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:84e830951f8e72d42f7758a0e20455cd25d7ded5221e86214bdfa45fe249038b`  
		Last Modified: Wed, 23 Apr 2025 17:47:21 GMT  
		Size: 65.0 MB (64995235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4ca36a29217019897c66876ebfc030007ad29e01249d3ff6626e22595a1d5a`  
		Last Modified: Wed, 23 Apr 2025 17:47:18 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f136e664fe8a12b3eee400953044ec54bbaef7ec33c7fb8b365ebf71079096c`  
		Last Modified: Wed, 23 Apr 2025 17:47:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b154f2447b562562c50b617d2df6107164ea9443e56607aa223ebfc2a996ec56`  
		Last Modified: Wed, 23 Apr 2025 17:47:18 GMT  
		Size: 10.8 KB (10809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f605f79a6c4ffbeddaab3e7078b4f7260222f6c9d4fce6c1e0034b5f216117c1`  
		Last Modified: Wed, 23 Apr 2025 17:47:20 GMT  
		Size: 1.6 MB (1630797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:5f0a52b55c200097d9c1a88c5db41085d90386276974a0bdac0ac97fa4348dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f26419f5d3cfe54c4a514f3f228db4ed0402e8b72609148aaf0fff3f43c925`

```dockerfile
```

-	Layers:
	-	`sha256:e85185cf151c1de543f0bdb64c3ad1bd26ec93a4f7ce31e4bb6e78b5556eca0a`  
		Last Modified: Wed, 23 Apr 2025 17:47:20 GMT  
		Size: 3.8 MB (3802897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5730d758864228cf0fc8e090210c4810909f806bd008dde201bfeb01c291b51`  
		Last Modified: Wed, 23 Apr 2025 17:47:18 GMT  
		Size: 34.5 KB (34450 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:9ecb2bd793f063ae330fe4f0ef233a63ca30ea40944e92ced606130bac3d0aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154676002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2054d03e5f9b105c099c425d44d1dff3fcde48750f3c27976c24ec82f3242939`
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
ARG SOLR_DIST=-slim
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST=-slim SOLR_SHA512=e760696cad89ba5c1858eeb3d7e8a873206dadcb961580ae3c79375de819d164d71ac896e90810ead19953b6b0589d31dfe8a765c8e197114956ad1b4de7559a SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:d5c4eb0266beab5626ed911c94d263f3eefef89fb9fd248bac216eaa87a28bef`  
		Last Modified: Wed, 23 Apr 2025 17:32:24 GMT  
		Size: 65.0 MB (64994664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6e8f4b247218b724c2315a754c277778d4e2a28e844a80ee507df4ebe2f255`  
		Last Modified: Wed, 23 Apr 2025 17:32:23 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ad805d3accca41c40cdcc6e630ac6076560f5720635c0e193f915051fefa88`  
		Last Modified: Wed, 23 Apr 2025 17:32:23 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab9de5b66bb11cbe804adf206a4024d1ae4d97c63cef418ea68cee1431779a5`  
		Last Modified: Wed, 23 Apr 2025 17:32:23 GMT  
		Size: 10.8 KB (10808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5314889f97e3b15bf2d5f9f5d8d6ac1b9ffd8f2004a1d891ea77a3350d5ff37`  
		Last Modified: Wed, 23 Apr 2025 17:32:24 GMT  
		Size: 1.6 MB (1558933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:39bd2544c082a8c21bae95fb6009ec8c70c4ea73c853bded2785f020f907c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95616c8629d348033227cf66d7c1503f76b2000c396dfd85d11e5599ea6b8f22`

```dockerfile
```

-	Layers:
	-	`sha256:5b8d2a183d70320786c124895c1b8c3d0d70023a0dbd1a41a7b3428a782b1b54`  
		Last Modified: Wed, 23 Apr 2025 17:32:23 GMT  
		Size: 3.8 MB (3800584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a767ed982ac6a78559f122c015758cacef6db2c6e494a12a4056fc4987e56c7`  
		Last Modified: Wed, 23 Apr 2025 17:32:23 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json
