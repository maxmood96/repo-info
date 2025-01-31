## `solr:latest`

```console
$ docker pull solr@sha256:0d68f774bcec166e26439643604f20deb4b5328e90da40e7cb209f76f349bbbf
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
$ docker pull solr@sha256:29bcb7b537760520a5e5cb21d10024ecc3a5ca4ca1bffaf2f12bcda0e766680d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.6 MB (480628588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b652c802a2066f575fe63037477860c20f10f9ac341feb76d50038f2b93da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Jan 2025 19:07:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:07:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_VERSION=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DIST=
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.version=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 Jan 2025 19:07:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
VOLUME [/var/solr]
# Tue, 21 Jan 2025 19:07:29 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 21 Jan 2025 19:07:29 GMT
WORKDIR /opt/solr
# Tue, 21 Jan 2025 19:07:29 GMT
USER 8983
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746a89fef7c9ed5a575e47d48c6120bc97ae3f93e4ab0ae1c08ff243e2e4b600`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 16.1 MB (16134936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2ca0b8abb633ae176227f8ed7ac61279dd8c7f23c90858105bbe06bf0a997`  
		Last Modified: Fri, 31 Jan 2025 01:30:59 GMT  
		Size: 47.0 MB (46952636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f56293176fa410b11d2198dc9dbe622695161a6e0ce63dbfb271e2d03a5376`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0c869e1f807bce22ac6fcdba0ec696d6ea42fdeb1836b9553e561744e4b9d`  
		Last Modified: Fri, 31 Jan 2025 01:30:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6772f6aba8fa343a23d01428cb13e4d7161d7d7cf001c5620db79346f448fd1`  
		Last Modified: Fri, 31 Jan 2025 02:16:25 GMT  
		Size: 386.4 MB (386370023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce34bdc19134c8ed701461a3eeaa06d7d114eed9e1e3ae7b7a7de3702ec768c`  
		Last Modified: Fri, 31 Jan 2025 02:16:19 GMT  
		Size: 4.3 KB (4278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e182815622bcbe6afb8c88922e963783eec364b35cf6aa43f4b057ea8eb6578d`  
		Last Modified: Fri, 31 Jan 2025 02:16:19 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b0c96db5ef14b0a40ca1338dc1c94f9745c1c7cae03c6aeaad600ee34ed101`  
		Last Modified: Fri, 31 Jan 2025 02:16:19 GMT  
		Size: 10.9 KB (10887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f7a58545be57afce13a8652631aebdf3ad4b1febc4dffe337d6deaa7c10030`  
		Last Modified: Fri, 31 Jan 2025 02:16:20 GMT  
		Size: 1.6 MB (1617460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:773b98bb20f17aa6304a8f12aae889527d840f3e4a699221f709f7c7316dfcde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4306bdf3c01833258689ced0d1761ac4dff9795979447393af84f213bd46dce`

```dockerfile
```

-	Layers:
	-	`sha256:ebda0c636a9e29c211adc255e4faf7c7399d335dd86d571c2007ae84c45def4a`  
		Last Modified: Fri, 31 Jan 2025 02:16:19 GMT  
		Size: 4.3 MB (4346759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02abb0c92d5a83ea0bea407b44611a1c559d52d54fd229b8e5e35f17293b1cfe`  
		Last Modified: Fri, 31 Jan 2025 02:16:19 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:c23194691ee339875a1b8ea0251771c48633eedeea7635d78f449cc55d2a4173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.7 MB (477746306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af2ed0a1489945fc604188cdae96a9508e42641cb9b2d94a436fa406dc2a840`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Jan 2025 19:07:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:07:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_VERSION=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DIST=
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.version=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 Jan 2025 19:07:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
VOLUME [/var/solr]
# Tue, 21 Jan 2025 19:07:29 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 21 Jan 2025 19:07:29 GMT
WORKDIR /opt/solr
# Tue, 21 Jan 2025 19:07:29 GMT
USER 8983
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360f49de6ba14f833932043a2b7635b6dbb1ec90797c695d682858e4d2a5a52`  
		Last Modified: Fri, 31 Jan 2025 01:42:56 GMT  
		Size: 46.5 MB (46463497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab08342d2d2022a4346660236d446ab4cb3711210932b0e608b45c35bf4a58d`  
		Last Modified: Fri, 31 Jan 2025 01:42:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e7d29b3d784556186e5dc47a775982b3b320fffdf0e1bdeeb2c075f0eb3f2`  
		Last Modified: Fri, 31 Jan 2025 01:42:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e032b23f7fe310790294a4f5eab2b00f4bb443d53f40a8ee4b2b75142794976d`  
		Last Modified: Fri, 31 Jan 2025 03:40:33 GMT  
		Size: 386.4 MB (386370114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba5b69711b96fb27524674cc4eb6a5fddc20a8c772ef4ed4c7c295881469f66`  
		Last Modified: Fri, 31 Jan 2025 03:40:25 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caba1f52edf870f760a9f466a2b7b5ab868d8b5b81e8cd99dfb23752a836680b`  
		Last Modified: Fri, 31 Jan 2025 03:40:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76caeea38acf71325812028931594060a020de69da5a8d7d09a84cbb24db93f8`  
		Last Modified: Fri, 31 Jan 2025 03:40:25 GMT  
		Size: 10.9 KB (10887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67025297082809aedc6f94aea0caa8f6c0d23539b9cafd33fb94f399e6e7651b`  
		Last Modified: Fri, 31 Jan 2025 03:40:26 GMT  
		Size: 1.5 MB (1474451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:ae2dd862ef5e82409b14fb27c0e0b98c9d51ef4c9f31b021b441b577048413e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b28f81253d259e350bb8d91c51465ecc756c71f1465c35a06affc435f9057f`

```dockerfile
```

-	Layers:
	-	`sha256:b224e75c359bebdc639b20dcbc499f26ed85cdd55c7feeb6cc42e88fafa21fc2`  
		Last Modified: Fri, 31 Jan 2025 03:40:25 GMT  
		Size: 4.3 MB (4348311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efccf47995665843eed239d4add9213bdf6b13afdf03d7151a4930c476b35648`  
		Last Modified: Fri, 31 Jan 2025 03:40:25 GMT  
		Size: 34.5 KB (34499 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:9e0ae2df20e504ef0a65bf86400c5ee4d8d459a357145557f1f479e8b04fa085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.9 MB (486880933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5ce22b6ce57bed3c05750215e482932da4860da40ba4468135c0b040c6db82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Jan 2025 19:07:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:07:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_VERSION=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DIST=
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.version=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 Jan 2025 19:07:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
VOLUME [/var/solr]
# Tue, 21 Jan 2025 19:07:29 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 21 Jan 2025 19:07:29 GMT
WORKDIR /opt/solr
# Tue, 21 Jan 2025 19:07:29 GMT
USER 8983
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1549ab3d8e534df8d96c792f2811628e2e2df295e9f3a0f7b600693d70ea4054`  
		Last Modified: Wed, 22 Jan 2025 18:30:54 GMT  
		Size: 17.7 MB (17651386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8a2e69084e70de91bac023061a94c98e934cd8f70d4ac4e895ab3263cfae4f`  
		Last Modified: Wed, 22 Jan 2025 18:48:50 GMT  
		Size: 46.8 MB (46762249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661022f0674ba1c13705a25771f1b9bbe1c11b6faa0268c00c51299efbc9190d`  
		Last Modified: Wed, 22 Jan 2025 18:48:48 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09373672e3e1cebfd280e93233d9f3dc0cb86bbc84437cbadd59ebe8055fca51`  
		Last Modified: Wed, 22 Jan 2025 18:48:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6db33080252b12c306f10985c294ea97f62bdf8bb609dfe96f006daac21b91`  
		Last Modified: Wed, 22 Jan 2025 21:23:07 GMT  
		Size: 386.4 MB (386370605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b715b0136f975d31de0e74ac3108ada4c9f1444b5259312845a16ebcb65ba50e`  
		Last Modified: Wed, 22 Jan 2025 21:22:46 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe25e89a1804b9e62621f9aa63f65d86fab1866237d0c6896fa4e7988fcdb32`  
		Last Modified: Wed, 22 Jan 2025 21:22:46 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8748a207a1488655de184fbf2f870b574c2574380cbf8fe9ee8abcd16131ced8`  
		Last Modified: Wed, 22 Jan 2025 21:22:46 GMT  
		Size: 10.9 KB (10903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2fc3f30a0811ed93d6e053b62cfa792fce92aa7814ce24a7511c8f7e9649c6`  
		Last Modified: Wed, 22 Jan 2025 21:22:47 GMT  
		Size: 1.6 MB (1630588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:d87db276112a266f79d95bddd6a762883232a6e3719a2a38f7ebe7b34a0f3542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4386936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037c65a43a1869362cc676bceb9302c6eafa292a8eb97227efb4a172d7e59ac5`

```dockerfile
```

-	Layers:
	-	`sha256:f83c8b76f115de3aacd4e60529e0f00d2cc8a87c9bf62b3e70c01b8586f60d89`  
		Last Modified: Wed, 22 Jan 2025 21:22:46 GMT  
		Size: 4.4 MB (4352546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e0a6778f5b1f80247b0328f81bb77275afdae1d642203883c441eab6aafc32e`  
		Last Modified: Wed, 22 Jan 2025 21:22:45 GMT  
		Size: 34.4 KB (34390 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:627cedf1152dc499e4afe0e867d7f2548a0431a22019f3af121badb041f51e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.0 MB (476040389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edf04d9063d80e2c879dd1be3315d840726dbd40f489c1cd8629d1e42bc4118`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Jan 2025 19:07:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:07:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_VERSION=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DIST=
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 21 Jan 2025 19:07:29 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.version=9.8.0
# Tue, 21 Jan 2025 19:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 21 Jan 2025 19:07:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
# ARGS: SOLR_VERSION=9.8.0 SOLR_DIST= SOLR_SHA512=e5db4fe32b5df45671c679d3ec5653bd5a969f43e28dad7e5f1b7633837c059250b610db7d593c13f674bf0edbaf4fe11ecb94c24fef6a22de952c6f2781800c SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 21 Jan 2025 19:07:29 GMT
VOLUME [/var/solr]
# Tue, 21 Jan 2025 19:07:29 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 21 Jan 2025 19:07:29 GMT
WORKDIR /opt/solr
# Tue, 21 Jan 2025 19:07:29 GMT
USER 8983
# Tue, 21 Jan 2025 19:07:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 19:07:29 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fce8df2d77e2997c97b30184cdfa23846196d4e5dfd005da96d8f36dcbc641a`  
		Last Modified: Wed, 22 Jan 2025 21:43:35 GMT  
		Size: 16.1 MB (16142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269211f1ea045e884f1175d77556df415d3093969647d5f33b870d33c557999`  
		Last Modified: Fri, 31 Jan 2025 01:43:28 GMT  
		Size: 43.9 MB (43949613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469f3a85ca4aad23caca93275437a25893f78888c8e35dcf3b777dfeec31c5e`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b248eed509cdcce48e80c1834adc9f5fb2a6d150447ac1b88ef4c81f5801ce`  
		Last Modified: Fri, 31 Jan 2025 01:43:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f784746e8bc6a2425a48dc40ef75444cea26dc2dc70e0461a1cdca7231ccd4`  
		Last Modified: Fri, 31 Jan 2025 02:34:19 GMT  
		Size: 386.4 MB (386370292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacc1a50febcd6469e606a1f8bb4e279c0afee229bc15dd6515bd855a909d4dd`  
		Last Modified: Fri, 31 Jan 2025 02:34:11 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfb953b1a52946961b952f20e33eea00c9fe85d68d7f60bf7dbadc78002ca88`  
		Last Modified: Fri, 31 Jan 2025 02:34:11 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51107e4ea761bdd1c3db3cf234c5056fe0f18a072b9193152f5107a343ff0622`  
		Last Modified: Fri, 31 Jan 2025 02:34:11 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3187896c44e9cbce32b6ae0afab6efe0e8b3836d24231f055bf0eb1dfa3ef83c`  
		Last Modified: Fri, 31 Jan 2025 02:34:12 GMT  
		Size: 1.6 MB (1559005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:ef2d790b677bdc364a5cf92acf2ae517c65fad6b76fef1731c9149bf9516ea40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4384566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8372c9dad754b46b04d580ca4df1bb3d5539c9fc891e3ca6cbb740b0c029599`

```dockerfile
```

-	Layers:
	-	`sha256:4caf63467a49888119bbf0ccf03ee8ed92c81cabc77e67132ddf7d0e512b303c`  
		Last Modified: Fri, 31 Jan 2025 02:34:10 GMT  
		Size: 4.4 MB (4350231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846888a6cad739db9286f8b5105c572f85aad4f4124469c918bc9faf45089ff8`  
		Last Modified: Fri, 31 Jan 2025 02:34:10 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json
