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
$ docker pull solr@sha256:afa60fe0ca0677c3498b86b2c75f01e2c1a99beddff31bc373774a95db6c10cd
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
$ docker pull solr@sha256:74b6fad9912f2025cd632186fe4fc70ed6171b3a0a32e6e17e663cce3fccbb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483442963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786008bff5ce8050e108cfcdd30e8d9e31b70d8fa6c447c1277b34df6b022697`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:31:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:56 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:56 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:56 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:56 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:56 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a37838215204e5eb9c43cc251f475f2f5e50406a4a528fe1a05b51a2b7c96b6`  
		Last Modified: Sat, 08 Nov 2025 20:59:51 GMT  
		Size: 389.1 MB (389064942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3de8b7c6486f9db8934d488c34db184555fc57b95dd653749ce77f760d9990`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 4.3 KB (4270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeb4c19a83cc1717b9d7e2013319389a3bdc3b758fb7524a20cb28cacea539b`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093065c795d8c45c6a275c11f09c9b52ab8bdfafc7286cf1d9f2bf6789ea4922`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb41ca25d99ba8892b89bca83d0c56cc69854923aae1a5dd77bc3bd83da9897`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 1.6 MB (1617898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:ff08adfa64fd27250c89895bba495152f113a76942223127db7fc59eca781456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa90777d1cd3907c02d1019d47614d737eedbae1117b1264ab4f898b6b0e25b`

```dockerfile
```

-	Layers:
	-	`sha256:b28da5559ae95a01eb11b4e497793b13d9d1e38a1f5a3cd4e48ba837e716b7ad`  
		Last Modified: Sat, 08 Nov 2025 20:58:27 GMT  
		Size: 4.5 MB (4539699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb424671e95073763f09ed69751c48c28eb447d7137d7f9fe5a2f9506db9b254`  
		Last Modified: Sat, 08 Nov 2025 20:58:28 GMT  
		Size: 34.3 KB (34308 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:aae405e78e12ef3c7fa14951ea986c700defe5c3c1ef9224dc3a35c60c0df66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480545650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8b8f0f630a23d7f3c5723b1c5148d0d48226391e18b014125c3e5ea5840983`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:30:54 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:04 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:04 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:04 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:04 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:04 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52f27b0761733cf2048af060549f8a5b7b5405c8e55aadc9a7052a004c9b1de`  
		Last Modified: Sat, 08 Nov 2025 21:01:02 GMT  
		Size: 389.1 MB (389065200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73923ba8ecddac21663225db5dddfc5ca2bda59ff16285f1d2eaf20f2b2cdffa`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da92b13d3c08fbfc56336ffd6f54de29d5cfa51dcfc4592ab2b06156d8ba843a`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b78509309dd28170dd8bb369388c9ad8957d65684139b54426f1eb84055279`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 10.9 KB (10886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51361437f6f8267d791897b7475d3b78a4295c8cef50113e1c5cd034dda51f77`  
		Last Modified: Sat, 08 Nov 2025 18:31:47 GMT  
		Size: 1.5 MB (1474848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:63ffced2c7b3c133b6bb255cd1548beb91f29679775965d61edb8154a276f5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4573847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d589682822ac2cfaa0af32b76a9e8cca70eb7705ce6e0b2050fdd4534389d`

```dockerfile
```

-	Layers:
	-	`sha256:21a993ccb9f7e7bcc6ec5f5e9075aee50576a953d434c2de7422c4c4b813a6c5`  
		Last Modified: Sat, 08 Nov 2025 20:58:33 GMT  
		Size: 4.5 MB (4539375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2918860ed4a844fb961be0a212329462606b08ebc5c0df18dc3e699a21212b5b`  
		Last Modified: Sat, 08 Nov 2025 20:58:34 GMT  
		Size: 34.5 KB (34472 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; ppc64le

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

### `solr:9` - unknown; unknown

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

### `solr:9` - linux; s390x

```console
$ docker pull solr@sha256:b5d4e2fbf3eccc4a377e782cf19b4f38d3e3ca2299253177192377ab56f02023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.8 MB (478825463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4610f5de76f4afe4313d8af77f36318398b6e6525d7d6d3dba27edfabfa3ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:50:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:50:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:50:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:50:36 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:50:36 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:50:41 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:50:41 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:50:41 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:50:42 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:50:42 GMT
USER 8983
# Sat, 08 Nov 2025 18:50:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:50:42 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3694c57a0c72262dc59f66e4b220aeca62a5558e36c9ce3d4374aa0b890291`  
		Last Modified: Sat, 08 Nov 2025 21:00:39 GMT  
		Size: 389.1 MB (389064782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9181a7b80fa4afee9fb9275a103a2012f274fdf5451ff0a1ec75e3fb3576d15`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bcdd71ac4320d5f4c8f430a2b5818ff8c53ff6924001e2a80fc38ddc7541c6`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6ca544c45c6093e36dc865e98ed86f586925ee1a56b464db9c86523f01fc0`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 10.9 KB (10888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b7fa825bca319dd389094237d9704ad65a1acd877141984d475643fec31142`  
		Last Modified: Sat, 08 Nov 2025 18:51:43 GMT  
		Size: 1.6 MB (1558972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:84f5c9d24bbf74ad1d8a93367e90eec64bdeea67aeef453b82c869fb298ff5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fd8481462e28078722361a6a654c11333b25ee3c1c36ff96c372eb77d19419`

```dockerfile
```

-	Layers:
	-	`sha256:9d82501c524367bfe9ac90b1f855a14425742551664c6f852a4085de2ade3ec0`  
		Last Modified: Sat, 08 Nov 2025 20:58:42 GMT  
		Size: 4.5 MB (4541295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c3069bcdc4c4a771f42e2c2333d16f234fd84daa6c2915f8ee664282a88635`  
		Last Modified: Sat, 08 Nov 2025 20:58:42 GMT  
		Size: 34.3 KB (34307 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9-slim`

```console
$ docker pull solr@sha256:e9e26ef53699a091c92a1936a2e74933bb19fd2fffb74c488415a62427274ae4
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
$ docker pull solr@sha256:72d1bd967a8e99c0a0272cd8616ca16b48e7e316e23eb0e1c1bd2b057f4d460c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160345009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7d1bcd8087cd5e87912c3e1efad6164a1e19a2a19889fe84f3aff6578d0e2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:31:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:55 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:55 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:55 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:55 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:55 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a9971b5b8ed4a21585204efd09f866feb175981eb3fdbe66aad7d810b47aea`  
		Last Modified: Sat, 08 Nov 2025 18:32:42 GMT  
		Size: 66.0 MB (65967095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbcf16454f251fa090a6d435bc13794e2ce6cddfb4274c383a427fb9a0bc095`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654ce9cd634ff87730d8740fddbb49d925a9717f9e5f8df646fa2b753e1e7848`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be26d8c2be11d663268630cc9365fa0d04a47c457449d5f7915d3ee7dbb7be5d`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10b2f6b04902b4c29d2db8a899602c26d07be18630f2aaf12a769f530eae59`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 1.6 MB (1617860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:2763db80a45130b186afc5f0cdefe1dbb58c2b7530a7ae5fc479bf1c864d453e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180eda9d571c96d6b847da3bddda4c5810cd982b7d3d863d94a736c64cdf54cb`

```dockerfile
```

-	Layers:
	-	`sha256:3c9ab19c5244e1388d11be71f496aa475b1d0eb959038d70bd0e3ef24bfa2d3a`  
		Last Modified: Sat, 08 Nov 2025 20:58:40 GMT  
		Size: 4.0 MB (3964559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555372a704b1b9e8c929f2fcb3a57ff126562209d4235c2426012016fb6dd39a`  
		Last Modified: Sat, 08 Nov 2025 20:58:41 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:1f1f3047539b136ca2df0c4bacc68b439f402c5695bd6037b2b50497db5c0276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157447663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3046aecd19a22fe6145188f602bbf2fe61e755bab3ce29f1e9d5ba3c95fba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:30:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:30:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:30:43 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:30:43 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:30:43 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:30:43 GMT
USER 8983
# Sat, 08 Nov 2025 18:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:43 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1e268fb03e895b2641fa3b07c8006558bd393472210a15a83c5145ffeaae8c`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 66.0 MB (65967286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f5505ff5dc50efdd82b7cd429e840266c35f5ddf0b20403f9996e06ceb411f`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e157a77924dd3c63be77ec05e15761c028aa4b44e7b5c280a2ef21864b64f4a`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e2fd19da09d55b1e0384f2bd2c6e487e0121b4a0ff44b0e90f1386651f955e`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f4bc0c1a2518f91a798bc390b4e81dd9b78302f3be46e7c234c2fd2dca6efc`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 1.5 MB (1474857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1060d01d7aaa49f9baf41cf421aea4135bf1812d8d21a90a2eadbc237fd61ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ccaeb7d73d570932eda47dcbef4f5ece730aa7d33977e8256cbde7824da74`

```dockerfile
```

-	Layers:
	-	`sha256:ee63595fb67ccfccbbe9d5fe46bc8188efe16ebf2ea124f67f23bdfb7e3b5c5f`  
		Last Modified: Sat, 08 Nov 2025 20:58:45 GMT  
		Size: 4.0 MB (3964235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cd8ac1267219686f5a1435a79dce3325f0b09216753460fb69adbaf4c9e361`  
		Last Modified: Sat, 08 Nov 2025 20:58:46 GMT  
		Size: 34.5 KB (34535 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:5d2b31801115efb851574322cb3165cd40234c1afc030eb22d11f5e82075244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166512861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee45148a071fd9a83c080d8b7e0a19b1c012ab3018afa278d0ce4992b3f5041`
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
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_DIST=-slim
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 06 Nov 2025 18:42:06 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 06 Nov 2025 18:42:06 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 06 Nov 2025 18:42:07 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 06 Nov 2025 18:42:07 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 06 Nov 2025 18:42:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 06 Nov 2025 18:42:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 06 Nov 2025 18:42:27 GMT
VOLUME [/var/solr]
# Thu, 06 Nov 2025 18:42:27 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 06 Nov 2025 18:42:28 GMT
WORKDIR /opt/solr
# Thu, 06 Nov 2025 18:42:28 GMT
USER 8983
# Thu, 06 Nov 2025 18:42:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Nov 2025 18:42:28 GMT
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
	-	`sha256:0a45614bdc82ce0f88ae81279327dbd56cc811053d794ea3b373de7187e2062b`  
		Last Modified: Thu, 06 Nov 2025 18:43:11 GMT  
		Size: 66.0 MB (65967585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9b92042d8a0e14fd1f8ca14584afc5d73595ce569d67cef9aa61fc08931495`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1487f27c374bcb92656b0f7cf4858bae67b93e17c11665bf916a8046476f640a`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d08e7964d186b9facc1aaffcbdf3946405eae9ddbd0863d135cdc46c8e06fb5`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7842016f6edd6456e558f8dc164507cb194c69bafcc49549c24d9d4f5ea5d67`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 1.6 MB (1630849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:520b612510202820bc19b335db516113343fbfb9bbf07ce4477ec12afca229b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f745c37ff4ec55164878a6f4543547a0e4fb651c9be1528c407e14e5ecf3a2f`

```dockerfile
```

-	Layers:
	-	`sha256:52e090a67949a2d9672cca0de93872d9671fa066a782f45850b6112bae1201f5`  
		Last Modified: Thu, 06 Nov 2025 20:58:58 GMT  
		Size: 4.0 MB (3968610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b412c93d4feaf0ac9a2b030be6f0a69395dd3ccec43b4a9c5b739de429645ca6`  
		Last Modified: Thu, 06 Nov 2025 20:58:59 GMT  
		Size: 34.4 KB (34418 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:6751b5bedcda362e76987db53a78525ec6cbde5be6322c6141a3589f9423d650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155727573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04a5c88f6cda250072be3d52c44b0e478335bf272dadc30319eee32cb513bfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:52:10 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:52:10 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:52:10 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:52:11 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:52:12 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:52:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:52:17 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:52:17 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:52:18 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:52:18 GMT
USER 8983
# Sat, 08 Nov 2025 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:52:18 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13f5ac86242f9ac0b877bb70716a889a145f1f75cf9a0205d61300d4a4671c5`  
		Last Modified: Sat, 08 Nov 2025 18:52:44 GMT  
		Size: 66.0 MB (65966962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677eaccb36699fbaf75cd29abdf762283a5de591572edd36da465002d3e024`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9c97d9ce0d83671daf2ceb896aeef1de8fcae7018f2082187f6b80de809d6a`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f395ca1c9714cb96ce2eec4f163d8dfcc5262965bd1e0342ab7b6ae795bfab`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f5684d46f1a4c5ae56b6f10b63cafb6872a7ae8dfe0010dc58ad3b332a3fc8`  
		Last Modified: Sat, 08 Nov 2025 18:52:50 GMT  
		Size: 1.6 MB (1558978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:4baf969b47d5c6192ba5afb504a61a04068496dda30eb04b76657193ff7add3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e344ef3551fa01ce6cabdfc75c8ba837b79c3a9c2496524c9854eb506c1047c3`

```dockerfile
```

-	Layers:
	-	`sha256:6b842a4b571b6a12ceb6750276bf117b9996eab4f9f85a9b0e067476a27df0b1`  
		Last Modified: Sat, 08 Nov 2025 20:58:53 GMT  
		Size: 4.0 MB (3966155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb428c0496da626ad0291a06521450ad4b131522a865a7c4fc740f95fc91177`  
		Last Modified: Sat, 08 Nov 2025 20:58:54 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.10`

```console
$ docker pull solr@sha256:afa60fe0ca0677c3498b86b2c75f01e2c1a99beddff31bc373774a95db6c10cd
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

### `solr:9.10` - linux; amd64

```console
$ docker pull solr@sha256:74b6fad9912f2025cd632186fe4fc70ed6171b3a0a32e6e17e663cce3fccbb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483442963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786008bff5ce8050e108cfcdd30e8d9e31b70d8fa6c447c1277b34df6b022697`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:31:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:56 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:56 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:56 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:56 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:56 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a37838215204e5eb9c43cc251f475f2f5e50406a4a528fe1a05b51a2b7c96b6`  
		Last Modified: Sat, 08 Nov 2025 20:59:51 GMT  
		Size: 389.1 MB (389064942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3de8b7c6486f9db8934d488c34db184555fc57b95dd653749ce77f760d9990`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 4.3 KB (4270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeb4c19a83cc1717b9d7e2013319389a3bdc3b758fb7524a20cb28cacea539b`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093065c795d8c45c6a275c11f09c9b52ab8bdfafc7286cf1d9f2bf6789ea4922`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb41ca25d99ba8892b89bca83d0c56cc69854923aae1a5dd77bc3bd83da9897`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 1.6 MB (1617898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10` - unknown; unknown

```console
$ docker pull solr@sha256:ff08adfa64fd27250c89895bba495152f113a76942223127db7fc59eca781456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa90777d1cd3907c02d1019d47614d737eedbae1117b1264ab4f898b6b0e25b`

```dockerfile
```

-	Layers:
	-	`sha256:b28da5559ae95a01eb11b4e497793b13d9d1e38a1f5a3cd4e48ba837e716b7ad`  
		Last Modified: Sat, 08 Nov 2025 20:58:27 GMT  
		Size: 4.5 MB (4539699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb424671e95073763f09ed69751c48c28eb447d7137d7f9fe5a2f9506db9b254`  
		Last Modified: Sat, 08 Nov 2025 20:58:28 GMT  
		Size: 34.3 KB (34308 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:aae405e78e12ef3c7fa14951ea986c700defe5c3c1ef9224dc3a35c60c0df66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480545650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8b8f0f630a23d7f3c5723b1c5148d0d48226391e18b014125c3e5ea5840983`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:30:54 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:04 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:04 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:04 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:04 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:04 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52f27b0761733cf2048af060549f8a5b7b5405c8e55aadc9a7052a004c9b1de`  
		Last Modified: Sat, 08 Nov 2025 21:01:02 GMT  
		Size: 389.1 MB (389065200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73923ba8ecddac21663225db5dddfc5ca2bda59ff16285f1d2eaf20f2b2cdffa`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da92b13d3c08fbfc56336ffd6f54de29d5cfa51dcfc4592ab2b06156d8ba843a`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b78509309dd28170dd8bb369388c9ad8957d65684139b54426f1eb84055279`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 10.9 KB (10886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51361437f6f8267d791897b7475d3b78a4295c8cef50113e1c5cd034dda51f77`  
		Last Modified: Sat, 08 Nov 2025 18:31:47 GMT  
		Size: 1.5 MB (1474848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10` - unknown; unknown

```console
$ docker pull solr@sha256:63ffced2c7b3c133b6bb255cd1548beb91f29679775965d61edb8154a276f5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4573847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d589682822ac2cfaa0af32b76a9e8cca70eb7705ce6e0b2050fdd4534389d`

```dockerfile
```

-	Layers:
	-	`sha256:21a993ccb9f7e7bcc6ec5f5e9075aee50576a953d434c2de7422c4c4b813a6c5`  
		Last Modified: Sat, 08 Nov 2025 20:58:33 GMT  
		Size: 4.5 MB (4539375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2918860ed4a844fb961be0a212329462606b08ebc5c0df18dc3e699a21212b5b`  
		Last Modified: Sat, 08 Nov 2025 20:58:34 GMT  
		Size: 34.5 KB (34472 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10` - linux; ppc64le

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

### `solr:9.10` - unknown; unknown

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

### `solr:9.10` - linux; s390x

```console
$ docker pull solr@sha256:b5d4e2fbf3eccc4a377e782cf19b4f38d3e3ca2299253177192377ab56f02023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.8 MB (478825463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4610f5de76f4afe4313d8af77f36318398b6e6525d7d6d3dba27edfabfa3ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:50:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:50:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:50:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:50:36 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:50:36 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:50:41 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:50:41 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:50:41 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:50:42 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:50:42 GMT
USER 8983
# Sat, 08 Nov 2025 18:50:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:50:42 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3694c57a0c72262dc59f66e4b220aeca62a5558e36c9ce3d4374aa0b890291`  
		Last Modified: Sat, 08 Nov 2025 21:00:39 GMT  
		Size: 389.1 MB (389064782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9181a7b80fa4afee9fb9275a103a2012f274fdf5451ff0a1ec75e3fb3576d15`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bcdd71ac4320d5f4c8f430a2b5818ff8c53ff6924001e2a80fc38ddc7541c6`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6ca544c45c6093e36dc865e98ed86f586925ee1a56b464db9c86523f01fc0`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 10.9 KB (10888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b7fa825bca319dd389094237d9704ad65a1acd877141984d475643fec31142`  
		Last Modified: Sat, 08 Nov 2025 18:51:43 GMT  
		Size: 1.6 MB (1558972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10` - unknown; unknown

```console
$ docker pull solr@sha256:84f5c9d24bbf74ad1d8a93367e90eec64bdeea67aeef453b82c869fb298ff5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fd8481462e28078722361a6a654c11333b25ee3c1c36ff96c372eb77d19419`

```dockerfile
```

-	Layers:
	-	`sha256:9d82501c524367bfe9ac90b1f855a14425742551664c6f852a4085de2ade3ec0`  
		Last Modified: Sat, 08 Nov 2025 20:58:42 GMT  
		Size: 4.5 MB (4541295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c3069bcdc4c4a771f42e2c2333d16f234fd84daa6c2915f8ee664282a88635`  
		Last Modified: Sat, 08 Nov 2025 20:58:42 GMT  
		Size: 34.3 KB (34307 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.10-slim`

```console
$ docker pull solr@sha256:e9e26ef53699a091c92a1936a2e74933bb19fd2fffb74c488415a62427274ae4
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

### `solr:9.10-slim` - linux; amd64

```console
$ docker pull solr@sha256:72d1bd967a8e99c0a0272cd8616ca16b48e7e316e23eb0e1c1bd2b057f4d460c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160345009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7d1bcd8087cd5e87912c3e1efad6164a1e19a2a19889fe84f3aff6578d0e2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:31:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:55 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:55 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:55 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:55 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:55 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a9971b5b8ed4a21585204efd09f866feb175981eb3fdbe66aad7d810b47aea`  
		Last Modified: Sat, 08 Nov 2025 18:32:42 GMT  
		Size: 66.0 MB (65967095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbcf16454f251fa090a6d435bc13794e2ce6cddfb4274c383a427fb9a0bc095`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654ce9cd634ff87730d8740fddbb49d925a9717f9e5f8df646fa2b753e1e7848`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be26d8c2be11d663268630cc9365fa0d04a47c457449d5f7915d3ee7dbb7be5d`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10b2f6b04902b4c29d2db8a899602c26d07be18630f2aaf12a769f530eae59`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 1.6 MB (1617860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:2763db80a45130b186afc5f0cdefe1dbb58c2b7530a7ae5fc479bf1c864d453e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180eda9d571c96d6b847da3bddda4c5810cd982b7d3d863d94a736c64cdf54cb`

```dockerfile
```

-	Layers:
	-	`sha256:3c9ab19c5244e1388d11be71f496aa475b1d0eb959038d70bd0e3ef24bfa2d3a`  
		Last Modified: Sat, 08 Nov 2025 20:58:40 GMT  
		Size: 4.0 MB (3964559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555372a704b1b9e8c929f2fcb3a57ff126562209d4235c2426012016fb6dd39a`  
		Last Modified: Sat, 08 Nov 2025 20:58:41 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:1f1f3047539b136ca2df0c4bacc68b439f402c5695bd6037b2b50497db5c0276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157447663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3046aecd19a22fe6145188f602bbf2fe61e755bab3ce29f1e9d5ba3c95fba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:30:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:30:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:30:43 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:30:43 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:30:43 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:30:43 GMT
USER 8983
# Sat, 08 Nov 2025 18:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:43 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1e268fb03e895b2641fa3b07c8006558bd393472210a15a83c5145ffeaae8c`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 66.0 MB (65967286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f5505ff5dc50efdd82b7cd429e840266c35f5ddf0b20403f9996e06ceb411f`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e157a77924dd3c63be77ec05e15761c028aa4b44e7b5c280a2ef21864b64f4a`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e2fd19da09d55b1e0384f2bd2c6e487e0121b4a0ff44b0e90f1386651f955e`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f4bc0c1a2518f91a798bc390b4e81dd9b78302f3be46e7c234c2fd2dca6efc`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 1.5 MB (1474857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1060d01d7aaa49f9baf41cf421aea4135bf1812d8d21a90a2eadbc237fd61ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ccaeb7d73d570932eda47dcbef4f5ece730aa7d33977e8256cbde7824da74`

```dockerfile
```

-	Layers:
	-	`sha256:ee63595fb67ccfccbbe9d5fe46bc8188efe16ebf2ea124f67f23bdfb7e3b5c5f`  
		Last Modified: Sat, 08 Nov 2025 20:58:45 GMT  
		Size: 4.0 MB (3964235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cd8ac1267219686f5a1435a79dce3325f0b09216753460fb69adbaf4c9e361`  
		Last Modified: Sat, 08 Nov 2025 20:58:46 GMT  
		Size: 34.5 KB (34535 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:5d2b31801115efb851574322cb3165cd40234c1afc030eb22d11f5e82075244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166512861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee45148a071fd9a83c080d8b7e0a19b1c012ab3018afa278d0ce4992b3f5041`
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
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_DIST=-slim
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 06 Nov 2025 18:42:06 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 06 Nov 2025 18:42:06 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 06 Nov 2025 18:42:07 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 06 Nov 2025 18:42:07 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 06 Nov 2025 18:42:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 06 Nov 2025 18:42:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 06 Nov 2025 18:42:27 GMT
VOLUME [/var/solr]
# Thu, 06 Nov 2025 18:42:27 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 06 Nov 2025 18:42:28 GMT
WORKDIR /opt/solr
# Thu, 06 Nov 2025 18:42:28 GMT
USER 8983
# Thu, 06 Nov 2025 18:42:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Nov 2025 18:42:28 GMT
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
	-	`sha256:0a45614bdc82ce0f88ae81279327dbd56cc811053d794ea3b373de7187e2062b`  
		Last Modified: Thu, 06 Nov 2025 18:43:11 GMT  
		Size: 66.0 MB (65967585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9b92042d8a0e14fd1f8ca14584afc5d73595ce569d67cef9aa61fc08931495`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1487f27c374bcb92656b0f7cf4858bae67b93e17c11665bf916a8046476f640a`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d08e7964d186b9facc1aaffcbdf3946405eae9ddbd0863d135cdc46c8e06fb5`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7842016f6edd6456e558f8dc164507cb194c69bafcc49549c24d9d4f5ea5d67`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 1.6 MB (1630849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:520b612510202820bc19b335db516113343fbfb9bbf07ce4477ec12afca229b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f745c37ff4ec55164878a6f4543547a0e4fb651c9be1528c407e14e5ecf3a2f`

```dockerfile
```

-	Layers:
	-	`sha256:52e090a67949a2d9672cca0de93872d9671fa066a782f45850b6112bae1201f5`  
		Last Modified: Thu, 06 Nov 2025 20:58:58 GMT  
		Size: 4.0 MB (3968610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b412c93d4feaf0ac9a2b030be6f0a69395dd3ccec43b4a9c5b739de429645ca6`  
		Last Modified: Thu, 06 Nov 2025 20:58:59 GMT  
		Size: 34.4 KB (34418 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10-slim` - linux; s390x

```console
$ docker pull solr@sha256:6751b5bedcda362e76987db53a78525ec6cbde5be6322c6141a3589f9423d650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155727573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04a5c88f6cda250072be3d52c44b0e478335bf272dadc30319eee32cb513bfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:52:10 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:52:10 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:52:10 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:52:11 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:52:12 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:52:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:52:17 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:52:17 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:52:18 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:52:18 GMT
USER 8983
# Sat, 08 Nov 2025 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:52:18 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13f5ac86242f9ac0b877bb70716a889a145f1f75cf9a0205d61300d4a4671c5`  
		Last Modified: Sat, 08 Nov 2025 18:52:44 GMT  
		Size: 66.0 MB (65966962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677eaccb36699fbaf75cd29abdf762283a5de591572edd36da465002d3e024`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9c97d9ce0d83671daf2ceb896aeef1de8fcae7018f2082187f6b80de809d6a`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f395ca1c9714cb96ce2eec4f163d8dfcc5262965bd1e0342ab7b6ae795bfab`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f5684d46f1a4c5ae56b6f10b63cafb6872a7ae8dfe0010dc58ad3b332a3fc8`  
		Last Modified: Sat, 08 Nov 2025 18:52:50 GMT  
		Size: 1.6 MB (1558978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:4baf969b47d5c6192ba5afb504a61a04068496dda30eb04b76657193ff7add3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e344ef3551fa01ce6cabdfc75c8ba837b79c3a9c2496524c9854eb506c1047c3`

```dockerfile
```

-	Layers:
	-	`sha256:6b842a4b571b6a12ceb6750276bf117b9996eab4f9f85a9b0e067476a27df0b1`  
		Last Modified: Sat, 08 Nov 2025 20:58:53 GMT  
		Size: 4.0 MB (3966155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb428c0496da626ad0291a06521450ad4b131522a865a7c4fc740f95fc91177`  
		Last Modified: Sat, 08 Nov 2025 20:58:54 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.10.0`

```console
$ docker pull solr@sha256:afa60fe0ca0677c3498b86b2c75f01e2c1a99beddff31bc373774a95db6c10cd
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

### `solr:9.10.0` - linux; amd64

```console
$ docker pull solr@sha256:74b6fad9912f2025cd632186fe4fc70ed6171b3a0a32e6e17e663cce3fccbb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483442963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786008bff5ce8050e108cfcdd30e8d9e31b70d8fa6c447c1277b34df6b022697`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:31:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:56 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:56 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:56 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:56 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:56 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a37838215204e5eb9c43cc251f475f2f5e50406a4a528fe1a05b51a2b7c96b6`  
		Last Modified: Sat, 08 Nov 2025 20:59:51 GMT  
		Size: 389.1 MB (389064942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3de8b7c6486f9db8934d488c34db184555fc57b95dd653749ce77f760d9990`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 4.3 KB (4270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeb4c19a83cc1717b9d7e2013319389a3bdc3b758fb7524a20cb28cacea539b`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093065c795d8c45c6a275c11f09c9b52ab8bdfafc7286cf1d9f2bf6789ea4922`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb41ca25d99ba8892b89bca83d0c56cc69854923aae1a5dd77bc3bd83da9897`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 1.6 MB (1617898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0` - unknown; unknown

```console
$ docker pull solr@sha256:ff08adfa64fd27250c89895bba495152f113a76942223127db7fc59eca781456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa90777d1cd3907c02d1019d47614d737eedbae1117b1264ab4f898b6b0e25b`

```dockerfile
```

-	Layers:
	-	`sha256:b28da5559ae95a01eb11b4e497793b13d9d1e38a1f5a3cd4e48ba837e716b7ad`  
		Last Modified: Sat, 08 Nov 2025 20:58:27 GMT  
		Size: 4.5 MB (4539699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb424671e95073763f09ed69751c48c28eb447d7137d7f9fe5a2f9506db9b254`  
		Last Modified: Sat, 08 Nov 2025 20:58:28 GMT  
		Size: 34.3 KB (34308 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:aae405e78e12ef3c7fa14951ea986c700defe5c3c1ef9224dc3a35c60c0df66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480545650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8b8f0f630a23d7f3c5723b1c5148d0d48226391e18b014125c3e5ea5840983`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:30:54 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:04 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:04 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:04 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:04 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:04 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52f27b0761733cf2048af060549f8a5b7b5405c8e55aadc9a7052a004c9b1de`  
		Last Modified: Sat, 08 Nov 2025 21:01:02 GMT  
		Size: 389.1 MB (389065200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73923ba8ecddac21663225db5dddfc5ca2bda59ff16285f1d2eaf20f2b2cdffa`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da92b13d3c08fbfc56336ffd6f54de29d5cfa51dcfc4592ab2b06156d8ba843a`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b78509309dd28170dd8bb369388c9ad8957d65684139b54426f1eb84055279`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 10.9 KB (10886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51361437f6f8267d791897b7475d3b78a4295c8cef50113e1c5cd034dda51f77`  
		Last Modified: Sat, 08 Nov 2025 18:31:47 GMT  
		Size: 1.5 MB (1474848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0` - unknown; unknown

```console
$ docker pull solr@sha256:63ffced2c7b3c133b6bb255cd1548beb91f29679775965d61edb8154a276f5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4573847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d589682822ac2cfaa0af32b76a9e8cca70eb7705ce6e0b2050fdd4534389d`

```dockerfile
```

-	Layers:
	-	`sha256:21a993ccb9f7e7bcc6ec5f5e9075aee50576a953d434c2de7422c4c4b813a6c5`  
		Last Modified: Sat, 08 Nov 2025 20:58:33 GMT  
		Size: 4.5 MB (4539375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2918860ed4a844fb961be0a212329462606b08ebc5c0df18dc3e699a21212b5b`  
		Last Modified: Sat, 08 Nov 2025 20:58:34 GMT  
		Size: 34.5 KB (34472 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10.0` - linux; ppc64le

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

### `solr:9.10.0` - unknown; unknown

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

### `solr:9.10.0` - linux; s390x

```console
$ docker pull solr@sha256:b5d4e2fbf3eccc4a377e782cf19b4f38d3e3ca2299253177192377ab56f02023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.8 MB (478825463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4610f5de76f4afe4313d8af77f36318398b6e6525d7d6d3dba27edfabfa3ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:50:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:50:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:50:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:50:36 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:50:36 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:50:41 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:50:41 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:50:41 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:50:42 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:50:42 GMT
USER 8983
# Sat, 08 Nov 2025 18:50:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:50:42 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3694c57a0c72262dc59f66e4b220aeca62a5558e36c9ce3d4374aa0b890291`  
		Last Modified: Sat, 08 Nov 2025 21:00:39 GMT  
		Size: 389.1 MB (389064782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9181a7b80fa4afee9fb9275a103a2012f274fdf5451ff0a1ec75e3fb3576d15`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bcdd71ac4320d5f4c8f430a2b5818ff8c53ff6924001e2a80fc38ddc7541c6`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6ca544c45c6093e36dc865e98ed86f586925ee1a56b464db9c86523f01fc0`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 10.9 KB (10888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b7fa825bca319dd389094237d9704ad65a1acd877141984d475643fec31142`  
		Last Modified: Sat, 08 Nov 2025 18:51:43 GMT  
		Size: 1.6 MB (1558972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0` - unknown; unknown

```console
$ docker pull solr@sha256:84f5c9d24bbf74ad1d8a93367e90eec64bdeea67aeef453b82c869fb298ff5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fd8481462e28078722361a6a654c11333b25ee3c1c36ff96c372eb77d19419`

```dockerfile
```

-	Layers:
	-	`sha256:9d82501c524367bfe9ac90b1f855a14425742551664c6f852a4085de2ade3ec0`  
		Last Modified: Sat, 08 Nov 2025 20:58:42 GMT  
		Size: 4.5 MB (4541295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c3069bcdc4c4a771f42e2c2333d16f234fd84daa6c2915f8ee664282a88635`  
		Last Modified: Sat, 08 Nov 2025 20:58:42 GMT  
		Size: 34.3 KB (34307 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.10.0-slim`

```console
$ docker pull solr@sha256:e9e26ef53699a091c92a1936a2e74933bb19fd2fffb74c488415a62427274ae4
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

### `solr:9.10.0-slim` - linux; amd64

```console
$ docker pull solr@sha256:72d1bd967a8e99c0a0272cd8616ca16b48e7e316e23eb0e1c1bd2b057f4d460c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160345009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7d1bcd8087cd5e87912c3e1efad6164a1e19a2a19889fe84f3aff6578d0e2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:31:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:55 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:55 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:55 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:55 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:55 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a9971b5b8ed4a21585204efd09f866feb175981eb3fdbe66aad7d810b47aea`  
		Last Modified: Sat, 08 Nov 2025 18:32:42 GMT  
		Size: 66.0 MB (65967095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbcf16454f251fa090a6d435bc13794e2ce6cddfb4274c383a427fb9a0bc095`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654ce9cd634ff87730d8740fddbb49d925a9717f9e5f8df646fa2b753e1e7848`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be26d8c2be11d663268630cc9365fa0d04a47c457449d5f7915d3ee7dbb7be5d`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10b2f6b04902b4c29d2db8a899602c26d07be18630f2aaf12a769f530eae59`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 1.6 MB (1617860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:2763db80a45130b186afc5f0cdefe1dbb58c2b7530a7ae5fc479bf1c864d453e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180eda9d571c96d6b847da3bddda4c5810cd982b7d3d863d94a736c64cdf54cb`

```dockerfile
```

-	Layers:
	-	`sha256:3c9ab19c5244e1388d11be71f496aa475b1d0eb959038d70bd0e3ef24bfa2d3a`  
		Last Modified: Sat, 08 Nov 2025 20:58:40 GMT  
		Size: 4.0 MB (3964559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555372a704b1b9e8c929f2fcb3a57ff126562209d4235c2426012016fb6dd39a`  
		Last Modified: Sat, 08 Nov 2025 20:58:41 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:1f1f3047539b136ca2df0c4bacc68b439f402c5695bd6037b2b50497db5c0276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157447663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3046aecd19a22fe6145188f602bbf2fe61e755bab3ce29f1e9d5ba3c95fba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:30:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:30:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:30:43 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:30:43 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:30:43 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:30:43 GMT
USER 8983
# Sat, 08 Nov 2025 18:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:43 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1e268fb03e895b2641fa3b07c8006558bd393472210a15a83c5145ffeaae8c`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 66.0 MB (65967286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f5505ff5dc50efdd82b7cd429e840266c35f5ddf0b20403f9996e06ceb411f`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e157a77924dd3c63be77ec05e15761c028aa4b44e7b5c280a2ef21864b64f4a`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e2fd19da09d55b1e0384f2bd2c6e487e0121b4a0ff44b0e90f1386651f955e`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f4bc0c1a2518f91a798bc390b4e81dd9b78302f3be46e7c234c2fd2dca6efc`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 1.5 MB (1474857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1060d01d7aaa49f9baf41cf421aea4135bf1812d8d21a90a2eadbc237fd61ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ccaeb7d73d570932eda47dcbef4f5ece730aa7d33977e8256cbde7824da74`

```dockerfile
```

-	Layers:
	-	`sha256:ee63595fb67ccfccbbe9d5fe46bc8188efe16ebf2ea124f67f23bdfb7e3b5c5f`  
		Last Modified: Sat, 08 Nov 2025 20:58:45 GMT  
		Size: 4.0 MB (3964235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cd8ac1267219686f5a1435a79dce3325f0b09216753460fb69adbaf4c9e361`  
		Last Modified: Sat, 08 Nov 2025 20:58:46 GMT  
		Size: 34.5 KB (34535 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10.0-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:5d2b31801115efb851574322cb3165cd40234c1afc030eb22d11f5e82075244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166512861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee45148a071fd9a83c080d8b7e0a19b1c012ab3018afa278d0ce4992b3f5041`
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
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_DIST=-slim
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 06 Nov 2025 18:42:06 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 06 Nov 2025 18:42:06 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 06 Nov 2025 18:42:07 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 06 Nov 2025 18:42:07 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 06 Nov 2025 18:42:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 06 Nov 2025 18:42:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 06 Nov 2025 18:42:27 GMT
VOLUME [/var/solr]
# Thu, 06 Nov 2025 18:42:27 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 06 Nov 2025 18:42:28 GMT
WORKDIR /opt/solr
# Thu, 06 Nov 2025 18:42:28 GMT
USER 8983
# Thu, 06 Nov 2025 18:42:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Nov 2025 18:42:28 GMT
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
	-	`sha256:0a45614bdc82ce0f88ae81279327dbd56cc811053d794ea3b373de7187e2062b`  
		Last Modified: Thu, 06 Nov 2025 18:43:11 GMT  
		Size: 66.0 MB (65967585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9b92042d8a0e14fd1f8ca14584afc5d73595ce569d67cef9aa61fc08931495`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1487f27c374bcb92656b0f7cf4858bae67b93e17c11665bf916a8046476f640a`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d08e7964d186b9facc1aaffcbdf3946405eae9ddbd0863d135cdc46c8e06fb5`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7842016f6edd6456e558f8dc164507cb194c69bafcc49549c24d9d4f5ea5d67`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 1.6 MB (1630849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:520b612510202820bc19b335db516113343fbfb9bbf07ce4477ec12afca229b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f745c37ff4ec55164878a6f4543547a0e4fb651c9be1528c407e14e5ecf3a2f`

```dockerfile
```

-	Layers:
	-	`sha256:52e090a67949a2d9672cca0de93872d9671fa066a782f45850b6112bae1201f5`  
		Last Modified: Thu, 06 Nov 2025 20:58:58 GMT  
		Size: 4.0 MB (3968610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b412c93d4feaf0ac9a2b030be6f0a69395dd3ccec43b4a9c5b739de429645ca6`  
		Last Modified: Thu, 06 Nov 2025 20:58:59 GMT  
		Size: 34.4 KB (34418 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10.0-slim` - linux; s390x

```console
$ docker pull solr@sha256:6751b5bedcda362e76987db53a78525ec6cbde5be6322c6141a3589f9423d650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155727573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04a5c88f6cda250072be3d52c44b0e478335bf272dadc30319eee32cb513bfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:52:10 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:52:10 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:52:10 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:52:11 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:52:12 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:52:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:52:17 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:52:17 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:52:18 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:52:18 GMT
USER 8983
# Sat, 08 Nov 2025 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:52:18 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13f5ac86242f9ac0b877bb70716a889a145f1f75cf9a0205d61300d4a4671c5`  
		Last Modified: Sat, 08 Nov 2025 18:52:44 GMT  
		Size: 66.0 MB (65966962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677eaccb36699fbaf75cd29abdf762283a5de591572edd36da465002d3e024`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9c97d9ce0d83671daf2ceb896aeef1de8fcae7018f2082187f6b80de809d6a`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f395ca1c9714cb96ce2eec4f163d8dfcc5262965bd1e0342ab7b6ae795bfab`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f5684d46f1a4c5ae56b6f10b63cafb6872a7ae8dfe0010dc58ad3b332a3fc8`  
		Last Modified: Sat, 08 Nov 2025 18:52:50 GMT  
		Size: 1.6 MB (1558978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:4baf969b47d5c6192ba5afb504a61a04068496dda30eb04b76657193ff7add3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e344ef3551fa01ce6cabdfc75c8ba837b79c3a9c2496524c9854eb506c1047c3`

```dockerfile
```

-	Layers:
	-	`sha256:6b842a4b571b6a12ceb6750276bf117b9996eab4f9f85a9b0e067476a27df0b1`  
		Last Modified: Sat, 08 Nov 2025 20:58:53 GMT  
		Size: 4.0 MB (3966155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb428c0496da626ad0291a06521450ad4b131522a865a7c4fc740f95fc91177`  
		Last Modified: Sat, 08 Nov 2025 20:58:54 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.9`

```console
$ docker pull solr@sha256:5a3f941518af59e170e2a62ed7c57235978bd0f666e2b3266d990d3d95d644bb
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
$ docker pull solr@sha256:942bcd505c809987e493a174025281a781197e0a68d5c422d7340f86adf70504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.2 MB (483208928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f14890c77ea52e4ab74e9d61bfeee6fca375f76561b3929869751ec97e8eb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:32:23 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 18:32:23 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:32:23 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Sat, 08 Nov 2025 18:32:23 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 18:32:23 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:32:23 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:32:23 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:32:23 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:32:23 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:32:23 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:32:30 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:32:30 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:32:30 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:32:30 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:32:30 GMT
USER 8983
# Sat, 08 Nov 2025 18:32:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:32:30 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71e5e905a3e5e9778eed748bb4f955507f13a96fd8566749dd96664aa4e3ac`  
		Last Modified: Sat, 08 Nov 2025 21:18:04 GMT  
		Size: 388.8 MB (388830912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3e78352b28c020095a78983aafa6a6b50e83437e537af5dac71a318675c7be`  
		Last Modified: Sat, 08 Nov 2025 18:33:17 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987101ee6a35f465aa060c15344a38c246b16b5c6bdfc9b0722e2be239e39fbb`  
		Last Modified: Sat, 08 Nov 2025 18:33:18 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798e820a2a930c4b24139a23835e2330783f0313f74aa1806a4e696d7b4c8483`  
		Last Modified: Sat, 08 Nov 2025 18:33:17 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdee554a9b5e1bb59766e873af46ca6a377839f2d175e997e51d7025bcb39a0c`  
		Last Modified: Sat, 08 Nov 2025 18:33:18 GMT  
		Size: 1.6 MB (1617881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9` - unknown; unknown

```console
$ docker pull solr@sha256:06aaa22efbb43eda34f695b5b546a11eb6100c7ccbdca5bfe6592510cd640f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4583246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40aa3dc440c974ad97d1b18ec8f448b50ccf5a02edc21f82daa5b7aef6c9bbdf`

```dockerfile
```

-	Layers:
	-	`sha256:ae2644b2ae2bc9a72d3eefc034c35cf39d941ef1bebe2d7080f5d81c4610d3e8`  
		Last Modified: Sat, 08 Nov 2025 20:59:06 GMT  
		Size: 4.5 MB (4549527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbca7ca6aa164308f410906eeb14ff753582b0a8dadbfeb4119f6b124aedf473`  
		Last Modified: Sat, 08 Nov 2025 20:59:07 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:b147cb256325e44696735cbd919bb64922b28b0419e02b781ef1b8a8d8bf438f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480311454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349a16aab7691dccf0858ed15cfc7ee423c484515292a024f8356a73961ea9d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:02 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 18:31:02 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:31:02 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Sat, 08 Nov 2025 18:31:02 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 18:31:02 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:31:02 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:31:02 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:31:03 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:31:03 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:31:03 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:13 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:13 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:13 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:13 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:13 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:13 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede005fb35678adeccbce2fbf3a6544c39760ca2555ebe2496344e5f26682110`  
		Last Modified: Sat, 08 Nov 2025 21:54:35 GMT  
		Size: 388.8 MB (388830977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d527fa72e8687feba6b38d2d80603391a6f9e925cd3967ef57eb41b567a7aa0`  
		Last Modified: Sat, 08 Nov 2025 19:36:03 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d53159b72307ddcb897c82b5b41211b3748e34526ad2b233bcf66f263d5292`  
		Last Modified: Sat, 08 Nov 2025 19:36:03 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ecf1380b82af15de517f43b8f9dfe83ca8c6c1a3155a556225b89d90ec4530`  
		Last Modified: Sat, 08 Nov 2025 19:36:03 GMT  
		Size: 10.9 KB (10889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e6de57b02d140064310a4aa27628c900163df68e23c8397228bb920319308c`  
		Last Modified: Sat, 08 Nov 2025 19:36:03 GMT  
		Size: 1.5 MB (1474874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9` - unknown; unknown

```console
$ docker pull solr@sha256:a5a9a3e3365b66af9a010d2db8530d12d2c7e8e99e8af17ad46a8c7c8ec8a379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4583037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5304eb9e36b4b8f8c850716fa2c4f2648c72f013c33b8c7ee95426326d496c`

```dockerfile
```

-	Layers:
	-	`sha256:960c628034dbfc2183921e6d6bef1807ee87e72465dbb4cc67a7a05e5b4d7734`  
		Last Modified: Sat, 08 Nov 2025 20:59:11 GMT  
		Size: 4.5 MB (4549179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1a149c62bdb848f5dd37eda977ec3862cd9efd81bfd4ee6051fff7c7c196a1`  
		Last Modified: Sat, 08 Nov 2025 20:59:11 GMT  
		Size: 33.9 KB (33858 bytes)  
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
$ docker pull solr@sha256:48fd6e616a6f8662db91b5c210cc99e27db44589e099e859b0a8c4211181b585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.6 MB (478591357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d92db1c7cc63f09f2e089c893e18dea203d36a570113a5c13c37ecc340acb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:04:20 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 19:04:20 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 19:04:20 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Sat, 08 Nov 2025 19:04:20 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 19:04:20 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 19:04:20 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 19:04:20 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 19:04:20 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 19:04:21 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 19:04:21 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 19:04:25 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 19:04:25 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 19:04:25 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 19:04:25 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 19:04:25 GMT
USER 8983
# Sat, 08 Nov 2025 19:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 19:04:25 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45394a2161eb7fbb5812b19c92d8f5adb4b18dcdeb418c8fc38e3dc1d720f46`  
		Last Modified: Sat, 08 Nov 2025 19:05:06 GMT  
		Size: 388.8 MB (388830700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377d1debe9df6021c6d6bdb894acc1961eb70e0db42f486bfcb55d2054056477`  
		Last Modified: Sat, 08 Nov 2025 19:51:05 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd407d7998ec89a98dbd4a965e2016b8934eb5c2f5d56f0109c7ae6def55b65`  
		Last Modified: Sat, 08 Nov 2025 19:51:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f218b3346668258e8bf7c1c9d642bc585cfdedc4f307af1869328d7e4d1ade3`  
		Last Modified: Sat, 08 Nov 2025 19:51:05 GMT  
		Size: 10.9 KB (10894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55051567de112059c42abdf4b4dd123808d894091d2ccc3c166e4a27ec6778c`  
		Last Modified: Sat, 08 Nov 2025 19:51:16 GMT  
		Size: 1.6 MB (1558938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9` - unknown; unknown

```console
$ docker pull solr@sha256:7cd6f0e3418dfba41ce92e30d8fcf239898d9d57040d36db565f5c3452d4c1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b6d0e8113df878d3bef71a3addbab4fac1fecc845497350b1e48e61baaf007`

```dockerfile
```

-	Layers:
	-	`sha256:8459bc2368a591320087cf0c5a0a7b70a713202ea5c69d4b1766b2b005046ff1`  
		Last Modified: Sat, 08 Nov 2025 20:59:19 GMT  
		Size: 4.6 MB (4551123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:433c4a582e132af5fd39db9ccdb661ce5c56b1c241a038dc73a624347b742585`  
		Last Modified: Sat, 08 Nov 2025 20:59:20 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.9-slim`

```console
$ docker pull solr@sha256:d44a4492fe01205e52c5783ebf4e07a67c30c78f8ae3fcfa8859df5eeedc6b01
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
$ docker pull solr@sha256:398d777de0e408f3c9f322e4202ccdfaca71f73ec86050d919e07ff91813bd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159996330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5aad99c07e4e484f1295e143421327dc15c947e5e8107c6721f0b55e10e2ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:32:10 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 18:32:10 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:32:10 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Sat, 08 Nov 2025 18:32:10 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 18:32:10 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:32:10 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:32:10 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:32:11 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:32:11 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:32:11 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:32:17 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:32:17 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:32:17 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:32:18 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:32:18 GMT
USER 8983
# Sat, 08 Nov 2025 18:32:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:32:18 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca500f4cfcf1dd97caa3a940c810fc2164f9c99208731fef4ba3058c0bd7350`  
		Last Modified: Sat, 08 Nov 2025 18:32:46 GMT  
		Size: 65.6 MB (65618455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b8931a0e3190982c115dadeed30123768851f38c3f29de501566d40e86fe69`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e38dd51f0594d4bbe75ddf00abf61b5bc6a2f5166dccca0fd8908dc7ff85bb`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56e32a4dc47804060747becde502f23f2eaf58bba94eb22deca9f8b60638ff1`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 10.8 KB (10808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea84a19ae0a611d8f67a0cc229a8c0c08fb5d8b8b0af82607685bf8c9fc4991e`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 1.6 MB (1617814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:9c5679c957951b10a83bbbdbd00daed237667c4898496f589a7763258f1cc673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4927217ca77ba75052d4bae5d7ac9c4cbed3d9de8a39aa0a8d40634a5f69acdf`

```dockerfile
```

-	Layers:
	-	`sha256:907f4328c1de76535f65cd03f0fbd43ab852429f7727ddc9448d644b7525025c`  
		Last Modified: Sat, 08 Nov 2025 20:59:19 GMT  
		Size: 4.0 MB (3962532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42cfaedecf75487ec8f66373ef76e15171b91b210ba95c2397b21801922bbb65`  
		Last Modified: Sat, 08 Nov 2025 20:59:20 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:627faf8e66f612197bd4480a68e87d33a7c422a6608cb41f93752212d789b3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157098974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa14634780ec100e13f236b185b4deaf558f5b97c3e7f2324d2583020d9b3d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:45 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 18:30:45 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:30:45 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Sat, 08 Nov 2025 18:30:45 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 18:30:45 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:30:45 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:30:45 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:30:45 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:30:46 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:30:46 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:30:53 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:30:53 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:30:53 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:30:53 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:30:53 GMT
USER 8983
# Sat, 08 Nov 2025 18:30:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:53 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae585826453b95c603f22d85186543cf31da4e104bacf3389d143c8a4753ada5`  
		Last Modified: Sat, 08 Nov 2025 18:31:24 GMT  
		Size: 65.6 MB (65618584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdf2ef32d7d23213977dd491d870c0716e7bfbf81fc010a17b1c3f5f082f9b`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065e0575a73de91d94d75308c61afdc6526232e884a4962c820273bbe31ab43e`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c1384b81989b719f33d6e9c518683c2790ab3adba0f51d2a12043cabe5b35`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 10.8 KB (10811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121f7539d20ab5a25d322ea73a568c3a09678f3ffda1a8499932449781ec192f`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 1.5 MB (1474856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1d827aa49e43f8ad87919b22fe73f8757730b19177f1c6725aecf93a48271153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f2671a7197875e0cff950cca402288d4347ba3d282cb57e8a99517ca33b3a0`

```dockerfile
```

-	Layers:
	-	`sha256:0a28fc60ccf5b3dda6be32c3d32ad33c7ef558ae32402ff4def73e62556d687b`  
		Last Modified: Sat, 08 Nov 2025 20:59:25 GMT  
		Size: 4.0 MB (3962184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78515e0a78b3955e05163c06380c5226eb13995d7fff5ed356549a4600ca5322`  
		Last Modified: Sat, 08 Nov 2025 20:59:26 GMT  
		Size: 33.9 KB (33916 bytes)  
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
$ docker pull solr@sha256:bcdbeec327fdf34d0527b08f44e63294efecde44e15914dbc1d076be6de11ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155378843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24cde9b96f4b63115a69343eac9b7b38225ece11c8c3a56bd2b1e11516c200b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:07:01 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 19:07:01 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 19:07:01 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Sat, 08 Nov 2025 19:07:01 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 19:07:01 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 19:07:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 19:07:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 19:07:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 19:07:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 19:07:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 19:07:04 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 19:07:04 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 19:07:04 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 19:07:04 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 19:07:04 GMT
USER 8983
# Sat, 08 Nov 2025 19:07:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 19:07:04 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fb718eedae862624338ece4e0b41271911b926edb43831bf4ac07f41797ef7`  
		Last Modified: Sat, 08 Nov 2025 19:11:13 GMT  
		Size: 65.6 MB (65618262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2148b1fe3a91d87ef52ebb98df61d071e29b424f01f8b24b552b749e6af77656`  
		Last Modified: Sat, 08 Nov 2025 19:11:07 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c37121f6a50b42f24c07098b52595f2c0ea774cbd793c21f85e4560de6edba`  
		Last Modified: Sat, 08 Nov 2025 19:11:07 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f6236922e6a1515ea65035820b8e5f0013b1c5ab92893b36371756fbae9567`  
		Last Modified: Sat, 08 Nov 2025 19:11:07 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012355addb04e953fe26a50fdecd679f7f8d8ab926ea73c5186b9b833a1ae210`  
		Last Modified: Sat, 08 Nov 2025 19:11:07 GMT  
		Size: 1.6 MB (1558944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:7f663c2c6129960d82449964d666448ebb7df841d25b48bc8e49ec3470cc9ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e337963ca810af0d3eac276f83a86cf8fd5c348a4656f0a330419ccb5980cb33`

```dockerfile
```

-	Layers:
	-	`sha256:e7db5c825c764b4443f549ccfed09a17c8f4315b040e0e66b1550bc9ed646965`  
		Last Modified: Sat, 08 Nov 2025 20:59:33 GMT  
		Size: 4.0 MB (3964128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a697c864640491091d524d25fbdb4dc2707857779485bc3f4bd0ec475805c2a`  
		Last Modified: Sat, 08 Nov 2025 20:59:34 GMT  
		Size: 33.8 KB (33775 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.9.0`

```console
$ docker pull solr@sha256:5a3f941518af59e170e2a62ed7c57235978bd0f666e2b3266d990d3d95d644bb
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
$ docker pull solr@sha256:942bcd505c809987e493a174025281a781197e0a68d5c422d7340f86adf70504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.2 MB (483208928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f14890c77ea52e4ab74e9d61bfeee6fca375f76561b3929869751ec97e8eb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:32:23 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 18:32:23 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:32:23 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Sat, 08 Nov 2025 18:32:23 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 18:32:23 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:32:23 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 18:32:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:32:23 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:32:23 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:32:23 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:32:23 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:32:30 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:32:30 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:32:30 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:32:30 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:32:30 GMT
USER 8983
# Sat, 08 Nov 2025 18:32:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:32:30 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e71e5e905a3e5e9778eed748bb4f955507f13a96fd8566749dd96664aa4e3ac`  
		Last Modified: Sat, 08 Nov 2025 21:18:04 GMT  
		Size: 388.8 MB (388830912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3e78352b28c020095a78983aafa6a6b50e83437e537af5dac71a318675c7be`  
		Last Modified: Sat, 08 Nov 2025 18:33:17 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987101ee6a35f465aa060c15344a38c246b16b5c6bdfc9b0722e2be239e39fbb`  
		Last Modified: Sat, 08 Nov 2025 18:33:18 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798e820a2a930c4b24139a23835e2330783f0313f74aa1806a4e696d7b4c8483`  
		Last Modified: Sat, 08 Nov 2025 18:33:17 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdee554a9b5e1bb59766e873af46ca6a377839f2d175e997e51d7025bcb39a0c`  
		Last Modified: Sat, 08 Nov 2025 18:33:18 GMT  
		Size: 1.6 MB (1617881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0` - unknown; unknown

```console
$ docker pull solr@sha256:06aaa22efbb43eda34f695b5b546a11eb6100c7ccbdca5bfe6592510cd640f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4583246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40aa3dc440c974ad97d1b18ec8f448b50ccf5a02edc21f82daa5b7aef6c9bbdf`

```dockerfile
```

-	Layers:
	-	`sha256:ae2644b2ae2bc9a72d3eefc034c35cf39d941ef1bebe2d7080f5d81c4610d3e8`  
		Last Modified: Sat, 08 Nov 2025 20:59:06 GMT  
		Size: 4.5 MB (4549527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbca7ca6aa164308f410906eeb14ff753582b0a8dadbfeb4119f6b124aedf473`  
		Last Modified: Sat, 08 Nov 2025 20:59:07 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:b147cb256325e44696735cbd919bb64922b28b0419e02b781ef1b8a8d8bf438f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480311454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349a16aab7691dccf0858ed15cfc7ee423c484515292a024f8356a73961ea9d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:02 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 18:31:02 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:31:02 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Sat, 08 Nov 2025 18:31:02 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 18:31:02 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:31:02 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 18:31:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:31:02 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:31:03 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:31:03 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:31:03 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:13 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:13 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:13 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:13 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:13 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:13 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede005fb35678adeccbce2fbf3a6544c39760ca2555ebe2496344e5f26682110`  
		Last Modified: Sat, 08 Nov 2025 21:54:35 GMT  
		Size: 388.8 MB (388830977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d527fa72e8687feba6b38d2d80603391a6f9e925cd3967ef57eb41b567a7aa0`  
		Last Modified: Sat, 08 Nov 2025 19:36:03 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d53159b72307ddcb897c82b5b41211b3748e34526ad2b233bcf66f263d5292`  
		Last Modified: Sat, 08 Nov 2025 19:36:03 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ecf1380b82af15de517f43b8f9dfe83ca8c6c1a3155a556225b89d90ec4530`  
		Last Modified: Sat, 08 Nov 2025 19:36:03 GMT  
		Size: 10.9 KB (10889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e6de57b02d140064310a4aa27628c900163df68e23c8397228bb920319308c`  
		Last Modified: Sat, 08 Nov 2025 19:36:03 GMT  
		Size: 1.5 MB (1474874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0` - unknown; unknown

```console
$ docker pull solr@sha256:a5a9a3e3365b66af9a010d2db8530d12d2c7e8e99e8af17ad46a8c7c8ec8a379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4583037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5304eb9e36b4b8f8c850716fa2c4f2648c72f013c33b8c7ee95426326d496c`

```dockerfile
```

-	Layers:
	-	`sha256:960c628034dbfc2183921e6d6bef1807ee87e72465dbb4cc67a7a05e5b4d7734`  
		Last Modified: Sat, 08 Nov 2025 20:59:11 GMT  
		Size: 4.5 MB (4549179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1a149c62bdb848f5dd37eda977ec3862cd9efd81bfd4ee6051fff7c7c196a1`  
		Last Modified: Sat, 08 Nov 2025 20:59:11 GMT  
		Size: 33.9 KB (33858 bytes)  
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
$ docker pull solr@sha256:48fd6e616a6f8662db91b5c210cc99e27db44589e099e859b0a8c4211181b585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.6 MB (478591357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d92db1c7cc63f09f2e089c893e18dea203d36a570113a5c13c37ecc340acb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:04:20 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 19:04:20 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 19:04:20 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Sat, 08 Nov 2025 19:04:20 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 19:04:20 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 19:04:20 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 19:04:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 19:04:20 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 19:04:20 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 19:04:21 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 19:04:21 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 19:04:25 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 19:04:25 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 19:04:25 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 19:04:25 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 19:04:25 GMT
USER 8983
# Sat, 08 Nov 2025 19:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 19:04:25 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45394a2161eb7fbb5812b19c92d8f5adb4b18dcdeb418c8fc38e3dc1d720f46`  
		Last Modified: Sat, 08 Nov 2025 19:05:06 GMT  
		Size: 388.8 MB (388830700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377d1debe9df6021c6d6bdb894acc1961eb70e0db42f486bfcb55d2054056477`  
		Last Modified: Sat, 08 Nov 2025 19:51:05 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd407d7998ec89a98dbd4a965e2016b8934eb5c2f5d56f0109c7ae6def55b65`  
		Last Modified: Sat, 08 Nov 2025 19:51:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f218b3346668258e8bf7c1c9d642bc585cfdedc4f307af1869328d7e4d1ade3`  
		Last Modified: Sat, 08 Nov 2025 19:51:05 GMT  
		Size: 10.9 KB (10894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55051567de112059c42abdf4b4dd123808d894091d2ccc3c166e4a27ec6778c`  
		Last Modified: Sat, 08 Nov 2025 19:51:16 GMT  
		Size: 1.6 MB (1558938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0` - unknown; unknown

```console
$ docker pull solr@sha256:7cd6f0e3418dfba41ce92e30d8fcf239898d9d57040d36db565f5c3452d4c1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b6d0e8113df878d3bef71a3addbab4fac1fecc845497350b1e48e61baaf007`

```dockerfile
```

-	Layers:
	-	`sha256:8459bc2368a591320087cf0c5a0a7b70a713202ea5c69d4b1766b2b005046ff1`  
		Last Modified: Sat, 08 Nov 2025 20:59:19 GMT  
		Size: 4.6 MB (4551123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:433c4a582e132af5fd39db9ccdb661ce5c56b1c241a038dc73a624347b742585`  
		Last Modified: Sat, 08 Nov 2025 20:59:20 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.9.0-slim`

```console
$ docker pull solr@sha256:d44a4492fe01205e52c5783ebf4e07a67c30c78f8ae3fcfa8859df5eeedc6b01
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
$ docker pull solr@sha256:398d777de0e408f3c9f322e4202ccdfaca71f73ec86050d919e07ff91813bd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159996330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5aad99c07e4e484f1295e143421327dc15c947e5e8107c6721f0b55e10e2ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:32:10 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 18:32:10 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:32:10 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Sat, 08 Nov 2025 18:32:10 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 18:32:10 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:32:10 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 18:32:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:32:10 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:32:11 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:32:11 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:32:11 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:32:17 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:32:17 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:32:17 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:32:18 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:32:18 GMT
USER 8983
# Sat, 08 Nov 2025 18:32:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:32:18 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca500f4cfcf1dd97caa3a940c810fc2164f9c99208731fef4ba3058c0bd7350`  
		Last Modified: Sat, 08 Nov 2025 18:32:46 GMT  
		Size: 65.6 MB (65618455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b8931a0e3190982c115dadeed30123768851f38c3f29de501566d40e86fe69`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e38dd51f0594d4bbe75ddf00abf61b5bc6a2f5166dccca0fd8908dc7ff85bb`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56e32a4dc47804060747becde502f23f2eaf58bba94eb22deca9f8b60638ff1`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 10.8 KB (10808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea84a19ae0a611d8f67a0cc229a8c0c08fb5d8b8b0af82607685bf8c9fc4991e`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 1.6 MB (1617814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:9c5679c957951b10a83bbbdbd00daed237667c4898496f589a7763258f1cc673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4927217ca77ba75052d4bae5d7ac9c4cbed3d9de8a39aa0a8d40634a5f69acdf`

```dockerfile
```

-	Layers:
	-	`sha256:907f4328c1de76535f65cd03f0fbd43ab852429f7727ddc9448d644b7525025c`  
		Last Modified: Sat, 08 Nov 2025 20:59:19 GMT  
		Size: 4.0 MB (3962532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42cfaedecf75487ec8f66373ef76e15171b91b210ba95c2397b21801922bbb65`  
		Last Modified: Sat, 08 Nov 2025 20:59:20 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:627faf8e66f612197bd4480a68e87d33a7c422a6608cb41f93752212d789b3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157098974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa14634780ec100e13f236b185b4deaf558f5b97c3e7f2324d2583020d9b3d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:45 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 18:30:45 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:30:45 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Sat, 08 Nov 2025 18:30:45 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 18:30:45 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:30:45 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 18:30:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:30:45 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:30:45 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:30:46 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:30:46 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:30:53 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:30:53 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:30:53 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:30:53 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:30:53 GMT
USER 8983
# Sat, 08 Nov 2025 18:30:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:53 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae585826453b95c603f22d85186543cf31da4e104bacf3389d143c8a4753ada5`  
		Last Modified: Sat, 08 Nov 2025 18:31:24 GMT  
		Size: 65.6 MB (65618584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdf2ef32d7d23213977dd491d870c0716e7bfbf81fc010a17b1c3f5f082f9b`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065e0575a73de91d94d75308c61afdc6526232e884a4962c820273bbe31ab43e`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c1384b81989b719f33d6e9c518683c2790ab3adba0f51d2a12043cabe5b35`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 10.8 KB (10811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121f7539d20ab5a25d322ea73a568c3a09678f3ffda1a8499932449781ec192f`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 1.5 MB (1474856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1d827aa49e43f8ad87919b22fe73f8757730b19177f1c6725aecf93a48271153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f2671a7197875e0cff950cca402288d4347ba3d282cb57e8a99517ca33b3a0`

```dockerfile
```

-	Layers:
	-	`sha256:0a28fc60ccf5b3dda6be32c3d32ad33c7ef558ae32402ff4def73e62556d687b`  
		Last Modified: Sat, 08 Nov 2025 20:59:25 GMT  
		Size: 4.0 MB (3962184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78515e0a78b3955e05163c06380c5226eb13995d7fff5ed356549a4600ca5322`  
		Last Modified: Sat, 08 Nov 2025 20:59:26 GMT  
		Size: 33.9 KB (33916 bytes)  
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
$ docker pull solr@sha256:bcdbeec327fdf34d0527b08f44e63294efecde44e15914dbc1d076be6de11ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155378843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24cde9b96f4b63115a69343eac9b7b38225ece11c8c3a56bd2b1e11516c200b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:07:01 GMT
ARG SOLR_VERSION=9.9.0
# Sat, 08 Nov 2025 19:07:01 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 19:07:01 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Sat, 08 Nov 2025 19:07:01 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 08 Nov 2025 19:07:01 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 19:07:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.version=9.9.0
# Sat, 08 Nov 2025 19:07:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 19:07:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 19:07:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 19:07:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 19:07:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 19:07:04 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 19:07:04 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 19:07:04 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 19:07:04 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 19:07:04 GMT
USER 8983
# Sat, 08 Nov 2025 19:07:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 19:07:04 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fb718eedae862624338ece4e0b41271911b926edb43831bf4ac07f41797ef7`  
		Last Modified: Sat, 08 Nov 2025 19:11:13 GMT  
		Size: 65.6 MB (65618262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2148b1fe3a91d87ef52ebb98df61d071e29b424f01f8b24b552b749e6af77656`  
		Last Modified: Sat, 08 Nov 2025 19:11:07 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c37121f6a50b42f24c07098b52595f2c0ea774cbd793c21f85e4560de6edba`  
		Last Modified: Sat, 08 Nov 2025 19:11:07 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f6236922e6a1515ea65035820b8e5f0013b1c5ab92893b36371756fbae9567`  
		Last Modified: Sat, 08 Nov 2025 19:11:07 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012355addb04e953fe26a50fdecd679f7f8d8ab926ea73c5186b9b833a1ae210`  
		Last Modified: Sat, 08 Nov 2025 19:11:07 GMT  
		Size: 1.6 MB (1558944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:7f663c2c6129960d82449964d666448ebb7df841d25b48bc8e49ec3470cc9ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e337963ca810af0d3eac276f83a86cf8fd5c348a4656f0a330419ccb5980cb33`

```dockerfile
```

-	Layers:
	-	`sha256:e7db5c825c764b4443f549ccfed09a17c8f4315b040e0e66b1550bc9ed646965`  
		Last Modified: Sat, 08 Nov 2025 20:59:33 GMT  
		Size: 4.0 MB (3964128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a697c864640491091d524d25fbdb4dc2707857779485bc3f4bd0ec475805c2a`  
		Last Modified: Sat, 08 Nov 2025 20:59:34 GMT  
		Size: 33.8 KB (33775 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:latest`

```console
$ docker pull solr@sha256:afa60fe0ca0677c3498b86b2c75f01e2c1a99beddff31bc373774a95db6c10cd
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
$ docker pull solr@sha256:74b6fad9912f2025cd632186fe4fc70ed6171b3a0a32e6e17e663cce3fccbb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483442963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786008bff5ce8050e108cfcdd30e8d9e31b70d8fa6c447c1277b34df6b022697`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:31:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:56 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:56 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:56 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:56 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:56 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a37838215204e5eb9c43cc251f475f2f5e50406a4a528fe1a05b51a2b7c96b6`  
		Last Modified: Sat, 08 Nov 2025 20:59:51 GMT  
		Size: 389.1 MB (389064942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3de8b7c6486f9db8934d488c34db184555fc57b95dd653749ce77f760d9990`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 4.3 KB (4270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeb4c19a83cc1717b9d7e2013319389a3bdc3b758fb7524a20cb28cacea539b`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093065c795d8c45c6a275c11f09c9b52ab8bdfafc7286cf1d9f2bf6789ea4922`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb41ca25d99ba8892b89bca83d0c56cc69854923aae1a5dd77bc3bd83da9897`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 1.6 MB (1617898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:ff08adfa64fd27250c89895bba495152f113a76942223127db7fc59eca781456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa90777d1cd3907c02d1019d47614d737eedbae1117b1264ab4f898b6b0e25b`

```dockerfile
```

-	Layers:
	-	`sha256:b28da5559ae95a01eb11b4e497793b13d9d1e38a1f5a3cd4e48ba837e716b7ad`  
		Last Modified: Sat, 08 Nov 2025 20:58:27 GMT  
		Size: 4.5 MB (4539699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb424671e95073763f09ed69751c48c28eb447d7137d7f9fe5a2f9506db9b254`  
		Last Modified: Sat, 08 Nov 2025 20:58:28 GMT  
		Size: 34.3 KB (34308 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:aae405e78e12ef3c7fa14951ea986c700defe5c3c1ef9224dc3a35c60c0df66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480545650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8b8f0f630a23d7f3c5723b1c5148d0d48226391e18b014125c3e5ea5840983`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:30:54 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:30:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:30:54 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:30:54 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:04 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:04 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:04 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:04 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:04 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52f27b0761733cf2048af060549f8a5b7b5405c8e55aadc9a7052a004c9b1de`  
		Last Modified: Sat, 08 Nov 2025 21:01:02 GMT  
		Size: 389.1 MB (389065200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73923ba8ecddac21663225db5dddfc5ca2bda59ff16285f1d2eaf20f2b2cdffa`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da92b13d3c08fbfc56336ffd6f54de29d5cfa51dcfc4592ab2b06156d8ba843a`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b78509309dd28170dd8bb369388c9ad8957d65684139b54426f1eb84055279`  
		Last Modified: Sat, 08 Nov 2025 18:31:46 GMT  
		Size: 10.9 KB (10886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51361437f6f8267d791897b7475d3b78a4295c8cef50113e1c5cd034dda51f77`  
		Last Modified: Sat, 08 Nov 2025 18:31:47 GMT  
		Size: 1.5 MB (1474848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:63ffced2c7b3c133b6bb255cd1548beb91f29679775965d61edb8154a276f5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4573847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d589682822ac2cfaa0af32b76a9e8cca70eb7705ce6e0b2050fdd4534389d`

```dockerfile
```

-	Layers:
	-	`sha256:21a993ccb9f7e7bcc6ec5f5e9075aee50576a953d434c2de7422c4c4b813a6c5`  
		Last Modified: Sat, 08 Nov 2025 20:58:33 GMT  
		Size: 4.5 MB (4539375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2918860ed4a844fb961be0a212329462606b08ebc5c0df18dc3e699a21212b5b`  
		Last Modified: Sat, 08 Nov 2025 20:58:34 GMT  
		Size: 34.5 KB (34472 bytes)  
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
$ docker pull solr@sha256:b5d4e2fbf3eccc4a377e782cf19b4f38d3e3ca2299253177192377ab56f02023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.8 MB (478825463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4610f5de76f4afe4313d8af77f36318398b6e6525d7d6d3dba27edfabfa3ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:50:35 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:50:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:50:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:50:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:50:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:50:36 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:50:36 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:50:41 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:50:41 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:50:41 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:50:42 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:50:42 GMT
USER 8983
# Sat, 08 Nov 2025 18:50:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:50:42 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3694c57a0c72262dc59f66e4b220aeca62a5558e36c9ce3d4374aa0b890291`  
		Last Modified: Sat, 08 Nov 2025 21:00:39 GMT  
		Size: 389.1 MB (389064782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9181a7b80fa4afee9fb9275a103a2012f274fdf5451ff0a1ec75e3fb3576d15`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bcdd71ac4320d5f4c8f430a2b5818ff8c53ff6924001e2a80fc38ddc7541c6`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6ca544c45c6093e36dc865e98ed86f586925ee1a56b464db9c86523f01fc0`  
		Last Modified: Sat, 08 Nov 2025 18:51:42 GMT  
		Size: 10.9 KB (10888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b7fa825bca319dd389094237d9704ad65a1acd877141984d475643fec31142`  
		Last Modified: Sat, 08 Nov 2025 18:51:43 GMT  
		Size: 1.6 MB (1558972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:84f5c9d24bbf74ad1d8a93367e90eec64bdeea67aeef453b82c869fb298ff5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fd8481462e28078722361a6a654c11333b25ee3c1c36ff96c372eb77d19419`

```dockerfile
```

-	Layers:
	-	`sha256:9d82501c524367bfe9ac90b1f855a14425742551664c6f852a4085de2ade3ec0`  
		Last Modified: Sat, 08 Nov 2025 20:58:42 GMT  
		Size: 4.5 MB (4541295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c3069bcdc4c4a771f42e2c2333d16f234fd84daa6c2915f8ee664282a88635`  
		Last Modified: Sat, 08 Nov 2025 20:58:42 GMT  
		Size: 34.3 KB (34307 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:slim`

```console
$ docker pull solr@sha256:e9e26ef53699a091c92a1936a2e74933bb19fd2fffb74c488415a62427274ae4
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
$ docker pull solr@sha256:72d1bd967a8e99c0a0272cd8616ca16b48e7e316e23eb0e1c1bd2b057f4d460c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160345009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7d1bcd8087cd5e87912c3e1efad6164a1e19a2a19889fe84f3aff6578d0e2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:31:48 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:31:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:31:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:31:49 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:31:55 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:31:55 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:31:55 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:31:55 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:31:55 GMT
USER 8983
# Sat, 08 Nov 2025 18:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bb83c7bd9f4bc0d73d917ad3179845af87fb762faac5dad12456a43e5dec5`  
		Last Modified: Sat, 08 Nov 2025 17:59:21 GMT  
		Size: 16.2 MB (16150395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46533b5422d76800c4f70873c67f6e4bdef3139ecad8c76eb2379f2a93200dd`  
		Last Modified: Sat, 08 Nov 2025 17:59:36 GMT  
		Size: 47.1 MB (47055077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943829239548ac8de7d1a2287a3e005956ce475368f6e918c7867085dd910c1`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f512b025c2abbd2b7a8835027f843230a5b9a94c28345e18ebf0582e6cd45462`  
		Last Modified: Sat, 08 Nov 2025 17:59:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a9971b5b8ed4a21585204efd09f866feb175981eb3fdbe66aad7d810b47aea`  
		Last Modified: Sat, 08 Nov 2025 18:32:42 GMT  
		Size: 66.0 MB (65967095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbcf16454f251fa090a6d435bc13794e2ce6cddfb4274c383a427fb9a0bc095`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654ce9cd634ff87730d8740fddbb49d925a9717f9e5f8df646fa2b753e1e7848`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be26d8c2be11d663268630cc9365fa0d04a47c457449d5f7915d3ee7dbb7be5d`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10b2f6b04902b4c29d2db8a899602c26d07be18630f2aaf12a769f530eae59`  
		Last Modified: Sat, 08 Nov 2025 18:32:37 GMT  
		Size: 1.6 MB (1617860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:2763db80a45130b186afc5f0cdefe1dbb58c2b7530a7ae5fc479bf1c864d453e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180eda9d571c96d6b847da3bddda4c5810cd982b7d3d863d94a736c64cdf54cb`

```dockerfile
```

-	Layers:
	-	`sha256:3c9ab19c5244e1388d11be71f496aa475b1d0eb959038d70bd0e3ef24bfa2d3a`  
		Last Modified: Sat, 08 Nov 2025 20:58:40 GMT  
		Size: 4.0 MB (3964559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555372a704b1b9e8c929f2fcb3a57ff126562209d4235c2426012016fb6dd39a`  
		Last Modified: Sat, 08 Nov 2025 20:58:41 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:1f1f3047539b136ca2df0c4bacc68b439f402c5695bd6037b2b50497db5c0276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157447663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3046aecd19a22fe6145188f602bbf2fe61e755bab3ce29f1e9d5ba3c95fba5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:30:35 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:30:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:30:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:30:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:30:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:30:43 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:30:43 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:30:43 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:30:43 GMT
USER 8983
# Sat, 08 Nov 2025 18:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:43 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679255ce7087c0a227c6066043e3dbaf06d8e3fc1e2803f49f84b2701d651b8`  
		Last Modified: Sat, 08 Nov 2025 17:58:47 GMT  
		Size: 16.1 MB (16066398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20489c2e0bcfe95bef1b1cecead7abb3869f703f4cb3f700ec6781e00892ff2`  
		Last Modified: Sat, 08 Nov 2025 17:58:51 GMT  
		Size: 46.5 MB (46538225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0971c039414b063933b4d5c0cf0296888b0d4c2f4e5d4dfddc4cbdcfe3e4c`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323aa1409f60c749222775d4e792344a2a9cf2cf393086581019065a805a9a3b`  
		Last Modified: Sat, 08 Nov 2025 17:58:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1e268fb03e895b2641fa3b07c8006558bd393472210a15a83c5145ffeaae8c`  
		Last Modified: Sat, 08 Nov 2025 18:31:17 GMT  
		Size: 66.0 MB (65967286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f5505ff5dc50efdd82b7cd429e840266c35f5ddf0b20403f9996e06ceb411f`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e157a77924dd3c63be77ec05e15761c028aa4b44e7b5c280a2ef21864b64f4a`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e2fd19da09d55b1e0384f2bd2c6e487e0121b4a0ff44b0e90f1386651f955e`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f4bc0c1a2518f91a798bc390b4e81dd9b78302f3be46e7c234c2fd2dca6efc`  
		Last Modified: Sat, 08 Nov 2025 18:31:12 GMT  
		Size: 1.5 MB (1474857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:1060d01d7aaa49f9baf41cf421aea4135bf1812d8d21a90a2eadbc237fd61ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2ccaeb7d73d570932eda47dcbef4f5ece730aa7d33977e8256cbde7824da74`

```dockerfile
```

-	Layers:
	-	`sha256:ee63595fb67ccfccbbe9d5fe46bc8188efe16ebf2ea124f67f23bdfb7e3b5c5f`  
		Last Modified: Sat, 08 Nov 2025 20:58:45 GMT  
		Size: 4.0 MB (3964235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cd8ac1267219686f5a1435a79dce3325f0b09216753460fb69adbaf4c9e361`  
		Last Modified: Sat, 08 Nov 2025 20:58:46 GMT  
		Size: 34.5 KB (34535 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:5d2b31801115efb851574322cb3165cd40234c1afc030eb22d11f5e82075244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166512861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee45148a071fd9a83c080d8b7e0a19b1c012ab3018afa278d0ce4992b3f5041`
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
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_DIST=-slim
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 06 Nov 2025 18:42:06 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 06 Nov 2025 18:42:06 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 06 Nov 2025 18:42:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 06 Nov 2025 18:42:06 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 06 Nov 2025 18:42:07 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 06 Nov 2025 18:42:07 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 06 Nov 2025 18:42:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 06 Nov 2025 18:42:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 06 Nov 2025 18:42:27 GMT
VOLUME [/var/solr]
# Thu, 06 Nov 2025 18:42:27 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 06 Nov 2025 18:42:28 GMT
WORKDIR /opt/solr
# Thu, 06 Nov 2025 18:42:28 GMT
USER 8983
# Thu, 06 Nov 2025 18:42:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Nov 2025 18:42:28 GMT
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
	-	`sha256:0a45614bdc82ce0f88ae81279327dbd56cc811053d794ea3b373de7187e2062b`  
		Last Modified: Thu, 06 Nov 2025 18:43:11 GMT  
		Size: 66.0 MB (65967585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9b92042d8a0e14fd1f8ca14584afc5d73595ce569d67cef9aa61fc08931495`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1487f27c374bcb92656b0f7cf4858bae67b93e17c11665bf916a8046476f640a`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d08e7964d186b9facc1aaffcbdf3946405eae9ddbd0863d135cdc46c8e06fb5`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7842016f6edd6456e558f8dc164507cb194c69bafcc49549c24d9d4f5ea5d67`  
		Last Modified: Thu, 06 Nov 2025 18:43:01 GMT  
		Size: 1.6 MB (1630849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:520b612510202820bc19b335db516113343fbfb9bbf07ce4477ec12afca229b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f745c37ff4ec55164878a6f4543547a0e4fb651c9be1528c407e14e5ecf3a2f`

```dockerfile
```

-	Layers:
	-	`sha256:52e090a67949a2d9672cca0de93872d9671fa066a782f45850b6112bae1201f5`  
		Last Modified: Thu, 06 Nov 2025 20:58:58 GMT  
		Size: 4.0 MB (3968610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b412c93d4feaf0ac9a2b030be6f0a69395dd3ccec43b4a9c5b739de429645ca6`  
		Last Modified: Thu, 06 Nov 2025 20:58:59 GMT  
		Size: 34.4 KB (34418 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:6751b5bedcda362e76987db53a78525ec6cbde5be6322c6141a3589f9423d650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155727573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04a5c88f6cda250072be3d52c44b0e478335bf272dadc30319eee32cb513bfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:13:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:13:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:13:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:13:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:04:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_DIST=-slim
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 18:52:10 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 18:52:10 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 18:52:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 18:52:10 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 18:52:10 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 18:52:11 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 18:52:12 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 18:52:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 18:52:17 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 18:52:17 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 18:52:18 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 18:52:18 GMT
USER 8983
# Sat, 08 Nov 2025 18:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:52:18 GMT
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
	-	`sha256:1e8ef71fc27960d6d6980b8b41b32ea514a106133c40c77ef3d346eced1fc713`  
		Last Modified: Sat, 08 Nov 2025 18:05:07 GMT  
		Size: 44.0 MB (44030808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e2268ac0399bcec6155a7fe3748f7c6051355c43c47d1df67613156ec7406`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608005395bc2548d8f3fc84d04531dc648f2bef5aebca0ae1101d554fbfc97d7`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13f5ac86242f9ac0b877bb70716a889a145f1f75cf9a0205d61300d4a4671c5`  
		Last Modified: Sat, 08 Nov 2025 18:52:44 GMT  
		Size: 66.0 MB (65966962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677eaccb36699fbaf75cd29abdf762283a5de591572edd36da465002d3e024`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9c97d9ce0d83671daf2ceb896aeef1de8fcae7018f2082187f6b80de809d6a`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f395ca1c9714cb96ce2eec4f163d8dfcc5262965bd1e0342ab7b6ae795bfab`  
		Last Modified: Sat, 08 Nov 2025 18:52:49 GMT  
		Size: 10.8 KB (10804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f5684d46f1a4c5ae56b6f10b63cafb6872a7ae8dfe0010dc58ad3b332a3fc8`  
		Last Modified: Sat, 08 Nov 2025 18:52:50 GMT  
		Size: 1.6 MB (1558978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:4baf969b47d5c6192ba5afb504a61a04068496dda30eb04b76657193ff7add3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e344ef3551fa01ce6cabdfc75c8ba837b79c3a9c2496524c9854eb506c1047c3`

```dockerfile
```

-	Layers:
	-	`sha256:6b842a4b571b6a12ceb6750276bf117b9996eab4f9f85a9b0e067476a27df0b1`  
		Last Modified: Sat, 08 Nov 2025 20:58:53 GMT  
		Size: 4.0 MB (3966155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb428c0496da626ad0291a06521450ad4b131522a865a7c4fc740f95fc91177`  
		Last Modified: Sat, 08 Nov 2025 20:58:54 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json
