## `solr:latest`

```console
$ docker pull solr@sha256:4f64dcc25e552945d748c54377697c8734afc46347387348cd6a7290bb23e84e
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
$ docker pull solr@sha256:a9f21feef371cc816c28f4e88b60b1682c6938c1890254969d499c5f147efa80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483373877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5634c6cf8a10466c4d2e2eb2ba98f8228844705064a4adec6bd1dc9619e04c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Nov 2025 18:40:28 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 06 Nov 2025 18:40:28 GMT
ARG SOLR_DIST=
# Thu, 06 Nov 2025 18:40:28 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Thu, 06 Nov 2025 18:40:28 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 06 Nov 2025 18:40:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 06 Nov 2025 18:40:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 06 Nov 2025 18:40:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 06 Nov 2025 18:40:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 06 Nov 2025 18:40:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 06 Nov 2025 18:40:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 06 Nov 2025 18:40:36 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 06 Nov 2025 18:40:36 GMT
VOLUME [/var/solr]
# Thu, 06 Nov 2025 18:40:36 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 06 Nov 2025 18:40:36 GMT
WORKDIR /opt/solr
# Thu, 06 Nov 2025 18:40:36 GMT
USER 8983
# Thu, 06 Nov 2025 18:40:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Nov 2025 18:40:36 GMT
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
	-	`sha256:59f90e7f1db184297a9b53c3fd733795c3de3e21f0ddd8b822061be922d39640`  
		Last Modified: Thu, 06 Nov 2025 20:59:44 GMT  
		Size: 389.1 MB (389065002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d5ce1cd6757b04805cf40ea0b568aef128e007dcbb73a17ae10ff6b09ca821`  
		Last Modified: Thu, 06 Nov 2025 18:41:16 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1979cbab9cc95849d5adc0e8a7b0f9130a97d8363a520f3bd974587505b2fb`  
		Last Modified: Thu, 06 Nov 2025 18:41:16 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b731f5daf81468b23bd316bfb83d87418b61de91408fda3f334b51539ecbd36`  
		Last Modified: Thu, 06 Nov 2025 18:41:17 GMT  
		Size: 10.9 KB (10884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838d9ab7abcad3e23100be8f6d3fc5aca8956a0fe33d75c76e302f3e640eb460`  
		Last Modified: Thu, 06 Nov 2025 18:41:16 GMT  
		Size: 1.6 MB (1617900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:d69c0d2942bf232df90d63582acb6be70298f82757a52365774261b910bd94c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1135c9bfcabd5e1472166876db7c72e3a091afc0af0df984d4387951d5a58a`

```dockerfile
```

-	Layers:
	-	`sha256:819e1dbccc5467f20625c0801ad0fc27a2ea48b12dc6a7c71db1c99a2123b665`  
		Last Modified: Thu, 06 Nov 2025 20:58:29 GMT  
		Size: 4.5 MB (4539697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5480c3c3a41e93425f8fba7b6312edbfaf33a6aba942191a27e56530c96553d4`  
		Last Modified: Thu, 06 Nov 2025 20:58:30 GMT  
		Size: 34.3 KB (34303 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:8c83d17b05eab0984a318893b83615a616352edbbe8fe0ea2079f2ef4d6fbf68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480488298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53357e5d7a057b6aa193d83b509194d073fba90a0b206f6e5f5a2f4c93e55e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Nov 2025 18:40:28 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 06 Nov 2025 18:40:28 GMT
ARG SOLR_DIST=
# Thu, 06 Nov 2025 18:40:28 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Thu, 06 Nov 2025 18:40:28 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 06 Nov 2025 18:40:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 06 Nov 2025 18:40:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 06 Nov 2025 18:40:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 06 Nov 2025 18:40:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 06 Nov 2025 18:40:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 06 Nov 2025 18:40:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 06 Nov 2025 18:40:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 06 Nov 2025 18:40:37 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 06 Nov 2025 18:40:37 GMT
VOLUME [/var/solr]
# Thu, 06 Nov 2025 18:40:37 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 06 Nov 2025 18:40:37 GMT
WORKDIR /opt/solr
# Thu, 06 Nov 2025 18:40:37 GMT
USER 8983
# Thu, 06 Nov 2025 18:40:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Nov 2025 18:40:37 GMT
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
	-	`sha256:26577de1db0db2d65eaacb8da29933cf9369e924c31821b70d4a424514c2a844`  
		Last Modified: Thu, 06 Nov 2025 21:00:45 GMT  
		Size: 389.1 MB (389065225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e844e742a21b5353b823ad7cc5a4ad071f164bdce57e39992fd07d7f84c224dd`  
		Last Modified: Thu, 06 Nov 2025 18:41:16 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1979cbab9cc95849d5adc0e8a7b0f9130a97d8363a520f3bd974587505b2fb`  
		Last Modified: Thu, 06 Nov 2025 18:41:16 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b731f5daf81468b23bd316bfb83d87418b61de91408fda3f334b51539ecbd36`  
		Last Modified: Thu, 06 Nov 2025 18:41:17 GMT  
		Size: 10.9 KB (10884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4647453fbf4c5f6990a667e3a2cd9c064346ef6b63bfd5bc457495984b1a5f2`  
		Last Modified: Thu, 06 Nov 2025 18:41:16 GMT  
		Size: 1.5 MB (1474805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:79c7d91255be822cc2f9fa64b06a8340bb7615c69aac2b5a7d268bd56aad2488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4573840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5cf82a563329cc17dda77de8eb8e39d05ee3c76fe2c985bddfda3c9ce0cd41`

```dockerfile
```

-	Layers:
	-	`sha256:ec8813b683ce59f5b65b044784f55a5253e60c7debec470694fb3f282681a1b8`  
		Last Modified: Thu, 06 Nov 2025 20:58:35 GMT  
		Size: 4.5 MB (4539373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea050cfc377423763de3cd47a90b8508e100fc4d1723bebf54229ce804f4393`  
		Last Modified: Thu, 06 Nov 2025 20:58:36 GMT  
		Size: 34.5 KB (34467 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:db082f3413e1b557f43424dd177e56f55e27ce2911647e0f30cfc560672af6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.6 MB (489610682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4763a49fcbc3b3ab8abfcfcb3d69c6fa866d6d5a0044b0b95ad05a203019109e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Nov 2025 18:39:32 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 06 Nov 2025 18:39:32 GMT
ARG SOLR_DIST=
# Thu, 06 Nov 2025 18:39:32 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Thu, 06 Nov 2025 18:39:32 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 06 Nov 2025 18:39:32 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 06 Nov 2025 18:39:32 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 06 Nov 2025 18:39:32 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 06 Nov 2025 18:39:32 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 06 Nov 2025 18:39:32 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 06 Nov 2025 18:39:32 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 06 Nov 2025 18:39:32 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 06 Nov 2025 18:39:32 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 06 Nov 2025 18:39:32 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 06 Nov 2025 18:39:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 06 Nov 2025 18:39:32 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 06 Nov 2025 18:39:34 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 06 Nov 2025 18:39:34 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 06 Nov 2025 18:39:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 06 Nov 2025 18:39:47 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 06 Nov 2025 18:39:47 GMT
VOLUME [/var/solr]
# Thu, 06 Nov 2025 18:39:47 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 06 Nov 2025 18:39:48 GMT
WORKDIR /opt/solr
# Thu, 06 Nov 2025 18:39:48 GMT
USER 8983
# Thu, 06 Nov 2025 18:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Nov 2025 18:39:48 GMT
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
	-	`sha256:492c31a6e1a50cefade4ac4db1ed516ae931a7ec6c1291a20b4385036c082a4a`  
		Last Modified: Thu, 06 Nov 2025 21:00:54 GMT  
		Size: 389.1 MB (389065366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895e53c5773787ae0d61f58c91921e5ffb2786bfdda514fd736cd6c18145a8e4`  
		Last Modified: Thu, 06 Nov 2025 18:40:57 GMT  
		Size: 4.3 KB (4280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014b727009a50c307c710c6cf4da18c363869efaed9e80a638afc03e3784bd2b`  
		Last Modified: Thu, 06 Nov 2025 18:40:57 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d65979ee2a9b7281f331a6270fd524d124410afb76a4aab2a75a74629fbb6c`  
		Last Modified: Thu, 06 Nov 2025 18:40:57 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdee2900b16ae1bf33e3ad642046a8a3f77bdfb5af165754f3db298ba9a5906`  
		Last Modified: Thu, 06 Nov 2025 18:40:57 GMT  
		Size: 1.6 MB (1630805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:b83e8fd955d1ad2135c1b5dfe48dd21a07cb80e9231b1a67d27692abff07150f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3aa6c3bc8a71cff8877e09dc3d9d1053f9231c2c256612f049e055cd1d8034`

```dockerfile
```

-	Layers:
	-	`sha256:dbc78a566ed5145498c4476d49632e2f5161aaef72da71c3d65702599b4acbf9`  
		Last Modified: Thu, 06 Nov 2025 20:58:41 GMT  
		Size: 4.5 MB (4543750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b59e6325ea25f9d23dbe873552eea8276774cd0cd07a075a5fec438de23c93`  
		Last Modified: Thu, 06 Nov 2025 20:58:42 GMT  
		Size: 34.4 KB (34355 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:eab7aff60d7ad29674a6053e09237894425e033159c5c8356dde5efa61f91a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.8 MB (478768408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4bcf4f225819d1848fa13bef5d118ce577b844e2ab10b9993bbcdb1b337e28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 06 Nov 2025 18:43:01 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 06 Nov 2025 18:43:01 GMT
ARG SOLR_DIST=
# Thu, 06 Nov 2025 18:43:01 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Thu, 06 Nov 2025 18:43:01 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 06 Nov 2025 18:43:01 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 06 Nov 2025 18:43:01 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 06 Nov 2025 18:43:01 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 06 Nov 2025 18:43:01 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 06 Nov 2025 18:43:01 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 06 Nov 2025 18:43:01 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 06 Nov 2025 18:43:01 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 06 Nov 2025 18:43:01 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 06 Nov 2025 18:43:01 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 06 Nov 2025 18:43:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 06 Nov 2025 18:43:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 06 Nov 2025 18:43:02 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 06 Nov 2025 18:43:03 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 06 Nov 2025 18:43:04 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 06 Nov 2025 18:43:10 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 06 Nov 2025 18:43:10 GMT
VOLUME [/var/solr]
# Thu, 06 Nov 2025 18:43:10 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 06 Nov 2025 18:43:10 GMT
WORKDIR /opt/solr
# Thu, 06 Nov 2025 18:43:10 GMT
USER 8983
# Thu, 06 Nov 2025 18:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Nov 2025 18:43:10 GMT
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
	-	`sha256:12ace1b79f4339f064b72c9f9d6a0c8829fa52ddb09728493e1ee8463f533c14`  
		Last Modified: Thu, 06 Nov 2025 21:01:31 GMT  
		Size: 389.1 MB (389064673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d825f72157449fe0e7a30d17e254deee56be7d2460e6d23e4027fae181d6af62`  
		Last Modified: Thu, 06 Nov 2025 18:44:30 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ea4a24e62f50dd4de619b2188a134cd8caba2e154bf425f25c2284f2de65f`  
		Last Modified: Thu, 06 Nov 2025 18:44:29 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d07850204e3d585db495d291320141417d5f7536f423ef26985291dee3190f`  
		Last Modified: Thu, 06 Nov 2025 18:44:29 GMT  
		Size: 10.9 KB (10892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590fc5ca2599a08ff8f665bf6711d17108dea778163332fe06ab68ba8f7a1d5`  
		Last Modified: Thu, 06 Nov 2025 18:44:30 GMT  
		Size: 1.6 MB (1558978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:72f52c4e0e5f83e58af0ac54d7c735a1d897e80dead347a4acf210fcd8ec1e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3325391d8c10fc7a5ec3b80ca7c7f10f99f08581fbb6e9ed0e42633d95e46396`

```dockerfile
```

-	Layers:
	-	`sha256:dc4447d39b6395182b1bbc03d2465f85003f79b2e72b88cd19627c960d705b4b`  
		Last Modified: Thu, 06 Nov 2025 20:58:50 GMT  
		Size: 4.5 MB (4541293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0b3f717ab12798b2be5b3a698282bd559d6318e1e1dd71071d5369d4177d7c5`  
		Last Modified: Thu, 06 Nov 2025 20:58:51 GMT  
		Size: 34.3 KB (34303 bytes)  
		MIME: application/vnd.in-toto+json
