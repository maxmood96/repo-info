## `solr:10-slim`

```console
$ docker pull solr@sha256:cf7c3da468539644200ca50fb5af2b1da15a19dca75228e596223ae2e6018b0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `solr:10-slim` - linux; amd64

```console
$ docker pull solr@sha256:ab0dc1b2b59769256609d9f3fa93482b0cdb3cf275569b4490fe478f86bff301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187072712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a71dac2f1b598c8d6a09a2e5eb64001d24fd329ff5db43462502fdff100b8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:55 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 08:15:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:15:17 GMT
ARG SOLR_VERSION=10.0.0
# Tue, 02 Jun 2026 09:15:17 GMT
ARG SOLR_DIST=-slim
# Tue, 02 Jun 2026 09:15:17 GMT
ARG SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1
# Tue, 02 Jun 2026 09:15:17 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 02 Jun 2026 09:15:17 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 02 Jun 2026 09:15:17 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 02 Jun 2026 09:15:17 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 02 Jun 2026 09:15:17 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 02 Jun 2026 09:15:17 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 02 Jun 2026 09:15:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 02 Jun 2026 09:15:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 02 Jun 2026 09:15:17 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 02 Jun 2026 09:15:17 GMT
LABEL org.opencontainers.image.version=10.0.0
# Tue, 02 Jun 2026 09:15:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 02 Jun 2026 09:15:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_HOST_BIND=0.0.0.0 SOLR_ZOOKEEPER_EMBEDDED_HOST=0.0.0.0
# Tue, 02 Jun 2026 09:15:17 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 02 Jun 2026 09:15:17 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 02 Jun 2026 09:15:17 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr; # buildkit
# Tue, 02 Jun 2026 09:15:22 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install curl acl lsof procps wget netcat-openbsd gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 02 Jun 2026 09:15:22 GMT
VOLUME [/var/solr]
# Tue, 02 Jun 2026 09:15:22 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 02 Jun 2026 09:15:22 GMT
WORKDIR /opt/solr
# Tue, 02 Jun 2026 09:15:22 GMT
USER 8983
# Tue, 02 Jun 2026 09:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 09:15:22 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d0df2f6a2ab4ebe6312620361d10bc95934f9c0b214263709202f165ca7dd2`  
		Last Modified: Tue, 02 Jun 2026 08:15:22 GMT  
		Size: 11.5 MB (11481021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9506eaedce63a0941d41b9b3b7f027e715f7d4724bb184a69093d8bfc11fac`  
		Last Modified: Tue, 02 Jun 2026 08:15:23 GMT  
		Size: 63.0 MB (63042669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c6a52a9f2d0a2c17c05bbf39b1d11933cf0c821cc38a4d29de0b85597dd6c0`  
		Last Modified: Tue, 02 Jun 2026 08:15:21 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a940d9e59275676fd417fdbe574b3f5e7e035a337840e22aab2eccea6d355660`  
		Last Modified: Tue, 02 Jun 2026 09:15:35 GMT  
		Size: 79.0 MB (79044390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9673c4d960479fe489236249c70f994211c8773a5362c68d5846a8c38e22a9`  
		Last Modified: Tue, 02 Jun 2026 09:15:33 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b0949ae341b866b37a60d42feeb4e5dfa608646c952c4b475bd3a48513a5e0`  
		Last Modified: Tue, 02 Jun 2026 09:15:33 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3921c6f6dee895d37d794718780e5e9847ec6497b01d2421c3831d7dd88802`  
		Last Modified: Tue, 02 Jun 2026 09:15:33 GMT  
		Size: 10.3 KB (10303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b1fb50effef4d0ce88571378172dcea79f65d2e2444591327373239416e5db`  
		Last Modified: Tue, 02 Jun 2026 09:15:34 GMT  
		Size: 3.8 MB (3757806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:ef800a58206746c7d59b13be048991eeb7d37350f1aae1bc5008cd66bb7d6f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3481588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:263437872dfd6c9eb296715cfd51c6ffc4906a345ccb8e38836bf3fcb8e6ea47`

```dockerfile
```

-	Layers:
	-	`sha256:b6e574611ac3609a5d7f24cb6568d7377568eb31db94d0e91d11babdde15b4ca`  
		Last Modified: Tue, 02 Jun 2026 09:15:33 GMT  
		Size: 3.4 MB (3447899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c484c9c1c0d7586d0112fbc0eff743debcd8ed0eff396c790edf3cea169ff70`  
		Last Modified: Tue, 02 Jun 2026 09:15:33 GMT  
		Size: 33.7 KB (33689 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:10-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:9acaec349658d0e619a0eb9a87ba2e833bc6b48e71f8606a5ec82e6c74e029a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185005570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6fab55c36b23349a67202750d3c658ca79cac7f8888460a112490519b089a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:16:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:16:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:16:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:16:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:16:20 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 08:16:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:16:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:16:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:23:38 GMT
ARG SOLR_VERSION=10.0.0
# Tue, 02 Jun 2026 09:23:38 GMT
ARG SOLR_DIST=-slim
# Tue, 02 Jun 2026 09:23:38 GMT
ARG SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1
# Tue, 02 Jun 2026 09:23:38 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 02 Jun 2026 09:23:38 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 02 Jun 2026 09:23:38 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 02 Jun 2026 09:23:38 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 02 Jun 2026 09:23:38 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 02 Jun 2026 09:23:38 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 02 Jun 2026 09:23:38 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 02 Jun 2026 09:23:38 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 02 Jun 2026 09:23:38 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 02 Jun 2026 09:23:38 GMT
LABEL org.opencontainers.image.version=10.0.0
# Tue, 02 Jun 2026 09:23:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 02 Jun 2026 09:23:38 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_HOST_BIND=0.0.0.0 SOLR_ZOOKEEPER_EMBEDDED_HOST=0.0.0.0
# Tue, 02 Jun 2026 09:23:39 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 02 Jun 2026 09:23:39 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 02 Jun 2026 09:23:39 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr; # buildkit
# Tue, 02 Jun 2026 09:23:45 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install curl acl lsof procps wget netcat-openbsd gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 02 Jun 2026 09:23:45 GMT
VOLUME [/var/solr]
# Tue, 02 Jun 2026 09:23:45 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 02 Jun 2026 09:23:45 GMT
WORKDIR /opt/solr
# Tue, 02 Jun 2026 09:23:45 GMT
USER 8983
# Tue, 02 Jun 2026 09:23:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 09:23:45 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b7f0fccaa95dd1f467cb56660e823611c5dceab12394080192b2d096b51837`  
		Last Modified: Tue, 02 Jun 2026 08:16:50 GMT  
		Size: 11.5 MB (11476696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedcf77a89a74305c7149e84edf17b9eead7a533f590a7794436a3ae0ee0e8c3`  
		Last Modified: Tue, 02 Jun 2026 08:16:51 GMT  
		Size: 61.9 MB (61943121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de26c161c75c21efc1e78e614f5b450580938483d69ea769b709551852428c24`  
		Last Modified: Tue, 02 Jun 2026 08:16:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae0a849cee0a943399a8f05bc1b999982c77f75add32d94ba51988c1f22cd3f`  
		Last Modified: Tue, 02 Jun 2026 09:24:00 GMT  
		Size: 79.0 MB (79046125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fddc76c3a0b0ce9a2c4771dca909a6ed3b0319fa9a545400e345f95a1605b2d`  
		Last Modified: Tue, 02 Jun 2026 09:23:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147445d4f0aa2c77e5c831fe5f79cfdbddf68a87cddd0b5ae1726726595e254b`  
		Last Modified: Tue, 02 Jun 2026 09:23:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007093e3c59c98a3f962634297f900e22fcbd29d0d438e9c32bc905b204abab8`  
		Last Modified: Tue, 02 Jun 2026 09:23:58 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e06a6cd659a8acf0ef2535c2966027fe67b5d8c0aacf095ce7c7f99ee6baec`  
		Last Modified: Tue, 02 Jun 2026 09:23:59 GMT  
		Size: 3.6 MB (3649202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:18b3e78109e531b090d2a997abf5f96709ac3e53c8c97426be290be670ca0629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3482218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8652fed39d206ba7d34251bbf185f32b7057fa858a234b7e54197be32e9a56f5`

```dockerfile
```

-	Layers:
	-	`sha256:e20102ed161e6b1566cf526c9f903366abc9a31200b1399c7d96864d883ac852`  
		Last Modified: Tue, 02 Jun 2026 09:23:58 GMT  
		Size: 3.4 MB (3448365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0f81baa55011420f7eef967bf9c36e0a7d82ce1e7d95763e02a368de23acdc7`  
		Last Modified: Tue, 02 Jun 2026 09:23:58 GMT  
		Size: 33.9 KB (33853 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:10-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:134ba7be0fb8de5634e59660a90df2744efde75e6651e82d90fb29981a90999c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192202852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123a959c8d7cff754c2a87a8778042300ee6dd6e5adfa398d9c218719e98bb69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:33 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 08:15:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:16:53 GMT
ARG SOLR_VERSION=10.0.0
# Tue, 02 Jun 2026 10:16:53 GMT
ARG SOLR_DIST=-slim
# Tue, 02 Jun 2026 10:16:53 GMT
ARG SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1
# Tue, 02 Jun 2026 10:16:53 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 02 Jun 2026 10:16:53 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 02 Jun 2026 10:16:53 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 02 Jun 2026 10:16:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 02 Jun 2026 10:16:53 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 02 Jun 2026 10:16:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 02 Jun 2026 10:16:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 02 Jun 2026 10:16:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 02 Jun 2026 10:16:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 02 Jun 2026 10:16:53 GMT
LABEL org.opencontainers.image.version=10.0.0
# Tue, 02 Jun 2026 10:16:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 02 Jun 2026 10:16:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_HOST_BIND=0.0.0.0 SOLR_ZOOKEEPER_EMBEDDED_HOST=0.0.0.0
# Tue, 02 Jun 2026 10:16:53 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 02 Jun 2026 10:16:54 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 02 Jun 2026 10:16:54 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr; # buildkit
# Tue, 02 Jun 2026 10:17:07 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install curl acl lsof procps wget netcat-openbsd gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 02 Jun 2026 10:17:07 GMT
VOLUME [/var/solr]
# Tue, 02 Jun 2026 10:17:07 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 02 Jun 2026 10:17:08 GMT
WORKDIR /opt/solr
# Tue, 02 Jun 2026 10:17:08 GMT
USER 8983
# Tue, 02 Jun 2026 10:17:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 10:17:08 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14555f1475b5161df9db41ed4a7e500e82373184731715cb4aa463c046a5eb8d`  
		Last Modified: Tue, 02 Jun 2026 08:15:28 GMT  
		Size: 12.0 MB (12047670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f4460cf7c7d2f0cdcc8e013a547be64a5626d1a813f4b843da16b4ab31dc26`  
		Last Modified: Tue, 02 Jun 2026 08:15:30 GMT  
		Size: 62.4 MB (62442841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e0bf549bb69914d40c79d648069e4c5e50b2e7b21e3c22e32064475d65a878`  
		Last Modified: Tue, 02 Jun 2026 08:15:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d8433be10ade41fa70330f89b4c07daf32ee7706dbed847b9a7d02a66967e`  
		Last Modified: Tue, 02 Jun 2026 10:17:46 GMT  
		Size: 79.1 MB (79113377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbf9489534a7e1f614701fc096aa7cd896c24cbcb05e18682b58ec40101f60f`  
		Last Modified: Tue, 02 Jun 2026 10:17:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572af874a27b6f1e75c3d9195605a4e1f5f4cce857099c30c20a01e1cf0088b3`  
		Last Modified: Tue, 02 Jun 2026 10:17:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e926e5635e665cd6cd8dbe3dbfd2eb5dfc7e4e1b6d755381ad6ddf7270a7e9`  
		Last Modified: Tue, 02 Jun 2026 10:17:44 GMT  
		Size: 10.3 KB (10307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe04ab69d258845b1a6836c01f8c2985686fa6cdde79d713716ccedfbbf17c5`  
		Last Modified: Tue, 02 Jun 2026 10:17:46 GMT  
		Size: 4.3 MB (4270836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:f709f17ce8382a15b5a76a5254544808d5d9c801887ee19209b34eb70439faea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10ab4f7a03ab23593a5deb265eda79a42f93fa2d6ffbd985124e8b00d93b839`

```dockerfile
```

-	Layers:
	-	`sha256:f4e084908e8c25ada4b21d9ea7c2fcee3c376eb7b2110c2343e6d46baad46621`  
		Last Modified: Tue, 02 Jun 2026 10:17:44 GMT  
		Size: 3.5 MB (3451332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3af84971efab26e9cdac43d8febeb498afe909048a699f5ec2daa79da7226c48`  
		Last Modified: Tue, 02 Jun 2026 10:17:44 GMT  
		Size: 33.7 KB (33741 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:10-slim` - linux; riscv64

```console
$ docker pull solr@sha256:00c23a9d295f1bedc267be09d54803e9f455c38c04c57d20425eb17bef0b8919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187056775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3100cbb0aefc276913ec1805eec038d42eab6a10ca4bb637144bbcae7158ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:24:05 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:24:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:24:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 09:24:43 GMT
ADD file:a9a4679e3df2846468311b83a8f6ab86f5a205bab966d3f236c9f30151010c5b in / 
# Fri, 10 Apr 2026 09:24:47 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 17:16:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 17:16:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 17:16:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Apr 2026 17:16:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 17:16:29 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:49:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:49:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:49:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:49:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 May 2026 00:42:00 GMT
ARG SOLR_VERSION=10.0.0
# Fri, 01 May 2026 00:42:00 GMT
ARG SOLR_DIST=-slim
# Fri, 01 May 2026 00:42:00 GMT
ARG SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1
# Fri, 01 May 2026 00:42:00 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Fri, 01 May 2026 00:42:00 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 01 May 2026 00:42:00 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.version=10.0.0
# Fri, 01 May 2026 00:42:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 01 May 2026 00:42:00 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_HOST_BIND=0.0.0.0 SOLR_ZOOKEEPER_EMBEDDED_HOST=0.0.0.0
# Fri, 01 May 2026 00:42:01 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 01 May 2026 00:42:01 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 01 May 2026 00:42:02 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr; # buildkit
# Fri, 01 May 2026 00:42:54 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install curl acl lsof procps wget netcat-openbsd gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 01 May 2026 00:42:54 GMT
VOLUME [/var/solr]
# Fri, 01 May 2026 00:42:54 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 01 May 2026 00:42:54 GMT
WORKDIR /opt/solr
# Fri, 01 May 2026 00:42:54 GMT
USER 8983
# Fri, 01 May 2026 00:42:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 00:42:54 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb1da3a1b0530db8bac4f80d6d7cf1cab174ba1fdb49b966e841ec211df17d0`  
		Last Modified: Thu, 16 Apr 2026 17:21:23 GMT  
		Size: 11.6 MB (11570962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40941cf16e4717c40e5532cf516bb886886846120960f18c87affbe922325b4e`  
		Last Modified: Thu, 30 Apr 2026 23:52:33 GMT  
		Size: 61.7 MB (61693654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614352beef2c40d720b7a1387b3a660d056f4e7578072704da8135acd2507070`  
		Last Modified: Thu, 30 Apr 2026 23:52:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a32acaa0c958dd35c41fc929f97715d724c7b774c338fadf79adea2341a238f`  
		Last Modified: Fri, 01 May 2026 00:45:51 GMT  
		Size: 79.1 MB (79059662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c1e3aa794edab81bb50eb594d17eb5ade7d6496c3ebc0fc5a006864296a72b`  
		Last Modified: Fri, 01 May 2026 00:45:38 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a84217abb97ae3c82e4cc4e4b224daee86fcc12766b8544268c4baf6131621`  
		Last Modified: Fri, 01 May 2026 00:45:38 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42865751b78261e36a3111ab399b126b0cdda6723015a3d03332839304dc8165`  
		Last Modified: Fri, 01 May 2026 00:45:39 GMT  
		Size: 10.3 KB (10317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea4e6000daf030a8f3906598a073d4c30ec58f9f0a5cca09398f12e73a79fc1`  
		Last Modified: Fri, 01 May 2026 00:45:41 GMT  
		Size: 3.8 MB (3753138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:8c315e710a658aedf232886642e39bb0267a6cd3c5b90311128f3d5318340e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3473687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19fff30edf6206a3bae156dec463eb0cac96f4ec0a01006300bc78ee3fc650d`

```dockerfile
```

-	Layers:
	-	`sha256:2b69029512db8161265e11687c7ec7be15f14a15d520d186d5a58fc0b410dc5f`  
		Last Modified: Fri, 01 May 2026 00:45:39 GMT  
		Size: 3.4 MB (3439946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5adaa68da26cc006ef4df9cfd06b61b571a24d02d0dfe6b17bd356d1c2ff2968`  
		Last Modified: Fri, 01 May 2026 00:45:38 GMT  
		Size: 33.7 KB (33741 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:10-slim` - linux; s390x

```console
$ docker pull solr@sha256:7450fa31c2b2bea1d305ff4df0a97e1c7060d1c0752a6aa71d527263d2cb63d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185087455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c22a36c7ef88eaad418cd1d2ea895203c6c75c8b922d7a5d94631a318093ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:11:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:11:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:11:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:11:28 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 08:11:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='8325460857162b85050622962cee64cbc441ca9baf07f93a7535fd3f9962ca33';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:11:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:11:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:33:17 GMT
ARG SOLR_VERSION=10.0.0
# Tue, 02 Jun 2026 09:33:17 GMT
ARG SOLR_DIST=-slim
# Tue, 02 Jun 2026 09:33:17 GMT
ARG SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1
# Tue, 02 Jun 2026 09:33:17 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 02 Jun 2026 09:33:17 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 02 Jun 2026 09:33:17 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 02 Jun 2026 09:33:17 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 02 Jun 2026 09:33:17 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 02 Jun 2026 09:33:17 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 02 Jun 2026 09:33:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 02 Jun 2026 09:33:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 02 Jun 2026 09:33:17 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 02 Jun 2026 09:33:17 GMT
LABEL org.opencontainers.image.version=10.0.0
# Tue, 02 Jun 2026 09:33:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 02 Jun 2026 09:33:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_HOST_BIND=0.0.0.0 SOLR_ZOOKEEPER_EMBEDDED_HOST=0.0.0.0
# Tue, 02 Jun 2026 09:33:17 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 02 Jun 2026 09:33:17 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 02 Jun 2026 09:33:17 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr; # buildkit
# Tue, 02 Jun 2026 09:33:22 GMT
# ARGS: SOLR_VERSION=10.0.0 SOLR_DIST=-slim SOLR_SHA512=18817965956567405f5788f391ac94b88777ecb2ebb0ee11ef88e6bd117508461b735f926cdf2e138b9ffb48c51700c104f3f20722f85d4e5bc8c9f790d16ef1 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install curl acl lsof procps wget netcat-openbsd gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 02 Jun 2026 09:33:22 GMT
VOLUME [/var/solr]
# Tue, 02 Jun 2026 09:33:22 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 02 Jun 2026 09:33:22 GMT
WORKDIR /opt/solr
# Tue, 02 Jun 2026 09:33:22 GMT
USER 8983
# Tue, 02 Jun 2026 09:33:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 09:33:22 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a6c1347d2071e585abbda6faebc016cf3adb9603862f369e8bf6e3e4a04cdc`  
		Last Modified: Tue, 02 Jun 2026 08:12:00 GMT  
		Size: 11.8 MB (11758188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5a75241f89dfa61867b04cf818ca7cc81e06f565d067527aca7eaf4c77d4f`  
		Last Modified: Tue, 02 Jun 2026 08:12:01 GMT  
		Size: 60.5 MB (60531627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ad705c368036c8d2aaf4d7deff0c053a7a5d7389f543fa32b710c17040099f`  
		Last Modified: Tue, 02 Jun 2026 08:11:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aabfe87f14e4af7201126ea42275db4d7521dc7893941294517598fd9f93d6c`  
		Last Modified: Tue, 02 Jun 2026 09:33:41 GMT  
		Size: 79.1 MB (79069681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aa26e2f2e3c2d50700674cb68dee9edeabbd631545426cf5791e20685028f4`  
		Last Modified: Tue, 02 Jun 2026 09:33:40 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0c34e52c1883ea2ba9baec3ab834adfd5577a607e2340c4b635b6c0af648c7`  
		Last Modified: Tue, 02 Jun 2026 09:33:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cce52c07ba5324a94127069b42630f7c549c618222481de208e8ccd04d35228`  
		Last Modified: Tue, 02 Jun 2026 09:33:40 GMT  
		Size: 10.3 KB (10305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428a12bd1ee3ea3c9a0a18107ba1b3c2086806cb60b9926f6a09be277ff5e20a`  
		Last Modified: Tue, 02 Jun 2026 09:33:41 GMT  
		Size: 3.8 MB (3801101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:10-slim` - unknown; unknown

```console
$ docker pull solr@sha256:8b9e5500fd11d743878f8c4636ed9b8c587f75098639eee29f253a6fb9c25e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3483169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3159e8af14940f3e06a11c726158e69d68cab92948f4bc64227af1dd4f51c667`

```dockerfile
```

-	Layers:
	-	`sha256:c51139496e158f37fcb39f46ea1a0cd3b1112a8a383f492cbc81f1959ea1f06f`  
		Last Modified: Tue, 02 Jun 2026 09:33:40 GMT  
		Size: 3.4 MB (3449480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca35860f71707f10da941c0e3e775df4549544e5e268834118b3dabba2d4bf5`  
		Last Modified: Tue, 02 Jun 2026 09:33:40 GMT  
		Size: 33.7 KB (33689 bytes)  
		MIME: application/vnd.in-toto+json
