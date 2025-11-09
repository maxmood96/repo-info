## `solr:latest`

```console
$ docker pull solr@sha256:9765bae3bf17d872b8f2caa95bdff13da30b4d35c3007c49d76352ac35023342
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
$ docker pull solr@sha256:c05546d5b0f53b0c9c17cc4c49b5a14627cbc34886270542a1dc8b457320a411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.7 MB (489665801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffeebfd202deb05d4bbac1b7a7b3cd0df45392012f48b12888d192de20a8cdfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Thu, 02 Oct 2025 01:17:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Oct 2025 01:17:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Oct 2025 01:17:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Oct 2025 01:17:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 01:17:59 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:15:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:15:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:15:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:15:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 20:31:19 GMT
ARG SOLR_VERSION=9.10.0
# Sat, 08 Nov 2025 20:31:19 GMT
ARG SOLR_DIST=
# Sat, 08 Nov 2025 20:31:19 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Sat, 08 Nov 2025 20:31:19 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Sat, 08 Nov 2025 20:31:19 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 08 Nov 2025 20:31:19 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Sat, 08 Nov 2025 20:31:19 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 08 Nov 2025 20:31:19 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Sat, 08 Nov 2025 20:31:19 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 08 Nov 2025 20:31:19 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 08 Nov 2025 20:31:19 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 08 Nov 2025 20:31:19 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 08 Nov 2025 20:31:19 GMT
LABEL org.opencontainers.image.version=9.10.0
# Sat, 08 Nov 2025 20:31:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 08 Nov 2025 20:31:19 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 08 Nov 2025 20:31:19 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 08 Nov 2025 20:31:20 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Sat, 08 Nov 2025 20:31:20 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Sat, 08 Nov 2025 20:31:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Sat, 08 Nov 2025 20:31:29 GMT
VOLUME [/var/solr]
# Sat, 08 Nov 2025 20:31:29 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 08 Nov 2025 20:31:30 GMT
WORKDIR /opt/solr
# Sat, 08 Nov 2025 20:31:30 GMT
USER 8983
# Sat, 08 Nov 2025 20:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 20:31:30 GMT
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
	-	`sha256:0104670d5e6da865b4b88cd9bc61191ca43fd2ed27ab1483145fb0f36d46b694`  
		Last Modified: Sat, 08 Nov 2025 18:16:26 GMT  
		Size: 46.9 MB (46881233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8d2d4364d266318229f93a7df9d0933e2e24afe844e7e7d2b138d750b18bf`  
		Last Modified: Sat, 08 Nov 2025 18:16:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c76616592bb95c3807991245131992a94dc98152c99c7fa4347459ac97341d`  
		Last Modified: Sat, 08 Nov 2025 18:16:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa59f41a0e620739d68aad126ce854fcefa9deb992c7a861b1d5fd9aadef3020`  
		Last Modified: Sat, 08 Nov 2025 20:32:30 GMT  
		Size: 389.1 MB (389065445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad8b960c6d40c7123fa866a860f7749bad945aa28753ff9a09f8b53de4f8f58`  
		Last Modified: Sat, 08 Nov 2025 20:32:37 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45bf7e73c488c1f83c2d6717ac205ee75e6d912e8d3357e5e3def3dce27715f`  
		Last Modified: Sat, 08 Nov 2025 20:32:37 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bad63e2ec8fae3bbea6de59f41a5df04f74a1b778bc45d14eedf6d59775ed3a`  
		Last Modified: Sat, 08 Nov 2025 20:32:37 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7af10312c55b12c41566a3ff1db802da919a3081bd0647426dce7245367382b`  
		Last Modified: Sat, 08 Nov 2025 20:32:38 GMT  
		Size: 1.6 MB (1630817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:21199fb945bd95205f3b48c1a15706ad012e0143c3d78211879450ca68912d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834b0b68e3bd39af6b3f9716b53e1581b66852991a3c53139646f09aedb5814d`

```dockerfile
```

-	Layers:
	-	`sha256:84786650fb9ad13689c58965a1f72b45c10a7e4475204cf78defcaa728b2e675`  
		Last Modified: Sat, 08 Nov 2025 23:58:24 GMT  
		Size: 4.5 MB (4543752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b9f2f5f651891bf3b895ec799f2aa223c81509a19ede5367ae6f1ba720351f`  
		Last Modified: Sat, 08 Nov 2025 23:58:25 GMT  
		Size: 34.4 KB (34360 bytes)  
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
