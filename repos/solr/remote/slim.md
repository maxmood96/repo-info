## `solr:slim`

```console
$ docker pull solr@sha256:d8f60b98737965a4411a0be53213b1fa8c313a6035be3200a8c9233085827b31
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
$ docker pull solr@sha256:dc7f72ca586672e5da840651649d33419d4ba46519207b3b7128e163fce3d18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159261474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca07413c96b38fd218bca97d2a36baa91692a0c0d9ae0a542cce3a85c8202216`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
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
	-	`sha256:6dbdd66677ae28be6f823c23b8d51a41a37c8a90b681cfd70a7b2e96aa6c105a`  
		Last Modified: Wed, 09 Apr 2025 01:16:02 GMT  
		Size: 16.1 MB (16145981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398a057cfd5d1a9035ebf597cf462a19c5c1196c0974ed065194227c98f6d8e`  
		Last Modified: Wed, 09 Apr 2025 01:16:02 GMT  
		Size: 47.0 MB (46952605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e4752518b6204aa4ba8b84224f9310138f8df9508501b556a7be2bc5ddf229`  
		Last Modified: Wed, 09 Apr 2025 01:16:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755fa637644516f5e5f0689940dec99aec73146e683ab7675190d51c696bf50`  
		Last Modified: Wed, 09 Apr 2025 01:16:02 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05678096149f43a3fca3d3cffc89c30a68f520e0c0f4b2e28423e4ce8152f339`  
		Last Modified: Wed, 09 Apr 2025 02:47:55 GMT  
		Size: 65.0 MB (64994879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f312ab3ec22718d144fafe18212974dcead19866c59d730b2d18369d360858`  
		Last Modified: Wed, 09 Apr 2025 02:47:53 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f549e4723178c1c580a17802d21d18a70a2e92bd0818f1a0757bcb8a3f82ea`  
		Last Modified: Wed, 09 Apr 2025 02:47:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654f425b9e2d43bd386c6cedecf0a93c6e5a3d9456412a6b2bb98d50087356d0`  
		Last Modified: Wed, 09 Apr 2025 02:47:53 GMT  
		Size: 10.8 KB (10803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5630d66436b449c2aca4e8c3129a43bc0170535318cbcfdf182eb22256f230a`  
		Last Modified: Wed, 09 Apr 2025 02:47:54 GMT  
		Size: 1.6 MB (1617886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:91583f8f943e6e63e16c0665e03e49ce6bbe9b169c6622462763eac9799e39f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698dfe9534134c962d4b7ae2243c599f448a668b916ccf999bdcd3b620204c0f`

```dockerfile
```

-	Layers:
	-	`sha256:9ffcf235b709c99c10c81ffeb100b83b12eb5acf8da72f1e7cb06763b8aab639`  
		Last Modified: Wed, 09 Apr 2025 02:47:53 GMT  
		Size: 3.8 MB (3798988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e00e02b55a24fa257c931eb58ecb2cc2616bec0767435c55a796879198b4061e`  
		Last Modified: Wed, 09 Apr 2025 02:47:53 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:c519924db4bbb1d912e05cebb9b96c99c59a7aef6e79b1800ec77883dda51559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156361795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0bade76575f94bb9dd1efea53ee8106b0b91010d41a8a6c5f99ddada30fa9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cdf344ce31106e3e5ac67eee27b0e8010b825882fbd536b820a7fbc2ede17b`  
		Last Modified: Tue, 11 Mar 2025 23:26:47 GMT  
		Size: 65.0 MB (64994930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8b2aa95045fa29c7d55bdd82d01623f3d3f28931e5141291d08dfad134c4df`  
		Last Modified: Tue, 11 Mar 2025 23:26:45 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f95469b18bd53eb9edbb43f722837a04a01599aa966fe9922a26d78d694f40c`  
		Last Modified: Tue, 11 Mar 2025 23:26:45 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cafd47630935328096d80ecdd2da91723668090b484c8a7aee9910b64bafcb`  
		Last Modified: Tue, 11 Mar 2025 23:26:45 GMT  
		Size: 10.8 KB (10801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0e4b3d3f24d7a2cec0986cd8f9d20e591c6e7c7d121ef3913d4ecc0b78cadf`  
		Last Modified: Tue, 11 Mar 2025 23:26:47 GMT  
		Size: 1.5 MB (1474680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:d8079dac25c708663c027838c94424ada2afe158b98e7e16d2825a68724464ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c8e2a9151d5a9eb8d85f86fd9c7e838a8e11c9124507a9203150ce62353014`

```dockerfile
```

-	Layers:
	-	`sha256:18a40034dc95d1731c9639dc3ccf4c98919c77e1e79497b0852f20a6f01165ff`  
		Last Modified: Tue, 11 Mar 2025 23:26:46 GMT  
		Size: 3.8 MB (3796876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ae9d3ca78c63aa4ddcf3a5badd62266e11717481799fcbf51e96990d9c7ca5`  
		Last Modified: Tue, 11 Mar 2025 23:26:45 GMT  
		Size: 34.6 KB (34562 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:5c837926d274af9db0435682984ea436af81f9a5067fab677a3db7993a6d0d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165503476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4838368c1cb74e7daabc889e0a5a565f5c9885d32f590106ca9e4ba44d23ff5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
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
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71de2d980599cbec4dab5c3bd7274078312e68d7cc81171b5d8bda1a98eb2403`  
		Last Modified: Tue, 04 Feb 2025 07:32:10 GMT  
		Size: 17.6 MB (17642335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30b6dc9603fa30cfaeaf94b4f0afc490673bc37614634f344ef2172f29afa74`  
		Last Modified: Tue, 04 Feb 2025 07:44:12 GMT  
		Size: 46.8 MB (46769698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c04307e9c18ff1b510c546e4467455954ff8ab916e0e48044941ce74965ac83`  
		Last Modified: Tue, 04 Feb 2025 07:44:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640f96035063c914d8c6861a46f9131b45dc5967d86d34cb927cfa5c131d7750`  
		Last Modified: Tue, 04 Feb 2025 07:44:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9558cbffc811d3b1bd7fb7e8895835e2e8dba12d2906de388c04ed2f7bab00`  
		Last Modified: Tue, 11 Mar 2025 23:28:04 GMT  
		Size: 65.0 MB (64995122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0920e4c4e4d8f7429da95c2fe5192e8a1754c23a1e7ee1e873c6d9b3f07de653`  
		Last Modified: Tue, 11 Mar 2025 23:28:01 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75b8a33c6e88b639f1efbbecc0065bcd20a48dac7ea3b16c74b29118b03922`  
		Last Modified: Tue, 11 Mar 2025 23:28:01 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f070bf9f04395d2ba35dfdd1558047e45c623be2e2131c40c04d3ecd8eeb62d`  
		Last Modified: Tue, 11 Mar 2025 23:28:02 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b52d2e7d3f3835d7e3d4225f5b754978a02c959a54c96bc3e3281d2b7c3396`  
		Last Modified: Tue, 11 Mar 2025 23:28:03 GMT  
		Size: 1.6 MB (1630615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:406c9dbe845e49a12daf95f717931e90bb52c6021f858c9f89423de287e950dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53d014c4b407a813a452a261a5d0376b0846f09835e5c08b8727b7e7154d89e`

```dockerfile
```

-	Layers:
	-	`sha256:330c4087b90fd55232b7ceca509c58ee14362d3f97474ceda0b07d17b691dc7e`  
		Last Modified: Tue, 11 Mar 2025 23:28:02 GMT  
		Size: 3.8 MB (3801109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d1716cc0aae2ecc3985f74b734f80a42bbb074f962d1fc73e0db7c33fd755d2`  
		Last Modified: Tue, 11 Mar 2025 23:28:01 GMT  
		Size: 34.5 KB (34450 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:85446204747e99602af645ff4e1226f25099fcf8420b58e1fa75ca066f511313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154664702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad279af2da055adf94e2af88f5221ea3f73a9b409cdf674a5fdd5e334f963f43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
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
	-	`sha256:bc0185ff1fe24ff27980b2adf7a65b3a05510d98cee059380f8c4a7884953738`  
		Last Modified: Wed, 09 Apr 2025 04:23:14 GMT  
		Size: 43.9 MB (43949614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae6b1bf32d9c4d5260f66bbf416c75a51d3cc4e8b61033dc4da31066883a4de`  
		Last Modified: Wed, 09 Apr 2025 04:23:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2633fd87d03e2beccef8cebf02b5b117ed3756653d6600ba704e0075e8d43e58`  
		Last Modified: Wed, 09 Apr 2025 04:23:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f00a8c34a3323d3c59c10d34ed9e47ecc9380e114666614f76d860b351970c`  
		Last Modified: Wed, 09 Apr 2025 06:13:04 GMT  
		Size: 65.0 MB (64994686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345330948131ca8b04e24e001a20586abdd4df8ffba9aa954bbe542600c21da5`  
		Last Modified: Wed, 09 Apr 2025 06:13:02 GMT  
		Size: 4.3 KB (4303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f449f1014a4c7b6564f5d1ff41ba0ef8536ee67331befaac5e7487adf932a`  
		Last Modified: Wed, 09 Apr 2025 06:13:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40a6b80c36a7be68fa2880c596311b2d2ed8a4f2a81e6412d642702ed8909e0`  
		Last Modified: Wed, 09 Apr 2025 06:13:02 GMT  
		Size: 10.8 KB (10803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6af35c47eb8ff76f8eafb8d20bd075ed3a32422ee623d3db3272f6e8e9fcf02`  
		Last Modified: Wed, 09 Apr 2025 06:13:03 GMT  
		Size: 1.6 MB (1558936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:118c231681b84c671029dff1e6bcd235888c290b554e0e53f4b2582d963461c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab7bde5990de0e71ef693f5e66760e8cc7d38d325b16d7c0e71db42ac22629e`

```dockerfile
```

-	Layers:
	-	`sha256:7d3d1077530a588e51f4277bd356b468d6fb56bc4756e442f7fbe3f1b4119fa9`  
		Last Modified: Wed, 09 Apr 2025 06:13:02 GMT  
		Size: 3.8 MB (3800584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29152bb5f38eec9da610ff9e6a8ac2447b181b9f00ee7448ea0c6bc49c9ff734`  
		Last Modified: Wed, 09 Apr 2025 06:13:02 GMT  
		Size: 34.4 KB (34398 bytes)  
		MIME: application/vnd.in-toto+json
