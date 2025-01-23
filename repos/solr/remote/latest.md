## `solr:latest`

```console
$ docker pull solr@sha256:c1bb6d9ed0365f08f6cc3c26998c9b09ab4222f3a3a40d754f4eb5b97ecaeac9
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
$ docker pull solr@sha256:c868b71c31a1278ee3eec4659a5803f669c3f460ca74cdc3194c0ab93e23320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.6 MB (480627485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d801799f6bc4aeed2293dd9d877009f2c8ff35ec84b4602502d2ecdea47d8b`
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb863ad3341b296314c0087afee51d271d66481a9c4c93543fea5cb3f2b0034`  
		Last Modified: Wed, 22 Jan 2025 18:28:02 GMT  
		Size: 16.1 MB (16144395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aa630608356fc36b220aabcb3685a1860a2e3ad37841d355b189fba38875d3`  
		Last Modified: Wed, 22 Jan 2025 18:28:02 GMT  
		Size: 46.9 MB (46942122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7439c7b9afaefa8b208dfb371dbf621f71db1e1ee5b5b14bf598265b787a34a7`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0da6393fd47cfa1a49b58091b48da741160efaefb8c68549b15e6d93ed3547`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600a885e65d1dd1b40a70247d633df15c28f8bd40000d7ace4e35ca20abd6e96`  
		Last Modified: Wed, 22 Jan 2025 19:40:12 GMT  
		Size: 386.4 MB (386369981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4113768be039cbfa8aa4a1f7e67945d40f4c91188e62fc3fac2af51b5c5c233`  
		Last Modified: Wed, 22 Jan 2025 19:40:07 GMT  
		Size: 4.3 KB (4275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f07d099a71a2b0b12f2d502954e778e43c39ed0629c1be0648998949432dcd7`  
		Last Modified: Wed, 22 Jan 2025 19:40:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c506e13926ab83e13c36618ea3b30b7b0df3a379c030b2bfda5c674ee973b17`  
		Last Modified: Wed, 22 Jan 2025 19:40:08 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f71e12fa55df6d0aa343a7351e47b9129073cc5ac83ff7a7ca6a48ab04cf82c`  
		Last Modified: Wed, 22 Jan 2025 19:40:08 GMT  
		Size: 1.6 MB (1617456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:fb9a4d3e6131ce5b98e571beb6ba52aa044515673aa581e6e4bfb5f313ace561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b14a7df719a359f3eef663c0b9fe6f34e82074cfd906b6723fdea05253370f2`

```dockerfile
```

-	Layers:
	-	`sha256:24f5c80715a98363c1ebe141da4e267f0c0453fac87572041cda7a7c07b86c6c`  
		Last Modified: Wed, 22 Jan 2025 19:40:07 GMT  
		Size: 4.3 MB (4348637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3212f9dab8e435fc649d5804c5ba2dc27d5f4a1bfaae39519c84ea9254f8be30`  
		Last Modified: Wed, 22 Jan 2025 19:40:07 GMT  
		Size: 34.3 KB (34340 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:a3b5390ede5c76aa64fc26147eb508033784357c8dab99dc985cc3a3d39b0c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.7 MB (477713787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717b010a45e63307a797fe53254a845fe221821e2aca5109b660d52616c8e849`
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
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
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
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Last Modified: Thu, 24 Oct 2024 00:58:15 GMT  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c88cd8dd8835e47c7a890ad7abd2ca59cf691145582518cf5843edbd6d6bfa0`  
		Last Modified: Thu, 24 Oct 2024 01:12:30 GMT  
		Size: 46.4 MB (46430856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c3c08b455337af9ba6b5fe522389a1d0a2b621fe437f3832a54289cac03397`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26811a6e12de121df2970871f9027eb19d2c672b0045944972cf63a39c74aa15`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f61a8f51594fa41265ab4128e1f9a18654878730678a4d575f29164b56b954`  
		Last Modified: Tue, 21 Jan 2025 23:31:03 GMT  
		Size: 386.4 MB (386370152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e0749dad876579fbc34b38aebbdffba4c05ffff4819300f46ed8302c76dae0`  
		Last Modified: Tue, 21 Jan 2025 23:30:55 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0052880ac2056fe970aabb8e587f05ad5b47298d6172eb004540443e891eb7d`  
		Last Modified: Tue, 21 Jan 2025 23:30:55 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab4cb208b2002fea4b8f16be1320717aed2d1c728800b8d60c2c8d20d5c973`  
		Last Modified: Tue, 21 Jan 2025 23:30:55 GMT  
		Size: 10.9 KB (10885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286e0e2725f20a11d897b1381880eee2dcd40d9802ce3ae079fa507c24744e39`  
		Last Modified: Tue, 21 Jan 2025 23:30:56 GMT  
		Size: 1.5 MB (1474451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:4a2a71beaba7364ca7573a09adf44241dd08d5bdaf86c04a4538c32cb22e0871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30243b7b9fcfba269c8a4db1f422cfc99347b7089e9510e7a047bfde317a3b22`

```dockerfile
```

-	Layers:
	-	`sha256:f84e09deca20618d5b4cedf0701bb25193027428f52b0d7a8f3cd96d7146776b`  
		Last Modified: Tue, 21 Jan 2025 23:30:55 GMT  
		Size: 4.3 MB (4348313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0e39ea08f43606690e04cc56b98b8c7ccdff384bec5bea673a8cd73cae4c57f`  
		Last Modified: Tue, 21 Jan 2025 23:30:55 GMT  
		Size: 34.5 KB (34504 bytes)  
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
$ docker pull solr@sha256:0a46685d1ddb294f7788a38225c978efb8741d05353826ad8dbe8bf651d0a5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.0 MB (476034268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cbd31dfecd57fcd4bd54bd64a947caab62229eee850830ab3b2aa15a2a35d1`
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
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
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
	-	`sha256:9994cad72290d99d0275f342ad14206d889a15e886b2243fd599e3d74aeac9f8`  
		Last Modified: Thu, 24 Oct 2024 17:04:51 GMT  
		Size: 16.1 MB (16141938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202da4a4f6d062585c4f0ceae45eeca1c654d6feae753209341ae2fe55213d41`  
		Last Modified: Thu, 24 Oct 2024 17:32:49 GMT  
		Size: 43.9 MB (43943407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f26b56544cb69df62eeb7f99607b83222cc0287008fbeca07554cb171de6100`  
		Last Modified: Thu, 24 Oct 2024 17:32:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb36841c35a2b10c356fdb612c0af05dd3474471d0535c2747539deef4c45426`  
		Last Modified: Thu, 24 Oct 2024 17:32:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ede2e522b89c0ae73287b29be30f3fdd928e628f77dec01443d1c972469a7d8`  
		Last Modified: Tue, 21 Jan 2025 23:31:26 GMT  
		Size: 386.4 MB (386370410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9167e0f196c3e1a4e4dc735206e0be0aa48d1f0ec6cf9adc24a583cf6ecefe2e`  
		Last Modified: Tue, 21 Jan 2025 23:31:20 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fe7f0998922ea21cf5ea1bb9f7d8b75c1501c26cdbf5757ec7c241343e9500`  
		Last Modified: Tue, 21 Jan 2025 23:31:22 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ef7a3d1dec254c84d8d86b183a0303ec9d0c1551ebc68af1a4fd88d3225f44`  
		Last Modified: Tue, 21 Jan 2025 23:31:20 GMT  
		Size: 10.9 KB (10886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b089bb8512b6e6155faafcd15b65ccff62de39222f1cb9d71ff9703a2a200d`  
		Last Modified: Tue, 21 Jan 2025 23:31:21 GMT  
		Size: 1.6 MB (1559162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:c2ce2c1ea7ad3c7fc823136e3d1d9901612cc65008fc9c5dfba271cacb9d9295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4384573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae05d8e42327836deff4a6ae1c95eeef406389a61ec75512f6e9062cd90c3be`

```dockerfile
```

-	Layers:
	-	`sha256:a7650a43e2b7c05adb87b32238a37343ad60171c9543aacdae50173801627a9f`  
		Last Modified: Tue, 21 Jan 2025 23:31:20 GMT  
		Size: 4.4 MB (4350233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77c8d8ea2c41438843bc3a297a0c30af8e1f1f2c6b03703d6b847326bbf0019`  
		Last Modified: Tue, 21 Jan 2025 23:31:19 GMT  
		Size: 34.3 KB (34340 bytes)  
		MIME: application/vnd.in-toto+json
