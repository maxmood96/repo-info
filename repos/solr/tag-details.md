<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `solr`

-	[`solr:9`](#solr9)
-	[`solr:9-slim`](#solr9-slim)
-	[`solr:9.10`](#solr910)
-	[`solr:9.10-slim`](#solr910-slim)
-	[`solr:9.10.0`](#solr9100)
-	[`solr:9.10.0-slim`](#solr9100-slim)
-	[`solr:9.9`](#solr99)
-	[`solr:9.9-slim`](#solr99-slim)
-	[`solr:9.9.0`](#solr990)
-	[`solr:9.9.0-slim`](#solr990-slim)
-	[`solr:latest`](#solrlatest)
-	[`solr:slim`](#solrslim)

## `solr:9`

```console
$ docker pull solr@sha256:474f49c476d6742e1387d08971fb23f4bdbdf547c753838522e0c1a5cf07f044
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

### `solr:9` - linux; amd64

```console
$ docker pull solr@sha256:1184999572da4718bf4e8be7b1859289ff387ffe3dcfb0107d3929c6f013d437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.1 MB (483139769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea57e9b266756a844fdc234b8910f751bef4b524add8727825ca78355d1a9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efb96dabddfc76bb255f2062ea58cc0d71a35402242455e6ff541f2dd8c6e`  
		Last Modified: Thu, 02 Oct 2025 06:14:54 GMT  
		Size: 16.2 MB (16150246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9d91201f400dafb912bd4f1706e04991b2937d459b71d1c80ebf821ecb75be`  
		Last Modified: Thu, 02 Oct 2025 05:02:17 GMT  
		Size: 47.0 MB (46986074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b76b382631799417a3c67471e880b5248f8398eeee30b9bfc9903c52f0c211`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601f2c23751f6ef5043f76650593a141fb9eeb8fb9ae70269595b12d1e5d8069`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54670d52ce1ad1505f827a28103fac576dc41cafb17e3704445858e67b147594`  
		Last Modified: Thu, 02 Oct 2025 09:36:02 GMT  
		Size: 388.8 MB (388830900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42669950ac1eec3a3953cee523f879853b7ade662979c466537f17976ef5ff0`  
		Last Modified: Thu, 02 Oct 2025 08:42:03 GMT  
		Size: 4.3 KB (4269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc644d8725a8ee159d760bf0b9389878aab0b88c4d958c23d742b4045f8761f`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41738644700c2ab2034dc9f4d520475e54278b85e568d9c7948363704a9487ae`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbbdf3587600faed33fdeb339aea876fe2784d4dbee3982ff1e22366985ed8a`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 1.6 MB (1617893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:73f8ef8e83c58ba1fb838610d4a99dcb8543e66828c6e972479f98a7909f0961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b988352289ac947823ae3eda97c65c3a6364ea02e3a3ac26f224ee1fd3c92853`

```dockerfile
```

-	Layers:
	-	`sha256:528a057e5dfbd7ad7172b60ff9a05a1a2825360b93c957ab9f2c0f9fe5402478`  
		Last Modified: Thu, 02 Oct 2025 10:58:20 GMT  
		Size: 4.6 MB (4550103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59c7f2a3df1c872476f88d4c415435258385e39cfb64f974c3bd1a476fbc04f`  
		Last Modified: Thu, 02 Oct 2025 10:58:21 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:76008e266b6183562a31f7b5ce1e7e14950a381c27d90a73e4ff9947d08ed732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480253946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59914a9f4b174caa111a25a55b16070ab7ec7e134d02d737cb6594670c217724`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b48ce0fa3fcfd3966ce55ee451545585dfe3da5e248e92a6d1b0d45f55dc27`  
		Last Modified: Thu, 02 Oct 2025 01:18:01 GMT  
		Size: 16.1 MB (16065703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18baf420dc060a02e6b4427a9b58a8f8aec826c4c91e595be84693728113140`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 46.5 MB (46481588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04407eaefaf8d0ee0effa63673aad83ebb9283b7cfba66253ecc311d67aaf558`  
		Last Modified: Thu, 02 Oct 2025 01:18:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ab097c3dabb4e6cecd9895cc9bdbc4e0acef286bb1eef5f6a5780116b38ae8`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d9f89ac2a48472c772d1724870239dbbe58e1831b6982925883c4eb5a773c0`  
		Last Modified: Thu, 02 Oct 2025 05:01:41 GMT  
		Size: 388.8 MB (388830902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00ef8b83fb1422aad1310291d9e24da5bdbd69dab1234af94bfea6ccdbaf90`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 4.3 KB (4301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fa610fc85471289f7d8c9921dc9e39a307cfa4d31fb6ed754684b5071edc26`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2568d7c7aae7622652bbc8fb0acc028eec079af2c6c4bf1d5a1330147c8dae`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 10.9 KB (10889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d2bce847a1b4487b6a09b21a11ade8476d5fa02181c6169d2380c3553e6c15`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 1.5 MB (1474774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:05d1f296e984ee0fe899ec5f73d5d846b36544971793a3b4c85d2fee5df7ef8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2378bfa7c4001aa91c0aa587a1047953171af2876f52b1dc55c55e581c2b96d`

```dockerfile
```

-	Layers:
	-	`sha256:e69fef67f0e76642968f385e922a70e5627489ef4bec51db1f77c5cbe54fa899`  
		Last Modified: Thu, 02 Oct 2025 04:58:28 GMT  
		Size: 4.5 MB (4549779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d37421d08aeec678727598bcd7c47fded4b54ab6393d6522b74b07ee8f35b8a6`  
		Last Modified: Thu, 02 Oct 2025 04:58:29 GMT  
		Size: 34.5 KB (34499 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; ppc64le

```console
$ docker pull solr@sha256:c5753e77f4d02393765ceb113e311d088692a76791262b8f627cb1efac073d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.4 MB (489376497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157b67b6d9a319fae3a9d1d65bd0f426f119492ea950fa98209a6f0d02eb741c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe9254f7488179acffc6d4fe22874ac523780d1d1c9e70f598251442a3a8b7`  
		Last Modified: Thu, 02 Oct 2025 01:19:02 GMT  
		Size: 17.6 MB (17623675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c1dbab248f00072fac2b930ca77ed36f86048d5c4ec6feded0a8b7d6e36fd5`  
		Last Modified: Thu, 02 Oct 2025 01:33:00 GMT  
		Size: 46.8 MB (46826196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb99ff66ae304853960cda05446ebfd53e06f9036817bfcce2a88d57080869`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18cee3e6a628a50b6b6c6cc9804934404caac93f9c48f980c4e76681b47ebaf`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd38542341ce5da818bde1ebcb35e3625cf5e5b3312e806f5b11ba26c346a037`  
		Last Modified: Thu, 02 Oct 2025 07:11:56 GMT  
		Size: 388.8 MB (388831196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5041e5151337bb4f73668771edcc87dd70ff91e32155e7ee588b9fb2110841`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 4.3 KB (4267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbd91c75744142e8853f5e72f7f8f6bd3e53bb623f6fb4eae85466d38cd8a63`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e7aa2b6e76b871e786eb1ff57068eb465a3462870157ad69822689a6dfbbef`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415a413a4beea68bb4bf4535fd715fba90efba1c77abb8451ed9d51f18f22966`  
		Last Modified: Thu, 02 Oct 2025 06:47:13 GMT  
		Size: 1.6 MB (1630798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:5a2e5812778db0e7cb7b2788461e40dc5a54c8f8ab0cd09bdbe18ba42c1e0e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4588543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c168518cec35715fcb55d9a2393852fa3503573b702a8b656f37ed984f50865`

```dockerfile
```

-	Layers:
	-	`sha256:3d94514b374af5cbb9882ae157e356a61e74b8fc0ba8c5a9804f20928ac3dc9f`  
		Last Modified: Thu, 02 Oct 2025 07:58:24 GMT  
		Size: 4.6 MB (4554156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c6fe8c06d890c6058fb6ef4a43fefac31359979226130c891945e9cfb66d1d6`  
		Last Modified: Thu, 02 Oct 2025 07:58:25 GMT  
		Size: 34.4 KB (34387 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; s390x

```console
$ docker pull solr@sha256:4c8e8390f38cc37156a512e7d977a1332042288fcd45286a60bdf1bdcdc27d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.5 MB (478534361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8df0009a7b141720dc3da6a340a8c6929ba3c6b8c0c7665d11c03e7dcfb61c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa057040468c4605ce5fb8ed262a9f172e925905b6ab54206a3c9fdecdb0775`  
		Last Modified: Thu, 02 Oct 2025 01:15:00 GMT  
		Size: 16.1 MB (16149615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b3cd93688739505fe8d2dd5931e3a33e46e0acaab94ebfe0a47f8e03fe7dbc`  
		Last Modified: Thu, 02 Oct 2025 01:20:10 GMT  
		Size: 44.0 MB (43973850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930f491eada45b104be02c555f05bb5f1aeeae21bb31ec5cd9bf1bcbe668d40`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae07338a40ce04ab829bc61ace554a85c92ee69a26d5001a62e8c9225b168c2`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f162d79fc0a8ad37058ee42f04c8a498358fd687b78d2c0861457159f8eb0bb`  
		Last Modified: Thu, 02 Oct 2025 04:13:47 GMT  
		Size: 388.8 MB (388830690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc427c37362e4ee092e4a327b870c230aec5973af589d4330edf440b5d6838`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e5c9013b1608aec7c7166c654c750b2bbf85c3bbfb0a64d08f18dd86d5168c`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26595036f47876da19cddd6060d42f7c83df63863fa9e725ac751f720b05187`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84bf63c653c481c26bd587d9850da365184173186401b73b10b810ac1f56888`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 1.6 MB (1558919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:de9f24cb8ee2153e55645a59ebf93c02c0df8704860093c82b5e5ae2b20b9be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4586034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3b49a154be60f532f8cb3d3b4513912549ccd7d40536e6d5cecbfa37167eec`

```dockerfile
```

-	Layers:
	-	`sha256:99c3b6c6f287f5bb7e6d750e6c3dfc7e7a4ccee7e7cf1281f1e2f9b9ff9d0c8a`  
		Last Modified: Thu, 02 Oct 2025 04:58:37 GMT  
		Size: 4.6 MB (4551699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc091fcecc073b841f0edba7541fd1ab9b237427264ec153916badef8b26c08`  
		Last Modified: Thu, 02 Oct 2025 04:58:38 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9-slim`

```console
$ docker pull solr@sha256:bd326b59064e9b2656efb8419f539cfc342e28a6e854a2fa86558bfb2e4becfb
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
$ docker pull solr@sha256:2cf7da27570699186755c431c4f2e3ee18fbdc7d51e11702db3fd8b04cb9b386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159927336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7677515e900be3af5f717dc4035f85f923a1391d84dd56e09c6d95bfdfcae3cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efb96dabddfc76bb255f2062ea58cc0d71a35402242455e6ff541f2dd8c6e`  
		Last Modified: Thu, 02 Oct 2025 06:14:54 GMT  
		Size: 16.2 MB (16150246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9d91201f400dafb912bd4f1706e04991b2937d459b71d1c80ebf821ecb75be`  
		Last Modified: Thu, 02 Oct 2025 05:02:17 GMT  
		Size: 47.0 MB (46986074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b76b382631799417a3c67471e880b5248f8398eeee30b9bfc9903c52f0c211`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601f2c23751f6ef5043f76650593a141fb9eeb8fb9ae70269595b12d1e5d8069`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa4a9e7abd268d5d88689727a7ba11c57d9c08a4dccd1acad3dc4155abe1b9`  
		Last Modified: Thu, 02 Oct 2025 09:36:08 GMT  
		Size: 65.6 MB (65618514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e391a4d786cdb41b082aa91aec9e7ae321e3cf0feaf41958ffb21c8d224dfbc`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 4.3 KB (4268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dbaa69c6b4c53d606802d3f525be0f9925439aef9863a73890e5d26e3eef0d`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb02c76f0d15e2b564efa8decdb24d6b6c0dfff01a0fb20360ae3fba452d20a`  
		Last Modified: Thu, 02 Oct 2025 09:33:31 GMT  
		Size: 10.8 KB (10806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5092229b9b7cd3851ddd78ca4f2da61a9a97c7bdfa35b05c6717805d74c0e61`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 1.6 MB (1617925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:a4c6f16a2557e28be000c602a6eb6a08ad541db9d4707bbed32bcc04e4b19b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3860b265b2e087fe2f02e87336c763cf38c732b03a3ec80556eac5a91190fc6`

```dockerfile
```

-	Layers:
	-	`sha256:f195b0b8cd59f58d2f18dffb2336d81d78af1201d867dabf0376cda44e83344e`  
		Last Modified: Thu, 02 Oct 2025 10:58:28 GMT  
		Size: 4.0 MB (3963114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf25511365a9506bf219e8a33e0a581d4e8a57ad7ad6d06cd7870512243f58e`  
		Last Modified: Thu, 02 Oct 2025 10:58:29 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:ca5895f18d242854ed8f75afef4839a79a5334ce237b3544263292f136726715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157041593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a264b8de12e72c8a23c28331a02e9316c59569dafeb78aab0173d44283f9c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b48ce0fa3fcfd3966ce55ee451545585dfe3da5e248e92a6d1b0d45f55dc27`  
		Last Modified: Thu, 02 Oct 2025 01:18:01 GMT  
		Size: 16.1 MB (16065703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18baf420dc060a02e6b4427a9b58a8f8aec826c4c91e595be84693728113140`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 46.5 MB (46481588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04407eaefaf8d0ee0effa63673aad83ebb9283b7cfba66253ecc311d67aaf558`  
		Last Modified: Thu, 02 Oct 2025 01:18:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ab097c3dabb4e6cecd9895cc9bdbc4e0acef286bb1eef5f6a5780116b38ae8`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1788c12a8a00486d15c57601dcf161a77ed5dea586cd478f62f940f2380e8a14`  
		Last Modified: Thu, 02 Oct 2025 02:28:00 GMT  
		Size: 65.6 MB (65618603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea20739a0dd6f84a5787bba3e627b5cb833a97a8048a0c5dd4294bfbeb28d79b`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afe6708e36ad5ef40d9fe52c0c5f4f04b986249c200ae0272d83fcbce50665b`  
		Last Modified: Thu, 02 Oct 2025 02:27:55 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9531714abba676aa977a548cc1cc705823e4215e79d2c263ef93c38eafd3592a`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6114d5516094d6860a79d02444d3e35d6e7fc7da0906cbdf7e583ed9505d72a3`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 1.5 MB (1474801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:cd2cef292d7887d14606562431c9cf3e4d71d94af62fab231cec0a84d1cda9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccf89bfeee10a7edd221eb6f0206bd691a60c409e9ba90b82c0bcd64e4f9e17`

```dockerfile
```

-	Layers:
	-	`sha256:6d7658bb916802c2a8190af6541fe275017b54987cad73b0886492b8b0dfe17b`  
		Last Modified: Thu, 02 Oct 2025 04:58:36 GMT  
		Size: 4.0 MB (3962790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd55b1955b2379919285a5f02b2489d57f9b52ca7f2a0a644eaeca7e95330aff`  
		Last Modified: Thu, 02 Oct 2025 04:58:37 GMT  
		Size: 34.6 KB (34561 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:93450a34e431e1f50f13ec39b6522a1b69736a54392d81e57c6979e97a7412c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166164111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da97ffcce00632f4ceaca536916f8a60f4d42464b4b320e4d1f03e07267c14d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe9254f7488179acffc6d4fe22874ac523780d1d1c9e70f598251442a3a8b7`  
		Last Modified: Thu, 02 Oct 2025 01:19:02 GMT  
		Size: 17.6 MB (17623675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c1dbab248f00072fac2b930ca77ed36f86048d5c4ec6feded0a8b7d6e36fd5`  
		Last Modified: Thu, 02 Oct 2025 01:33:00 GMT  
		Size: 46.8 MB (46826196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb99ff66ae304853960cda05446ebfd53e06f9036817bfcce2a88d57080869`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18cee3e6a628a50b6b6c6cc9804934404caac93f9c48f980c4e76681b47ebaf`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb467ce9858a45c79645d7c7a5ac0ee11357cdc9b65d566ee99005fb488724a3`  
		Last Modified: Thu, 02 Oct 2025 07:59:00 GMT  
		Size: 65.6 MB (65618910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d782a7ee53e95c1066111b7906abb56c7d79735460a79e0315b36186d2201b2`  
		Last Modified: Thu, 02 Oct 2025 07:21:04 GMT  
		Size: 4.3 KB (4265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f063ac5d6e50ceb728a48f391180a759f20ba997cbc0af712d05cc7d8930d8`  
		Last Modified: Thu, 02 Oct 2025 07:21:07 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6216d1919f03bf4d336a064c428b0b3edce673595fdd570b6551765452e977`  
		Last Modified: Thu, 02 Oct 2025 07:21:10 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f7df8f164dac94273e8f95276ab9afbd3e7f34939c9c3b262fe81a005a8903`  
		Last Modified: Thu, 02 Oct 2025 07:21:13 GMT  
		Size: 1.6 MB (1630787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:5c1db0532d66a16a686f12bcf4bea22e3bdd7c0a3aaa6976deb1a62473b18f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfcd6085af973ea1fbb3186cc151de649f6b82cd2072e74167c863a91cffcff`

```dockerfile
```

-	Layers:
	-	`sha256:0f00eee7e2d23b94ec71a38823b8532c9c1044840d9943ad7913c51f8405df04`  
		Last Modified: Thu, 02 Oct 2025 07:58:29 GMT  
		Size: 4.0 MB (3967167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24384ff2c1342941160401966e98a861dd83d613aacce1fd17754429dda32962`  
		Last Modified: Thu, 02 Oct 2025 07:58:29 GMT  
		Size: 34.5 KB (34450 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:81394debe7ef2b733de098e50bbc835592d6a1d45c5160af43416a2d37e11c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155321791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ade1748d587553ab347605082a9b4dfe72a269962b61bf4c7468ce6b7798e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa057040468c4605ce5fb8ed262a9f172e925905b6ab54206a3c9fdecdb0775`  
		Last Modified: Thu, 02 Oct 2025 01:15:00 GMT  
		Size: 16.1 MB (16149615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b3cd93688739505fe8d2dd5931e3a33e46e0acaab94ebfe0a47f8e03fe7dbc`  
		Last Modified: Thu, 02 Oct 2025 01:20:10 GMT  
		Size: 44.0 MB (43973850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930f491eada45b104be02c555f05bb5f1aeeae21bb31ec5cd9bf1bcbe668d40`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae07338a40ce04ab829bc61ace554a85c92ee69a26d5001a62e8c9225b168c2`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bb5ca63550de993646e21b3efe5ee741d92e1dbf1f44100d49f442d096a334`  
		Last Modified: Thu, 02 Oct 2025 03:39:06 GMT  
		Size: 65.6 MB (65618204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c96895d4a82cc44f5c3a6154bbca1e62cf6bbe1f19293d18a8e57d8e512c69`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8428320aa2a8ec906dd93c37135b8ff4435c6ea42f0a5ab42e2c8b54986761`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6895a57397abc92df039149f9065c63d69f084f0435bdde59e7652108c6b8e`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb6501a43479515a34b9ccd79cbb2373dd062269c16d81b8e22d6d096e85d12`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 1.6 MB (1558915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:b6a972c8f8ea32ef937956f282da3c68901d9a20bd88e76d75e3da929e8c4035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3999108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b65da4092443c8f9e823c8d8432352e4bea271186c2df5df5293018d1e6a96d`

```dockerfile
```

-	Layers:
	-	`sha256:5158a0663a0060bd3b0f0d8d41de42570ca67f685c7028749ddcd85010057b5e`  
		Last Modified: Thu, 02 Oct 2025 04:58:50 GMT  
		Size: 4.0 MB (3964710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7523b5ac7f5ef4ebde3f85a3a023772d50597f17e31843a8c564f3d947f16bac`  
		Last Modified: Thu, 02 Oct 2025 04:58:51 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.10`

**does not exist** (yet?)

## `solr:9.10-slim`

**does not exist** (yet?)

## `solr:9.10.0`

**does not exist** (yet?)

## `solr:9.10.0-slim`

**does not exist** (yet?)

## `solr:9.9`

```console
$ docker pull solr@sha256:474f49c476d6742e1387d08971fb23f4bdbdf547c753838522e0c1a5cf07f044
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

### `solr:9.9` - linux; amd64

```console
$ docker pull solr@sha256:1184999572da4718bf4e8be7b1859289ff387ffe3dcfb0107d3929c6f013d437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.1 MB (483139769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea57e9b266756a844fdc234b8910f751bef4b524add8727825ca78355d1a9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efb96dabddfc76bb255f2062ea58cc0d71a35402242455e6ff541f2dd8c6e`  
		Last Modified: Thu, 02 Oct 2025 06:14:54 GMT  
		Size: 16.2 MB (16150246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9d91201f400dafb912bd4f1706e04991b2937d459b71d1c80ebf821ecb75be`  
		Last Modified: Thu, 02 Oct 2025 05:02:17 GMT  
		Size: 47.0 MB (46986074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b76b382631799417a3c67471e880b5248f8398eeee30b9bfc9903c52f0c211`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601f2c23751f6ef5043f76650593a141fb9eeb8fb9ae70269595b12d1e5d8069`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54670d52ce1ad1505f827a28103fac576dc41cafb17e3704445858e67b147594`  
		Last Modified: Thu, 02 Oct 2025 09:36:02 GMT  
		Size: 388.8 MB (388830900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42669950ac1eec3a3953cee523f879853b7ade662979c466537f17976ef5ff0`  
		Last Modified: Thu, 02 Oct 2025 08:42:03 GMT  
		Size: 4.3 KB (4269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc644d8725a8ee159d760bf0b9389878aab0b88c4d958c23d742b4045f8761f`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41738644700c2ab2034dc9f4d520475e54278b85e568d9c7948363704a9487ae`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbbdf3587600faed33fdeb339aea876fe2784d4dbee3982ff1e22366985ed8a`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 1.6 MB (1617893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9` - unknown; unknown

```console
$ docker pull solr@sha256:73f8ef8e83c58ba1fb838610d4a99dcb8543e66828c6e972479f98a7909f0961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b988352289ac947823ae3eda97c65c3a6364ea02e3a3ac26f224ee1fd3c92853`

```dockerfile
```

-	Layers:
	-	`sha256:528a057e5dfbd7ad7172b60ff9a05a1a2825360b93c957ab9f2c0f9fe5402478`  
		Last Modified: Thu, 02 Oct 2025 10:58:20 GMT  
		Size: 4.6 MB (4550103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59c7f2a3df1c872476f88d4c415435258385e39cfb64f974c3bd1a476fbc04f`  
		Last Modified: Thu, 02 Oct 2025 10:58:21 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:76008e266b6183562a31f7b5ce1e7e14950a381c27d90a73e4ff9947d08ed732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480253946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59914a9f4b174caa111a25a55b16070ab7ec7e134d02d737cb6594670c217724`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b48ce0fa3fcfd3966ce55ee451545585dfe3da5e248e92a6d1b0d45f55dc27`  
		Last Modified: Thu, 02 Oct 2025 01:18:01 GMT  
		Size: 16.1 MB (16065703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18baf420dc060a02e6b4427a9b58a8f8aec826c4c91e595be84693728113140`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 46.5 MB (46481588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04407eaefaf8d0ee0effa63673aad83ebb9283b7cfba66253ecc311d67aaf558`  
		Last Modified: Thu, 02 Oct 2025 01:18:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ab097c3dabb4e6cecd9895cc9bdbc4e0acef286bb1eef5f6a5780116b38ae8`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d9f89ac2a48472c772d1724870239dbbe58e1831b6982925883c4eb5a773c0`  
		Last Modified: Thu, 02 Oct 2025 05:01:41 GMT  
		Size: 388.8 MB (388830902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00ef8b83fb1422aad1310291d9e24da5bdbd69dab1234af94bfea6ccdbaf90`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 4.3 KB (4301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fa610fc85471289f7d8c9921dc9e39a307cfa4d31fb6ed754684b5071edc26`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2568d7c7aae7622652bbc8fb0acc028eec079af2c6c4bf1d5a1330147c8dae`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 10.9 KB (10889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d2bce847a1b4487b6a09b21a11ade8476d5fa02181c6169d2380c3553e6c15`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 1.5 MB (1474774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9` - unknown; unknown

```console
$ docker pull solr@sha256:05d1f296e984ee0fe899ec5f73d5d846b36544971793a3b4c85d2fee5df7ef8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2378bfa7c4001aa91c0aa587a1047953171af2876f52b1dc55c55e581c2b96d`

```dockerfile
```

-	Layers:
	-	`sha256:e69fef67f0e76642968f385e922a70e5627489ef4bec51db1f77c5cbe54fa899`  
		Last Modified: Thu, 02 Oct 2025 04:58:28 GMT  
		Size: 4.5 MB (4549779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d37421d08aeec678727598bcd7c47fded4b54ab6393d6522b74b07ee8f35b8a6`  
		Last Modified: Thu, 02 Oct 2025 04:58:29 GMT  
		Size: 34.5 KB (34499 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9` - linux; ppc64le

```console
$ docker pull solr@sha256:c5753e77f4d02393765ceb113e311d088692a76791262b8f627cb1efac073d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.4 MB (489376497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157b67b6d9a319fae3a9d1d65bd0f426f119492ea950fa98209a6f0d02eb741c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe9254f7488179acffc6d4fe22874ac523780d1d1c9e70f598251442a3a8b7`  
		Last Modified: Thu, 02 Oct 2025 01:19:02 GMT  
		Size: 17.6 MB (17623675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c1dbab248f00072fac2b930ca77ed36f86048d5c4ec6feded0a8b7d6e36fd5`  
		Last Modified: Thu, 02 Oct 2025 01:33:00 GMT  
		Size: 46.8 MB (46826196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb99ff66ae304853960cda05446ebfd53e06f9036817bfcce2a88d57080869`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18cee3e6a628a50b6b6c6cc9804934404caac93f9c48f980c4e76681b47ebaf`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd38542341ce5da818bde1ebcb35e3625cf5e5b3312e806f5b11ba26c346a037`  
		Last Modified: Thu, 02 Oct 2025 07:11:56 GMT  
		Size: 388.8 MB (388831196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5041e5151337bb4f73668771edcc87dd70ff91e32155e7ee588b9fb2110841`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 4.3 KB (4267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbd91c75744142e8853f5e72f7f8f6bd3e53bb623f6fb4eae85466d38cd8a63`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e7aa2b6e76b871e786eb1ff57068eb465a3462870157ad69822689a6dfbbef`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415a413a4beea68bb4bf4535fd715fba90efba1c77abb8451ed9d51f18f22966`  
		Last Modified: Thu, 02 Oct 2025 06:47:13 GMT  
		Size: 1.6 MB (1630798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9` - unknown; unknown

```console
$ docker pull solr@sha256:5a2e5812778db0e7cb7b2788461e40dc5a54c8f8ab0cd09bdbe18ba42c1e0e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4588543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c168518cec35715fcb55d9a2393852fa3503573b702a8b656f37ed984f50865`

```dockerfile
```

-	Layers:
	-	`sha256:3d94514b374af5cbb9882ae157e356a61e74b8fc0ba8c5a9804f20928ac3dc9f`  
		Last Modified: Thu, 02 Oct 2025 07:58:24 GMT  
		Size: 4.6 MB (4554156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c6fe8c06d890c6058fb6ef4a43fefac31359979226130c891945e9cfb66d1d6`  
		Last Modified: Thu, 02 Oct 2025 07:58:25 GMT  
		Size: 34.4 KB (34387 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9` - linux; s390x

```console
$ docker pull solr@sha256:4c8e8390f38cc37156a512e7d977a1332042288fcd45286a60bdf1bdcdc27d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.5 MB (478534361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8df0009a7b141720dc3da6a340a8c6929ba3c6b8c0c7665d11c03e7dcfb61c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa057040468c4605ce5fb8ed262a9f172e925905b6ab54206a3c9fdecdb0775`  
		Last Modified: Thu, 02 Oct 2025 01:15:00 GMT  
		Size: 16.1 MB (16149615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b3cd93688739505fe8d2dd5931e3a33e46e0acaab94ebfe0a47f8e03fe7dbc`  
		Last Modified: Thu, 02 Oct 2025 01:20:10 GMT  
		Size: 44.0 MB (43973850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930f491eada45b104be02c555f05bb5f1aeeae21bb31ec5cd9bf1bcbe668d40`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae07338a40ce04ab829bc61ace554a85c92ee69a26d5001a62e8c9225b168c2`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f162d79fc0a8ad37058ee42f04c8a498358fd687b78d2c0861457159f8eb0bb`  
		Last Modified: Thu, 02 Oct 2025 04:13:47 GMT  
		Size: 388.8 MB (388830690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc427c37362e4ee092e4a327b870c230aec5973af589d4330edf440b5d6838`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e5c9013b1608aec7c7166c654c750b2bbf85c3bbfb0a64d08f18dd86d5168c`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26595036f47876da19cddd6060d42f7c83df63863fa9e725ac751f720b05187`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84bf63c653c481c26bd587d9850da365184173186401b73b10b810ac1f56888`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 1.6 MB (1558919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9` - unknown; unknown

```console
$ docker pull solr@sha256:de9f24cb8ee2153e55645a59ebf93c02c0df8704860093c82b5e5ae2b20b9be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4586034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3b49a154be60f532f8cb3d3b4513912549ccd7d40536e6d5cecbfa37167eec`

```dockerfile
```

-	Layers:
	-	`sha256:99c3b6c6f287f5bb7e6d750e6c3dfc7e7a4ccee7e7cf1281f1e2f9b9ff9d0c8a`  
		Last Modified: Thu, 02 Oct 2025 04:58:37 GMT  
		Size: 4.6 MB (4551699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc091fcecc073b841f0edba7541fd1ab9b237427264ec153916badef8b26c08`  
		Last Modified: Thu, 02 Oct 2025 04:58:38 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.9-slim`

```console
$ docker pull solr@sha256:bd326b59064e9b2656efb8419f539cfc342e28a6e854a2fa86558bfb2e4becfb
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

### `solr:9.9-slim` - linux; amd64

```console
$ docker pull solr@sha256:2cf7da27570699186755c431c4f2e3ee18fbdc7d51e11702db3fd8b04cb9b386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159927336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7677515e900be3af5f717dc4035f85f923a1391d84dd56e09c6d95bfdfcae3cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efb96dabddfc76bb255f2062ea58cc0d71a35402242455e6ff541f2dd8c6e`  
		Last Modified: Thu, 02 Oct 2025 06:14:54 GMT  
		Size: 16.2 MB (16150246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9d91201f400dafb912bd4f1706e04991b2937d459b71d1c80ebf821ecb75be`  
		Last Modified: Thu, 02 Oct 2025 05:02:17 GMT  
		Size: 47.0 MB (46986074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b76b382631799417a3c67471e880b5248f8398eeee30b9bfc9903c52f0c211`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601f2c23751f6ef5043f76650593a141fb9eeb8fb9ae70269595b12d1e5d8069`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa4a9e7abd268d5d88689727a7ba11c57d9c08a4dccd1acad3dc4155abe1b9`  
		Last Modified: Thu, 02 Oct 2025 09:36:08 GMT  
		Size: 65.6 MB (65618514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e391a4d786cdb41b082aa91aec9e7ae321e3cf0feaf41958ffb21c8d224dfbc`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 4.3 KB (4268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dbaa69c6b4c53d606802d3f525be0f9925439aef9863a73890e5d26e3eef0d`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb02c76f0d15e2b564efa8decdb24d6b6c0dfff01a0fb20360ae3fba452d20a`  
		Last Modified: Thu, 02 Oct 2025 09:33:31 GMT  
		Size: 10.8 KB (10806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5092229b9b7cd3851ddd78ca4f2da61a9a97c7bdfa35b05c6717805d74c0e61`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 1.6 MB (1617925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:a4c6f16a2557e28be000c602a6eb6a08ad541db9d4707bbed32bcc04e4b19b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3860b265b2e087fe2f02e87336c763cf38c732b03a3ec80556eac5a91190fc6`

```dockerfile
```

-	Layers:
	-	`sha256:f195b0b8cd59f58d2f18dffb2336d81d78af1201d867dabf0376cda44e83344e`  
		Last Modified: Thu, 02 Oct 2025 10:58:28 GMT  
		Size: 4.0 MB (3963114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf25511365a9506bf219e8a33e0a581d4e8a57ad7ad6d06cd7870512243f58e`  
		Last Modified: Thu, 02 Oct 2025 10:58:29 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:ca5895f18d242854ed8f75afef4839a79a5334ce237b3544263292f136726715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157041593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a264b8de12e72c8a23c28331a02e9316c59569dafeb78aab0173d44283f9c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b48ce0fa3fcfd3966ce55ee451545585dfe3da5e248e92a6d1b0d45f55dc27`  
		Last Modified: Thu, 02 Oct 2025 01:18:01 GMT  
		Size: 16.1 MB (16065703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18baf420dc060a02e6b4427a9b58a8f8aec826c4c91e595be84693728113140`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 46.5 MB (46481588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04407eaefaf8d0ee0effa63673aad83ebb9283b7cfba66253ecc311d67aaf558`  
		Last Modified: Thu, 02 Oct 2025 01:18:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ab097c3dabb4e6cecd9895cc9bdbc4e0acef286bb1eef5f6a5780116b38ae8`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1788c12a8a00486d15c57601dcf161a77ed5dea586cd478f62f940f2380e8a14`  
		Last Modified: Thu, 02 Oct 2025 02:28:00 GMT  
		Size: 65.6 MB (65618603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea20739a0dd6f84a5787bba3e627b5cb833a97a8048a0c5dd4294bfbeb28d79b`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afe6708e36ad5ef40d9fe52c0c5f4f04b986249c200ae0272d83fcbce50665b`  
		Last Modified: Thu, 02 Oct 2025 02:27:55 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9531714abba676aa977a548cc1cc705823e4215e79d2c263ef93c38eafd3592a`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6114d5516094d6860a79d02444d3e35d6e7fc7da0906cbdf7e583ed9505d72a3`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 1.5 MB (1474801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:cd2cef292d7887d14606562431c9cf3e4d71d94af62fab231cec0a84d1cda9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccf89bfeee10a7edd221eb6f0206bd691a60c409e9ba90b82c0bcd64e4f9e17`

```dockerfile
```

-	Layers:
	-	`sha256:6d7658bb916802c2a8190af6541fe275017b54987cad73b0886492b8b0dfe17b`  
		Last Modified: Thu, 02 Oct 2025 04:58:36 GMT  
		Size: 4.0 MB (3962790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd55b1955b2379919285a5f02b2489d57f9b52ca7f2a0a644eaeca7e95330aff`  
		Last Modified: Thu, 02 Oct 2025 04:58:37 GMT  
		Size: 34.6 KB (34561 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:93450a34e431e1f50f13ec39b6522a1b69736a54392d81e57c6979e97a7412c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166164111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da97ffcce00632f4ceaca536916f8a60f4d42464b4b320e4d1f03e07267c14d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe9254f7488179acffc6d4fe22874ac523780d1d1c9e70f598251442a3a8b7`  
		Last Modified: Thu, 02 Oct 2025 01:19:02 GMT  
		Size: 17.6 MB (17623675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c1dbab248f00072fac2b930ca77ed36f86048d5c4ec6feded0a8b7d6e36fd5`  
		Last Modified: Thu, 02 Oct 2025 01:33:00 GMT  
		Size: 46.8 MB (46826196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb99ff66ae304853960cda05446ebfd53e06f9036817bfcce2a88d57080869`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18cee3e6a628a50b6b6c6cc9804934404caac93f9c48f980c4e76681b47ebaf`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb467ce9858a45c79645d7c7a5ac0ee11357cdc9b65d566ee99005fb488724a3`  
		Last Modified: Thu, 02 Oct 2025 07:59:00 GMT  
		Size: 65.6 MB (65618910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d782a7ee53e95c1066111b7906abb56c7d79735460a79e0315b36186d2201b2`  
		Last Modified: Thu, 02 Oct 2025 07:21:04 GMT  
		Size: 4.3 KB (4265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f063ac5d6e50ceb728a48f391180a759f20ba997cbc0af712d05cc7d8930d8`  
		Last Modified: Thu, 02 Oct 2025 07:21:07 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6216d1919f03bf4d336a064c428b0b3edce673595fdd570b6551765452e977`  
		Last Modified: Thu, 02 Oct 2025 07:21:10 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f7df8f164dac94273e8f95276ab9afbd3e7f34939c9c3b262fe81a005a8903`  
		Last Modified: Thu, 02 Oct 2025 07:21:13 GMT  
		Size: 1.6 MB (1630787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:5c1db0532d66a16a686f12bcf4bea22e3bdd7c0a3aaa6976deb1a62473b18f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfcd6085af973ea1fbb3186cc151de649f6b82cd2072e74167c863a91cffcff`

```dockerfile
```

-	Layers:
	-	`sha256:0f00eee7e2d23b94ec71a38823b8532c9c1044840d9943ad7913c51f8405df04`  
		Last Modified: Thu, 02 Oct 2025 07:58:29 GMT  
		Size: 4.0 MB (3967167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24384ff2c1342941160401966e98a861dd83d613aacce1fd17754429dda32962`  
		Last Modified: Thu, 02 Oct 2025 07:58:29 GMT  
		Size: 34.5 KB (34450 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9-slim` - linux; s390x

```console
$ docker pull solr@sha256:81394debe7ef2b733de098e50bbc835592d6a1d45c5160af43416a2d37e11c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155321791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ade1748d587553ab347605082a9b4dfe72a269962b61bf4c7468ce6b7798e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa057040468c4605ce5fb8ed262a9f172e925905b6ab54206a3c9fdecdb0775`  
		Last Modified: Thu, 02 Oct 2025 01:15:00 GMT  
		Size: 16.1 MB (16149615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b3cd93688739505fe8d2dd5931e3a33e46e0acaab94ebfe0a47f8e03fe7dbc`  
		Last Modified: Thu, 02 Oct 2025 01:20:10 GMT  
		Size: 44.0 MB (43973850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930f491eada45b104be02c555f05bb5f1aeeae21bb31ec5cd9bf1bcbe668d40`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae07338a40ce04ab829bc61ace554a85c92ee69a26d5001a62e8c9225b168c2`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bb5ca63550de993646e21b3efe5ee741d92e1dbf1f44100d49f442d096a334`  
		Last Modified: Thu, 02 Oct 2025 03:39:06 GMT  
		Size: 65.6 MB (65618204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c96895d4a82cc44f5c3a6154bbca1e62cf6bbe1f19293d18a8e57d8e512c69`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8428320aa2a8ec906dd93c37135b8ff4435c6ea42f0a5ab42e2c8b54986761`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6895a57397abc92df039149f9065c63d69f084f0435bdde59e7652108c6b8e`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb6501a43479515a34b9ccd79cbb2373dd062269c16d81b8e22d6d096e85d12`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 1.6 MB (1558915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:b6a972c8f8ea32ef937956f282da3c68901d9a20bd88e76d75e3da929e8c4035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3999108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b65da4092443c8f9e823c8d8432352e4bea271186c2df5df5293018d1e6a96d`

```dockerfile
```

-	Layers:
	-	`sha256:5158a0663a0060bd3b0f0d8d41de42570ca67f685c7028749ddcd85010057b5e`  
		Last Modified: Thu, 02 Oct 2025 04:58:50 GMT  
		Size: 4.0 MB (3964710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7523b5ac7f5ef4ebde3f85a3a023772d50597f17e31843a8c564f3d947f16bac`  
		Last Modified: Thu, 02 Oct 2025 04:58:51 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.9.0`

```console
$ docker pull solr@sha256:474f49c476d6742e1387d08971fb23f4bdbdf547c753838522e0c1a5cf07f044
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

### `solr:9.9.0` - linux; amd64

```console
$ docker pull solr@sha256:1184999572da4718bf4e8be7b1859289ff387ffe3dcfb0107d3929c6f013d437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.1 MB (483139769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea57e9b266756a844fdc234b8910f751bef4b524add8727825ca78355d1a9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efb96dabddfc76bb255f2062ea58cc0d71a35402242455e6ff541f2dd8c6e`  
		Last Modified: Thu, 02 Oct 2025 06:14:54 GMT  
		Size: 16.2 MB (16150246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9d91201f400dafb912bd4f1706e04991b2937d459b71d1c80ebf821ecb75be`  
		Last Modified: Thu, 02 Oct 2025 05:02:17 GMT  
		Size: 47.0 MB (46986074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b76b382631799417a3c67471e880b5248f8398eeee30b9bfc9903c52f0c211`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601f2c23751f6ef5043f76650593a141fb9eeb8fb9ae70269595b12d1e5d8069`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54670d52ce1ad1505f827a28103fac576dc41cafb17e3704445858e67b147594`  
		Last Modified: Thu, 02 Oct 2025 09:36:02 GMT  
		Size: 388.8 MB (388830900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42669950ac1eec3a3953cee523f879853b7ade662979c466537f17976ef5ff0`  
		Last Modified: Thu, 02 Oct 2025 08:42:03 GMT  
		Size: 4.3 KB (4269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc644d8725a8ee159d760bf0b9389878aab0b88c4d958c23d742b4045f8761f`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41738644700c2ab2034dc9f4d520475e54278b85e568d9c7948363704a9487ae`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbbdf3587600faed33fdeb339aea876fe2784d4dbee3982ff1e22366985ed8a`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 1.6 MB (1617893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0` - unknown; unknown

```console
$ docker pull solr@sha256:73f8ef8e83c58ba1fb838610d4a99dcb8543e66828c6e972479f98a7909f0961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b988352289ac947823ae3eda97c65c3a6364ea02e3a3ac26f224ee1fd3c92853`

```dockerfile
```

-	Layers:
	-	`sha256:528a057e5dfbd7ad7172b60ff9a05a1a2825360b93c957ab9f2c0f9fe5402478`  
		Last Modified: Thu, 02 Oct 2025 10:58:20 GMT  
		Size: 4.6 MB (4550103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59c7f2a3df1c872476f88d4c415435258385e39cfb64f974c3bd1a476fbc04f`  
		Last Modified: Thu, 02 Oct 2025 10:58:21 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:76008e266b6183562a31f7b5ce1e7e14950a381c27d90a73e4ff9947d08ed732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480253946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59914a9f4b174caa111a25a55b16070ab7ec7e134d02d737cb6594670c217724`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b48ce0fa3fcfd3966ce55ee451545585dfe3da5e248e92a6d1b0d45f55dc27`  
		Last Modified: Thu, 02 Oct 2025 01:18:01 GMT  
		Size: 16.1 MB (16065703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18baf420dc060a02e6b4427a9b58a8f8aec826c4c91e595be84693728113140`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 46.5 MB (46481588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04407eaefaf8d0ee0effa63673aad83ebb9283b7cfba66253ecc311d67aaf558`  
		Last Modified: Thu, 02 Oct 2025 01:18:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ab097c3dabb4e6cecd9895cc9bdbc4e0acef286bb1eef5f6a5780116b38ae8`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d9f89ac2a48472c772d1724870239dbbe58e1831b6982925883c4eb5a773c0`  
		Last Modified: Thu, 02 Oct 2025 05:01:41 GMT  
		Size: 388.8 MB (388830902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00ef8b83fb1422aad1310291d9e24da5bdbd69dab1234af94bfea6ccdbaf90`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 4.3 KB (4301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fa610fc85471289f7d8c9921dc9e39a307cfa4d31fb6ed754684b5071edc26`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2568d7c7aae7622652bbc8fb0acc028eec079af2c6c4bf1d5a1330147c8dae`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 10.9 KB (10889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d2bce847a1b4487b6a09b21a11ade8476d5fa02181c6169d2380c3553e6c15`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 1.5 MB (1474774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0` - unknown; unknown

```console
$ docker pull solr@sha256:05d1f296e984ee0fe899ec5f73d5d846b36544971793a3b4c85d2fee5df7ef8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2378bfa7c4001aa91c0aa587a1047953171af2876f52b1dc55c55e581c2b96d`

```dockerfile
```

-	Layers:
	-	`sha256:e69fef67f0e76642968f385e922a70e5627489ef4bec51db1f77c5cbe54fa899`  
		Last Modified: Thu, 02 Oct 2025 04:58:28 GMT  
		Size: 4.5 MB (4549779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d37421d08aeec678727598bcd7c47fded4b54ab6393d6522b74b07ee8f35b8a6`  
		Last Modified: Thu, 02 Oct 2025 04:58:29 GMT  
		Size: 34.5 KB (34499 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0` - linux; ppc64le

```console
$ docker pull solr@sha256:c5753e77f4d02393765ceb113e311d088692a76791262b8f627cb1efac073d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.4 MB (489376497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157b67b6d9a319fae3a9d1d65bd0f426f119492ea950fa98209a6f0d02eb741c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe9254f7488179acffc6d4fe22874ac523780d1d1c9e70f598251442a3a8b7`  
		Last Modified: Thu, 02 Oct 2025 01:19:02 GMT  
		Size: 17.6 MB (17623675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c1dbab248f00072fac2b930ca77ed36f86048d5c4ec6feded0a8b7d6e36fd5`  
		Last Modified: Thu, 02 Oct 2025 01:33:00 GMT  
		Size: 46.8 MB (46826196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb99ff66ae304853960cda05446ebfd53e06f9036817bfcce2a88d57080869`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18cee3e6a628a50b6b6c6cc9804934404caac93f9c48f980c4e76681b47ebaf`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd38542341ce5da818bde1ebcb35e3625cf5e5b3312e806f5b11ba26c346a037`  
		Last Modified: Thu, 02 Oct 2025 07:11:56 GMT  
		Size: 388.8 MB (388831196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5041e5151337bb4f73668771edcc87dd70ff91e32155e7ee588b9fb2110841`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 4.3 KB (4267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbd91c75744142e8853f5e72f7f8f6bd3e53bb623f6fb4eae85466d38cd8a63`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e7aa2b6e76b871e786eb1ff57068eb465a3462870157ad69822689a6dfbbef`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415a413a4beea68bb4bf4535fd715fba90efba1c77abb8451ed9d51f18f22966`  
		Last Modified: Thu, 02 Oct 2025 06:47:13 GMT  
		Size: 1.6 MB (1630798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0` - unknown; unknown

```console
$ docker pull solr@sha256:5a2e5812778db0e7cb7b2788461e40dc5a54c8f8ab0cd09bdbe18ba42c1e0e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4588543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c168518cec35715fcb55d9a2393852fa3503573b702a8b656f37ed984f50865`

```dockerfile
```

-	Layers:
	-	`sha256:3d94514b374af5cbb9882ae157e356a61e74b8fc0ba8c5a9804f20928ac3dc9f`  
		Last Modified: Thu, 02 Oct 2025 07:58:24 GMT  
		Size: 4.6 MB (4554156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c6fe8c06d890c6058fb6ef4a43fefac31359979226130c891945e9cfb66d1d6`  
		Last Modified: Thu, 02 Oct 2025 07:58:25 GMT  
		Size: 34.4 KB (34387 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0` - linux; s390x

```console
$ docker pull solr@sha256:4c8e8390f38cc37156a512e7d977a1332042288fcd45286a60bdf1bdcdc27d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.5 MB (478534361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8df0009a7b141720dc3da6a340a8c6929ba3c6b8c0c7665d11c03e7dcfb61c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa057040468c4605ce5fb8ed262a9f172e925905b6ab54206a3c9fdecdb0775`  
		Last Modified: Thu, 02 Oct 2025 01:15:00 GMT  
		Size: 16.1 MB (16149615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b3cd93688739505fe8d2dd5931e3a33e46e0acaab94ebfe0a47f8e03fe7dbc`  
		Last Modified: Thu, 02 Oct 2025 01:20:10 GMT  
		Size: 44.0 MB (43973850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930f491eada45b104be02c555f05bb5f1aeeae21bb31ec5cd9bf1bcbe668d40`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae07338a40ce04ab829bc61ace554a85c92ee69a26d5001a62e8c9225b168c2`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f162d79fc0a8ad37058ee42f04c8a498358fd687b78d2c0861457159f8eb0bb`  
		Last Modified: Thu, 02 Oct 2025 04:13:47 GMT  
		Size: 388.8 MB (388830690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc427c37362e4ee092e4a327b870c230aec5973af589d4330edf440b5d6838`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e5c9013b1608aec7c7166c654c750b2bbf85c3bbfb0a64d08f18dd86d5168c`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26595036f47876da19cddd6060d42f7c83df63863fa9e725ac751f720b05187`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84bf63c653c481c26bd587d9850da365184173186401b73b10b810ac1f56888`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 1.6 MB (1558919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0` - unknown; unknown

```console
$ docker pull solr@sha256:de9f24cb8ee2153e55645a59ebf93c02c0df8704860093c82b5e5ae2b20b9be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4586034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3b49a154be60f532f8cb3d3b4513912549ccd7d40536e6d5cecbfa37167eec`

```dockerfile
```

-	Layers:
	-	`sha256:99c3b6c6f287f5bb7e6d750e6c3dfc7e7a4ccee7e7cf1281f1e2f9b9ff9d0c8a`  
		Last Modified: Thu, 02 Oct 2025 04:58:37 GMT  
		Size: 4.6 MB (4551699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc091fcecc073b841f0edba7541fd1ab9b237427264ec153916badef8b26c08`  
		Last Modified: Thu, 02 Oct 2025 04:58:38 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.9.0-slim`

```console
$ docker pull solr@sha256:bd326b59064e9b2656efb8419f539cfc342e28a6e854a2fa86558bfb2e4becfb
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

### `solr:9.9.0-slim` - linux; amd64

```console
$ docker pull solr@sha256:2cf7da27570699186755c431c4f2e3ee18fbdc7d51e11702db3fd8b04cb9b386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159927336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7677515e900be3af5f717dc4035f85f923a1391d84dd56e09c6d95bfdfcae3cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efb96dabddfc76bb255f2062ea58cc0d71a35402242455e6ff541f2dd8c6e`  
		Last Modified: Thu, 02 Oct 2025 06:14:54 GMT  
		Size: 16.2 MB (16150246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9d91201f400dafb912bd4f1706e04991b2937d459b71d1c80ebf821ecb75be`  
		Last Modified: Thu, 02 Oct 2025 05:02:17 GMT  
		Size: 47.0 MB (46986074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b76b382631799417a3c67471e880b5248f8398eeee30b9bfc9903c52f0c211`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601f2c23751f6ef5043f76650593a141fb9eeb8fb9ae70269595b12d1e5d8069`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa4a9e7abd268d5d88689727a7ba11c57d9c08a4dccd1acad3dc4155abe1b9`  
		Last Modified: Thu, 02 Oct 2025 09:36:08 GMT  
		Size: 65.6 MB (65618514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e391a4d786cdb41b082aa91aec9e7ae321e3cf0feaf41958ffb21c8d224dfbc`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 4.3 KB (4268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dbaa69c6b4c53d606802d3f525be0f9925439aef9863a73890e5d26e3eef0d`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb02c76f0d15e2b564efa8decdb24d6b6c0dfff01a0fb20360ae3fba452d20a`  
		Last Modified: Thu, 02 Oct 2025 09:33:31 GMT  
		Size: 10.8 KB (10806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5092229b9b7cd3851ddd78ca4f2da61a9a97c7bdfa35b05c6717805d74c0e61`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 1.6 MB (1617925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:a4c6f16a2557e28be000c602a6eb6a08ad541db9d4707bbed32bcc04e4b19b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3860b265b2e087fe2f02e87336c763cf38c732b03a3ec80556eac5a91190fc6`

```dockerfile
```

-	Layers:
	-	`sha256:f195b0b8cd59f58d2f18dffb2336d81d78af1201d867dabf0376cda44e83344e`  
		Last Modified: Thu, 02 Oct 2025 10:58:28 GMT  
		Size: 4.0 MB (3963114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf25511365a9506bf219e8a33e0a581d4e8a57ad7ad6d06cd7870512243f58e`  
		Last Modified: Thu, 02 Oct 2025 10:58:29 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:ca5895f18d242854ed8f75afef4839a79a5334ce237b3544263292f136726715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157041593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a264b8de12e72c8a23c28331a02e9316c59569dafeb78aab0173d44283f9c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b48ce0fa3fcfd3966ce55ee451545585dfe3da5e248e92a6d1b0d45f55dc27`  
		Last Modified: Thu, 02 Oct 2025 01:18:01 GMT  
		Size: 16.1 MB (16065703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18baf420dc060a02e6b4427a9b58a8f8aec826c4c91e595be84693728113140`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 46.5 MB (46481588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04407eaefaf8d0ee0effa63673aad83ebb9283b7cfba66253ecc311d67aaf558`  
		Last Modified: Thu, 02 Oct 2025 01:18:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ab097c3dabb4e6cecd9895cc9bdbc4e0acef286bb1eef5f6a5780116b38ae8`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1788c12a8a00486d15c57601dcf161a77ed5dea586cd478f62f940f2380e8a14`  
		Last Modified: Thu, 02 Oct 2025 02:28:00 GMT  
		Size: 65.6 MB (65618603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea20739a0dd6f84a5787bba3e627b5cb833a97a8048a0c5dd4294bfbeb28d79b`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afe6708e36ad5ef40d9fe52c0c5f4f04b986249c200ae0272d83fcbce50665b`  
		Last Modified: Thu, 02 Oct 2025 02:27:55 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9531714abba676aa977a548cc1cc705823e4215e79d2c263ef93c38eafd3592a`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6114d5516094d6860a79d02444d3e35d6e7fc7da0906cbdf7e583ed9505d72a3`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 1.5 MB (1474801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:cd2cef292d7887d14606562431c9cf3e4d71d94af62fab231cec0a84d1cda9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccf89bfeee10a7edd221eb6f0206bd691a60c409e9ba90b82c0bcd64e4f9e17`

```dockerfile
```

-	Layers:
	-	`sha256:6d7658bb916802c2a8190af6541fe275017b54987cad73b0886492b8b0dfe17b`  
		Last Modified: Thu, 02 Oct 2025 04:58:36 GMT  
		Size: 4.0 MB (3962790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd55b1955b2379919285a5f02b2489d57f9b52ca7f2a0a644eaeca7e95330aff`  
		Last Modified: Thu, 02 Oct 2025 04:58:37 GMT  
		Size: 34.6 KB (34561 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:93450a34e431e1f50f13ec39b6522a1b69736a54392d81e57c6979e97a7412c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166164111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da97ffcce00632f4ceaca536916f8a60f4d42464b4b320e4d1f03e07267c14d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe9254f7488179acffc6d4fe22874ac523780d1d1c9e70f598251442a3a8b7`  
		Last Modified: Thu, 02 Oct 2025 01:19:02 GMT  
		Size: 17.6 MB (17623675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c1dbab248f00072fac2b930ca77ed36f86048d5c4ec6feded0a8b7d6e36fd5`  
		Last Modified: Thu, 02 Oct 2025 01:33:00 GMT  
		Size: 46.8 MB (46826196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb99ff66ae304853960cda05446ebfd53e06f9036817bfcce2a88d57080869`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18cee3e6a628a50b6b6c6cc9804934404caac93f9c48f980c4e76681b47ebaf`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb467ce9858a45c79645d7c7a5ac0ee11357cdc9b65d566ee99005fb488724a3`  
		Last Modified: Thu, 02 Oct 2025 07:59:00 GMT  
		Size: 65.6 MB (65618910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d782a7ee53e95c1066111b7906abb56c7d79735460a79e0315b36186d2201b2`  
		Last Modified: Thu, 02 Oct 2025 07:21:04 GMT  
		Size: 4.3 KB (4265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f063ac5d6e50ceb728a48f391180a759f20ba997cbc0af712d05cc7d8930d8`  
		Last Modified: Thu, 02 Oct 2025 07:21:07 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6216d1919f03bf4d336a064c428b0b3edce673595fdd570b6551765452e977`  
		Last Modified: Thu, 02 Oct 2025 07:21:10 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f7df8f164dac94273e8f95276ab9afbd3e7f34939c9c3b262fe81a005a8903`  
		Last Modified: Thu, 02 Oct 2025 07:21:13 GMT  
		Size: 1.6 MB (1630787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:5c1db0532d66a16a686f12bcf4bea22e3bdd7c0a3aaa6976deb1a62473b18f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfcd6085af973ea1fbb3186cc151de649f6b82cd2072e74167c863a91cffcff`

```dockerfile
```

-	Layers:
	-	`sha256:0f00eee7e2d23b94ec71a38823b8532c9c1044840d9943ad7913c51f8405df04`  
		Last Modified: Thu, 02 Oct 2025 07:58:29 GMT  
		Size: 4.0 MB (3967167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24384ff2c1342941160401966e98a861dd83d613aacce1fd17754429dda32962`  
		Last Modified: Thu, 02 Oct 2025 07:58:29 GMT  
		Size: 34.5 KB (34450 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0-slim` - linux; s390x

```console
$ docker pull solr@sha256:81394debe7ef2b733de098e50bbc835592d6a1d45c5160af43416a2d37e11c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155321791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ade1748d587553ab347605082a9b4dfe72a269962b61bf4c7468ce6b7798e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa057040468c4605ce5fb8ed262a9f172e925905b6ab54206a3c9fdecdb0775`  
		Last Modified: Thu, 02 Oct 2025 01:15:00 GMT  
		Size: 16.1 MB (16149615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b3cd93688739505fe8d2dd5931e3a33e46e0acaab94ebfe0a47f8e03fe7dbc`  
		Last Modified: Thu, 02 Oct 2025 01:20:10 GMT  
		Size: 44.0 MB (43973850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930f491eada45b104be02c555f05bb5f1aeeae21bb31ec5cd9bf1bcbe668d40`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae07338a40ce04ab829bc61ace554a85c92ee69a26d5001a62e8c9225b168c2`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bb5ca63550de993646e21b3efe5ee741d92e1dbf1f44100d49f442d096a334`  
		Last Modified: Thu, 02 Oct 2025 03:39:06 GMT  
		Size: 65.6 MB (65618204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c96895d4a82cc44f5c3a6154bbca1e62cf6bbe1f19293d18a8e57d8e512c69`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8428320aa2a8ec906dd93c37135b8ff4435c6ea42f0a5ab42e2c8b54986761`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6895a57397abc92df039149f9065c63d69f084f0435bdde59e7652108c6b8e`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb6501a43479515a34b9ccd79cbb2373dd062269c16d81b8e22d6d096e85d12`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 1.6 MB (1558915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:b6a972c8f8ea32ef937956f282da3c68901d9a20bd88e76d75e3da929e8c4035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3999108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b65da4092443c8f9e823c8d8432352e4bea271186c2df5df5293018d1e6a96d`

```dockerfile
```

-	Layers:
	-	`sha256:5158a0663a0060bd3b0f0d8d41de42570ca67f685c7028749ddcd85010057b5e`  
		Last Modified: Thu, 02 Oct 2025 04:58:50 GMT  
		Size: 4.0 MB (3964710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7523b5ac7f5ef4ebde3f85a3a023772d50597f17e31843a8c564f3d947f16bac`  
		Last Modified: Thu, 02 Oct 2025 04:58:51 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:latest`

```console
$ docker pull solr@sha256:474f49c476d6742e1387d08971fb23f4bdbdf547c753838522e0c1a5cf07f044
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
$ docker pull solr@sha256:1184999572da4718bf4e8be7b1859289ff387ffe3dcfb0107d3929c6f013d437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.1 MB (483139769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea57e9b266756a844fdc234b8910f751bef4b524add8727825ca78355d1a9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efb96dabddfc76bb255f2062ea58cc0d71a35402242455e6ff541f2dd8c6e`  
		Last Modified: Thu, 02 Oct 2025 06:14:54 GMT  
		Size: 16.2 MB (16150246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9d91201f400dafb912bd4f1706e04991b2937d459b71d1c80ebf821ecb75be`  
		Last Modified: Thu, 02 Oct 2025 05:02:17 GMT  
		Size: 47.0 MB (46986074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b76b382631799417a3c67471e880b5248f8398eeee30b9bfc9903c52f0c211`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601f2c23751f6ef5043f76650593a141fb9eeb8fb9ae70269595b12d1e5d8069`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54670d52ce1ad1505f827a28103fac576dc41cafb17e3704445858e67b147594`  
		Last Modified: Thu, 02 Oct 2025 09:36:02 GMT  
		Size: 388.8 MB (388830900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42669950ac1eec3a3953cee523f879853b7ade662979c466537f17976ef5ff0`  
		Last Modified: Thu, 02 Oct 2025 08:42:03 GMT  
		Size: 4.3 KB (4269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc644d8725a8ee159d760bf0b9389878aab0b88c4d958c23d742b4045f8761f`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41738644700c2ab2034dc9f4d520475e54278b85e568d9c7948363704a9487ae`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbbdf3587600faed33fdeb339aea876fe2784d4dbee3982ff1e22366985ed8a`  
		Last Modified: Thu, 02 Oct 2025 08:42:04 GMT  
		Size: 1.6 MB (1617893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:73f8ef8e83c58ba1fb838610d4a99dcb8543e66828c6e972479f98a7909f0961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b988352289ac947823ae3eda97c65c3a6364ea02e3a3ac26f224ee1fd3c92853`

```dockerfile
```

-	Layers:
	-	`sha256:528a057e5dfbd7ad7172b60ff9a05a1a2825360b93c957ab9f2c0f9fe5402478`  
		Last Modified: Thu, 02 Oct 2025 10:58:20 GMT  
		Size: 4.6 MB (4550103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59c7f2a3df1c872476f88d4c415435258385e39cfb64f974c3bd1a476fbc04f`  
		Last Modified: Thu, 02 Oct 2025 10:58:21 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:76008e266b6183562a31f7b5ce1e7e14950a381c27d90a73e4ff9947d08ed732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480253946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59914a9f4b174caa111a25a55b16070ab7ec7e134d02d737cb6594670c217724`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b48ce0fa3fcfd3966ce55ee451545585dfe3da5e248e92a6d1b0d45f55dc27`  
		Last Modified: Thu, 02 Oct 2025 01:18:01 GMT  
		Size: 16.1 MB (16065703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18baf420dc060a02e6b4427a9b58a8f8aec826c4c91e595be84693728113140`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 46.5 MB (46481588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04407eaefaf8d0ee0effa63673aad83ebb9283b7cfba66253ecc311d67aaf558`  
		Last Modified: Thu, 02 Oct 2025 01:18:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ab097c3dabb4e6cecd9895cc9bdbc4e0acef286bb1eef5f6a5780116b38ae8`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d9f89ac2a48472c772d1724870239dbbe58e1831b6982925883c4eb5a773c0`  
		Last Modified: Thu, 02 Oct 2025 05:01:41 GMT  
		Size: 388.8 MB (388830902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00ef8b83fb1422aad1310291d9e24da5bdbd69dab1234af94bfea6ccdbaf90`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 4.3 KB (4301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fa610fc85471289f7d8c9921dc9e39a307cfa4d31fb6ed754684b5071edc26`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2568d7c7aae7622652bbc8fb0acc028eec079af2c6c4bf1d5a1330147c8dae`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 10.9 KB (10889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d2bce847a1b4487b6a09b21a11ade8476d5fa02181c6169d2380c3553e6c15`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 1.5 MB (1474774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:05d1f296e984ee0fe899ec5f73d5d846b36544971793a3b4c85d2fee5df7ef8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2378bfa7c4001aa91c0aa587a1047953171af2876f52b1dc55c55e581c2b96d`

```dockerfile
```

-	Layers:
	-	`sha256:e69fef67f0e76642968f385e922a70e5627489ef4bec51db1f77c5cbe54fa899`  
		Last Modified: Thu, 02 Oct 2025 04:58:28 GMT  
		Size: 4.5 MB (4549779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d37421d08aeec678727598bcd7c47fded4b54ab6393d6522b74b07ee8f35b8a6`  
		Last Modified: Thu, 02 Oct 2025 04:58:29 GMT  
		Size: 34.5 KB (34499 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:c5753e77f4d02393765ceb113e311d088692a76791262b8f627cb1efac073d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.4 MB (489376497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157b67b6d9a319fae3a9d1d65bd0f426f119492ea950fa98209a6f0d02eb741c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe9254f7488179acffc6d4fe22874ac523780d1d1c9e70f598251442a3a8b7`  
		Last Modified: Thu, 02 Oct 2025 01:19:02 GMT  
		Size: 17.6 MB (17623675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c1dbab248f00072fac2b930ca77ed36f86048d5c4ec6feded0a8b7d6e36fd5`  
		Last Modified: Thu, 02 Oct 2025 01:33:00 GMT  
		Size: 46.8 MB (46826196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb99ff66ae304853960cda05446ebfd53e06f9036817bfcce2a88d57080869`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18cee3e6a628a50b6b6c6cc9804934404caac93f9c48f980c4e76681b47ebaf`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd38542341ce5da818bde1ebcb35e3625cf5e5b3312e806f5b11ba26c346a037`  
		Last Modified: Thu, 02 Oct 2025 07:11:56 GMT  
		Size: 388.8 MB (388831196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5041e5151337bb4f73668771edcc87dd70ff91e32155e7ee588b9fb2110841`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 4.3 KB (4267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbd91c75744142e8853f5e72f7f8f6bd3e53bb623f6fb4eae85466d38cd8a63`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e7aa2b6e76b871e786eb1ff57068eb465a3462870157ad69822689a6dfbbef`  
		Last Modified: Thu, 02 Oct 2025 06:47:12 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415a413a4beea68bb4bf4535fd715fba90efba1c77abb8451ed9d51f18f22966`  
		Last Modified: Thu, 02 Oct 2025 06:47:13 GMT  
		Size: 1.6 MB (1630798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:5a2e5812778db0e7cb7b2788461e40dc5a54c8f8ab0cd09bdbe18ba42c1e0e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4588543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c168518cec35715fcb55d9a2393852fa3503573b702a8b656f37ed984f50865`

```dockerfile
```

-	Layers:
	-	`sha256:3d94514b374af5cbb9882ae157e356a61e74b8fc0ba8c5a9804f20928ac3dc9f`  
		Last Modified: Thu, 02 Oct 2025 07:58:24 GMT  
		Size: 4.6 MB (4554156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c6fe8c06d890c6058fb6ef4a43fefac31359979226130c891945e9cfb66d1d6`  
		Last Modified: Thu, 02 Oct 2025 07:58:25 GMT  
		Size: 34.4 KB (34387 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:4c8e8390f38cc37156a512e7d977a1332042288fcd45286a60bdf1bdcdc27d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.5 MB (478534361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8df0009a7b141720dc3da6a340a8c6929ba3c6b8c0c7665d11c03e7dcfb61c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa057040468c4605ce5fb8ed262a9f172e925905b6ab54206a3c9fdecdb0775`  
		Last Modified: Thu, 02 Oct 2025 01:15:00 GMT  
		Size: 16.1 MB (16149615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b3cd93688739505fe8d2dd5931e3a33e46e0acaab94ebfe0a47f8e03fe7dbc`  
		Last Modified: Thu, 02 Oct 2025 01:20:10 GMT  
		Size: 44.0 MB (43973850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930f491eada45b104be02c555f05bb5f1aeeae21bb31ec5cd9bf1bcbe668d40`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae07338a40ce04ab829bc61ace554a85c92ee69a26d5001a62e8c9225b168c2`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f162d79fc0a8ad37058ee42f04c8a498358fd687b78d2c0861457159f8eb0bb`  
		Last Modified: Thu, 02 Oct 2025 04:13:47 GMT  
		Size: 388.8 MB (388830690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc427c37362e4ee092e4a327b870c230aec5973af589d4330edf440b5d6838`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e5c9013b1608aec7c7166c654c750b2bbf85c3bbfb0a64d08f18dd86d5168c`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26595036f47876da19cddd6060d42f7c83df63863fa9e725ac751f720b05187`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84bf63c653c481c26bd587d9850da365184173186401b73b10b810ac1f56888`  
		Last Modified: Thu, 02 Oct 2025 03:38:11 GMT  
		Size: 1.6 MB (1558919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:de9f24cb8ee2153e55645a59ebf93c02c0df8704860093c82b5e5ae2b20b9be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4586034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3b49a154be60f532f8cb3d3b4513912549ccd7d40536e6d5cecbfa37167eec`

```dockerfile
```

-	Layers:
	-	`sha256:99c3b6c6f287f5bb7e6d750e6c3dfc7e7a4ccee7e7cf1281f1e2f9b9ff9d0c8a`  
		Last Modified: Thu, 02 Oct 2025 04:58:37 GMT  
		Size: 4.6 MB (4551699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc091fcecc073b841f0edba7541fd1ab9b237427264ec153916badef8b26c08`  
		Last Modified: Thu, 02 Oct 2025 04:58:38 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:slim`

```console
$ docker pull solr@sha256:bd326b59064e9b2656efb8419f539cfc342e28a6e854a2fa86558bfb2e4becfb
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
$ docker pull solr@sha256:2cf7da27570699186755c431c4f2e3ee18fbdc7d51e11702db3fd8b04cb9b386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159927336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7677515e900be3af5f717dc4035f85f923a1391d84dd56e09c6d95bfdfcae3cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efb96dabddfc76bb255f2062ea58cc0d71a35402242455e6ff541f2dd8c6e`  
		Last Modified: Thu, 02 Oct 2025 06:14:54 GMT  
		Size: 16.2 MB (16150246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9d91201f400dafb912bd4f1706e04991b2937d459b71d1c80ebf821ecb75be`  
		Last Modified: Thu, 02 Oct 2025 05:02:17 GMT  
		Size: 47.0 MB (46986074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b76b382631799417a3c67471e880b5248f8398eeee30b9bfc9903c52f0c211`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601f2c23751f6ef5043f76650593a141fb9eeb8fb9ae70269595b12d1e5d8069`  
		Last Modified: Thu, 02 Oct 2025 05:02:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa4a9e7abd268d5d88689727a7ba11c57d9c08a4dccd1acad3dc4155abe1b9`  
		Last Modified: Thu, 02 Oct 2025 09:36:08 GMT  
		Size: 65.6 MB (65618514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e391a4d786cdb41b082aa91aec9e7ae321e3cf0feaf41958ffb21c8d224dfbc`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 4.3 KB (4268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dbaa69c6b4c53d606802d3f525be0f9925439aef9863a73890e5d26e3eef0d`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb02c76f0d15e2b564efa8decdb24d6b6c0dfff01a0fb20360ae3fba452d20a`  
		Last Modified: Thu, 02 Oct 2025 09:33:31 GMT  
		Size: 10.8 KB (10806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5092229b9b7cd3851ddd78ca4f2da61a9a97c7bdfa35b05c6717805d74c0e61`  
		Last Modified: Thu, 02 Oct 2025 09:33:30 GMT  
		Size: 1.6 MB (1617925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:a4c6f16a2557e28be000c602a6eb6a08ad541db9d4707bbed32bcc04e4b19b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3860b265b2e087fe2f02e87336c763cf38c732b03a3ec80556eac5a91190fc6`

```dockerfile
```

-	Layers:
	-	`sha256:f195b0b8cd59f58d2f18dffb2336d81d78af1201d867dabf0376cda44e83344e`  
		Last Modified: Thu, 02 Oct 2025 10:58:28 GMT  
		Size: 4.0 MB (3963114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf25511365a9506bf219e8a33e0a581d4e8a57ad7ad6d06cd7870512243f58e`  
		Last Modified: Thu, 02 Oct 2025 10:58:29 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:ca5895f18d242854ed8f75afef4839a79a5334ce237b3544263292f136726715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157041593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a264b8de12e72c8a23c28331a02e9316c59569dafeb78aab0173d44283f9c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b48ce0fa3fcfd3966ce55ee451545585dfe3da5e248e92a6d1b0d45f55dc27`  
		Last Modified: Thu, 02 Oct 2025 01:18:01 GMT  
		Size: 16.1 MB (16065703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18baf420dc060a02e6b4427a9b58a8f8aec826c4c91e595be84693728113140`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 46.5 MB (46481588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04407eaefaf8d0ee0effa63673aad83ebb9283b7cfba66253ecc311d67aaf558`  
		Last Modified: Thu, 02 Oct 2025 01:18:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ab097c3dabb4e6cecd9895cc9bdbc4e0acef286bb1eef5f6a5780116b38ae8`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1788c12a8a00486d15c57601dcf161a77ed5dea586cd478f62f940f2380e8a14`  
		Last Modified: Thu, 02 Oct 2025 02:28:00 GMT  
		Size: 65.6 MB (65618603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea20739a0dd6f84a5787bba3e627b5cb833a97a8048a0c5dd4294bfbeb28d79b`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afe6708e36ad5ef40d9fe52c0c5f4f04b986249c200ae0272d83fcbce50665b`  
		Last Modified: Thu, 02 Oct 2025 02:27:55 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9531714abba676aa977a548cc1cc705823e4215e79d2c263ef93c38eafd3592a`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6114d5516094d6860a79d02444d3e35d6e7fc7da0906cbdf7e583ed9505d72a3`  
		Last Modified: Thu, 02 Oct 2025 02:27:56 GMT  
		Size: 1.5 MB (1474801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:cd2cef292d7887d14606562431c9cf3e4d71d94af62fab231cec0a84d1cda9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccf89bfeee10a7edd221eb6f0206bd691a60c409e9ba90b82c0bcd64e4f9e17`

```dockerfile
```

-	Layers:
	-	`sha256:6d7658bb916802c2a8190af6541fe275017b54987cad73b0886492b8b0dfe17b`  
		Last Modified: Thu, 02 Oct 2025 04:58:36 GMT  
		Size: 4.0 MB (3962790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd55b1955b2379919285a5f02b2489d57f9b52ca7f2a0a644eaeca7e95330aff`  
		Last Modified: Thu, 02 Oct 2025 04:58:37 GMT  
		Size: 34.6 KB (34561 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:93450a34e431e1f50f13ec39b6522a1b69736a54392d81e57c6979e97a7412c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166164111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da97ffcce00632f4ceaca536916f8a60f4d42464b4b320e4d1f03e07267c14d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe9254f7488179acffc6d4fe22874ac523780d1d1c9e70f598251442a3a8b7`  
		Last Modified: Thu, 02 Oct 2025 01:19:02 GMT  
		Size: 17.6 MB (17623675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c1dbab248f00072fac2b930ca77ed36f86048d5c4ec6feded0a8b7d6e36fd5`  
		Last Modified: Thu, 02 Oct 2025 01:33:00 GMT  
		Size: 46.8 MB (46826196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb99ff66ae304853960cda05446ebfd53e06f9036817bfcce2a88d57080869`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18cee3e6a628a50b6b6c6cc9804934404caac93f9c48f980c4e76681b47ebaf`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb467ce9858a45c79645d7c7a5ac0ee11357cdc9b65d566ee99005fb488724a3`  
		Last Modified: Thu, 02 Oct 2025 07:59:00 GMT  
		Size: 65.6 MB (65618910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d782a7ee53e95c1066111b7906abb56c7d79735460a79e0315b36186d2201b2`  
		Last Modified: Thu, 02 Oct 2025 07:21:04 GMT  
		Size: 4.3 KB (4265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f063ac5d6e50ceb728a48f391180a759f20ba997cbc0af712d05cc7d8930d8`  
		Last Modified: Thu, 02 Oct 2025 07:21:07 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6216d1919f03bf4d336a064c428b0b3edce673595fdd570b6551765452e977`  
		Last Modified: Thu, 02 Oct 2025 07:21:10 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f7df8f164dac94273e8f95276ab9afbd3e7f34939c9c3b262fe81a005a8903`  
		Last Modified: Thu, 02 Oct 2025 07:21:13 GMT  
		Size: 1.6 MB (1630787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:5c1db0532d66a16a686f12bcf4bea22e3bdd7c0a3aaa6976deb1a62473b18f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfcd6085af973ea1fbb3186cc151de649f6b82cd2072e74167c863a91cffcff`

```dockerfile
```

-	Layers:
	-	`sha256:0f00eee7e2d23b94ec71a38823b8532c9c1044840d9943ad7913c51f8405df04`  
		Last Modified: Thu, 02 Oct 2025 07:58:29 GMT  
		Size: 4.0 MB (3967167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24384ff2c1342941160401966e98a861dd83d613aacce1fd17754429dda32962`  
		Last Modified: Thu, 02 Oct 2025 07:58:29 GMT  
		Size: 34.5 KB (34450 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:81394debe7ef2b733de098e50bbc835592d6a1d45c5160af43416a2d37e11c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155321791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ade1748d587553ab347605082a9b4dfe72a269962b61bf4c7468ce6b7798e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 24 Jul 2025 18:14:50 GMT
ARG RELEASE
# Thu, 24 Jul 2025 18:14:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 24 Jul 2025 18:14:50 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["/bin/bash"]
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Jul 2025 18:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 18:14:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DIST=-slim
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 24 Jul 2025 18:14:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 24 Jul 2025 18:14:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jul 2025 18:14:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 24 Jul 2025 18:14:50 GMT
VOLUME [/var/solr]
# Thu, 24 Jul 2025 18:14:50 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 24 Jul 2025 18:14:50 GMT
WORKDIR /opt/solr
# Thu, 24 Jul 2025 18:14:50 GMT
USER 8983
# Thu, 24 Jul 2025 18:14:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jul 2025 18:14:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa057040468c4605ce5fb8ed262a9f172e925905b6ab54206a3c9fdecdb0775`  
		Last Modified: Thu, 02 Oct 2025 01:15:00 GMT  
		Size: 16.1 MB (16149615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b3cd93688739505fe8d2dd5931e3a33e46e0acaab94ebfe0a47f8e03fe7dbc`  
		Last Modified: Thu, 02 Oct 2025 01:20:10 GMT  
		Size: 44.0 MB (43973850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930f491eada45b104be02c555f05bb5f1aeeae21bb31ec5cd9bf1bcbe668d40`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae07338a40ce04ab829bc61ace554a85c92ee69a26d5001a62e8c9225b168c2`  
		Last Modified: Thu, 02 Oct 2025 01:20:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bb5ca63550de993646e21b3efe5ee741d92e1dbf1f44100d49f442d096a334`  
		Last Modified: Thu, 02 Oct 2025 03:39:06 GMT  
		Size: 65.6 MB (65618204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c96895d4a82cc44f5c3a6154bbca1e62cf6bbe1f19293d18a8e57d8e512c69`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8428320aa2a8ec906dd93c37135b8ff4435c6ea42f0a5ab42e2c8b54986761`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6895a57397abc92df039149f9065c63d69f084f0435bdde59e7652108c6b8e`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb6501a43479515a34b9ccd79cbb2373dd062269c16d81b8e22d6d096e85d12`  
		Last Modified: Thu, 02 Oct 2025 03:39:03 GMT  
		Size: 1.6 MB (1558915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:b6a972c8f8ea32ef937956f282da3c68901d9a20bd88e76d75e3da929e8c4035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3999108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b65da4092443c8f9e823c8d8432352e4bea271186c2df5df5293018d1e6a96d`

```dockerfile
```

-	Layers:
	-	`sha256:5158a0663a0060bd3b0f0d8d41de42570ca67f685c7028749ddcd85010057b5e`  
		Last Modified: Thu, 02 Oct 2025 04:58:50 GMT  
		Size: 4.0 MB (3964710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7523b5ac7f5ef4ebde3f85a3a023772d50597f17e31843a8c564f3d947f16bac`  
		Last Modified: Thu, 02 Oct 2025 04:58:51 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json
