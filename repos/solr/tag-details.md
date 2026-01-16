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
$ docker pull solr@sha256:9cc09d6681452681bc9121c815a3b3914c5e1c2e6c8ac7060ead1e5574aa03b1
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
$ docker pull solr@sha256:4e3281a953e1e7677d9e7072963639359adc579a2a66441ed2426f3898c6c80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483443041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484b8e9933b08710c8a185bf1c0316b23fc560becde45d0a354ff71148edcaa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:43 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:35:50 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:35:50 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:35:50 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:35:50 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:35:50 GMT
USER 8983
# Fri, 14 Nov 2025 00:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e780b6448e9fcbd386e57fc0127236f683fe2f65d97d0735b5ba5e63626e05f4`  
		Last Modified: Tue, 13 Jan 2026 03:04:02 GMT  
		Size: 389.1 MB (389064967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d8eb5d5688a4ea06162e591c7205198e53600ba53092c08bcacb51389a1588`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734bac102ccc37f3ab93cfa278a624c6b93f7e47eeefccd91ad53aae841ea1e`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2067c6be7bc6f45ecc74223dbd370617c87a6ec03bc22cc9d6bcc92caaf21dd`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 10.9 KB (10887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b748ff60cfb17a17f4bc5f8f1d362c4f3cc539c2a6c337aaba8738423146dc`  
		Last Modified: Tue, 13 Jan 2026 01:23:32 GMT  
		Size: 1.6 MB (1617938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:cba4f7d65ecd061458bdd7632c4b1e9028491e9dd7af98627a7db722755c90bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3280c2bb80206d2bb82b98866c604f55640d16b42e27134e12da0658e3f84161`

```dockerfile
```

-	Layers:
	-	`sha256:cd0d333605bd31938060b486dceb993b0dc8e21ed645c1d04043ebc66854c11a`  
		Last Modified: Tue, 13 Jan 2026 05:32:05 GMT  
		Size: 4.5 MB (4539699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6107657ecd586fe1302225c5867d15ca7d577daa119f0d0461e55566d3404c1`  
		Last Modified: Tue, 13 Jan 2026 05:32:04 GMT  
		Size: 34.3 KB (34307 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:f3a1fac578e93748dbca67913ab6e48b66d0cdbab2c26d7085b15d42a4ea8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480546239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc587a2f38c1bcaa610560c1d385a874795b92f3b26b05723b6a9074f2317cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:36:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:36:08 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:36:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:36:09 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:36:09 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:36:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:36:17 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:36:17 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:36:17 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:36:17 GMT
USER 8983
# Fri, 14 Nov 2025 00:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:17 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e8a0efe291a4f0cec1852e7a27ae5247c9aba0d3fbb94b2ccb10fd50dd9ff0`  
		Last Modified: Tue, 13 Jan 2026 05:40:26 GMT  
		Size: 389.1 MB (389065240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463e9887baf7fb87ac4fcfd13f24ccaf53effd855328dd28af3be6fe3d2c8b82`  
		Last Modified: Tue, 13 Jan 2026 01:24:52 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d766c279905383234c823e55a7e5392d61f0949b622bc2f9f31cde49dbb8f4a`  
		Last Modified: Tue, 13 Jan 2026 01:24:55 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4510d58c61fc56a7f8f12a99604474ea0f949c9557a4c995ee53d5497d26c5a`  
		Last Modified: Tue, 13 Jan 2026 01:24:56 GMT  
		Size: 10.9 KB (10886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf5a7d409faa4a9d1b88da54ec75c24d8017bc83426942fd70a1123570f8ea`  
		Last Modified: Tue, 13 Jan 2026 01:25:02 GMT  
		Size: 1.5 MB (1474808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:f718ef78f36eec53829f8e22d6554429856f866a1406736d90eef04747505b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4573846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1363ae3c879252ef415c827abec007d01f1211ba3071f8e6f535d3bfb88b4008`

```dockerfile
```

-	Layers:
	-	`sha256:c17f1fb8a16bc279fef4a42e8bd3e81be0cfadce9d9c200e14aa9c0398273280`  
		Last Modified: Tue, 13 Jan 2026 05:40:15 GMT  
		Size: 4.5 MB (4539375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9da6f21a0b2c5f54845d3ec318ba725285c84e06f787b6e83e20d9c8650bea`  
		Last Modified: Tue, 13 Jan 2026 05:40:14 GMT  
		Size: 34.5 KB (34471 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; ppc64le

```console
$ docker pull solr@sha256:1365dd69b9c196dac1e19ac77c654962b697a71a1fcfdf7af278b4863809627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.7 MB (489666110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c29f7cdb659e2132bfa1a9abf9d14a30ffd242304b7c3e6f2143a85dfaa588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 04:31:46 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 04:31:46 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 04:31:46 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 04:31:47 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 04:31:47 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 04:31:57 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 04:31:57 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 04:31:57 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 04:31:57 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 04:31:57 GMT
USER 8983
# Fri, 14 Nov 2025 04:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 04:31:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1a4d01af248389fc55dc07be999fb61aaf3790771097ec36981b3f4a82d54f`  
		Last Modified: Wed, 14 Jan 2026 19:53:39 GMT  
		Size: 389.1 MB (389065509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b9f4ec3295bc0c813a4d4b9c9df3b0ee3166501ffc1104391ae8b3e36522ac`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27b54999556b765a81b88931073200863c941418b3e937941c49a2af62b12de`  
		Last Modified: Tue, 13 Jan 2026 19:54:16 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59502c0008feea87e98877ecf40704cacc2e0e563146b2157f8a81e79f917dc5`  
		Last Modified: Tue, 13 Jan 2026 19:54:16 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2066f119df598b5375b20a7d39225c27bd4e3f9f4b16d0da166759d7ded983`  
		Last Modified: Wed, 14 Jan 2026 19:53:16 GMT  
		Size: 1.6 MB (1630924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:2f6ffaa0d23f0ee4461e3c064c31f8f049d4039717a43ad24e5969bc7613a3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8648388f7533dc048043a8d0fdf45c4af9a797c9a56cdd572b4c693fe68d3f53`

```dockerfile
```

-	Layers:
	-	`sha256:76878f45b530d9fc043ff643ed4fb533c2c464f3da20db05066033a53684e207`  
		Last Modified: Thu, 15 Jan 2026 01:03:01 GMT  
		Size: 4.5 MB (4543752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86ba99289ff949bfc110c7ec171062f29ddc9a169bcaeac9a7b29ef204d89d6`  
		Last Modified: Thu, 15 Jan 2026 01:03:00 GMT  
		Size: 34.4 KB (34360 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; s390x

```console
$ docker pull solr@sha256:5aef9f7191b5ad822adde27da21fda6c9d5727a95be555c3b0d92f1d49612123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.8 MB (478821645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ae68499340401fc6e4cd1d64750ab013541735883c92381f8351d95ff65d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_DIST=
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 22:59:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 22:59:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 22:59:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 22:59:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 22:59:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 22:59:33 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 22:59:33 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 22:59:33 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 22:59:33 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 22:59:33 GMT
USER 8983
# Thu, 15 Jan 2026 22:59:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:33 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc779feb1349838bef15e24d4230a9fd7a894de4f1481b9f60ffa8ac398a5ab`  
		Last Modified: Thu, 15 Jan 2026 23:00:50 GMT  
		Size: 389.1 MB (389064641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3b67c408a6233a5a9de7160df365b07034611d0e871890d0bc5ae2935694d6`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa4a9f9d5f55a9b4f6a20bc0cb3ff7adeb2e67925592d086cd34eee580bd889`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b9ef21656508227ffef603c885585c06a83be7df8f0fa49c2ff77e9fbb88`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b2ddd98ff1568f7043593b8254dc4768e3120fe48393163a3f6fd081c49bfe`  
		Last Modified: Thu, 15 Jan 2026 23:00:24 GMT  
		Size: 1.6 MB (1558915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:d75ccf90491d755be01a77a21b7a09641666738d6b279f7578192574c569dd0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e344c8aa3fb719618ca9fbdc415e1a97baf89f1ceb96835b33d5e010caa7789`

```dockerfile
```

-	Layers:
	-	`sha256:94cdb9505999847bdca2dccc37f60f4e4dfab5bf25f781f833c170427b4d1b11`  
		Last Modified: Thu, 15 Jan 2026 23:59:54 GMT  
		Size: 4.5 MB (4541307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76e0290ec8670aca27d1c780e87c8dabd6156a4653a43dd895894c95bfd7a595`  
		Last Modified: Thu, 15 Jan 2026 23:59:55 GMT  
		Size: 34.3 KB (34308 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9-slim`

```console
$ docker pull solr@sha256:616e6a30a46115d7a63a8bf78c6561c465595510be0858c2c08e91ebab901761
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
$ docker pull solr@sha256:312e9aea54a32811a43bf076dd5ab995f61aaf757fef43624630ae07c736fe89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160345232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfde5e40ebe42675499b306697cf5500bbf6779b2e9c04735f975a07a7b4dda4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:27 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:35:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:35:35 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:35:35 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:35:35 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:35:35 GMT
USER 8983
# Fri, 14 Nov 2025 00:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:35 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5447750fb19a6560e8c2542b39f1114e72621600e34f05840b59905f67f45b1c`  
		Last Modified: Tue, 13 Jan 2026 02:17:48 GMT  
		Size: 66.0 MB (65967198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6fc48a5d5b531498cfe22c2a6deafcea97641c5b15905d0b0b6bf5fcb441c9`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d09ae6cb9cdbefce05fc6bd747cae51f79a5f4c9dd2845c7294bda5de3fb502`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d546ae266e921fe6d9c2558837c70cc4647bbbda7e6f0edf1090ea0b1f28c`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 10.8 KB (10800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6230a4dad4beb67a5c79fa44d2ccf59a1cd46080c81807baeeb1bdbc0610090d`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 1.6 MB (1617979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:e171081c72963a33f4b8f72fc565090bca81111b3f24e61eddb7fdb3b7ed6563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36d121e431044233fe37728b82dd77cd1f883b8d409d4e1cadd9cc1048ac4a2`

```dockerfile
```

-	Layers:
	-	`sha256:c5057e6818814d3a2cf07fbe33432dcf6e242af534f7693e1d4ab79d29aa8e16`  
		Last Modified: Tue, 13 Jan 2026 04:56:36 GMT  
		Size: 4.0 MB (3964559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dfb26e314e2fb2185306c58acc85f027ac15905def86f0869800feb154b1209`  
		Last Modified: Tue, 13 Jan 2026 04:56:26 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:69106b4ac08ebc728cb30e72146c82314da23fd208947233cecd651e016e9338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157448199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9c1af8df56abb0bdb7c9b3297624b10f339f034c684ee82c28a6e7a55b7726`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:59 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:36:00 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:36:06 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:36:06 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:36:06 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:36:06 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:36:06 GMT
USER 8983
# Fri, 14 Nov 2025 00:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:06 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4f496ea89d577a3cc866a679850332736cfaa6ab638f040879f443f390e4e2`  
		Last Modified: Wed, 14 Jan 2026 09:08:27 GMT  
		Size: 66.0 MB (65967274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964c00e880758d0c3c88e86ae4d881ab717e1c348806313ec59e48f43ae7e189`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ea0d24facd340a636e91ba2011ac7ccb7b4e515d541d28c84806baf200c354`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf27a22c1b1a7cae544b3e2993a96889a32d33afbabe1723c0d905f5d1a314`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 10.8 KB (10803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3894133efebec657330190414c35c9788f4337b5b401e2b96e25093813680f7c`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 1.5 MB (1474815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:be492e2906d23c445a8575289e44bbbecba8ad4958c1a06a4617df63a99bb340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd2406f2ea1047d8b3ec8582815ab30258229961770bb29a673639d6718b73c`

```dockerfile
```

-	Layers:
	-	`sha256:55fbbf022b0b7571df220cdabbbfee33d316d2e6e5104f068a7b0bba9bb4a6f5`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 4.0 MB (3964235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb48fc445efdbbee0a22926eb743bef5b09c1156c511d0f7c4dd520c64e099ff`  
		Last Modified: Thu, 15 Jan 2026 01:13:48 GMT  
		Size: 34.5 KB (34535 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:a99e6082f0736afceb9e6c85390992c325ac6506eeb534f2b5c1db406981adfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166568120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda91e717d9ae00f166b5c20537afb86e5b0a71b101e49273a203bbdb14e3e2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 14:04:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 14:04:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 14:04:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 14:04:18 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 14:04:18 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 14:04:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 14:04:29 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 14:04:29 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 14:04:30 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 14:04:30 GMT
USER 8983
# Fri, 14 Nov 2025 14:04:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 14:04:30 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06f5ae29c6cff72a11a62824248910a854e775ecee4be4bc5bf9546d2ee83fc`  
		Last Modified: Thu, 15 Jan 2026 01:13:53 GMT  
		Size: 66.0 MB (65967575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd713f6377e2dc498f3d946ec705a29d94df4937304309a01ccfbdc1b960af9e`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 4.3 KB (4275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15cc300151d2eb660ebc114e6b0aad7a6531174ae9e18c679c3257d326e4af`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4a2dbdeeda970c2be87f66d1478b422be63e1f560e2a56fea4dec5ac6c580`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 10.8 KB (10802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9586fb2adb28afa6ca2af97103beed57c7c1d8e5c7f9425c542d406eae87d6bd`  
		Last Modified: Thu, 15 Jan 2026 01:13:53 GMT  
		Size: 1.6 MB (1630948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1b2d6786e20ab17a458b171f003edd2fa9a04f0b17a41489a05afe432132c297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a9548333b295fddabd640ccd93788df36ebc507520a55e38d68c138beb44d`

```dockerfile
```

-	Layers:
	-	`sha256:e96b4d198f15a8bbcbaea2a60e94c471f4ac99ca44c5c787ce1d071ef94c514d`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 4.0 MB (3968612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e72a7e7a35d5dacbea993e97df734f5de196474e77077d8f70040e55e508177`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 34.4 KB (34423 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:394d572789469b3075c0dec8e101b9650c089be6e7baeffa01c5b62a4d46fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155723785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019d7f18ec21f589094594f3989c7039c3bae51334c4131cfb0d0e1ebcc73ad4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DIST=-slim
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 22:59:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 22:59:58 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 22:59:58 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 22:59:58 GMT
USER 8983
# Thu, 15 Jan 2026 22:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:58 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1c7bd7f24e4f79699b9353cc94a420490b2385db8291d8779d31303119a64f`  
		Last Modified: Thu, 15 Jan 2026 23:00:46 GMT  
		Size: 66.0 MB (65966875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee3674b02d159e68fd01accec04080b7e00675d3cb6befaa16f6a90bca5d26`  
		Last Modified: Thu, 15 Jan 2026 23:00:21 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6f56235a90a5be2425b29583a71dce7afef6a88ed2e5061557d0adcc1b9c7d`  
		Last Modified: Thu, 15 Jan 2026 23:00:25 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a647bf99141242ed0894bb32c621167c63c3be8468b3010d3fde61bd5705df`  
		Last Modified: Thu, 15 Jan 2026 23:00:16 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffd466dd881958780804f22bff07b0609a4a64c7490dfcf3209f5cf985233e1`  
		Last Modified: Thu, 15 Jan 2026 23:00:26 GMT  
		Size: 1.6 MB (1558903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:d559c2a29105b9397cd9803fcc1f2887143954427f36092bb1ef28211944be3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150acf99bc0a7b4447f5041e95893d70bd01acec9edf0ab24abec0abb13ead90`

```dockerfile
```

-	Layers:
	-	`sha256:2c1e92858adae42e3560da7d9350524434f75674b46b14688d0d997815bb955b`  
		Last Modified: Thu, 15 Jan 2026 23:59:59 GMT  
		Size: 4.0 MB (3966167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d967474a68982e8450550b5af8291450a0222f2cb6c958b67d43be53c93dae0`  
		Last Modified: Fri, 16 Jan 2026 00:00:00 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.10`

```console
$ docker pull solr@sha256:9cc09d6681452681bc9121c815a3b3914c5e1c2e6c8ac7060ead1e5574aa03b1
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
$ docker pull solr@sha256:4e3281a953e1e7677d9e7072963639359adc579a2a66441ed2426f3898c6c80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483443041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484b8e9933b08710c8a185bf1c0316b23fc560becde45d0a354ff71148edcaa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:43 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:35:50 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:35:50 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:35:50 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:35:50 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:35:50 GMT
USER 8983
# Fri, 14 Nov 2025 00:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e780b6448e9fcbd386e57fc0127236f683fe2f65d97d0735b5ba5e63626e05f4`  
		Last Modified: Tue, 13 Jan 2026 03:04:02 GMT  
		Size: 389.1 MB (389064967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d8eb5d5688a4ea06162e591c7205198e53600ba53092c08bcacb51389a1588`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734bac102ccc37f3ab93cfa278a624c6b93f7e47eeefccd91ad53aae841ea1e`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2067c6be7bc6f45ecc74223dbd370617c87a6ec03bc22cc9d6bcc92caaf21dd`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 10.9 KB (10887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b748ff60cfb17a17f4bc5f8f1d362c4f3cc539c2a6c337aaba8738423146dc`  
		Last Modified: Tue, 13 Jan 2026 01:23:32 GMT  
		Size: 1.6 MB (1617938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10` - unknown; unknown

```console
$ docker pull solr@sha256:cba4f7d65ecd061458bdd7632c4b1e9028491e9dd7af98627a7db722755c90bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3280c2bb80206d2bb82b98866c604f55640d16b42e27134e12da0658e3f84161`

```dockerfile
```

-	Layers:
	-	`sha256:cd0d333605bd31938060b486dceb993b0dc8e21ed645c1d04043ebc66854c11a`  
		Last Modified: Tue, 13 Jan 2026 05:32:05 GMT  
		Size: 4.5 MB (4539699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6107657ecd586fe1302225c5867d15ca7d577daa119f0d0461e55566d3404c1`  
		Last Modified: Tue, 13 Jan 2026 05:32:04 GMT  
		Size: 34.3 KB (34307 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:f3a1fac578e93748dbca67913ab6e48b66d0cdbab2c26d7085b15d42a4ea8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480546239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc587a2f38c1bcaa610560c1d385a874795b92f3b26b05723b6a9074f2317cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:36:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:36:08 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:36:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:36:09 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:36:09 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:36:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:36:17 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:36:17 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:36:17 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:36:17 GMT
USER 8983
# Fri, 14 Nov 2025 00:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:17 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e8a0efe291a4f0cec1852e7a27ae5247c9aba0d3fbb94b2ccb10fd50dd9ff0`  
		Last Modified: Tue, 13 Jan 2026 05:40:26 GMT  
		Size: 389.1 MB (389065240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463e9887baf7fb87ac4fcfd13f24ccaf53effd855328dd28af3be6fe3d2c8b82`  
		Last Modified: Tue, 13 Jan 2026 01:24:52 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d766c279905383234c823e55a7e5392d61f0949b622bc2f9f31cde49dbb8f4a`  
		Last Modified: Tue, 13 Jan 2026 01:24:55 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4510d58c61fc56a7f8f12a99604474ea0f949c9557a4c995ee53d5497d26c5a`  
		Last Modified: Tue, 13 Jan 2026 01:24:56 GMT  
		Size: 10.9 KB (10886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf5a7d409faa4a9d1b88da54ec75c24d8017bc83426942fd70a1123570f8ea`  
		Last Modified: Tue, 13 Jan 2026 01:25:02 GMT  
		Size: 1.5 MB (1474808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10` - unknown; unknown

```console
$ docker pull solr@sha256:f718ef78f36eec53829f8e22d6554429856f866a1406736d90eef04747505b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4573846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1363ae3c879252ef415c827abec007d01f1211ba3071f8e6f535d3bfb88b4008`

```dockerfile
```

-	Layers:
	-	`sha256:c17f1fb8a16bc279fef4a42e8bd3e81be0cfadce9d9c200e14aa9c0398273280`  
		Last Modified: Tue, 13 Jan 2026 05:40:15 GMT  
		Size: 4.5 MB (4539375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9da6f21a0b2c5f54845d3ec318ba725285c84e06f787b6e83e20d9c8650bea`  
		Last Modified: Tue, 13 Jan 2026 05:40:14 GMT  
		Size: 34.5 KB (34471 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10` - linux; ppc64le

```console
$ docker pull solr@sha256:1365dd69b9c196dac1e19ac77c654962b697a71a1fcfdf7af278b4863809627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.7 MB (489666110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c29f7cdb659e2132bfa1a9abf9d14a30ffd242304b7c3e6f2143a85dfaa588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 04:31:46 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 04:31:46 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 04:31:46 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 04:31:47 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 04:31:47 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 04:31:57 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 04:31:57 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 04:31:57 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 04:31:57 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 04:31:57 GMT
USER 8983
# Fri, 14 Nov 2025 04:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 04:31:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1a4d01af248389fc55dc07be999fb61aaf3790771097ec36981b3f4a82d54f`  
		Last Modified: Wed, 14 Jan 2026 19:53:39 GMT  
		Size: 389.1 MB (389065509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b9f4ec3295bc0c813a4d4b9c9df3b0ee3166501ffc1104391ae8b3e36522ac`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27b54999556b765a81b88931073200863c941418b3e937941c49a2af62b12de`  
		Last Modified: Tue, 13 Jan 2026 19:54:16 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59502c0008feea87e98877ecf40704cacc2e0e563146b2157f8a81e79f917dc5`  
		Last Modified: Tue, 13 Jan 2026 19:54:16 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2066f119df598b5375b20a7d39225c27bd4e3f9f4b16d0da166759d7ded983`  
		Last Modified: Wed, 14 Jan 2026 19:53:16 GMT  
		Size: 1.6 MB (1630924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10` - unknown; unknown

```console
$ docker pull solr@sha256:2f6ffaa0d23f0ee4461e3c064c31f8f049d4039717a43ad24e5969bc7613a3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8648388f7533dc048043a8d0fdf45c4af9a797c9a56cdd572b4c693fe68d3f53`

```dockerfile
```

-	Layers:
	-	`sha256:76878f45b530d9fc043ff643ed4fb533c2c464f3da20db05066033a53684e207`  
		Last Modified: Thu, 15 Jan 2026 01:03:01 GMT  
		Size: 4.5 MB (4543752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86ba99289ff949bfc110c7ec171062f29ddc9a169bcaeac9a7b29ef204d89d6`  
		Last Modified: Thu, 15 Jan 2026 01:03:00 GMT  
		Size: 34.4 KB (34360 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10` - linux; s390x

```console
$ docker pull solr@sha256:5aef9f7191b5ad822adde27da21fda6c9d5727a95be555c3b0d92f1d49612123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.8 MB (478821645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ae68499340401fc6e4cd1d64750ab013541735883c92381f8351d95ff65d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_DIST=
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 22:59:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 22:59:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 22:59:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 22:59:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 22:59:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 22:59:33 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 22:59:33 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 22:59:33 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 22:59:33 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 22:59:33 GMT
USER 8983
# Thu, 15 Jan 2026 22:59:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:33 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc779feb1349838bef15e24d4230a9fd7a894de4f1481b9f60ffa8ac398a5ab`  
		Last Modified: Thu, 15 Jan 2026 23:00:50 GMT  
		Size: 389.1 MB (389064641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3b67c408a6233a5a9de7160df365b07034611d0e871890d0bc5ae2935694d6`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa4a9f9d5f55a9b4f6a20bc0cb3ff7adeb2e67925592d086cd34eee580bd889`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b9ef21656508227ffef603c885585c06a83be7df8f0fa49c2ff77e9fbb88`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b2ddd98ff1568f7043593b8254dc4768e3120fe48393163a3f6fd081c49bfe`  
		Last Modified: Thu, 15 Jan 2026 23:00:24 GMT  
		Size: 1.6 MB (1558915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10` - unknown; unknown

```console
$ docker pull solr@sha256:d75ccf90491d755be01a77a21b7a09641666738d6b279f7578192574c569dd0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e344c8aa3fb719618ca9fbdc415e1a97baf89f1ceb96835b33d5e010caa7789`

```dockerfile
```

-	Layers:
	-	`sha256:94cdb9505999847bdca2dccc37f60f4e4dfab5bf25f781f833c170427b4d1b11`  
		Last Modified: Thu, 15 Jan 2026 23:59:54 GMT  
		Size: 4.5 MB (4541307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76e0290ec8670aca27d1c780e87c8dabd6156a4653a43dd895894c95bfd7a595`  
		Last Modified: Thu, 15 Jan 2026 23:59:55 GMT  
		Size: 34.3 KB (34308 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.10-slim`

```console
$ docker pull solr@sha256:616e6a30a46115d7a63a8bf78c6561c465595510be0858c2c08e91ebab901761
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
$ docker pull solr@sha256:312e9aea54a32811a43bf076dd5ab995f61aaf757fef43624630ae07c736fe89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160345232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfde5e40ebe42675499b306697cf5500bbf6779b2e9c04735f975a07a7b4dda4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:27 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:35:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:35:35 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:35:35 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:35:35 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:35:35 GMT
USER 8983
# Fri, 14 Nov 2025 00:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:35 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5447750fb19a6560e8c2542b39f1114e72621600e34f05840b59905f67f45b1c`  
		Last Modified: Tue, 13 Jan 2026 02:17:48 GMT  
		Size: 66.0 MB (65967198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6fc48a5d5b531498cfe22c2a6deafcea97641c5b15905d0b0b6bf5fcb441c9`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d09ae6cb9cdbefce05fc6bd747cae51f79a5f4c9dd2845c7294bda5de3fb502`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d546ae266e921fe6d9c2558837c70cc4647bbbda7e6f0edf1090ea0b1f28c`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 10.8 KB (10800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6230a4dad4beb67a5c79fa44d2ccf59a1cd46080c81807baeeb1bdbc0610090d`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 1.6 MB (1617979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:e171081c72963a33f4b8f72fc565090bca81111b3f24e61eddb7fdb3b7ed6563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36d121e431044233fe37728b82dd77cd1f883b8d409d4e1cadd9cc1048ac4a2`

```dockerfile
```

-	Layers:
	-	`sha256:c5057e6818814d3a2cf07fbe33432dcf6e242af534f7693e1d4ab79d29aa8e16`  
		Last Modified: Tue, 13 Jan 2026 04:56:36 GMT  
		Size: 4.0 MB (3964559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dfb26e314e2fb2185306c58acc85f027ac15905def86f0869800feb154b1209`  
		Last Modified: Tue, 13 Jan 2026 04:56:26 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:69106b4ac08ebc728cb30e72146c82314da23fd208947233cecd651e016e9338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157448199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9c1af8df56abb0bdb7c9b3297624b10f339f034c684ee82c28a6e7a55b7726`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:59 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:36:00 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:36:06 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:36:06 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:36:06 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:36:06 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:36:06 GMT
USER 8983
# Fri, 14 Nov 2025 00:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:06 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4f496ea89d577a3cc866a679850332736cfaa6ab638f040879f443f390e4e2`  
		Last Modified: Wed, 14 Jan 2026 09:08:27 GMT  
		Size: 66.0 MB (65967274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964c00e880758d0c3c88e86ae4d881ab717e1c348806313ec59e48f43ae7e189`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ea0d24facd340a636e91ba2011ac7ccb7b4e515d541d28c84806baf200c354`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf27a22c1b1a7cae544b3e2993a96889a32d33afbabe1723c0d905f5d1a314`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 10.8 KB (10803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3894133efebec657330190414c35c9788f4337b5b401e2b96e25093813680f7c`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 1.5 MB (1474815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:be492e2906d23c445a8575289e44bbbecba8ad4958c1a06a4617df63a99bb340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd2406f2ea1047d8b3ec8582815ab30258229961770bb29a673639d6718b73c`

```dockerfile
```

-	Layers:
	-	`sha256:55fbbf022b0b7571df220cdabbbfee33d316d2e6e5104f068a7b0bba9bb4a6f5`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 4.0 MB (3964235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb48fc445efdbbee0a22926eb743bef5b09c1156c511d0f7c4dd520c64e099ff`  
		Last Modified: Thu, 15 Jan 2026 01:13:48 GMT  
		Size: 34.5 KB (34535 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:a99e6082f0736afceb9e6c85390992c325ac6506eeb534f2b5c1db406981adfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166568120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda91e717d9ae00f166b5c20537afb86e5b0a71b101e49273a203bbdb14e3e2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 14:04:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 14:04:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 14:04:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 14:04:18 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 14:04:18 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 14:04:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 14:04:29 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 14:04:29 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 14:04:30 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 14:04:30 GMT
USER 8983
# Fri, 14 Nov 2025 14:04:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 14:04:30 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06f5ae29c6cff72a11a62824248910a854e775ecee4be4bc5bf9546d2ee83fc`  
		Last Modified: Thu, 15 Jan 2026 01:13:53 GMT  
		Size: 66.0 MB (65967575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd713f6377e2dc498f3d946ec705a29d94df4937304309a01ccfbdc1b960af9e`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 4.3 KB (4275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15cc300151d2eb660ebc114e6b0aad7a6531174ae9e18c679c3257d326e4af`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4a2dbdeeda970c2be87f66d1478b422be63e1f560e2a56fea4dec5ac6c580`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 10.8 KB (10802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9586fb2adb28afa6ca2af97103beed57c7c1d8e5c7f9425c542d406eae87d6bd`  
		Last Modified: Thu, 15 Jan 2026 01:13:53 GMT  
		Size: 1.6 MB (1630948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1b2d6786e20ab17a458b171f003edd2fa9a04f0b17a41489a05afe432132c297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a9548333b295fddabd640ccd93788df36ebc507520a55e38d68c138beb44d`

```dockerfile
```

-	Layers:
	-	`sha256:e96b4d198f15a8bbcbaea2a60e94c471f4ac99ca44c5c787ce1d071ef94c514d`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 4.0 MB (3968612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e72a7e7a35d5dacbea993e97df734f5de196474e77077d8f70040e55e508177`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 34.4 KB (34423 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10-slim` - linux; s390x

```console
$ docker pull solr@sha256:394d572789469b3075c0dec8e101b9650c089be6e7baeffa01c5b62a4d46fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155723785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019d7f18ec21f589094594f3989c7039c3bae51334c4131cfb0d0e1ebcc73ad4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DIST=-slim
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 22:59:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 22:59:58 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 22:59:58 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 22:59:58 GMT
USER 8983
# Thu, 15 Jan 2026 22:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:58 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1c7bd7f24e4f79699b9353cc94a420490b2385db8291d8779d31303119a64f`  
		Last Modified: Thu, 15 Jan 2026 23:00:46 GMT  
		Size: 66.0 MB (65966875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee3674b02d159e68fd01accec04080b7e00675d3cb6befaa16f6a90bca5d26`  
		Last Modified: Thu, 15 Jan 2026 23:00:21 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6f56235a90a5be2425b29583a71dce7afef6a88ed2e5061557d0adcc1b9c7d`  
		Last Modified: Thu, 15 Jan 2026 23:00:25 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a647bf99141242ed0894bb32c621167c63c3be8468b3010d3fde61bd5705df`  
		Last Modified: Thu, 15 Jan 2026 23:00:16 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffd466dd881958780804f22bff07b0609a4a64c7490dfcf3209f5cf985233e1`  
		Last Modified: Thu, 15 Jan 2026 23:00:26 GMT  
		Size: 1.6 MB (1558903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:d559c2a29105b9397cd9803fcc1f2887143954427f36092bb1ef28211944be3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150acf99bc0a7b4447f5041e95893d70bd01acec9edf0ab24abec0abb13ead90`

```dockerfile
```

-	Layers:
	-	`sha256:2c1e92858adae42e3560da7d9350524434f75674b46b14688d0d997815bb955b`  
		Last Modified: Thu, 15 Jan 2026 23:59:59 GMT  
		Size: 4.0 MB (3966167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d967474a68982e8450550b5af8291450a0222f2cb6c958b67d43be53c93dae0`  
		Last Modified: Fri, 16 Jan 2026 00:00:00 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.10.0`

```console
$ docker pull solr@sha256:9cc09d6681452681bc9121c815a3b3914c5e1c2e6c8ac7060ead1e5574aa03b1
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
$ docker pull solr@sha256:4e3281a953e1e7677d9e7072963639359adc579a2a66441ed2426f3898c6c80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483443041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484b8e9933b08710c8a185bf1c0316b23fc560becde45d0a354ff71148edcaa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:43 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:35:50 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:35:50 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:35:50 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:35:50 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:35:50 GMT
USER 8983
# Fri, 14 Nov 2025 00:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e780b6448e9fcbd386e57fc0127236f683fe2f65d97d0735b5ba5e63626e05f4`  
		Last Modified: Tue, 13 Jan 2026 03:04:02 GMT  
		Size: 389.1 MB (389064967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d8eb5d5688a4ea06162e591c7205198e53600ba53092c08bcacb51389a1588`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734bac102ccc37f3ab93cfa278a624c6b93f7e47eeefccd91ad53aae841ea1e`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2067c6be7bc6f45ecc74223dbd370617c87a6ec03bc22cc9d6bcc92caaf21dd`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 10.9 KB (10887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b748ff60cfb17a17f4bc5f8f1d362c4f3cc539c2a6c337aaba8738423146dc`  
		Last Modified: Tue, 13 Jan 2026 01:23:32 GMT  
		Size: 1.6 MB (1617938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0` - unknown; unknown

```console
$ docker pull solr@sha256:cba4f7d65ecd061458bdd7632c4b1e9028491e9dd7af98627a7db722755c90bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3280c2bb80206d2bb82b98866c604f55640d16b42e27134e12da0658e3f84161`

```dockerfile
```

-	Layers:
	-	`sha256:cd0d333605bd31938060b486dceb993b0dc8e21ed645c1d04043ebc66854c11a`  
		Last Modified: Tue, 13 Jan 2026 05:32:05 GMT  
		Size: 4.5 MB (4539699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6107657ecd586fe1302225c5867d15ca7d577daa119f0d0461e55566d3404c1`  
		Last Modified: Tue, 13 Jan 2026 05:32:04 GMT  
		Size: 34.3 KB (34307 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:f3a1fac578e93748dbca67913ab6e48b66d0cdbab2c26d7085b15d42a4ea8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480546239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc587a2f38c1bcaa610560c1d385a874795b92f3b26b05723b6a9074f2317cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:36:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:36:08 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:36:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:36:09 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:36:09 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:36:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:36:17 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:36:17 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:36:17 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:36:17 GMT
USER 8983
# Fri, 14 Nov 2025 00:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:17 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e8a0efe291a4f0cec1852e7a27ae5247c9aba0d3fbb94b2ccb10fd50dd9ff0`  
		Last Modified: Tue, 13 Jan 2026 05:40:26 GMT  
		Size: 389.1 MB (389065240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463e9887baf7fb87ac4fcfd13f24ccaf53effd855328dd28af3be6fe3d2c8b82`  
		Last Modified: Tue, 13 Jan 2026 01:24:52 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d766c279905383234c823e55a7e5392d61f0949b622bc2f9f31cde49dbb8f4a`  
		Last Modified: Tue, 13 Jan 2026 01:24:55 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4510d58c61fc56a7f8f12a99604474ea0f949c9557a4c995ee53d5497d26c5a`  
		Last Modified: Tue, 13 Jan 2026 01:24:56 GMT  
		Size: 10.9 KB (10886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf5a7d409faa4a9d1b88da54ec75c24d8017bc83426942fd70a1123570f8ea`  
		Last Modified: Tue, 13 Jan 2026 01:25:02 GMT  
		Size: 1.5 MB (1474808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0` - unknown; unknown

```console
$ docker pull solr@sha256:f718ef78f36eec53829f8e22d6554429856f866a1406736d90eef04747505b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4573846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1363ae3c879252ef415c827abec007d01f1211ba3071f8e6f535d3bfb88b4008`

```dockerfile
```

-	Layers:
	-	`sha256:c17f1fb8a16bc279fef4a42e8bd3e81be0cfadce9d9c200e14aa9c0398273280`  
		Last Modified: Tue, 13 Jan 2026 05:40:15 GMT  
		Size: 4.5 MB (4539375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9da6f21a0b2c5f54845d3ec318ba725285c84e06f787b6e83e20d9c8650bea`  
		Last Modified: Tue, 13 Jan 2026 05:40:14 GMT  
		Size: 34.5 KB (34471 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10.0` - linux; ppc64le

```console
$ docker pull solr@sha256:1365dd69b9c196dac1e19ac77c654962b697a71a1fcfdf7af278b4863809627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.7 MB (489666110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c29f7cdb659e2132bfa1a9abf9d14a30ffd242304b7c3e6f2143a85dfaa588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 04:31:46 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 04:31:46 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 04:31:46 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 04:31:47 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 04:31:47 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 04:31:57 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 04:31:57 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 04:31:57 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 04:31:57 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 04:31:57 GMT
USER 8983
# Fri, 14 Nov 2025 04:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 04:31:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1a4d01af248389fc55dc07be999fb61aaf3790771097ec36981b3f4a82d54f`  
		Last Modified: Wed, 14 Jan 2026 19:53:39 GMT  
		Size: 389.1 MB (389065509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b9f4ec3295bc0c813a4d4b9c9df3b0ee3166501ffc1104391ae8b3e36522ac`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27b54999556b765a81b88931073200863c941418b3e937941c49a2af62b12de`  
		Last Modified: Tue, 13 Jan 2026 19:54:16 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59502c0008feea87e98877ecf40704cacc2e0e563146b2157f8a81e79f917dc5`  
		Last Modified: Tue, 13 Jan 2026 19:54:16 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2066f119df598b5375b20a7d39225c27bd4e3f9f4b16d0da166759d7ded983`  
		Last Modified: Wed, 14 Jan 2026 19:53:16 GMT  
		Size: 1.6 MB (1630924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0` - unknown; unknown

```console
$ docker pull solr@sha256:2f6ffaa0d23f0ee4461e3c064c31f8f049d4039717a43ad24e5969bc7613a3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8648388f7533dc048043a8d0fdf45c4af9a797c9a56cdd572b4c693fe68d3f53`

```dockerfile
```

-	Layers:
	-	`sha256:76878f45b530d9fc043ff643ed4fb533c2c464f3da20db05066033a53684e207`  
		Last Modified: Thu, 15 Jan 2026 01:03:01 GMT  
		Size: 4.5 MB (4543752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86ba99289ff949bfc110c7ec171062f29ddc9a169bcaeac9a7b29ef204d89d6`  
		Last Modified: Thu, 15 Jan 2026 01:03:00 GMT  
		Size: 34.4 KB (34360 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10.0` - linux; s390x

```console
$ docker pull solr@sha256:5aef9f7191b5ad822adde27da21fda6c9d5727a95be555c3b0d92f1d49612123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.8 MB (478821645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ae68499340401fc6e4cd1d64750ab013541735883c92381f8351d95ff65d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_DIST=
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 22:59:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 22:59:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 22:59:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 22:59:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 22:59:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 22:59:33 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 22:59:33 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 22:59:33 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 22:59:33 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 22:59:33 GMT
USER 8983
# Thu, 15 Jan 2026 22:59:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:33 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc779feb1349838bef15e24d4230a9fd7a894de4f1481b9f60ffa8ac398a5ab`  
		Last Modified: Thu, 15 Jan 2026 23:00:50 GMT  
		Size: 389.1 MB (389064641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3b67c408a6233a5a9de7160df365b07034611d0e871890d0bc5ae2935694d6`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa4a9f9d5f55a9b4f6a20bc0cb3ff7adeb2e67925592d086cd34eee580bd889`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b9ef21656508227ffef603c885585c06a83be7df8f0fa49c2ff77e9fbb88`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b2ddd98ff1568f7043593b8254dc4768e3120fe48393163a3f6fd081c49bfe`  
		Last Modified: Thu, 15 Jan 2026 23:00:24 GMT  
		Size: 1.6 MB (1558915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0` - unknown; unknown

```console
$ docker pull solr@sha256:d75ccf90491d755be01a77a21b7a09641666738d6b279f7578192574c569dd0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e344c8aa3fb719618ca9fbdc415e1a97baf89f1ceb96835b33d5e010caa7789`

```dockerfile
```

-	Layers:
	-	`sha256:94cdb9505999847bdca2dccc37f60f4e4dfab5bf25f781f833c170427b4d1b11`  
		Last Modified: Thu, 15 Jan 2026 23:59:54 GMT  
		Size: 4.5 MB (4541307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76e0290ec8670aca27d1c780e87c8dabd6156a4653a43dd895894c95bfd7a595`  
		Last Modified: Thu, 15 Jan 2026 23:59:55 GMT  
		Size: 34.3 KB (34308 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.10.0-slim`

```console
$ docker pull solr@sha256:616e6a30a46115d7a63a8bf78c6561c465595510be0858c2c08e91ebab901761
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
$ docker pull solr@sha256:312e9aea54a32811a43bf076dd5ab995f61aaf757fef43624630ae07c736fe89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160345232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfde5e40ebe42675499b306697cf5500bbf6779b2e9c04735f975a07a7b4dda4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:27 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:35:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:35:35 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:35:35 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:35:35 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:35:35 GMT
USER 8983
# Fri, 14 Nov 2025 00:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:35 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5447750fb19a6560e8c2542b39f1114e72621600e34f05840b59905f67f45b1c`  
		Last Modified: Tue, 13 Jan 2026 02:17:48 GMT  
		Size: 66.0 MB (65967198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6fc48a5d5b531498cfe22c2a6deafcea97641c5b15905d0b0b6bf5fcb441c9`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d09ae6cb9cdbefce05fc6bd747cae51f79a5f4c9dd2845c7294bda5de3fb502`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d546ae266e921fe6d9c2558837c70cc4647bbbda7e6f0edf1090ea0b1f28c`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 10.8 KB (10800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6230a4dad4beb67a5c79fa44d2ccf59a1cd46080c81807baeeb1bdbc0610090d`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 1.6 MB (1617979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:e171081c72963a33f4b8f72fc565090bca81111b3f24e61eddb7fdb3b7ed6563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36d121e431044233fe37728b82dd77cd1f883b8d409d4e1cadd9cc1048ac4a2`

```dockerfile
```

-	Layers:
	-	`sha256:c5057e6818814d3a2cf07fbe33432dcf6e242af534f7693e1d4ab79d29aa8e16`  
		Last Modified: Tue, 13 Jan 2026 04:56:36 GMT  
		Size: 4.0 MB (3964559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dfb26e314e2fb2185306c58acc85f027ac15905def86f0869800feb154b1209`  
		Last Modified: Tue, 13 Jan 2026 04:56:26 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:69106b4ac08ebc728cb30e72146c82314da23fd208947233cecd651e016e9338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157448199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9c1af8df56abb0bdb7c9b3297624b10f339f034c684ee82c28a6e7a55b7726`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:59 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:36:00 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:36:06 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:36:06 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:36:06 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:36:06 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:36:06 GMT
USER 8983
# Fri, 14 Nov 2025 00:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:06 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4f496ea89d577a3cc866a679850332736cfaa6ab638f040879f443f390e4e2`  
		Last Modified: Wed, 14 Jan 2026 09:08:27 GMT  
		Size: 66.0 MB (65967274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964c00e880758d0c3c88e86ae4d881ab717e1c348806313ec59e48f43ae7e189`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ea0d24facd340a636e91ba2011ac7ccb7b4e515d541d28c84806baf200c354`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf27a22c1b1a7cae544b3e2993a96889a32d33afbabe1723c0d905f5d1a314`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 10.8 KB (10803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3894133efebec657330190414c35c9788f4337b5b401e2b96e25093813680f7c`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 1.5 MB (1474815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:be492e2906d23c445a8575289e44bbbecba8ad4958c1a06a4617df63a99bb340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd2406f2ea1047d8b3ec8582815ab30258229961770bb29a673639d6718b73c`

```dockerfile
```

-	Layers:
	-	`sha256:55fbbf022b0b7571df220cdabbbfee33d316d2e6e5104f068a7b0bba9bb4a6f5`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 4.0 MB (3964235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb48fc445efdbbee0a22926eb743bef5b09c1156c511d0f7c4dd520c64e099ff`  
		Last Modified: Thu, 15 Jan 2026 01:13:48 GMT  
		Size: 34.5 KB (34535 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10.0-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:a99e6082f0736afceb9e6c85390992c325ac6506eeb534f2b5c1db406981adfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166568120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda91e717d9ae00f166b5c20537afb86e5b0a71b101e49273a203bbdb14e3e2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 14:04:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 14:04:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 14:04:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 14:04:18 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 14:04:18 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 14:04:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 14:04:29 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 14:04:29 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 14:04:30 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 14:04:30 GMT
USER 8983
# Fri, 14 Nov 2025 14:04:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 14:04:30 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06f5ae29c6cff72a11a62824248910a854e775ecee4be4bc5bf9546d2ee83fc`  
		Last Modified: Thu, 15 Jan 2026 01:13:53 GMT  
		Size: 66.0 MB (65967575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd713f6377e2dc498f3d946ec705a29d94df4937304309a01ccfbdc1b960af9e`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 4.3 KB (4275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15cc300151d2eb660ebc114e6b0aad7a6531174ae9e18c679c3257d326e4af`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4a2dbdeeda970c2be87f66d1478b422be63e1f560e2a56fea4dec5ac6c580`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 10.8 KB (10802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9586fb2adb28afa6ca2af97103beed57c7c1d8e5c7f9425c542d406eae87d6bd`  
		Last Modified: Thu, 15 Jan 2026 01:13:53 GMT  
		Size: 1.6 MB (1630948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1b2d6786e20ab17a458b171f003edd2fa9a04f0b17a41489a05afe432132c297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a9548333b295fddabd640ccd93788df36ebc507520a55e38d68c138beb44d`

```dockerfile
```

-	Layers:
	-	`sha256:e96b4d198f15a8bbcbaea2a60e94c471f4ac99ca44c5c787ce1d071ef94c514d`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 4.0 MB (3968612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e72a7e7a35d5dacbea993e97df734f5de196474e77077d8f70040e55e508177`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 34.4 KB (34423 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.10.0-slim` - linux; s390x

```console
$ docker pull solr@sha256:394d572789469b3075c0dec8e101b9650c089be6e7baeffa01c5b62a4d46fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155723785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019d7f18ec21f589094594f3989c7039c3bae51334c4131cfb0d0e1ebcc73ad4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DIST=-slim
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 22:59:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 22:59:58 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 22:59:58 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 22:59:58 GMT
USER 8983
# Thu, 15 Jan 2026 22:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:58 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1c7bd7f24e4f79699b9353cc94a420490b2385db8291d8779d31303119a64f`  
		Last Modified: Thu, 15 Jan 2026 23:00:46 GMT  
		Size: 66.0 MB (65966875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee3674b02d159e68fd01accec04080b7e00675d3cb6befaa16f6a90bca5d26`  
		Last Modified: Thu, 15 Jan 2026 23:00:21 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6f56235a90a5be2425b29583a71dce7afef6a88ed2e5061557d0adcc1b9c7d`  
		Last Modified: Thu, 15 Jan 2026 23:00:25 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a647bf99141242ed0894bb32c621167c63c3be8468b3010d3fde61bd5705df`  
		Last Modified: Thu, 15 Jan 2026 23:00:16 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffd466dd881958780804f22bff07b0609a4a64c7490dfcf3209f5cf985233e1`  
		Last Modified: Thu, 15 Jan 2026 23:00:26 GMT  
		Size: 1.6 MB (1558903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.10.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:d559c2a29105b9397cd9803fcc1f2887143954427f36092bb1ef28211944be3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150acf99bc0a7b4447f5041e95893d70bd01acec9edf0ab24abec0abb13ead90`

```dockerfile
```

-	Layers:
	-	`sha256:2c1e92858adae42e3560da7d9350524434f75674b46b14688d0d997815bb955b`  
		Last Modified: Thu, 15 Jan 2026 23:59:59 GMT  
		Size: 4.0 MB (3966167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d967474a68982e8450550b5af8291450a0222f2cb6c958b67d43be53c93dae0`  
		Last Modified: Fri, 16 Jan 2026 00:00:00 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.9`

```console
$ docker pull solr@sha256:87e57b6ab760e3182718c3f47b8bc492f9cb47da41aa26d9ab8260c17c5574f7
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
$ docker pull solr@sha256:761a1581a6b214b2cca93189821be3f8c1307e9201f635e2aaf7e7f2d6e6f332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.2 MB (483209058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b0a77304ab46c5d7b2f8cee19d6c080ee67d5b10365c89664e65ac54b3f8c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:05:59 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 01:05:59 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 01:05:59 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Fri, 14 Nov 2025 01:05:59 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 01:05:59 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 01:05:59 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 01:05:59 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 01:06:00 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 01:06:00 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 01:06:00 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 01:06:06 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 01:06:06 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 01:06:06 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 01:06:06 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 01:06:06 GMT
USER 8983
# Fri, 14 Nov 2025 01:06:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 01:06:06 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7f9fc3ed7a65b326c76083bb9b87438f2c70f475c70aa89e117a928578c99f`  
		Last Modified: Tue, 13 Jan 2026 04:59:17 GMT  
		Size: 388.8 MB (388830955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1d51b45870daf28adf6f438924342b30c2f80aec0445bf3fc8ac38605d8996`  
		Last Modified: Tue, 13 Jan 2026 04:13:19 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c76e1f39cbd744a18346c1b30c2c25c19582d86a86b8c4b30c7db8c536e106e`  
		Last Modified: Tue, 13 Jan 2026 04:13:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66d7047db406697d73ec6983abde43579c8da748241b169da8ab660fe583240`  
		Last Modified: Tue, 13 Jan 2026 04:13:20 GMT  
		Size: 10.9 KB (10888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f0fc80d8aa8be7916250d721649ea73069cdccd2072d27894c7d38d38046e`  
		Last Modified: Tue, 13 Jan 2026 04:13:20 GMT  
		Size: 1.6 MB (1617967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9` - unknown; unknown

```console
$ docker pull solr@sha256:0983006436f0f03bbcd61ebd7d1306058394342fbb24252c23e61aa4869ff486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4583246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5a6875c8d50f3a9743eedfc9cbdf6a87e4bc464d12babfb3147b768b873729`

```dockerfile
```

-	Layers:
	-	`sha256:dc705ef5f0cffc11ed1dd7c785f5fdffc5ba65d8f818131b7f914205c7870a7f`  
		Last Modified: Tue, 13 Jan 2026 10:23:10 GMT  
		Size: 4.5 MB (4549527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2a8b2aab65f0a042734cd3202c5ed16eb16a47027afd1ea15b9c16e7351735`  
		Last Modified: Tue, 13 Jan 2026 10:23:08 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:0d1cce2a9a4a9ce8379e547ecea96809d4d4fbdde3e69f52eaa191d433fa69be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480312021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0cb0d81a209c2e3efee558cd04198bef95f7436495c2e7462e3ffadca6a1e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:23:42 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 01:23:42 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 01:23:42 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Fri, 14 Nov 2025 01:23:42 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 01:23:42 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 01:23:42 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 01:23:42 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 01:23:42 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 01:23:42 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 01:23:42 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 01:23:49 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 01:23:49 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 01:23:49 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 01:23:49 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 01:23:49 GMT
USER 8983
# Fri, 14 Nov 2025 01:23:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 01:23:49 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc99619d40c068548eeeea0c20eb144d97057500de8415fa284038cb2dbb16b`  
		Last Modified: Tue, 13 Jan 2026 08:11:25 GMT  
		Size: 388.8 MB (388830994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fcfc8c91c80cfa0ca5b987b2d9e39601da5d81ace9d65e682bddb6aee05347`  
		Last Modified: Tue, 13 Jan 2026 08:11:14 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a447bcac8cb1b0c8aa3e6dd674fecf6381745cb6b0bc40510449520e36336b13`  
		Last Modified: Tue, 13 Jan 2026 08:11:15 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b9088f3d4994305ab2c6068b6d829b3fb80df1f49ca32834725eeb9ba6acdf`  
		Last Modified: Tue, 13 Jan 2026 08:11:15 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2458c3e05a9c1a3413657edcaaf4dafe31b0e3c4afc736788a10903c682886c1`  
		Last Modified: Tue, 13 Jan 2026 08:11:16 GMT  
		Size: 1.5 MB (1474830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9` - unknown; unknown

```console
$ docker pull solr@sha256:6674c3a7711b5977f8c0360c8ebdf7196a281dd1a0e19f0ebdfe409e5955901f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4583038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268f47cbba218b3670b213ebd6366c740243b6f400c3c1a530dc0d19b076b6ed`

```dockerfile
```

-	Layers:
	-	`sha256:a1361bead7505d778fed2da10567809800f93ed14b2267f226d3d99bcf409fe7`  
		Last Modified: Thu, 15 Jan 2026 00:56:12 GMT  
		Size: 4.5 MB (4549179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd97af7fa6a19e0262cd9fb0bf1fb2d4e76406e125dc74403514f25553061f83`  
		Last Modified: Thu, 15 Jan 2026 00:56:10 GMT  
		Size: 33.9 KB (33859 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9` - linux; ppc64le

```console
$ docker pull solr@sha256:a06a2f08cbcc181fe3d5c0591ca83f62bd87014db99b62e8909406b7d6901b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.4 MB (489431933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4d0678af8b848a2808680f62ba01d0d1d35a13cf6dce844fc615b00e395b33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 05:08:15 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 05:08:15 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 05:08:15 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Fri, 14 Nov 2025 05:08:15 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 05:08:15 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 05:08:15 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 05:08:15 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 05:08:16 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 05:08:16 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 05:08:16 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 05:08:25 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 05:08:25 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 05:08:25 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 05:08:25 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 05:08:25 GMT
USER 8983
# Fri, 14 Nov 2025 05:08:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 05:08:25 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31186313e6962e688550330ca7a06aee0804e90eaf9b42b1ff9ebd9f2cf09e3`  
		Last Modified: Thu, 15 Jan 2026 00:56:30 GMT  
		Size: 388.8 MB (388831323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c7aee70c50cbaded2816003e3f8e64c3343b7cb50f6b856260d09bf2920b0`  
		Last Modified: Thu, 15 Jan 2026 00:56:11 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3a4a3018a90b682de6cb1fbf85bfb1e2949c76c1a6cd5af86ec6116bc69146`  
		Last Modified: Thu, 15 Jan 2026 00:56:11 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d9002ed5c942e9c87c8413a0cfb5a0cb5e8a3cdc116330c353057b7ab46085`  
		Last Modified: Thu, 15 Jan 2026 00:56:11 GMT  
		Size: 10.9 KB (10892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd39b05194299ccdfc485ffc7fcd012e01304ee980bf4de11b276a4361a8649`  
		Last Modified: Thu, 15 Jan 2026 00:56:14 GMT  
		Size: 1.6 MB (1630929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9` - unknown; unknown

```console
$ docker pull solr@sha256:0a07635a5b11a7129918e9b1caf43838f979425ec767b922f5b4ef110b1c1b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4587327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cbdf555971df3bb3383cfd23a49b966353196605c7895b895021b63fb05973`

```dockerfile
```

-	Layers:
	-	`sha256:e82e0301ba36effaa5d84847d09b9609909ddbbf33cb3e6038cd9a6ee53d8477`  
		Last Modified: Thu, 15 Jan 2026 00:56:17 GMT  
		Size: 4.6 MB (4553568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aaf09fdb93f68953d40edd3838609c99deb27bf87a12dd7e3c5006eecddc384`  
		Last Modified: Thu, 15 Jan 2026 00:56:15 GMT  
		Size: 33.8 KB (33759 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9` - linux; s390x

```console
$ docker pull solr@sha256:ea3f61584d89ac8dcdbb36801995ed266552de443b9afe1bb8d91edd9d3127ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.6 MB (478587635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b319728a81982ec30f9d7a69ea471d2364803cd43b5007e933bdd376671a7f34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:00:04 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 15 Jan 2026 23:00:04 GMT
ARG SOLR_DIST=
# Thu, 15 Jan 2026 23:00:04 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 15 Jan 2026 23:00:04 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 15 Jan 2026 23:00:04 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 23:00:04 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 23:00:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 23:00:04 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 23:00:04 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 23:00:05 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 23:00:07 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 23:00:07 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 23:00:07 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 23:00:07 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 23:00:07 GMT
USER 8983
# Thu, 15 Jan 2026 23:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:00:07 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c15eabc6c828402d0f52290257aa3c1c8fb9c8e1e855b616aa144564ee516b`  
		Last Modified: Thu, 15 Jan 2026 23:01:38 GMT  
		Size: 388.8 MB (388830624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302690fb47612b707b412f19a6157098e975db36329fe756850cc3456b56de80`  
		Last Modified: Thu, 15 Jan 2026 23:00:56 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e05006a8aab44fd82e506cd4e753804c826880639ec0c0de2987cc762d2a60f`  
		Last Modified: Thu, 15 Jan 2026 23:00:56 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96596ae1affa36478c1258533a81d8cfd2945fa42a0a81b7e15dd966884b1477`  
		Last Modified: Thu, 15 Jan 2026 23:00:55 GMT  
		Size: 10.9 KB (10895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5809c1f57c03f352f79c28d29ea9046596f3c4cc309caaadffbdb7f57fb09c`  
		Last Modified: Thu, 15 Jan 2026 23:00:56 GMT  
		Size: 1.6 MB (1558912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9` - unknown; unknown

```console
$ docker pull solr@sha256:94ba8eafa626c8a27e8a773f73f93b46ef86f3cc75be8c461017377bfd15f82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22337fcbe66be8931e47e9b28182f510d7d06f9fc66875a535489a8a3b9f4ba7`

```dockerfile
```

-	Layers:
	-	`sha256:6435ab25642e1c0278cd1b5400602d2495aaa3fda1edf195b2c51e6884745801`  
		Last Modified: Fri, 16 Jan 2026 00:00:36 GMT  
		Size: 4.6 MB (4551135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efe75207fead6c9511f62c298bd4c0a12cb5b75302170ca2967999c56aba2f64`  
		Last Modified: Fri, 16 Jan 2026 00:00:37 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.9-slim`

```console
$ docker pull solr@sha256:220aac3989fbf6f20dca4a8f9bab9bed7ee338d9dd7db84402b8887a02e3c1a9
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
$ docker pull solr@sha256:0ba506aaf6497feef5f921cfa8e82086c73930b8697c9ac5aa9617b728904ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159996568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66401b6776c033405113511a174610b065322b877e59932b4f8573f95cffb42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:47:12 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 00:47:12 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:47:12 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Fri, 14 Nov 2025 00:47:12 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 00:47:12 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:47:12 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:47:12 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:47:12 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:47:12 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:47:12 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:47:20 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:47:20 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:47:20 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:47:20 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:47:20 GMT
USER 8983
# Fri, 14 Nov 2025 00:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:47:20 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99489bcb68ac1c4a394151b66e498bcb745faf6f65234ba3535b456eca4e87c9`  
		Last Modified: Tue, 13 Jan 2026 05:26:07 GMT  
		Size: 65.6 MB (65618531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031fcaa45c2b5aeaba2a41badf93830576bb59a7624fd2fe1f215cb2dbc5e331`  
		Last Modified: Tue, 13 Jan 2026 05:01:43 GMT  
		Size: 4.3 KB (4279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2676a22fdd93f9bb42915ad157099ecbaf4d0e4f2cd9b9f34ae213f6e4a01238`  
		Last Modified: Tue, 13 Jan 2026 05:25:54 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b3a8b880cd2c6b76933f8cf2cf4e42ad0622c70ab868f7ff939b6cb7b510eb`  
		Last Modified: Tue, 13 Jan 2026 05:25:56 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd339c74eb0bcfaa836161914654cceec116f06f5c6963a1423e461ce75f2ce`  
		Last Modified: Tue, 13 Jan 2026 05:02:03 GMT  
		Size: 1.6 MB (1617974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:bfcb7eb636b30e182ba51c1eca69d6246a6af4aab521973db9a3a25ed3155995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeeb5790adbaeb3c069deef15e35f0fb89292454e84efa7b140e0773affd9e2`

```dockerfile
```

-	Layers:
	-	`sha256:fe7403529dd12876a747fb77eacfad8619db92a87a654b7df2dae76bfe56b598`  
		Last Modified: Tue, 13 Jan 2026 10:39:10 GMT  
		Size: 4.0 MB (3962532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8363c2b9d193af2dc02aaf02558ae28e108031c0a4f0d26483da8d29e818f887`  
		Last Modified: Tue, 13 Jan 2026 10:39:08 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:71289d4492230f0ffb5d0c9287e449fd26d47deb0e71944b3c06563dc2b39925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157099561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0d707b1546f44116d3866a334cebc62c63bb10e2ff69fdeea342f30b92310c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:48:50 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 00:48:50 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:48:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Fri, 14 Nov 2025 00:48:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 00:48:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:48:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:48:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:48:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:48:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:48:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:48:57 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:48:57 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:48:57 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:48:57 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:48:57 GMT
USER 8983
# Fri, 14 Nov 2025 00:48:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:48:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056d893e0d371c5487791a65e23fc262baaded50a7defea0a6c4e6216b7433d`  
		Last Modified: Wed, 14 Jan 2026 06:32:38 GMT  
		Size: 65.6 MB (65618611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a6c41f13e11fd38ec3d181326a5cdb266c838320d702cb290f6f916d84107e`  
		Last Modified: Wed, 14 Jan 2026 06:32:18 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4784c1ffa4396772b71552b5990bf1c09cd99ea13b27043feaf0799a25739281`  
		Last Modified: Wed, 14 Jan 2026 06:32:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ef8200be6c6416e6e16641f37b4c7b36520dc727ff18ae6f81c6c4e9a6a1f1`  
		Last Modified: Wed, 14 Jan 2026 06:32:24 GMT  
		Size: 10.8 KB (10806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcbaadb9dd0683ef564e539def610626c425677d509e77fe806977b68813b96`  
		Last Modified: Wed, 14 Jan 2026 06:32:20 GMT  
		Size: 1.5 MB (1474834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:a40350be2f64a3b736d3683861d1800a8d1068b087c29cbc6916956720e66153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de6de86597488b7157c1f55a55a3deb7eaaf40e21ca29b73c5e24abaae44c33`

```dockerfile
```

-	Layers:
	-	`sha256:f2c8ced645fc1e36f66eda5c275090c44d00e22ad5f2c06f222005cefffd68b0`  
		Last Modified: Fri, 16 Jan 2026 00:00:44 GMT  
		Size: 4.0 MB (3962184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52276c9131438cedf48fbe2ecf47817e4bbb33e8add13ba95b749df749bc3395`  
		Last Modified: Fri, 16 Jan 2026 00:00:44 GMT  
		Size: 33.9 KB (33915 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:e5aaee534d1250fdf14bbb53bff26e92810792b1db87009b72b214fe01e48b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166219483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7530ea55d8ec559342f343bf2ee8edd490eba9c45eb1ad4ab15d52c47adf5ae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 14:14:01 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 14:14:01 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 14:14:01 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Fri, 14 Nov 2025 14:14:01 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 14:14:01 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 14:14:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 14:14:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 14:14:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 14:14:02 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 14:14:02 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 14:14:09 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 14:14:09 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 14:14:09 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 14:14:10 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 14:14:10 GMT
USER 8983
# Fri, 14 Nov 2025 14:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 14:14:10 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b2a3c8fdb941fa42e3573115c6d391ea1006f66a5964bc67d8ee3a18c678de`  
		Last Modified: Fri, 14 Nov 2025 14:14:40 GMT  
		Size: 65.6 MB (65618949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5161c537f2bd9245482902fb355cb629d3016bc6b41840b2c0efd44564b00ed1`  
		Last Modified: Thu, 15 Jan 2026 00:55:11 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9affcd3c285d166d505f2b88409f886eeb64924db5f025295b9f1cfbecdb88`  
		Last Modified: Fri, 14 Nov 2025 14:14:38 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938ea035663b8bcd02bc99d768d1c7f7f0236e33ffff3331511e6201c528b1e1`  
		Last Modified: Thu, 15 Jan 2026 00:55:12 GMT  
		Size: 10.8 KB (10810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad44c748b9d30e924e15498cb727b99086f4b42d8a2765cf83ef509b1d46db99`  
		Last Modified: Fri, 14 Nov 2025 14:14:39 GMT  
		Size: 1.6 MB (1630929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:4961a5ce190d7f254dba5c3886dab58974f428387ac261b86257e20238001a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffc702327b47ff89accd79694d1cd51e82731350c10532185db02b1cf2257f9`

```dockerfile
```

-	Layers:
	-	`sha256:1fc155a629d646593cbbee3842a39c3d637a26c07eaad5fd1d59fddf412318cc`  
		Last Modified: Thu, 15 Jan 2026 00:55:11 GMT  
		Size: 4.0 MB (3966573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e338c4bc42b96f68f43ab9e9c9257754941a41bc9c67c4038ff1c7b7d46d72`  
		Last Modified: Thu, 15 Jan 2026 00:55:10 GMT  
		Size: 33.8 KB (33814 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9-slim` - linux; s390x

```console
$ docker pull solr@sha256:a0d61523a208992ad6f1f56bfab16aa779fe26df7deb10f000b11f4e3797ec14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155375114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ceb9e8e59cec785c91dfc83af284946747fde5ca3e4491c39dc3be35262665`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DIST=-slim
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 22:59:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 22:59:58 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 22:59:58 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 22:59:58 GMT
USER 8983
# Thu, 15 Jan 2026 22:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:58 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4fc3db087134a8591eb0232569737616b78669dfa623436e49eed5c213cfb0`  
		Last Modified: Thu, 15 Jan 2026 23:00:28 GMT  
		Size: 65.6 MB (65618178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee3674b02d159e68fd01accec04080b7e00675d3cb6befaa16f6a90bca5d26`  
		Last Modified: Thu, 15 Jan 2026 23:00:21 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc4256577e72c1120f696253a9d9e8b9e5e18f7e20b2c83f7f97dd020c90509`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02756500fcfdc8f3aa79e4c669fd9a4e3f240540d572dfa4ba82d6d736922d01`  
		Last Modified: Thu, 15 Jan 2026 23:00:21 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab32a0110aac88c99a3a9db32c5b5f4c621c58c3e37dedaeb3d9b52b2e33df2`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 1.6 MB (1558921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:af6c187f973be975997af0524eb5d8a077ad04a77cb63bc7daed25b2afe861ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2a0180453b07f04a0625706940da310d0f68cd6b3c5a2a8a5642fb0ec60cdb`

```dockerfile
```

-	Layers:
	-	`sha256:d15d359372ed30889f7821e4053c7e0cbb8aae048bb1864cd34766e058c12d6d`  
		Last Modified: Fri, 16 Jan 2026 00:00:58 GMT  
		Size: 4.0 MB (3964140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7fe8282c8d284618c87bfa4a43d07098bb850bf686db09431e7c9c1bd4b83e`  
		Last Modified: Fri, 16 Jan 2026 00:00:59 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.9.0`

```console
$ docker pull solr@sha256:87e57b6ab760e3182718c3f47b8bc492f9cb47da41aa26d9ab8260c17c5574f7
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
$ docker pull solr@sha256:761a1581a6b214b2cca93189821be3f8c1307e9201f635e2aaf7e7f2d6e6f332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.2 MB (483209058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b0a77304ab46c5d7b2f8cee19d6c080ee67d5b10365c89664e65ac54b3f8c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:05:59 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 01:05:59 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 01:05:59 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Fri, 14 Nov 2025 01:05:59 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 01:05:59 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 01:05:59 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 01:05:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 01:05:59 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 01:06:00 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 01:06:00 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 01:06:00 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 01:06:06 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 01:06:06 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 01:06:06 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 01:06:06 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 01:06:06 GMT
USER 8983
# Fri, 14 Nov 2025 01:06:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 01:06:06 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7f9fc3ed7a65b326c76083bb9b87438f2c70f475c70aa89e117a928578c99f`  
		Last Modified: Tue, 13 Jan 2026 04:59:17 GMT  
		Size: 388.8 MB (388830955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1d51b45870daf28adf6f438924342b30c2f80aec0445bf3fc8ac38605d8996`  
		Last Modified: Tue, 13 Jan 2026 04:13:19 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c76e1f39cbd744a18346c1b30c2c25c19582d86a86b8c4b30c7db8c536e106e`  
		Last Modified: Tue, 13 Jan 2026 04:13:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66d7047db406697d73ec6983abde43579c8da748241b169da8ab660fe583240`  
		Last Modified: Tue, 13 Jan 2026 04:13:20 GMT  
		Size: 10.9 KB (10888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f0fc80d8aa8be7916250d721649ea73069cdccd2072d27894c7d38d38046e`  
		Last Modified: Tue, 13 Jan 2026 04:13:20 GMT  
		Size: 1.6 MB (1617967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0` - unknown; unknown

```console
$ docker pull solr@sha256:0983006436f0f03bbcd61ebd7d1306058394342fbb24252c23e61aa4869ff486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4583246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5a6875c8d50f3a9743eedfc9cbdf6a87e4bc464d12babfb3147b768b873729`

```dockerfile
```

-	Layers:
	-	`sha256:dc705ef5f0cffc11ed1dd7c785f5fdffc5ba65d8f818131b7f914205c7870a7f`  
		Last Modified: Tue, 13 Jan 2026 10:23:10 GMT  
		Size: 4.5 MB (4549527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2a8b2aab65f0a042734cd3202c5ed16eb16a47027afd1ea15b9c16e7351735`  
		Last Modified: Tue, 13 Jan 2026 10:23:08 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:0d1cce2a9a4a9ce8379e547ecea96809d4d4fbdde3e69f52eaa191d433fa69be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480312021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0cb0d81a209c2e3efee558cd04198bef95f7436495c2e7462e3ffadca6a1e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:23:42 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 01:23:42 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 01:23:42 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Fri, 14 Nov 2025 01:23:42 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 01:23:42 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 01:23:42 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 01:23:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 01:23:42 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 01:23:42 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 01:23:42 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 01:23:42 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 01:23:49 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 01:23:49 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 01:23:49 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 01:23:49 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 01:23:49 GMT
USER 8983
# Fri, 14 Nov 2025 01:23:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 01:23:49 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc99619d40c068548eeeea0c20eb144d97057500de8415fa284038cb2dbb16b`  
		Last Modified: Tue, 13 Jan 2026 08:11:25 GMT  
		Size: 388.8 MB (388830994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fcfc8c91c80cfa0ca5b987b2d9e39601da5d81ace9d65e682bddb6aee05347`  
		Last Modified: Tue, 13 Jan 2026 08:11:14 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a447bcac8cb1b0c8aa3e6dd674fecf6381745cb6b0bc40510449520e36336b13`  
		Last Modified: Tue, 13 Jan 2026 08:11:15 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b9088f3d4994305ab2c6068b6d829b3fb80df1f49ca32834725eeb9ba6acdf`  
		Last Modified: Tue, 13 Jan 2026 08:11:15 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2458c3e05a9c1a3413657edcaaf4dafe31b0e3c4afc736788a10903c682886c1`  
		Last Modified: Tue, 13 Jan 2026 08:11:16 GMT  
		Size: 1.5 MB (1474830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0` - unknown; unknown

```console
$ docker pull solr@sha256:6674c3a7711b5977f8c0360c8ebdf7196a281dd1a0e19f0ebdfe409e5955901f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4583038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268f47cbba218b3670b213ebd6366c740243b6f400c3c1a530dc0d19b076b6ed`

```dockerfile
```

-	Layers:
	-	`sha256:a1361bead7505d778fed2da10567809800f93ed14b2267f226d3d99bcf409fe7`  
		Last Modified: Thu, 15 Jan 2026 00:56:12 GMT  
		Size: 4.5 MB (4549179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd97af7fa6a19e0262cd9fb0bf1fb2d4e76406e125dc74403514f25553061f83`  
		Last Modified: Thu, 15 Jan 2026 00:56:10 GMT  
		Size: 33.9 KB (33859 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0` - linux; ppc64le

```console
$ docker pull solr@sha256:a06a2f08cbcc181fe3d5c0591ca83f62bd87014db99b62e8909406b7d6901b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.4 MB (489431933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4d0678af8b848a2808680f62ba01d0d1d35a13cf6dce844fc615b00e395b33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 05:08:15 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 05:08:15 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 05:08:15 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Fri, 14 Nov 2025 05:08:15 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 05:08:15 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 05:08:15 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 05:08:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 05:08:15 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 05:08:16 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 05:08:16 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 05:08:16 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 05:08:25 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 05:08:25 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 05:08:25 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 05:08:25 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 05:08:25 GMT
USER 8983
# Fri, 14 Nov 2025 05:08:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 05:08:25 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31186313e6962e688550330ca7a06aee0804e90eaf9b42b1ff9ebd9f2cf09e3`  
		Last Modified: Thu, 15 Jan 2026 00:56:30 GMT  
		Size: 388.8 MB (388831323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c7aee70c50cbaded2816003e3f8e64c3343b7cb50f6b856260d09bf2920b0`  
		Last Modified: Thu, 15 Jan 2026 00:56:11 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3a4a3018a90b682de6cb1fbf85bfb1e2949c76c1a6cd5af86ec6116bc69146`  
		Last Modified: Thu, 15 Jan 2026 00:56:11 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d9002ed5c942e9c87c8413a0cfb5a0cb5e8a3cdc116330c353057b7ab46085`  
		Last Modified: Thu, 15 Jan 2026 00:56:11 GMT  
		Size: 10.9 KB (10892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd39b05194299ccdfc485ffc7fcd012e01304ee980bf4de11b276a4361a8649`  
		Last Modified: Thu, 15 Jan 2026 00:56:14 GMT  
		Size: 1.6 MB (1630929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0` - unknown; unknown

```console
$ docker pull solr@sha256:0a07635a5b11a7129918e9b1caf43838f979425ec767b922f5b4ef110b1c1b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4587327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cbdf555971df3bb3383cfd23a49b966353196605c7895b895021b63fb05973`

```dockerfile
```

-	Layers:
	-	`sha256:e82e0301ba36effaa5d84847d09b9609909ddbbf33cb3e6038cd9a6ee53d8477`  
		Last Modified: Thu, 15 Jan 2026 00:56:17 GMT  
		Size: 4.6 MB (4553568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aaf09fdb93f68953d40edd3838609c99deb27bf87a12dd7e3c5006eecddc384`  
		Last Modified: Thu, 15 Jan 2026 00:56:15 GMT  
		Size: 33.8 KB (33759 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0` - linux; s390x

```console
$ docker pull solr@sha256:ea3f61584d89ac8dcdbb36801995ed266552de443b9afe1bb8d91edd9d3127ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.6 MB (478587635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b319728a81982ec30f9d7a69ea471d2364803cd43b5007e933bdd376671a7f34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:00:04 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 15 Jan 2026 23:00:04 GMT
ARG SOLR_DIST=
# Thu, 15 Jan 2026 23:00:04 GMT
ARG SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d
# Thu, 15 Jan 2026 23:00:04 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 15 Jan 2026 23:00:04 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 23:00:04 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 15 Jan 2026 23:00:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 23:00:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 23:00:04 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 23:00:04 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 23:00:05 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 23:00:07 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST= SOLR_SHA512=7b93dab3f0fd09c820a45574c4ef60dff0e8245b8b3a8913bc5874b6e12595ebbd3bb9c856a213ba1643673e461041e95e7e85031523dfb208686c41c366825d SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 23:00:07 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 23:00:07 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 23:00:07 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 23:00:07 GMT
USER 8983
# Thu, 15 Jan 2026 23:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:00:07 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c15eabc6c828402d0f52290257aa3c1c8fb9c8e1e855b616aa144564ee516b`  
		Last Modified: Thu, 15 Jan 2026 23:01:38 GMT  
		Size: 388.8 MB (388830624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302690fb47612b707b412f19a6157098e975db36329fe756850cc3456b56de80`  
		Last Modified: Thu, 15 Jan 2026 23:00:56 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e05006a8aab44fd82e506cd4e753804c826880639ec0c0de2987cc762d2a60f`  
		Last Modified: Thu, 15 Jan 2026 23:00:56 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96596ae1affa36478c1258533a81d8cfd2945fa42a0a81b7e15dd966884b1477`  
		Last Modified: Thu, 15 Jan 2026 23:00:55 GMT  
		Size: 10.9 KB (10895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5809c1f57c03f352f79c28d29ea9046596f3c4cc309caaadffbdb7f57fb09c`  
		Last Modified: Thu, 15 Jan 2026 23:00:56 GMT  
		Size: 1.6 MB (1558912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0` - unknown; unknown

```console
$ docker pull solr@sha256:94ba8eafa626c8a27e8a773f73f93b46ef86f3cc75be8c461017377bfd15f82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22337fcbe66be8931e47e9b28182f510d7d06f9fc66875a535489a8a3b9f4ba7`

```dockerfile
```

-	Layers:
	-	`sha256:6435ab25642e1c0278cd1b5400602d2495aaa3fda1edf195b2c51e6884745801`  
		Last Modified: Fri, 16 Jan 2026 00:00:36 GMT  
		Size: 4.6 MB (4551135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efe75207fead6c9511f62c298bd4c0a12cb5b75302170ca2967999c56aba2f64`  
		Last Modified: Fri, 16 Jan 2026 00:00:37 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.9.0-slim`

```console
$ docker pull solr@sha256:220aac3989fbf6f20dca4a8f9bab9bed7ee338d9dd7db84402b8887a02e3c1a9
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
$ docker pull solr@sha256:0ba506aaf6497feef5f921cfa8e82086c73930b8697c9ac5aa9617b728904ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159996568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66401b6776c033405113511a174610b065322b877e59932b4f8573f95cffb42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:47:12 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 00:47:12 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:47:12 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Fri, 14 Nov 2025 00:47:12 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 00:47:12 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:47:12 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 00:47:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:47:12 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:47:12 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:47:12 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:47:12 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:47:20 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:47:20 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:47:20 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:47:20 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:47:20 GMT
USER 8983
# Fri, 14 Nov 2025 00:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:47:20 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99489bcb68ac1c4a394151b66e498bcb745faf6f65234ba3535b456eca4e87c9`  
		Last Modified: Tue, 13 Jan 2026 05:26:07 GMT  
		Size: 65.6 MB (65618531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031fcaa45c2b5aeaba2a41badf93830576bb59a7624fd2fe1f215cb2dbc5e331`  
		Last Modified: Tue, 13 Jan 2026 05:01:43 GMT  
		Size: 4.3 KB (4279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2676a22fdd93f9bb42915ad157099ecbaf4d0e4f2cd9b9f34ae213f6e4a01238`  
		Last Modified: Tue, 13 Jan 2026 05:25:54 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b3a8b880cd2c6b76933f8cf2cf4e42ad0622c70ab868f7ff939b6cb7b510eb`  
		Last Modified: Tue, 13 Jan 2026 05:25:56 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd339c74eb0bcfaa836161914654cceec116f06f5c6963a1423e461ce75f2ce`  
		Last Modified: Tue, 13 Jan 2026 05:02:03 GMT  
		Size: 1.6 MB (1617974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:bfcb7eb636b30e182ba51c1eca69d6246a6af4aab521973db9a3a25ed3155995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeeb5790adbaeb3c069deef15e35f0fb89292454e84efa7b140e0773affd9e2`

```dockerfile
```

-	Layers:
	-	`sha256:fe7403529dd12876a747fb77eacfad8619db92a87a654b7df2dae76bfe56b598`  
		Last Modified: Tue, 13 Jan 2026 10:39:10 GMT  
		Size: 4.0 MB (3962532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8363c2b9d193af2dc02aaf02558ae28e108031c0a4f0d26483da8d29e818f887`  
		Last Modified: Tue, 13 Jan 2026 10:39:08 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:71289d4492230f0ffb5d0c9287e449fd26d47deb0e71944b3c06563dc2b39925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157099561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0d707b1546f44116d3866a334cebc62c63bb10e2ff69fdeea342f30b92310c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:48:50 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 00:48:50 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:48:50 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Fri, 14 Nov 2025 00:48:50 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 00:48:50 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:48:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 00:48:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:48:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:48:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:48:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:48:50 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:48:57 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:48:57 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:48:57 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:48:57 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:48:57 GMT
USER 8983
# Fri, 14 Nov 2025 00:48:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:48:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7056d893e0d371c5487791a65e23fc262baaded50a7defea0a6c4e6216b7433d`  
		Last Modified: Wed, 14 Jan 2026 06:32:38 GMT  
		Size: 65.6 MB (65618611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a6c41f13e11fd38ec3d181326a5cdb266c838320d702cb290f6f916d84107e`  
		Last Modified: Wed, 14 Jan 2026 06:32:18 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4784c1ffa4396772b71552b5990bf1c09cd99ea13b27043feaf0799a25739281`  
		Last Modified: Wed, 14 Jan 2026 06:32:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ef8200be6c6416e6e16641f37b4c7b36520dc727ff18ae6f81c6c4e9a6a1f1`  
		Last Modified: Wed, 14 Jan 2026 06:32:24 GMT  
		Size: 10.8 KB (10806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcbaadb9dd0683ef564e539def610626c425677d509e77fe806977b68813b96`  
		Last Modified: Wed, 14 Jan 2026 06:32:20 GMT  
		Size: 1.5 MB (1474834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:a40350be2f64a3b736d3683861d1800a8d1068b087c29cbc6916956720e66153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de6de86597488b7157c1f55a55a3deb7eaaf40e21ca29b73c5e24abaae44c33`

```dockerfile
```

-	Layers:
	-	`sha256:f2c8ced645fc1e36f66eda5c275090c44d00e22ad5f2c06f222005cefffd68b0`  
		Last Modified: Fri, 16 Jan 2026 00:00:44 GMT  
		Size: 4.0 MB (3962184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52276c9131438cedf48fbe2ecf47817e4bbb33e8add13ba95b749df749bc3395`  
		Last Modified: Fri, 16 Jan 2026 00:00:44 GMT  
		Size: 33.9 KB (33915 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:e5aaee534d1250fdf14bbb53bff26e92810792b1db87009b72b214fe01e48b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166219483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7530ea55d8ec559342f343bf2ee8edd490eba9c45eb1ad4ab15d52c47adf5ae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 14:14:01 GMT
ARG SOLR_VERSION=9.9.0
# Fri, 14 Nov 2025 14:14:01 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 14:14:01 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Fri, 14 Nov 2025 14:14:01 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 14 Nov 2025 14:14:01 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 14:14:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.version=9.9.0
# Fri, 14 Nov 2025 14:14:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 14:14:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 14:14:01 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 14:14:02 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 14:14:02 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 14:14:09 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 14:14:09 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 14:14:09 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 14:14:10 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 14:14:10 GMT
USER 8983
# Fri, 14 Nov 2025 14:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 14:14:10 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b2a3c8fdb941fa42e3573115c6d391ea1006f66a5964bc67d8ee3a18c678de`  
		Last Modified: Fri, 14 Nov 2025 14:14:40 GMT  
		Size: 65.6 MB (65618949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5161c537f2bd9245482902fb355cb629d3016bc6b41840b2c0efd44564b00ed1`  
		Last Modified: Thu, 15 Jan 2026 00:55:11 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9affcd3c285d166d505f2b88409f886eeb64924db5f025295b9f1cfbecdb88`  
		Last Modified: Fri, 14 Nov 2025 14:14:38 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938ea035663b8bcd02bc99d768d1c7f7f0236e33ffff3331511e6201c528b1e1`  
		Last Modified: Thu, 15 Jan 2026 00:55:12 GMT  
		Size: 10.8 KB (10810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad44c748b9d30e924e15498cb727b99086f4b42d8a2765cf83ef509b1d46db99`  
		Last Modified: Fri, 14 Nov 2025 14:14:39 GMT  
		Size: 1.6 MB (1630929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:4961a5ce190d7f254dba5c3886dab58974f428387ac261b86257e20238001a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffc702327b47ff89accd79694d1cd51e82731350c10532185db02b1cf2257f9`

```dockerfile
```

-	Layers:
	-	`sha256:1fc155a629d646593cbbee3842a39c3d637a26c07eaad5fd1d59fddf412318cc`  
		Last Modified: Thu, 15 Jan 2026 00:55:11 GMT  
		Size: 4.0 MB (3966573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e338c4bc42b96f68f43ab9e9c9257754941a41bc9c67c4038ff1c7b7d46d72`  
		Last Modified: Thu, 15 Jan 2026 00:55:10 GMT  
		Size: 33.8 KB (33814 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.9.0-slim` - linux; s390x

```console
$ docker pull solr@sha256:a0d61523a208992ad6f1f56bfab16aa779fe26df7deb10f000b11f4e3797ec14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155375114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ceb9e8e59cec785c91dfc83af284946747fde5ca3e4491c39dc3be35262665`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_VERSION=9.9.0
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DIST=-slim
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.version=9.9.0
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 22:59:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
# ARGS: SOLR_VERSION=9.9.0 SOLR_DIST=-slim SOLR_SHA512=0e4011aa1defd4b82e06bddabeb90200168139d26286b70fe81cab8b9020057302e77fabc4c9f63e4e9e7976fad2b8e21a2d22d1d60a12efd5b5f9ed45d697d5 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 22:59:58 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 22:59:58 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 22:59:58 GMT
USER 8983
# Thu, 15 Jan 2026 22:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:58 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4fc3db087134a8591eb0232569737616b78669dfa623436e49eed5c213cfb0`  
		Last Modified: Thu, 15 Jan 2026 23:00:28 GMT  
		Size: 65.6 MB (65618178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee3674b02d159e68fd01accec04080b7e00675d3cb6befaa16f6a90bca5d26`  
		Last Modified: Thu, 15 Jan 2026 23:00:21 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc4256577e72c1120f696253a9d9e8b9e5e18f7e20b2c83f7f97dd020c90509`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02756500fcfdc8f3aa79e4c669fd9a4e3f240540d572dfa4ba82d6d736922d01`  
		Last Modified: Thu, 15 Jan 2026 23:00:21 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab32a0110aac88c99a3a9db32c5b5f4c621c58c3e37dedaeb3d9b52b2e33df2`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 1.6 MB (1558921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.9.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:af6c187f973be975997af0524eb5d8a077ad04a77cb63bc7daed25b2afe861ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2a0180453b07f04a0625706940da310d0f68cd6b3c5a2a8a5642fb0ec60cdb`

```dockerfile
```

-	Layers:
	-	`sha256:d15d359372ed30889f7821e4053c7e0cbb8aae048bb1864cd34766e058c12d6d`  
		Last Modified: Fri, 16 Jan 2026 00:00:58 GMT  
		Size: 4.0 MB (3964140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7fe8282c8d284618c87bfa4a43d07098bb850bf686db09431e7c9c1bd4b83e`  
		Last Modified: Fri, 16 Jan 2026 00:00:59 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:latest`

```console
$ docker pull solr@sha256:9cc09d6681452681bc9121c815a3b3914c5e1c2e6c8ac7060ead1e5574aa03b1
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
$ docker pull solr@sha256:4e3281a953e1e7677d9e7072963639359adc579a2a66441ed2426f3898c6c80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483443041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484b8e9933b08710c8a185bf1c0316b23fc560becde45d0a354ff71148edcaa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:43 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:43 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:35:50 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:35:50 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:35:50 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:35:50 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:35:50 GMT
USER 8983
# Fri, 14 Nov 2025 00:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:50 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e780b6448e9fcbd386e57fc0127236f683fe2f65d97d0735b5ba5e63626e05f4`  
		Last Modified: Tue, 13 Jan 2026 03:04:02 GMT  
		Size: 389.1 MB (389064967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d8eb5d5688a4ea06162e591c7205198e53600ba53092c08bcacb51389a1588`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734bac102ccc37f3ab93cfa278a624c6b93f7e47eeefccd91ad53aae841ea1e`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2067c6be7bc6f45ecc74223dbd370617c87a6ec03bc22cc9d6bcc92caaf21dd`  
		Last Modified: Tue, 13 Jan 2026 01:23:31 GMT  
		Size: 10.9 KB (10887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b748ff60cfb17a17f4bc5f8f1d362c4f3cc539c2a6c337aaba8738423146dc`  
		Last Modified: Tue, 13 Jan 2026 01:23:32 GMT  
		Size: 1.6 MB (1617938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:cba4f7d65ecd061458bdd7632c4b1e9028491e9dd7af98627a7db722755c90bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4574006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3280c2bb80206d2bb82b98866c604f55640d16b42e27134e12da0658e3f84161`

```dockerfile
```

-	Layers:
	-	`sha256:cd0d333605bd31938060b486dceb993b0dc8e21ed645c1d04043ebc66854c11a`  
		Last Modified: Tue, 13 Jan 2026 05:32:05 GMT  
		Size: 4.5 MB (4539699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6107657ecd586fe1302225c5867d15ca7d577daa119f0d0461e55566d3404c1`  
		Last Modified: Tue, 13 Jan 2026 05:32:04 GMT  
		Size: 34.3 KB (34307 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:f3a1fac578e93748dbca67913ab6e48b66d0cdbab2c26d7085b15d42a4ea8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480546239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc587a2f38c1bcaa610560c1d385a874795b92f3b26b05723b6a9074f2317cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:36:08 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:36:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:36:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:36:08 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:36:08 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:36:09 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:36:09 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:36:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:36:17 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:36:17 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:36:17 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:36:17 GMT
USER 8983
# Fri, 14 Nov 2025 00:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:17 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e8a0efe291a4f0cec1852e7a27ae5247c9aba0d3fbb94b2ccb10fd50dd9ff0`  
		Last Modified: Tue, 13 Jan 2026 05:40:26 GMT  
		Size: 389.1 MB (389065240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463e9887baf7fb87ac4fcfd13f24ccaf53effd855328dd28af3be6fe3d2c8b82`  
		Last Modified: Tue, 13 Jan 2026 01:24:52 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d766c279905383234c823e55a7e5392d61f0949b622bc2f9f31cde49dbb8f4a`  
		Last Modified: Tue, 13 Jan 2026 01:24:55 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4510d58c61fc56a7f8f12a99604474ea0f949c9557a4c995ee53d5497d26c5a`  
		Last Modified: Tue, 13 Jan 2026 01:24:56 GMT  
		Size: 10.9 KB (10886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf5a7d409faa4a9d1b88da54ec75c24d8017bc83426942fd70a1123570f8ea`  
		Last Modified: Tue, 13 Jan 2026 01:25:02 GMT  
		Size: 1.5 MB (1474808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:f718ef78f36eec53829f8e22d6554429856f866a1406736d90eef04747505b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4573846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1363ae3c879252ef415c827abec007d01f1211ba3071f8e6f535d3bfb88b4008`

```dockerfile
```

-	Layers:
	-	`sha256:c17f1fb8a16bc279fef4a42e8bd3e81be0cfadce9d9c200e14aa9c0398273280`  
		Last Modified: Tue, 13 Jan 2026 05:40:15 GMT  
		Size: 4.5 MB (4539375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9da6f21a0b2c5f54845d3ec318ba725285c84e06f787b6e83e20d9c8650bea`  
		Last Modified: Tue, 13 Jan 2026 05:40:14 GMT  
		Size: 34.5 KB (34471 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:1365dd69b9c196dac1e19ac77c654962b697a71a1fcfdf7af278b4863809627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.7 MB (489666110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c29f7cdb659e2132bfa1a9abf9d14a30ffd242304b7c3e6f2143a85dfaa588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_DIST=
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 04:31:46 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 04:31:46 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 04:31:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 04:31:46 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 04:31:46 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 04:31:47 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 04:31:47 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 04:31:57 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 04:31:57 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 04:31:57 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 04:31:57 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 04:31:57 GMT
USER 8983
# Fri, 14 Nov 2025 04:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 04:31:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1a4d01af248389fc55dc07be999fb61aaf3790771097ec36981b3f4a82d54f`  
		Last Modified: Wed, 14 Jan 2026 19:53:39 GMT  
		Size: 389.1 MB (389065509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b9f4ec3295bc0c813a4d4b9c9df3b0ee3166501ffc1104391ae8b3e36522ac`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27b54999556b765a81b88931073200863c941418b3e937941c49a2af62b12de`  
		Last Modified: Tue, 13 Jan 2026 19:54:16 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59502c0008feea87e98877ecf40704cacc2e0e563146b2157f8a81e79f917dc5`  
		Last Modified: Tue, 13 Jan 2026 19:54:16 GMT  
		Size: 10.9 KB (10891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2066f119df598b5375b20a7d39225c27bd4e3f9f4b16d0da166759d7ded983`  
		Last Modified: Wed, 14 Jan 2026 19:53:16 GMT  
		Size: 1.6 MB (1630924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:2f6ffaa0d23f0ee4461e3c064c31f8f049d4039717a43ad24e5969bc7613a3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8648388f7533dc048043a8d0fdf45c4af9a797c9a56cdd572b4c693fe68d3f53`

```dockerfile
```

-	Layers:
	-	`sha256:76878f45b530d9fc043ff643ed4fb533c2c464f3da20db05066033a53684e207`  
		Last Modified: Thu, 15 Jan 2026 01:03:01 GMT  
		Size: 4.5 MB (4543752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86ba99289ff949bfc110c7ec171062f29ddc9a169bcaeac9a7b29ef204d89d6`  
		Last Modified: Thu, 15 Jan 2026 01:03:00 GMT  
		Size: 34.4 KB (34360 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:5aef9f7191b5ad822adde27da21fda6c9d5727a95be555c3b0d92f1d49612123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.8 MB (478821645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ae68499340401fc6e4cd1d64750ab013541735883c92381f8351d95ff65d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_DIST=
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 15 Jan 2026 22:59:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 22:59:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 15 Jan 2026 22:59:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 22:59:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 22:59:28 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 22:59:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 22:59:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 22:59:33 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST= SOLR_SHA512=f97153ce12a1b88134b54c4a5a74f6eedd67e06092b6caa3cc9ddaff7b65fa3d4816e7702fb07a54cc0e83724eb9ceab78af77100b688cd68323b5a988e031be SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 22:59:33 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 22:59:33 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 22:59:33 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 22:59:33 GMT
USER 8983
# Thu, 15 Jan 2026 22:59:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:33 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc779feb1349838bef15e24d4230a9fd7a894de4f1481b9f60ffa8ac398a5ab`  
		Last Modified: Thu, 15 Jan 2026 23:00:50 GMT  
		Size: 389.1 MB (389064641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3b67c408a6233a5a9de7160df365b07034611d0e871890d0bc5ae2935694d6`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa4a9f9d5f55a9b4f6a20bc0cb3ff7adeb2e67925592d086cd34eee580bd889`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b9ef21656508227ffef603c885585c06a83be7df8f0fa49c2ff77e9fbb88`  
		Last Modified: Thu, 15 Jan 2026 23:00:22 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b2ddd98ff1568f7043593b8254dc4768e3120fe48393163a3f6fd081c49bfe`  
		Last Modified: Thu, 15 Jan 2026 23:00:24 GMT  
		Size: 1.6 MB (1558915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:d75ccf90491d755be01a77a21b7a09641666738d6b279f7578192574c569dd0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e344c8aa3fb719618ca9fbdc415e1a97baf89f1ceb96835b33d5e010caa7789`

```dockerfile
```

-	Layers:
	-	`sha256:94cdb9505999847bdca2dccc37f60f4e4dfab5bf25f781f833c170427b4d1b11`  
		Last Modified: Thu, 15 Jan 2026 23:59:54 GMT  
		Size: 4.5 MB (4541307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76e0290ec8670aca27d1c780e87c8dabd6156a4653a43dd895894c95bfd7a595`  
		Last Modified: Thu, 15 Jan 2026 23:59:55 GMT  
		Size: 34.3 KB (34308 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:slim`

```console
$ docker pull solr@sha256:616e6a30a46115d7a63a8bf78c6561c465595510be0858c2c08e91ebab901761
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
$ docker pull solr@sha256:312e9aea54a32811a43bf076dd5ab995f61aaf757fef43624630ae07c736fe89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160345232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfde5e40ebe42675499b306697cf5500bbf6779b2e9c04735f975a07a7b4dda4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:27 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:27 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:35:27 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:35:35 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:35:35 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:35:35 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:35:35 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:35:35 GMT
USER 8983
# Fri, 14 Nov 2025 00:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:35 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5447750fb19a6560e8c2542b39f1114e72621600e34f05840b59905f67f45b1c`  
		Last Modified: Tue, 13 Jan 2026 02:17:48 GMT  
		Size: 66.0 MB (65967198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6fc48a5d5b531498cfe22c2a6deafcea97641c5b15905d0b0b6bf5fcb441c9`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d09ae6cb9cdbefce05fc6bd747cae51f79a5f4c9dd2845c7294bda5de3fb502`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d546ae266e921fe6d9c2558837c70cc4647bbbda7e6f0edf1090ea0b1f28c`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 10.8 KB (10800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6230a4dad4beb67a5c79fa44d2ccf59a1cd46080c81807baeeb1bdbc0610090d`  
		Last Modified: Tue, 13 Jan 2026 02:17:46 GMT  
		Size: 1.6 MB (1617979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:e171081c72963a33f4b8f72fc565090bca81111b3f24e61eddb7fdb3b7ed6563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36d121e431044233fe37728b82dd77cd1f883b8d409d4e1cadd9cc1048ac4a2`

```dockerfile
```

-	Layers:
	-	`sha256:c5057e6818814d3a2cf07fbe33432dcf6e242af534f7693e1d4ab79d29aa8e16`  
		Last Modified: Tue, 13 Jan 2026 04:56:36 GMT  
		Size: 4.0 MB (3964559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dfb26e314e2fb2185306c58acc85f027ac15905def86f0869800feb154b1209`  
		Last Modified: Tue, 13 Jan 2026 04:56:26 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:69106b4ac08ebc728cb30e72146c82314da23fd208947233cecd651e016e9338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157448199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9c1af8df56abb0bdb7c9b3297624b10f339f034c684ee82c28a6e7a55b7726`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 00:35:59 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 00:35:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 00:35:59 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 00:35:59 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 00:36:00 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 00:36:06 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 00:36:06 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 00:36:06 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 00:36:06 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 00:36:06 GMT
USER 8983
# Fri, 14 Nov 2025 00:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:36:06 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4f496ea89d577a3cc866a679850332736cfaa6ab638f040879f443f390e4e2`  
		Last Modified: Wed, 14 Jan 2026 09:08:27 GMT  
		Size: 66.0 MB (65967274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964c00e880758d0c3c88e86ae4d881ab717e1c348806313ec59e48f43ae7e189`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ea0d24facd340a636e91ba2011ac7ccb7b4e515d541d28c84806baf200c354`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf27a22c1b1a7cae544b3e2993a96889a32d33afbabe1723c0d905f5d1a314`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 10.8 KB (10803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3894133efebec657330190414c35c9788f4337b5b401e2b96e25093813680f7c`  
		Last Modified: Wed, 14 Jan 2026 09:08:19 GMT  
		Size: 1.5 MB (1474815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:be492e2906d23c445a8575289e44bbbecba8ad4958c1a06a4617df63a99bb340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd2406f2ea1047d8b3ec8582815ab30258229961770bb29a673639d6718b73c`

```dockerfile
```

-	Layers:
	-	`sha256:55fbbf022b0b7571df220cdabbbfee33d316d2e6e5104f068a7b0bba9bb4a6f5`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 4.0 MB (3964235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb48fc445efdbbee0a22926eb743bef5b09c1156c511d0f7c4dd520c64e099ff`  
		Last Modified: Thu, 15 Jan 2026 01:13:48 GMT  
		Size: 34.5 KB (34535 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:a99e6082f0736afceb9e6c85390992c325ac6506eeb534f2b5c1db406981adfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166568120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda91e717d9ae00f166b5c20537afb86e5b0a71b101e49273a203bbdb14e3e2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_VERSION=9.10.0
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_DIST=-slim
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Fri, 14 Nov 2025 14:04:17 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 14 Nov 2025 14:04:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.version=9.10.0
# Fri, 14 Nov 2025 14:04:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 14 Nov 2025 14:04:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 14 Nov 2025 14:04:17 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 14 Nov 2025 14:04:18 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 14 Nov 2025 14:04:18 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 14 Nov 2025 14:04:29 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 14 Nov 2025 14:04:29 GMT
VOLUME [/var/solr]
# Fri, 14 Nov 2025 14:04:29 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 14 Nov 2025 14:04:30 GMT
WORKDIR /opt/solr
# Fri, 14 Nov 2025 14:04:30 GMT
USER 8983
# Fri, 14 Nov 2025 14:04:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 14:04:30 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06f5ae29c6cff72a11a62824248910a854e775ecee4be4bc5bf9546d2ee83fc`  
		Last Modified: Thu, 15 Jan 2026 01:13:53 GMT  
		Size: 66.0 MB (65967575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd713f6377e2dc498f3d946ec705a29d94df4937304309a01ccfbdc1b960af9e`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 4.3 KB (4275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15cc300151d2eb660ebc114e6b0aad7a6531174ae9e18c679c3257d326e4af`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4a2dbdeeda970c2be87f66d1478b422be63e1f560e2a56fea4dec5ac6c580`  
		Last Modified: Thu, 15 Jan 2026 01:13:50 GMT  
		Size: 10.8 KB (10802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9586fb2adb28afa6ca2af97103beed57c7c1d8e5c7f9425c542d406eae87d6bd`  
		Last Modified: Thu, 15 Jan 2026 01:13:53 GMT  
		Size: 1.6 MB (1630948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:1b2d6786e20ab17a458b171f003edd2fa9a04f0b17a41489a05afe432132c297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a9548333b295fddabd640ccd93788df36ebc507520a55e38d68c138beb44d`

```dockerfile
```

-	Layers:
	-	`sha256:e96b4d198f15a8bbcbaea2a60e94c471f4ac99ca44c5c787ce1d071ef94c514d`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 4.0 MB (3968612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e72a7e7a35d5dacbea993e97df734f5de196474e77077d8f70040e55e508177`  
		Last Modified: Thu, 15 Jan 2026 01:13:51 GMT  
		Size: 34.4 KB (34423 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:394d572789469b3075c0dec8e101b9650c089be6e7baeffa01c5b62a4d46fdca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155723785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019d7f18ec21f589094594f3989c7039c3bae51334c4131cfb0d0e1ebcc73ad4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_VERSION=9.10.0
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DIST=-slim
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 15 Jan 2026 22:59:53 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.version=9.10.0
# Thu, 15 Jan 2026 22:59:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 15 Jan 2026 22:59:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Thu, 15 Jan 2026 22:59:53 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
# ARGS: SOLR_VERSION=9.10.0 SOLR_DIST=-slim SOLR_SHA512=815868aac78e459a07fa8b5e2163d1ae70ded151735373463a769f3a58c03cd5cf3ec30ff500cd4b8ab445ecc94ca423bfe2b75d89ba0eedc8a0daf8fb325fc2 SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 15 Jan 2026 22:59:58 GMT
VOLUME [/var/solr]
# Thu, 15 Jan 2026 22:59:58 GMT
EXPOSE map[8983/tcp:{}]
# Thu, 15 Jan 2026 22:59:58 GMT
WORKDIR /opt/solr
# Thu, 15 Jan 2026 22:59:58 GMT
USER 8983
# Thu, 15 Jan 2026 22:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:59:58 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1c7bd7f24e4f79699b9353cc94a420490b2385db8291d8779d31303119a64f`  
		Last Modified: Thu, 15 Jan 2026 23:00:46 GMT  
		Size: 66.0 MB (65966875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee3674b02d159e68fd01accec04080b7e00675d3cb6befaa16f6a90bca5d26`  
		Last Modified: Thu, 15 Jan 2026 23:00:21 GMT  
		Size: 4.3 KB (4302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6f56235a90a5be2425b29583a71dce7afef6a88ed2e5061557d0adcc1b9c7d`  
		Last Modified: Thu, 15 Jan 2026 23:00:25 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a647bf99141242ed0894bb32c621167c63c3be8468b3010d3fde61bd5705df`  
		Last Modified: Thu, 15 Jan 2026 23:00:16 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffd466dd881958780804f22bff07b0609a4a64c7490dfcf3209f5cf985233e1`  
		Last Modified: Thu, 15 Jan 2026 23:00:26 GMT  
		Size: 1.6 MB (1558903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:d559c2a29105b9397cd9803fcc1f2887143954427f36092bb1ef28211944be3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150acf99bc0a7b4447f5041e95893d70bd01acec9edf0ab24abec0abb13ead90`

```dockerfile
```

-	Layers:
	-	`sha256:2c1e92858adae42e3560da7d9350524434f75674b46b14688d0d997815bb955b`  
		Last Modified: Thu, 15 Jan 2026 23:59:59 GMT  
		Size: 4.0 MB (3966167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d967474a68982e8450550b5af8291450a0222f2cb6c958b67d43be53c93dae0`  
		Last Modified: Fri, 16 Jan 2026 00:00:00 GMT  
		Size: 34.4 KB (34371 bytes)  
		MIME: application/vnd.in-toto+json
