## `solr:8-slim`

```console
$ docker pull solr@sha256:af39e7a655475b63f1bc57f313da4dadc3d449f978fda3bf4735a551d2b6d58d
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

### `solr:8-slim` - linux; amd64

```console
$ docker pull solr@sha256:aa9cbecbf1c039c9556aa883a78260ba0de4521da1e6129a6107d7b0320fc015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321763252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086d8154edf0d740f7408437b7d6057abe34cfface198a57cb7327e0a8b451da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 24 Sep 2024 23:29:11 GMT
ARG RELEASE
# Tue, 24 Sep 2024 23:29:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 24 Sep 2024 23:29:11 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 24 Sep 2024 23:29:11 GMT
CMD ["/bin/bash"]
# Tue, 24 Sep 2024 23:29:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Sep 2024 23:29:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Sep 2024 23:29:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_VERSION=8.11.4
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.4/solr-8.11.4.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.4/solr-8.11.4.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.4/solr-8.11.4.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
COPY --chown=0:0 scripts /opt/docker-solr/scripts # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
VOLUME [/var/solr]
# Tue, 24 Sep 2024 23:29:11 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 24 Sep 2024 23:29:11 GMT
WORKDIR /opt/solr
# Tue, 24 Sep 2024 23:29:11 GMT
USER 8983
# Tue, 24 Sep 2024 23:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Sep 2024 23:29:11 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0080f4e3086d24049ee68c3a03ea0664aba99c4d5502d156b62d079480b313`  
		Last Modified: Wed, 22 Jan 2025 18:27:50 GMT  
		Size: 20.3 MB (20257588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e4519bd327e3e49242c4cc7742524d87a3d87206ce25f7f97e8599e981e9fa`  
		Last Modified: Wed, 22 Jan 2025 18:27:51 GMT  
		Size: 47.2 MB (47217111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4941c723167d4e436a2e547abaf8f102c2fc90f759651c14e8aeeb7081c647`  
		Last Modified: Wed, 22 Jan 2025 18:27:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5e65b4a9c46765a9e8ddc624dc0117966755c21202830d823f4b7eb5cf4fb4`  
		Last Modified: Wed, 22 Jan 2025 18:27:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f205208e167776b7b22a716609693067cc7bdb0e569779e0b61834c10959fb`  
		Last Modified: Wed, 22 Jan 2025 19:33:55 GMT  
		Size: 1.3 MB (1347573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c9712a09ba77f6632a0249ca9eb926f9c5fedcb19580ef6360f9e900e7661`  
		Last Modified: Wed, 22 Jan 2025 19:33:55 GMT  
		Size: 4.3 KB (4275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08e56e0db3965e04caa175b3b641694119b0e016740542bfa4bce5c1c99f333`  
		Last Modified: Wed, 22 Jan 2025 19:33:55 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228adcf13b6dba4f05dc0ffd9244da9796eed9e5ba76b0ac039a3dcdc70c6a3d`  
		Last Modified: Wed, 22 Jan 2025 19:33:58 GMT  
		Size: 225.4 MB (225414009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea859eb2353690ad251c19c9821d86616dd4297457a81e50f8e60afe153e8814`  
		Last Modified: Wed, 22 Jan 2025 19:33:55 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1a304fe01dca1b6178fdbe38429671df6410fe45c6f8171ebc9cc7e562f7065f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3155c3004c12388e9d6970a96369a5ed0e4f61ec4c71f55a970a85c2ef0dfa40`

```dockerfile
```

-	Layers:
	-	`sha256:da7abc8bc1efe6a9a30ebe9f4d9b5c34d11e76429ca80723e8dec39047ae4953`  
		Last Modified: Wed, 22 Jan 2025 19:33:55 GMT  
		Size: 4.2 MB (4192035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d34dc652729b8eaf986b23330fd35c9aea9fc329a440339222a2a0b5b3437e`  
		Last Modified: Wed, 22 Jan 2025 19:33:54 GMT  
		Size: 36.4 KB (36351 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:0dd2dac0b34a7fbaa5bce2d9e4031496597f01db8fd9a9689ea9c3b4fd4e199e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318284878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0b0e0ce00eca5cee10bdaf34cc449a162730ef53d26012cabb52634ead62eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 24 Sep 2024 23:29:11 GMT
ARG RELEASE
# Tue, 24 Sep 2024 23:29:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 24 Sep 2024 23:29:11 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 24 Sep 2024 23:29:11 GMT
CMD ["/bin/bash"]
# Tue, 24 Sep 2024 23:29:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Sep 2024 23:29:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Sep 2024 23:29:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_VERSION=8.11.4
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.4/solr-8.11.4.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.4/solr-8.11.4.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.4/solr-8.11.4.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
COPY --chown=0:0 scripts /opt/docker-solr/scripts # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
VOLUME [/var/solr]
# Tue, 24 Sep 2024 23:29:11 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 24 Sep 2024 23:29:11 GMT
WORKDIR /opt/solr
# Tue, 24 Sep 2024 23:29:11 GMT
USER 8983
# Tue, 24 Sep 2024 23:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Sep 2024 23:29:11 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2db15fd1b470809728870bf4ec27554e69c771afb42f21d3044f23478346f97`  
		Last Modified: Wed, 22 Jan 2025 20:59:31 GMT  
		Size: 45.6 MB (45577789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c52098bad66b3bcf3c513afe961d5689aa8d59729277d9cdfde426d7d83cdd9`  
		Last Modified: Wed, 22 Jan 2025 20:59:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b901979fd2c225a813b00294f36eeaf9a07b2df476aed75bbc3788487942718b`  
		Last Modified: Wed, 22 Jan 2025 20:59:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46142c5055145f8009d13c6b9ad67c7fe34ff6ee1203f48bb14ac4bbd4e3e086`  
		Last Modified: Thu, 23 Jan 2025 00:59:36 GMT  
		Size: 1.2 MB (1208711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e600100c2d636e5c78a176f280a63a559ad6a677d6079e118d132ff0722f27a4`  
		Last Modified: Thu, 23 Jan 2025 00:59:36 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ff2a87599d0b0662cdd598f4f20334f823f86842931651c2112914346e9079`  
		Last Modified: Thu, 23 Jan 2025 00:59:36 GMT  
		Size: 2.9 KB (2895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4e4cf13898deea5f22596a251682e26deaf7fb91b04568c4d809b9380775a0`  
		Last Modified: Thu, 23 Jan 2025 00:59:41 GMT  
		Size: 225.4 MB (225413962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d13b015719dd4502147793c51e4a37d03085914281b805fdd6b0c52a49d22f`  
		Last Modified: Thu, 23 Jan 2025 00:59:37 GMT  
		Size: 6.3 KB (6277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:d8dfe8583424b6ec3f6171ffd30a985576e067b90e7040eb521601f13a5b9432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9f7a546c8b1e05702360eaf64dbc46dcd40423361f787f9118bb013f812166`

```dockerfile
```

-	Layers:
	-	`sha256:803062fcef53bec67895c21655cbcda2e3b25070e2a83df1549c45434edcf6b7`  
		Last Modified: Thu, 23 Jan 2025 00:59:55 GMT  
		Size: 4.2 MB (4192302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaa9bc514333378552c6c31d1607b3bdc3b8c0746fcc27e2ad3c3938c039c30f`  
		Last Modified: Thu, 23 Jan 2025 00:59:54 GMT  
		Size: 36.5 KB (36488 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:e8068d7f87d3b1f36da47f15de7f8d1b700615a8edb4e959338128f0edc4cd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323970694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57798b036fd7032eeecf27dd518ea659adb84fffc2c4defc3725f832bdb9c460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 24 Sep 2024 23:29:11 GMT
ARG RELEASE
# Tue, 24 Sep 2024 23:29:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 24 Sep 2024 23:29:11 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Tue, 24 Sep 2024 23:29:11 GMT
CMD ["/bin/bash"]
# Tue, 24 Sep 2024 23:29:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Sep 2024 23:29:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Sep 2024 23:29:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_VERSION=8.11.4
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.4/solr-8.11.4.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.4/solr-8.11.4.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.4/solr-8.11.4.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
COPY --chown=0:0 scripts /opt/docker-solr/scripts # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
VOLUME [/var/solr]
# Tue, 24 Sep 2024 23:29:11 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 24 Sep 2024 23:29:11 GMT
WORKDIR /opt/solr
# Tue, 24 Sep 2024 23:29:11 GMT
USER 8983
# Tue, 24 Sep 2024 23:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Sep 2024 23:29:11 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f87c2fb3d121a254124d3a3171cab48a218a493e68f9620a9d15f0bd3bfc103`  
		Last Modified: Wed, 22 Jan 2025 18:28:55 GMT  
		Size: 22.4 MB (22419717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8208fca6f868abc75bdd2b7e13ba30a8e318dd2da220746b16ba0a2ea213520`  
		Last Modified: Wed, 22 Jan 2025 18:39:31 GMT  
		Size: 42.7 MB (42675656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f317ea68efbe39d187d37e7e0163ecec24e8f9daa34fd62655bf531d9b6d0c81`  
		Last Modified: Wed, 22 Jan 2025 18:39:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fd79d5cd75ae1da461517dee972f089e36f39826d89eb323f0100090b60905`  
		Last Modified: Wed, 22 Jan 2025 18:39:29 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce057432db9235bd4b96ad1f184aa9624eace2869da70e0c7033ca67ba51f38`  
		Last Modified: Wed, 22 Jan 2025 21:28:05 GMT  
		Size: 1.4 MB (1368911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1ee0bd2d48be9a9b48314aec932e4d47f3d1748ad20ea62b547d2fc9afcae`  
		Last Modified: Wed, 22 Jan 2025 21:28:04 GMT  
		Size: 4.3 KB (4284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f52bfa28973ba2f1378125c32dea1d6be918482065e964169bd65e29eb4ca22`  
		Last Modified: Wed, 22 Jan 2025 21:28:04 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1409c275a6fb528550e158c4029a5fd58b7ad527dde89a2b5924fb1f2539a06`  
		Last Modified: Wed, 22 Jan 2025 21:28:17 GMT  
		Size: 225.4 MB (225413980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d403baecf4dbefa9d2d48bf9f4a591641bc9d262b63460265f5dbae2385d1a`  
		Last Modified: Wed, 22 Jan 2025 21:28:05 GMT  
		Size: 6.3 KB (6277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:8cf4f939043a2172574f39ce483eee13031b851e2496c8ffde0ff1dda5f471e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ed6e24ab5952085376798eecacf59a351c2e3760ec26cdf0ce60943e3025e6`

```dockerfile
```

-	Layers:
	-	`sha256:9023745347a8bb4f4db703967a9152a56f40031bb039e4ac5843a63f0a4415d0`  
		Last Modified: Wed, 22 Jan 2025 21:28:58 GMT  
		Size: 4.2 MB (4195917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a1a8791d7e151199a2a72d7d4a00adc329526539d381585be9b9e4880e82d8`  
		Last Modified: Wed, 22 Jan 2025 21:28:58 GMT  
		Size: 36.4 KB (36395 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; s390x

```console
$ docker pull solr@sha256:ef052acd36abc3128603205f73a89d4f38f8b97c326cf8770bd3b5c313beae3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313800335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e75ae512f6cff1a2b8430d4a94aa4905c10de61a0fed64cb0d389b3b5b0f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 24 Sep 2024 23:29:11 GMT
ARG RELEASE
# Tue, 24 Sep 2024 23:29:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 24 Sep 2024 23:29:11 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Tue, 24 Sep 2024 23:29:11 GMT
CMD ["/bin/bash"]
# Tue, 24 Sep 2024 23:29:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Sep 2024 23:29:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Sep 2024 23:29:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 24 Sep 2024 23:29:11 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_VERSION=8.11.4
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 24 Sep 2024 23:29:11 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.4/solr-8.11.4.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.4/solr-8.11.4.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.4/solr-8.11.4.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
# ARGS: SOLR_VERSION=8.11.4 SOLR_SHA512=828a7c3c06f3ccca852f2c3f91d72bf032cf102646283f4e603bbc3c3f3753978ce8b5c014c4263fb66c251b6726105956ad726baee63af6568637eba0416612 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
COPY --chown=0:0 scripts /opt/docker-solr/scripts # buildkit
# Tue, 24 Sep 2024 23:29:11 GMT
VOLUME [/var/solr]
# Tue, 24 Sep 2024 23:29:11 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 24 Sep 2024 23:29:11 GMT
WORKDIR /opt/solr
# Tue, 24 Sep 2024 23:29:11 GMT
USER 8983
# Tue, 24 Sep 2024 23:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Sep 2024 23:29:11 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f6b14778eb4fed5cbb0bd80eea19d48526571f3b2dfa0196faf63f42fdb8c6c2`  
		Last Modified: Fri, 11 Oct 2024 04:41:53 GMT  
		Size: 26.4 MB (26365979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb249cf2bb79e7c454a96cbf6cd56dc7ed7161f5a8b48921c7a48c6ae4882f2`  
		Last Modified: Wed, 22 Jan 2025 21:41:39 GMT  
		Size: 19.9 MB (19901189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e36961cb1b37f36a8c31b3edeae986f5351b5e021bffc39e63da028fdfdbc8`  
		Last Modified: Wed, 22 Jan 2025 21:48:02 GMT  
		Size: 40.8 MB (40840999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cd77bdf5eb5abd1869850e42902dd34dc4a310f6db2a3edfb89fcc5b1bbe1`  
		Last Modified: Wed, 22 Jan 2025 21:48:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70c333af6f6676628ed0d3ea0f2ba203a6b38859e0daba882e2a890b021968d`  
		Last Modified: Wed, 22 Jan 2025 21:48:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebc2c67eaf6f643660e7bb039e0aae0cf3fc6fcb7b4f73bbdf60549bf479c8a`  
		Last Modified: Thu, 23 Jan 2025 02:29:46 GMT  
		Size: 1.3 MB (1262229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fff4bb03af8cc1007de12dc65f3c858a13b22c4d629bc43efc5a8721a10cdf`  
		Last Modified: Thu, 23 Jan 2025 02:29:46 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b99f0a48ccbcc30c410662620f98f4e5388875e7a88939f2f4e7360eaa91462`  
		Last Modified: Thu, 23 Jan 2025 02:29:45 GMT  
		Size: 2.9 KB (2890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a5ce880f3ca42af617e183871f3aeca98160ec5cb5dc197c529e297e81712e`  
		Last Modified: Thu, 23 Jan 2025 02:29:52 GMT  
		Size: 225.4 MB (225413991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44614235e7d9ecb9de368b962b87f083f6854dc6e18bd41cc8259d2f6c34125`  
		Last Modified: Thu, 23 Jan 2025 02:29:46 GMT  
		Size: 6.3 KB (6277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1709b4c176df3d4e74b19c6861ee25da0826309fcec71dab0d003c213ffdd988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b5bfc3a23f9b06f97e5aca8b95fb6d092f7baeff7bed9d4a1b7847fbf4b6b9`

```dockerfile
```

-	Layers:
	-	`sha256:6082e38a292df60ad3cc33de2cd160e52cc828d1b6b0f3a571ef8a120c09f73c`  
		Last Modified: Thu, 23 Jan 2025 02:30:29 GMT  
		Size: 4.2 MB (4192833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f071b1088478eaec40ba7c721000180feff809e27315a5cd92ce5dc1af91d9b`  
		Last Modified: Thu, 23 Jan 2025 02:30:29 GMT  
		Size: 36.4 KB (36351 bytes)  
		MIME: application/vnd.in-toto+json
