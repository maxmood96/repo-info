## `solr:slim`

```console
$ docker pull solr@sha256:68ff7e1ddf18279aebec1e31219dc803fa40add7c9ef1589bdec1d605a230cfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `solr:slim` - linux; amd64

```console
$ docker pull solr@sha256:03dbdddca69315d53a8c77d9e01407341369c273e4e291652f486d8ad4161b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156531024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67274ab7af7db88d950fc981d897f63fff6cfc22dc3db3e7950eab72861b1418`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=-slim
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7c5a42f2fad87126e0a61b4605e0b8b0b8100485fbffb0fa0e14e87400873`  
		Last Modified: Thu, 25 Apr 2024 22:13:22 GMT  
		Size: 12.9 MB (12905143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7fcad56b7f8a33a6681a9ae067f80cc8ad2a08502172c8dda569c1338752bc`  
		Last Modified: Thu, 25 Apr 2024 22:16:38 GMT  
		Size: 47.3 MB (47256188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75513697e6ba945551856344dc1f1c94b25b9b98458dd13e8f1a25811e2424cc`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e30da527722230ddaac2aa5e9ae62f333caa596c7853ae2b516c06d2d6f321f`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a19bdce016f3fc2196a3f8b7bbf1d5b0f3b37761962b13b4a8789e049aa2dc6`  
		Last Modified: Thu, 25 Apr 2024 22:51:30 GMT  
		Size: 64.3 MB (64325218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e46dd6605ab6c8c0ca45ce3465ae78217799408e15b3025469a26ba3a0eb15b`  
		Last Modified: Thu, 25 Apr 2024 22:51:30 GMT  
		Size: 4.3 KB (4268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ba540be25fb1c50ce6e15c7d014b0898799c19a5e1c912baecab1c9abae17e`  
		Last Modified: Thu, 25 Apr 2024 22:51:30 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e46ac30353594b3e227d921db7fd6374993e5bf275e9f0ad13dda6ba6b4207a`  
		Last Modified: Thu, 25 Apr 2024 22:51:30 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e866a923a2d070d81279330562496f4506fe760d5d3cc56bd339d3394c969e95`  
		Last Modified: Thu, 25 Apr 2024 22:51:31 GMT  
		Size: 1.6 MB (1588549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:c37d2434091a96af4a1afb4e9d910aac4bdfcc04f7c7c73e67762efa28859f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3693567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a295eef6f5d0b62b10c0e9bc2aca4b9e80b47e0a9e1bd02783954f596a86795`

```dockerfile
```

-	Layers:
	-	`sha256:735b0096afe284e1cd6a3d20c8bb190560aa4eae8d6e7e72aa9193e14d87033c`  
		Last Modified: Thu, 25 Apr 2024 22:51:29 GMT  
		Size: 3.7 MB (3658697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf71f64f53ed7adf321f07b542485fb8b2421868ba54e4d7c557d1ea7af45f3`  
		Last Modified: Thu, 25 Apr 2024 22:51:29 GMT  
		Size: 34.9 KB (34870 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:0fc6173068ab8f74b59a921d31e338ee0594636532eab56384c5867b83943dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150699184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bd5bfbb0556e1a0557860bf91bb2f3fa380d37313c7bf3b67f34a8c8504bdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:511fd2f076c60f46f9185a7e8c176585251f3eec5c08d6b4cb8efdb0a9bb53fb in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=-slim
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:071d1faceffed6640d770a55f271b5d135ce2ffc51ec5653810e9f20e5c4c5fd`  
		Last Modified: Thu, 18 Apr 2024 01:33:02 GMT  
		Size: 27.5 MB (27534148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002cecbb9c98fb3389e41e26f05485fc9e85f910cff583a691fbb102ee905a42`  
		Last Modified: Thu, 25 Apr 2024 20:32:45 GMT  
		Size: 12.5 MB (12492638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f6e0163838b603fff5bd2b859818d2d4d95b42e5a473d9aeb55caae0dd9294`  
		Last Modified: Thu, 25 Apr 2024 20:35:54 GMT  
		Size: 44.9 MB (44917119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce20dd53ab5e75776355fb45f6ef2d2608f516124b855ad4991912ef1853286`  
		Last Modified: Thu, 25 Apr 2024 20:35:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c43bb76d1f4547b0f77e71254784d3235488fff0d81419914a76540c4179e2`  
		Last Modified: Thu, 25 Apr 2024 20:35:47 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f65b06e42006b1e6612a9353e4788705d1215d11e6b27d12da03e304c4a965b`  
		Last Modified: Fri, 26 Apr 2024 20:40:38 GMT  
		Size: 64.3 MB (64325408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286be7491092cf46b553c707a057282589aee042f56b770ac959c4c9603d45de`  
		Last Modified: Fri, 26 Apr 2024 20:40:36 GMT  
		Size: 4.2 KB (4208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782936382d74a6adb41a38b54b9ffc03fde2ebfae4ca507ab79fc52c790d2abe`  
		Last Modified: Fri, 26 Apr 2024 20:40:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e4fccb26464817858f84ecf17cd6f5eae3c180c264b5f1abb4e8f0406adc87`  
		Last Modified: Fri, 26 Apr 2024 20:40:36 GMT  
		Size: 10.8 KB (10786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b1b76b161b85970d6ff95b29dcfe59d0b4214c4f59781d51adcfacb515e871`  
		Last Modified: Fri, 26 Apr 2024 20:40:37 GMT  
		Size: 1.4 MB (1413739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:25f817b5607edad1afb646d74a7907afc26325bb12f72a70ad9337ef6b35e807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3694250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21813587ded5e646b8f1a3967042d6e7f2003636539ecbd81f740d757999b281`

```dockerfile
```

-	Layers:
	-	`sha256:373a28aacd2282561e6b48b063e04f58f84117fc28243b4b5c1b948f17b24e9e`  
		Last Modified: Fri, 26 Apr 2024 20:40:36 GMT  
		Size: 3.7 MB (3660074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dae425049eee4ccf42504983e746ecd46da0dc6d6b25b0308b20ef9159d7ab92`  
		Last Modified: Fri, 26 Apr 2024 20:40:36 GMT  
		Size: 34.2 KB (34176 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:298a3f3b17b74ec3b556652b8ad430a233ffe0eb41daa7b79f9c89782f2b8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153753147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ee91c08f08770865bad25dfd314421729d57b685829a3cede5ef8a6b0295b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=-slim
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f037ef0398100188bd636ef3da1525cc5cc7f04347a802ecc28ba3240408631`  
		Last Modified: Thu, 25 Apr 2024 21:59:12 GMT  
		Size: 12.8 MB (12846901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a9d01cdbea836fa98a88c869097ca339c17dd29480bc1c936f937840fbde4d`  
		Last Modified: Thu, 25 Apr 2024 22:02:15 GMT  
		Size: 46.7 MB (46716123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e659b60df2e1030cfa0f2df9583f9aab145276e83a37490b983bbcfa9322fde3`  
		Last Modified: Thu, 25 Apr 2024 22:02:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f320f164b70019d3de719bb4a4b380f596330be1d584f5d935f80a4344b5b48`  
		Last Modified: Thu, 25 Apr 2024 22:02:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419501423240a6cee4ca7320b086b7bb98c4fe044bfa0ab168c9a0ab80be5ade`  
		Last Modified: Fri, 26 Apr 2024 09:40:45 GMT  
		Size: 64.3 MB (64325415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a117a66a6769217b5565d936f5266352e672d11f1d2acafdd5578821f6bc0c8`  
		Last Modified: Fri, 26 Apr 2024 09:40:41 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fc1bbafccfa1bd40598abd78f7a2fb8bf2b649f674ee206fa0d188f1e7d3eb`  
		Last Modified: Fri, 26 Apr 2024 09:40:41 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc9904b6a4002d031a909f8ddaceeff15e2a6983252c748342f6f7e59684691`  
		Last Modified: Fri, 26 Apr 2024 09:40:41 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458a6a0ad6d7b683a0072727295e5707148256f89b16ed03a4ad96193f391972`  
		Last Modified: Fri, 26 Apr 2024 09:40:43 GMT  
		Size: 1.4 MB (1447477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:080194bda73a16eac1b4280863d9016860ec48bf78a1ff2e0a15f3e699606cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3693009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9242adaf38c12df96bcb481d0e24c93570a26d7fa824b7e69210bc488954d4e`

```dockerfile
```

-	Layers:
	-	`sha256:386463cbaa7a2e09f300000d2d08c1b53642d107ed1d94ad04933a262659733e`  
		Last Modified: Fri, 26 Apr 2024 09:40:42 GMT  
		Size: 3.7 MB (3658945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a99116d8b42fb81e2afd80c3fa63e7be0568d25c68eb8a75ca62b6f013842f3`  
		Last Modified: Fri, 26 Apr 2024 09:40:42 GMT  
		Size: 34.1 KB (34064 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:cfff311c432606ee4908cb8505bc8d851416c8c09c615e5c0bc43cdd78f4a148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162381928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5595e43b32588d7d27785a58076ea619345fe340c9fa4eb5dd67f0ab3d9a65e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=-slim
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a9466735f8829921e05503ca4d4d92bb6f06facd77aa4b2feb86645d7c27b1ba`  
		Last Modified: Thu, 25 Apr 2024 20:35:05 GMT  
		Size: 35.6 MB (35588305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0de467fd0448940d36a45afa474251ce2e8bd6e8f60ef7eb65adb86c07161a`  
		Last Modified: Thu, 25 Apr 2024 20:52:58 GMT  
		Size: 13.8 MB (13767010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139c1ea4e64d0b726f7d19518870f27a28d6bc36f6ac3db66d8eb91060a294de`  
		Last Modified: Thu, 25 Apr 2024 20:56:22 GMT  
		Size: 47.1 MB (47088915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8b1496c6d2c3bf4eee8880414a7a0f10b22fecc23b08012e3d6e7580bd8ac5`  
		Last Modified: Thu, 25 Apr 2024 20:56:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016cbc90916d690e8bd5221d91fa763a9df5fed03fdf320b50d50025a43d31ef`  
		Last Modified: Thu, 25 Apr 2024 20:56:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f168471a82cf217d26c29a303a243ef0841eb65d818004b8958684af037bfb`  
		Last Modified: Fri, 26 Apr 2024 17:38:44 GMT  
		Size: 64.3 MB (64325887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f118b09dfd8f3a03cbafba263edfd4532f322e2171f3ed7b8ee50e978672eaf9`  
		Last Modified: Fri, 26 Apr 2024 17:38:42 GMT  
		Size: 4.3 KB (4284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f47acf58ebaecfd416240a81f5b0fea12542c1b5fe2799a60cc631db71e986`  
		Last Modified: Fri, 26 Apr 2024 17:38:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea893a183348a0d5cdf4820e4a8f65daae6e45b3009d3faddf7bf8f9865b387`  
		Last Modified: Fri, 26 Apr 2024 17:38:42 GMT  
		Size: 10.8 KB (10787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0451e4613474a6d213191b44d3281b3e2df25c70f1d12535bc5276ddca0c14`  
		Last Modified: Fri, 26 Apr 2024 17:38:43 GMT  
		Size: 1.6 MB (1595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:0752fd02b57e22074dc33928fc5a73b31f525501f85d8e5b334a533bb9eb50f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3697323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63837ae9c5d9856e204d1ab2abe96964f03725b23f9c2e589216a9254290257d`

```dockerfile
```

-	Layers:
	-	`sha256:e56b2b82143259346ebf35e363662525a5e44330604bb6ae70ef3ddc99fc981c`  
		Last Modified: Fri, 26 Apr 2024 17:38:42 GMT  
		Size: 3.7 MB (3663223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc57915cbc2b4f3270091aec3ba4e2aaae21f71f5d03f41a2557141cd8252b93`  
		Last Modified: Fri, 26 Apr 2024 17:38:42 GMT  
		Size: 34.1 KB (34100 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:528dd5cc94d61cc21bdc00eba48bd61e1833fe31bc1ee72d34342fde697d5789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151332068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2f5c8d432752b70467f41c99055fda62b38ff3f0db8428ce0a74740f4ff59b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:f721f8e69988c4a423ddfb143b1001213ba52ffe029e8623c2f62e210d611fbc in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=-slim
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST=-slim SOLR_SHA512=9b94bbd4331aa5b871a388e39c38a381a8090041afabf8f0e338a776dbd1953bded419e8bbbee96771f4434f47884efa3eeb837f83b4ca55973b8c9f3bd045f6 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a9e3c76851ed4cb17ff69f864b6230094c69b50fc344074f5cccf18cabee6dbf`  
		Last Modified: Thu, 25 Apr 2024 20:58:17 GMT  
		Size: 28.6 MB (28637471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256964579a885020253dbe5c22f56c46052445d333305990618830cec3421a61`  
		Last Modified: Thu, 25 Apr 2024 21:19:46 GMT  
		Size: 13.0 MB (12986661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed742935159ae2c8d2eb3c9f9c197cd910b010bd4da24fa3b3742f4d490ab32a`  
		Last Modified: Thu, 25 Apr 2024 21:21:38 GMT  
		Size: 43.8 MB (43830966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb485526c73c1b0a7f4587028c9115bb0d739697e08a0ecee6641e11aca6ac9`  
		Last Modified: Thu, 25 Apr 2024 21:21:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c371f0304c7553249d1955cd601fbf909fbe857da6c62e96f58b2ea42297afaf`  
		Last Modified: Thu, 25 Apr 2024 21:21:32 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f32c97204df434b81b3f1a6d4c8ad832db5e02c903e3420a875e214279a8cf4`  
		Last Modified: Fri, 26 Apr 2024 20:36:21 GMT  
		Size: 64.3 MB (64325468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99c7e3ca279151e32ec1b11dfdc986fad95b733dbc60f308f9a418f03c5cde8`  
		Last Modified: Fri, 26 Apr 2024 20:36:18 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381f397ce45248ec60e4d53f0c70002bc87288d0852ecefccea406faa215f32e`  
		Last Modified: Fri, 26 Apr 2024 20:36:18 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8fa56c327b90da21a840d84737f489f6c4d0f33d7277bfc1aec5f62051f60`  
		Last Modified: Fri, 26 Apr 2024 20:36:18 GMT  
		Size: 10.8 KB (10790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0423f69b371b48a2ffa93ef07cf59fab85dce5b3adfc3606c5511dc370d9e2f`  
		Last Modified: Fri, 26 Apr 2024 20:36:20 GMT  
		Size: 1.5 MB (1535266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:7555c3b5a978931416af2edf9f0a310b0dbae92e2e1cd6119c919a0ab31ba102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3694015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1087bfbdfe8d2e85e71cab58bfb9e1171883e8ef2cc8d2225e38cd5463433e6`

```dockerfile
```

-	Layers:
	-	`sha256:caf83d6b0a6b10c3f9d76fbebde298029a27cffad83985ec94ebdd9a91478fa8`  
		Last Modified: Fri, 26 Apr 2024 20:36:19 GMT  
		Size: 3.7 MB (3659961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840b95efdd40b392cb735693add617413410f3c0cb0887b2920fa284371b412f`  
		Last Modified: Fri, 26 Apr 2024 20:36:18 GMT  
		Size: 34.1 KB (34054 bytes)  
		MIME: application/vnd.in-toto+json
