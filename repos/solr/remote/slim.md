## `solr:slim`

```console
$ docker pull solr@sha256:60f7f14f8a9a11e9eb151505bcb7b23caf4150468501481d7ec5200d11c946ec
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
$ docker pull solr@sha256:13fc736e71edb5c53724e4aa64a0d181e017ac0b16ed1f80f5b1aec1959bd9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156921034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe5989072c78babe6ca3b57aa686dcde5ff3f62ad46c533bfb311afa6f99943`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 29 May 2024 20:45:28 GMT
ARG RELEASE
# Wed, 29 May 2024 20:45:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 29 May 2024 20:45:28 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=-slim
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 20:45:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
VOLUME [/var/solr]
# Wed, 29 May 2024 20:45:28 GMT
EXPOSE map[8983/tcp:{}]
# Wed, 29 May 2024 20:45:28 GMT
WORKDIR /opt/solr
# Wed, 29 May 2024 20:45:28 GMT
USER 8983
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee59ca42def8dda96caccd58b671902e65195492ee8e5daa263e1e948033adc3`  
		Last Modified: Wed, 05 Jun 2024 05:01:21 GMT  
		Size: 47.3 MB (47256057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce2282f972ff7152adb0a2c757ddd63cf0c38d489c7d7952d7aa88ab1804bc5`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a9e456ba828f8cfc067a64b3717c10e4c0709fc1f0b95e5a5efd3ee816e643`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c652d8a3ec202b51e421fcc15f395647e85fb7d173beed876e9293b55c53d99c`  
		Last Modified: Wed, 05 Jun 2024 06:11:32 GMT  
		Size: 64.7 MB (64716194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dca81ae236982789f8509e90b8dcbf4864b518bcb0ed7c8c5a1e7fb3fa7c33d`  
		Last Modified: Wed, 05 Jun 2024 06:11:29 GMT  
		Size: 4.3 KB (4270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deebffb9dfb6984b48ccfc258fd1dc4bcb589890e2edb1282a76eb9035ca7f69`  
		Last Modified: Wed, 05 Jun 2024 06:11:29 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59abfcfa612f14de95834f1b8d4a27257f87037972d9e7bd92539effd2ac745d`  
		Last Modified: Wed, 05 Jun 2024 06:11:29 GMT  
		Size: 10.8 KB (10776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7028b1fba81cd0d31e10d5237da7b4c5f86eee84155bd6476765ee939a589a96`  
		Last Modified: Wed, 05 Jun 2024 06:11:31 GMT  
		Size: 1.6 MB (1588501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:e9d83685c69e233c01d2ff3fffdf8918831ebd30147f2723661bcdad1ce0af4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4bbfe6fb8289e06a062ff6d4d1edb2fd1a7f0cb3270efd0a3351acf33ce145`

```dockerfile
```

-	Layers:
	-	`sha256:99095d9d86cc5dec7e94ea14a8c78f8289792a67091bc8501921e2bcad7ea148`  
		Last Modified: Wed, 05 Jun 2024 06:11:30 GMT  
		Size: 3.7 MB (3656178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7c788026de6f8093a60e47ae806ddc98f40bdf61a428c72633b2ef539a5cb6`  
		Last Modified: Wed, 05 Jun 2024 06:11:29 GMT  
		Size: 34.1 KB (34054 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:6194ba7d483cc7b6f1d6b58b175f65b10166cd090baa04bbd2797c8a33485eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154144881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e64c0d7aaceb8a6d9110322e339d74e77c3b2f3be23af389b61a94b17629ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=-slim
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 20:45:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
VOLUME [/var/solr]
# Wed, 29 May 2024 20:45:28 GMT
EXPOSE map[8983/tcp:{}]
# Wed, 29 May 2024 20:45:28 GMT
WORKDIR /opt/solr
# Wed, 29 May 2024 20:45:28 GMT
USER 8983
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2472ac6840da0115175cae8b0be8d1b8c2b6b74acb5fc6bf185b0c9333b8a3`  
		Last Modified: Thu, 02 May 2024 04:17:28 GMT  
		Size: 12.8 MB (12847034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1725094f1f7082f023c1a047ec828bf8229f9aa4b95de8dfcf3433a5664a8625`  
		Last Modified: Thu, 02 May 2024 04:20:25 GMT  
		Size: 46.7 MB (46716197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e995ccba802f11ec98d823c76df9fc769ae179b10b0a6b239f526dcd74f907aa`  
		Last Modified: Thu, 02 May 2024 04:20:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7fbbe7faa2fd420d969dafb00e3a6a0cc66074e4786e50e8c8b4f22e7f754`  
		Last Modified: Thu, 02 May 2024 04:20:20 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aab1095daefd02d686b414c9902798928d2265a89617df5bec025cbae710bd`  
		Last Modified: Thu, 30 May 2024 14:41:00 GMT  
		Size: 64.7 MB (64716623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf49eb32c67b566f8fb4b4f17f767097836ee5ed42ab3c3969de5d367bb5241f`  
		Last Modified: Thu, 30 May 2024 14:40:58 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82343e6ba698a8474e4fb5d9902fe54ad7816e122798496f30ecb286caa3c8e`  
		Last Modified: Thu, 30 May 2024 14:40:58 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d0b85ab230a405539eb72a8f6a2f29346c2bfcf87c958522b9bf91fdb47f06`  
		Last Modified: Thu, 30 May 2024 14:40:58 GMT  
		Size: 10.8 KB (10778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60de381eca2569a9de88f9b806159dc31c6189101db5c75ae4a7bc9e591a075`  
		Last Modified: Thu, 30 May 2024 14:41:00 GMT  
		Size: 1.4 MB (1447624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:e3612b6eda47ecdda3e3b35694408d33980be3d1278d9351a5c53614875a62be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb98cc405c6dabfde1103cabbe0e0079aa2935b0f7beade3ef001693ad1d39a3`

```dockerfile
```

-	Layers:
	-	`sha256:a635752c78fbbd4ea033ac366f6d26bcf4e38308f85538fccf6c0465e858aac8`  
		Last Modified: Thu, 30 May 2024 14:40:58 GMT  
		Size: 3.7 MB (3656472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:369edb05cfec577d838e39a3d86c143336ead4654b2a7a1386813a24a07580a3`  
		Last Modified: Thu, 30 May 2024 14:40:58 GMT  
		Size: 34.4 KB (34370 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:0b7c5a57990c6b115e70ee6cd6c59ad6245c1d82f9aec2a65459ac243a3b9713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162773718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763e7e6a907ccd85827dc38d759982f028935d405a751875bda03caf27505341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=-slim
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 20:45:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
VOLUME [/var/solr]
# Wed, 29 May 2024 20:45:28 GMT
EXPOSE map[8983/tcp:{}]
# Wed, 29 May 2024 20:45:28 GMT
WORKDIR /opt/solr
# Wed, 29 May 2024 20:45:28 GMT
USER 8983
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615a40d637191fd38e803d020c6fd9ef07a75d9c895faae5c0a3a02afa988fbc`  
		Last Modified: Thu, 02 May 2024 01:51:41 GMT  
		Size: 13.8 MB (13767451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c01fd5e364e227e9c2afdb21e460d68edf0b920269b08948826b9d38cfd5b4`  
		Last Modified: Thu, 02 May 2024 01:55:07 GMT  
		Size: 47.1 MB (47089053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00d972a58c5b79fed7582e05e73a7299979cc4b00059d112b86d46a31d9b25d`  
		Last Modified: Thu, 02 May 2024 01:54:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e367dd9012c64c7676cc7610543f3bb6aedb443d7852a98137129a124b1e3f6`  
		Last Modified: Thu, 02 May 2024 01:54:59 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b0e64e7f86bc07211add553348bb308e8303329bdf7b2f1458471007505647`  
		Last Modified: Thu, 30 May 2024 02:25:16 GMT  
		Size: 64.7 MB (64716887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9953feccb255ffa2ac3e0d0f18cfd1271c12288a2a3f3c2989fc511f2d5cd00b`  
		Last Modified: Thu, 30 May 2024 02:25:14 GMT  
		Size: 4.3 KB (4275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacade3112f3d74045c71537c61ef417f69fb2ac2497b300bb79daa8d9cfc787`  
		Last Modified: Thu, 30 May 2024 02:25:14 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb0540f1a224217bf2dc1be1535b3b5d5b60cd53064dc1ac447a8381431d5b2`  
		Last Modified: Thu, 30 May 2024 02:25:14 GMT  
		Size: 10.8 KB (10780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ee3562393b70611b8460d5a7556b6dc2ceaeeab1907180f6928e561433a884`  
		Last Modified: Thu, 30 May 2024 02:25:15 GMT  
		Size: 1.6 MB (1595609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:bfdc14e8369c1db0ea1fead2aa72ed130a1fe5174e0dad2a6e3717d80c631d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3694805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5d0c54447e5a67066ba709f0d40b1b88e923b53c95fb1cd172058129828b7c`

```dockerfile
```

-	Layers:
	-	`sha256:17980129b7f3c42675681296e64c5f564067f048ec7f74eae05e0daaac79f54b`  
		Last Modified: Thu, 30 May 2024 02:25:14 GMT  
		Size: 3.7 MB (3660705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184a98ed2a062d8a3e39b821c85a59685b25d57e9fdc69238dbe6e9f9aeb9672`  
		Last Modified: Thu, 30 May 2024 02:25:14 GMT  
		Size: 34.1 KB (34100 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:105829ec1e393836e6a513a61bb341253dfcb80549e36476850847a2413606c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151722801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3f416c18f783499e80c2511881198c937173930ff47ec9c4e717459c1d992e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 29 May 2024 20:45:28 GMT
ARG RELEASE
# Wed, 29 May 2024 20:45:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 29 May 2024 20:45:28 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=-slim
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.version=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 29 May 2024 20:45:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST=-slim SOLR_SHA512=78e6558551c7710134f2519e5f86a32c636e5963f8efadc8c0391dfb99f7554b3d86197272aa92fa7b28589602d87389530eea043dd3d299983a1c49e38f0dc3 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
VOLUME [/var/solr]
# Wed, 29 May 2024 20:45:28 GMT
EXPOSE map[8983/tcp:{}]
# Wed, 29 May 2024 20:45:28 GMT
WORKDIR /opt/solr
# Wed, 29 May 2024 20:45:28 GMT
USER 8983
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87504bacc983be102c1f56d585bd6aeb2fba4f402fc20a73671274561ac7e98b`  
		Last Modified: Wed, 05 Jun 2024 03:12:32 GMT  
		Size: 13.0 MB (12986422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53042256a070472320cd249ecf218583c013740d8a9dea43f8c0b333dc089b1f`  
		Last Modified: Wed, 05 Jun 2024 03:14:16 GMT  
		Size: 43.8 MB (43830857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e62b2cd2c9eeb0fa7997477bb0f7d64165a00d62cda0237e742921ca21a15d`  
		Last Modified: Wed, 05 Jun 2024 03:14:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b87e70ca5e69a7ec02188fddd1add9f9d6ceb66eb5e6faab457af62967825bd`  
		Last Modified: Wed, 05 Jun 2024 03:14:09 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd2547c2248348b0046cef39dcbf156c4020a97615af817f27a921c21277d9e`  
		Last Modified: Wed, 05 Jun 2024 08:22:04 GMT  
		Size: 64.7 MB (64716579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ca033aa4b74d02805e85e593d0e1df5dac2a3ec4ccce0ae969138852862190`  
		Last Modified: Wed, 05 Jun 2024 08:22:02 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ae42c6a4821a8135d5fbdbecd51c4889c45c2be9ea8bfac8e3694f6dfc0824`  
		Last Modified: Wed, 05 Jun 2024 08:22:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27140e072d600173bc25d97ec5c9ce1933fe49ce8edb0af7c2bbb0520eda579b`  
		Last Modified: Wed, 05 Jun 2024 08:22:02 GMT  
		Size: 10.8 KB (10780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d680992104c50d0f1fcf3fb9544c465ce3cf2efd92f438a9fda077d9c43784`  
		Last Modified: Wed, 05 Jun 2024 08:22:03 GMT  
		Size: 1.5 MB (1535316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:2cf50ead264cc5898d929f01242bbfe3262f5318edddef1670dcb475b49d3aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bed49617974e07b5b9ec06e7a9ef090c2365009cd93c2af8f44c0c5505b517d`

```dockerfile
```

-	Layers:
	-	`sha256:526228ce12b7297f0ce3881ae2f56addcf27dd2a1233f94c198dffb77ad12dea`  
		Last Modified: Wed, 05 Jun 2024 08:22:02 GMT  
		Size: 3.7 MB (3657442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98a5c5578095be7908afe0788ef671ebb911251f0c64b4a4f9c50df26a1d027`  
		Last Modified: Wed, 05 Jun 2024 08:22:02 GMT  
		Size: 34.1 KB (34054 bytes)  
		MIME: application/vnd.in-toto+json
