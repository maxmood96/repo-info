## `solr:latest`

```console
$ docker pull solr@sha256:6cc61e53edc21b02fc0c86fc835c47061f57892b7ee01f189880000ac5602b16
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
$ docker pull solr@sha256:13e55ef0c8ab371de72da9d4e10830ceaab271c700f962f205714c6565d33687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.1 MB (483140437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8e75f2e3ca18aa44bb353fd8f85bf3e2e4d800142098952f6568a4b327426e`
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
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
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
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4670547904903aa6ce1e0f44562e27d151d319243c129b927d7c8515ecb66c07`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 16.2 MB (16150701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6898721bb2fa374368fa1fca91e491a141b71400687bfd48a9b159bb585eac3f`  
		Last Modified: Tue, 12 Aug 2025 17:24:40 GMT  
		Size: 47.0 MB (46986154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28927af8b0bd97d0ded0af3f583daa8c97528ed8958c8b7ff00e46565ab99ff`  
		Last Modified: Tue, 12 Aug 2025 17:24:35 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0543ed4affc53446f4fff9e9d582c304542c3ab4422b57c3c7af62779c6f84`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51019c5989095b01e0d24e45e99ce2ccea657501c457ba718a57c4222b786114`  
		Last Modified: Tue, 12 Aug 2025 20:00:07 GMT  
		Size: 388.8 MB (388830911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33420902c8ad922cca5fe8b1805b6de63be68f41790154174aed45e53f07c4ca`  
		Last Modified: Tue, 12 Aug 2025 18:02:16 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde75afa66f52de0dc64ce3ffd58c5dd5ac76d7f63bc613831b2b0327b7a1a78`  
		Last Modified: Tue, 12 Aug 2025 18:02:19 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757dfb6c1b95d6bd3b0bd5659596fbca3a9a238f74b769f97580c325607588dd`  
		Last Modified: Tue, 12 Aug 2025 18:02:22 GMT  
		Size: 10.9 KB (10888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bb0504dfc2d8dbc4b431e3f7ef2f16a6422f35c107e3d02207ab88cf2ec17c`  
		Last Modified: Tue, 12 Aug 2025 18:02:25 GMT  
		Size: 1.6 MB (1617838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:ef14e081c2ff3ca8a592af23f05c0cdef35eb7134ff3f6b92e5cdc689045d1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4650a01ed6efc90cb1ffa7cfe99ab609f2e34173e9c0b8631912c0d8d7212291`

```dockerfile
```

-	Layers:
	-	`sha256:52f14e8132b6c95478ef4892ffaa542ba6ff875f8d8f74b14fbb7f87d8969c84`  
		Last Modified: Tue, 12 Aug 2025 19:58:25 GMT  
		Size: 4.6 MB (4550087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92c14514d71f9595cc137a9c61c3fed0dafb9e21836c727a2d7c6048cf5506e1`  
		Last Modified: Tue, 12 Aug 2025 19:58:26 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:ef4abf2e49c2701fe0fdc30fb62b0ee38a5a5261d4d3c5a223965204098b8b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.2 MB (480228346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebeb2012e63c2f3996ab322f775ff298bd3011310e1b72a50cad2342baedccf`
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
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
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
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199b54d0379497df50867982d570bbd000004bfbf27017cd65c6f9eab785cc29`  
		Last Modified: Tue, 12 Aug 2025 18:37:19 GMT  
		Size: 46.5 MB (46481606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab45f69caeebdcfc0dcab7f12f318e6a8722b5101f1bf4043e99c86a6fbd7894`  
		Last Modified: Tue, 12 Aug 2025 18:37:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c74bc8d670c7b95bbe286937b0313a59d6ab9dd2b022249a7391012ef0a5da`  
		Last Modified: Tue, 12 Aug 2025 18:37:11 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6245460c8254d6bdddf32628bfbadfd4023da2ac43af6499ab636839eb71be6`  
		Last Modified: Wed, 13 Aug 2025 02:00:51 GMT  
		Size: 388.8 MB (388831059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f10e485e64128dffbc83b8c4f757042e4ecb71cefc74d4e64f035a0b1b2829f`  
		Last Modified: Wed, 13 Aug 2025 00:16:36 GMT  
		Size: 4.3 KB (4301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcef6a93db807300919aebf6d30f0c0f28978aac26ea8fa209bb602f9807206`  
		Last Modified: Wed, 13 Aug 2025 00:16:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e991633970bad6a69fa3fd14986cbdc62a93cde0f914e98f2fa26333451576e`  
		Last Modified: Wed, 13 Aug 2025 00:16:37 GMT  
		Size: 10.9 KB (10889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506a9da623f4e77dc204c74bd0e488acc99bc44bd0af1183f1ac4cd90b40430`  
		Last Modified: Wed, 13 Aug 2025 00:16:39 GMT  
		Size: 1.5 MB (1474821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:351749f27e06e782b04a55f164f79de970671c1cab4302af41ad771324df381f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89629cc9f0a5e4c07a6d588b45f1760ac34709056168292a6aa98ae4f0097885`

```dockerfile
```

-	Layers:
	-	`sha256:1c8183f7f6ca437eec9f9f0d989c5292d58b07a94bb5d06fa04128946f25f65d`  
		Last Modified: Wed, 13 Aug 2025 01:58:28 GMT  
		Size: 4.5 MB (4549763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a6eb46573810b70386283119d2f47661e97934cf52068d0a03b323b9a17448`  
		Last Modified: Wed, 13 Aug 2025 01:58:28 GMT  
		Size: 34.5 KB (34499 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:5c5c56a1f681e8d372dcba2ef22562f2da127d808658d8db828a4c7891cb6525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.4 MB (489373319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab572130b1f6e0732051b794c74dcc86a3d5a2f7d4d49263f8139956219201fc`
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
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
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
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c50520b2833414582dcec4e87265a64dd9e5acd7b3ec03378e25ec51523b3`  
		Last Modified: Tue, 12 Aug 2025 17:29:14 GMT  
		Size: 17.6 MB (17624214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb3c0b1536fe58f1d71970fd65e6541b64df3445d2eea58c017b922d91575d2`  
		Last Modified: Tue, 12 Aug 2025 19:56:46 GMT  
		Size: 46.8 MB (46826228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a22cfaf169bb1a9b3a30f0ff4c03599d0857880062e51c4f97a72acddb9b203`  
		Last Modified: Tue, 12 Aug 2025 18:22:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01334212dd4518b663caa14cbe8cddc3becdda25ad0d628881c8b62086970d9`  
		Last Modified: Tue, 12 Aug 2025 18:22:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681cf870bbcef19eddfa5177ca8d6c0ee12d2cac6f29624b746e4591bef7f44e`  
		Last Modified: Wed, 13 Aug 2025 06:46:36 GMT  
		Size: 388.8 MB (388831144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3aca027de1f9a02cd9bf32cb279a9eb0a379407ce2b2df4c1b8f4ea89eccdf0`  
		Last Modified: Wed, 13 Aug 2025 02:58:03 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc03f49d3752681ecb64a557e886f75b7b7cb2394e53931e69b9e97f65e71dea`  
		Last Modified: Wed, 13 Aug 2025 02:58:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1e39784e3d293c7fd8ed71aa583d516087850c6392a0381dc13a6b96258`  
		Last Modified: Wed, 13 Aug 2025 02:58:03 GMT  
		Size: 10.9 KB (10895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1368b1b7814ed3ce3895e14b94c0ba72e5721d0319ee019d95043da97a07af`  
		Last Modified: Wed, 13 Aug 2025 02:58:06 GMT  
		Size: 1.6 MB (1630735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:bb104b91f8ac2acca336b97569fda1b5a5127f3486bc46bf0a479803f018e722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4588527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff35121132802ae3375e66c78e613c4f21660d5bac77698cc0379cff1a61bea9`

```dockerfile
```

-	Layers:
	-	`sha256:9cc2b16d918348a0b742053009639ab4899caa4c99f1410b9d7a6e749d246e74`  
		Last Modified: Wed, 13 Aug 2025 04:58:34 GMT  
		Size: 4.6 MB (4554140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c573e9e16f7d4a6035d1d3f03a2a27072826bd54f2a96a8b4a3ec328d9620cf`  
		Last Modified: Wed, 13 Aug 2025 04:58:35 GMT  
		Size: 34.4 KB (34387 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:a3c5c06fe6ff5f63abbacfc2e06edfdf01dd679487533575478ecf77c4be64d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.5 MB (478534688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a94f1113630df9b14cddced44b2e03bc2d6d8e7eba786b4aa38e396f1fada7`
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
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
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
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ad5d5d8733c993217ed51c06da1f717784940dfd73d260506fcf34539cf5c7`  
		Last Modified: Tue, 12 Aug 2025 17:26:58 GMT  
		Size: 16.2 MB (16150057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3a6ef7bdcd30abb15d630d0ed47ea67815c291f7a3bf5b844731b8f7080ba5`  
		Last Modified: Tue, 12 Aug 2025 17:32:14 GMT  
		Size: 44.0 MB (43973854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64431dfe035d3b486eadae00fd28a970418a01518837b21a8c4bfc68bbd0776`  
		Last Modified: Tue, 12 Aug 2025 17:32:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933f71376c7ff52fa7a8da0684f951c61213dc6df3870edee38fa8865fd61665`  
		Last Modified: Tue, 12 Aug 2025 17:32:05 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40546b69982d8f5e1660ab3be6dc7eb794e7842218bf101e836341285f31ebd0`  
		Last Modified: Tue, 12 Aug 2025 21:00:38 GMT  
		Size: 388.8 MB (388830728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60227c9ca3d2c1edd4edbafeb5644d585250372d4ef68f77f457e952991ca740`  
		Last Modified: Tue, 12 Aug 2025 19:48:42 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654ff3d5b97e7baedbc0a80253a9cd4e45acffc867f42a7041a6a859c14bb93d`  
		Last Modified: Tue, 12 Aug 2025 19:48:42 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1e3d9836c855ae62fe379cf6d2550e8521e665965480477b8f07a8dce77842`  
		Last Modified: Tue, 12 Aug 2025 19:48:44 GMT  
		Size: 10.9 KB (10888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bba1b0173acc5d899cc66dd6826f54ebd44f9ba3638c675f3baff972ff748`  
		Last Modified: Tue, 12 Aug 2025 19:48:46 GMT  
		Size: 1.6 MB (1558950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:4c3cd17b69f0dfa9135fcc352e6cc10f9a1b9e2f5a09911bce974e2daabb6ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4586018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615c08b58de277393d36d7f074035fd50f011fe1ecba11c6fcdf0ff7ee42b9d9`

```dockerfile
```

-	Layers:
	-	`sha256:b61c6d42bf1cd8e6b2f0a2b0fdb8952ed0365648c1fc6e7b0ee6ea1ade96f8ed`  
		Last Modified: Tue, 12 Aug 2025 22:58:34 GMT  
		Size: 4.6 MB (4551683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebe20499ef80fa5a68eb9e2e0b068b0eb1399a8f6336bd9472ccf56310f47adc`  
		Last Modified: Tue, 12 Aug 2025 22:58:35 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json
