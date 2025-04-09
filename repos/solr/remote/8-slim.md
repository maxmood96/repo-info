## `solr:8-slim`

```console
$ docker pull solr@sha256:0639738bba60fcc052543c5bc0a57ba7b10ce3019d61b85b7e5e176841044c67
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
$ docker pull solr@sha256:aa23ed73202425113092b572691797c7148992c0cdafdb63891041e29d3eb4a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321765309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b085dddcd6d1c6838782be39215c5f308d735939ba59c60afed1549ba0a8952b`
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
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
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
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe913685dc07308206b8b9368edd760d45c0ed0c1ce0a008219f9ae4565668b6`  
		Last Modified: Wed, 09 Apr 2025 01:15:34 GMT  
		Size: 20.3 MB (20260214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0298071afd7ec797d4c38d0c29e19fe832ecf95e87bf51f6df5b5f5c220fb8a3`  
		Last Modified: Wed, 09 Apr 2025 01:15:34 GMT  
		Size: 47.2 MB (47217150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261c34eb718b577c4eb4d30527baae2184b689e59aaba4f624d32889c2a480fe`  
		Last Modified: Wed, 09 Apr 2025 01:15:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d15027f2149d0b63aec987947cbbfaa63e34e19b3922082fe2180bc11e2847`  
		Last Modified: Wed, 09 Apr 2025 01:15:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5d67ec18d1801dbccec7de79013bf8cb5b99d8d4afa2ec1da11ff31d2af962`  
		Last Modified: Wed, 09 Apr 2025 02:16:31 GMT  
		Size: 1.3 MB (1347644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74952777e39d8633bb10bf35181b5aae5d8dec1668e093ce4ed5775a9bfa46`  
		Last Modified: Wed, 09 Apr 2025 02:16:31 GMT  
		Size: 4.3 KB (4268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d52b1c46c4a9951fb661f508c2b38893b91bfcfaa5d9c044b3287e52f0514`  
		Last Modified: Wed, 09 Apr 2025 02:16:31 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb3cc14397902832afc1140e995d88e2645261263c02f57aa6f806d2bca5868`  
		Last Modified: Wed, 09 Apr 2025 02:16:38 GMT  
		Size: 225.4 MB (225414003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d6cb951664f524ae364ed94fefc0728e3d53ba043a6c575859f2b493d3e577`  
		Last Modified: Wed, 09 Apr 2025 02:16:32 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:d070472488fbe7de208e1d24b8ab1363023c061c909c48f64061763fa8045e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29dd84b36282944471fdb1abb8cd1ab8eee9f377b91fe68fbc25f098b10f15de`

```dockerfile
```

-	Layers:
	-	`sha256:7b7e5c224ff177b2e28c89cb7eb6aba5c397e71472f08674fa8343bf45eb8f12`  
		Last Modified: Wed, 09 Apr 2025 02:16:31 GMT  
		Size: 4.2 MB (4192715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d13add898604e1d5ce5e8c1f3e2bf96b3b19a3ddda9129ffd61415d5998f242`  
		Last Modified: Wed, 09 Apr 2025 02:16:31 GMT  
		Size: 36.4 KB (36351 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:7835e62a3f14e9bb2ab0dd0f98868a83c32b872479ec69ce63e29c06f91d5979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318284421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc70ffae088cd8eb455e2dde554e5c82523148d4cf990997641ae59e889aedf`
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
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:203c18bebe69acaf1fb23cd363bd034d334b70ba3724d31346f20df69a92bd6f`  
		Last Modified: Fri, 31 Jan 2025 01:37:51 GMT  
		Size: 45.6 MB (45577259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98978b8a278664a377653ceb4aa79e10f079fec7b8bc1ec4f53e76ce14493350`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0117505d88ab01de845679380d4b62ec37d59c7ac49ab749abdb9493781117ad`  
		Last Modified: Fri, 31 Jan 2025 01:37:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be5c95e0f66806a08f4ea7639681cc96bee14306f6e6e625c6f5ff43ea9358e`  
		Last Modified: Fri, 31 Jan 2025 03:44:46 GMT  
		Size: 1.2 MB (1208749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c0a09b4d7874b4956131d535a65f4840556cf805a1fbae7f5ad839f141ece2`  
		Last Modified: Fri, 31 Jan 2025 03:44:45 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83f91ead1e5f3d36adeca224df88f90ed2b616115f3ad7c9d9a68eb6eb9871c`  
		Last Modified: Fri, 31 Jan 2025 03:44:45 GMT  
		Size: 2.9 KB (2891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2b48742528210f6f4732e65cd4ce0f6328e100559053b26db4072d9607f64`  
		Last Modified: Fri, 31 Jan 2025 03:44:51 GMT  
		Size: 225.4 MB (225413998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79b25affa7e9c616181e3d0371a27d2ef0c67f37c141adfc843a0760d22f759`  
		Last Modified: Fri, 31 Jan 2025 03:44:46 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:f7acd6e61a8b3d9f18082ceecc22e8dd4902a0573092e88a65b48ef2e09c38f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c30836d86a5daa9b29c7032dbea3367cfd43f3b07edb164aa06527c74b10a7`

```dockerfile
```

-	Layers:
	-	`sha256:485d0d6dc013e3631cd629b828f7ba198fdae05fadb0398f0ae5e1f274b2bc72`  
		Last Modified: Fri, 31 Jan 2025 03:45:06 GMT  
		Size: 4.2 MB (4192302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d37033b211fac7e3cb4709cc07b062ed3f542dad0f82a72e35f3fb6edb6517`  
		Last Modified: Fri, 31 Jan 2025 03:45:05 GMT  
		Size: 36.5 KB (36487 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:0d34522b121ea6c7c523f9a57cc6ba405723e588b5dccb15fac9e764b758dced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323972269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da95f52febe590f6dfd041c87e03681087f4ace1551a5400c6b676c325a244b`
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
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:36abf3f81c420d4616a5636ec9705f495cdfdae6888d6ae3485fbc8dbbb509c9`  
		Last Modified: Fri, 31 Jan 2025 01:42:17 GMT  
		Size: 42.7 MB (42677206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8cbcf7b17def53b72faa7c4f8ea2c61f51e5654068211b401c26f51dac112e`  
		Last Modified: Fri, 31 Jan 2025 01:42:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b7c363f00702be77c74385711ee4e75703ce1da86fb80acba99659990b79a7`  
		Last Modified: Fri, 31 Jan 2025 01:42:15 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081c41707718a4288e5e926e4ecde9f3ffb9445c66eaf955de47b135ab430a1b`  
		Last Modified: Fri, 31 Jan 2025 05:34:32 GMT  
		Size: 1.4 MB (1368904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e002c775bb7f69014a514b6a0e660e2618f40c979a433b80bad867a533ea31`  
		Last Modified: Fri, 31 Jan 2025 05:34:32 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f60ee54d1f90576fee977fb412c489154c0a6f5949c707109858fdbf248cbb7`  
		Last Modified: Fri, 31 Jan 2025 05:34:32 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994c5ba486c190900eb769d68244a77ce6b1c4bf73413be1a4cdc704a5b12518`  
		Last Modified: Fri, 31 Jan 2025 05:34:38 GMT  
		Size: 225.4 MB (225414023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3759a15b97bfc6536d15172d52286c3ec3da90c5e0755aeb6279d7f340aec4`  
		Last Modified: Fri, 31 Jan 2025 05:34:33 GMT  
		Size: 6.3 KB (6273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:f1dd726e2481b40ea870a8efe28cc9af736a5d7c94ba1e5d8da09995f110541a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb293247cccf9770cd63b5a193dd4cb95b6b1ecf8c83570fb9326620fc6c3a16`

```dockerfile
```

-	Layers:
	-	`sha256:62587d766e3cb91973492fc15109949639efb30d3430bdb57fc1acd592f9ea77`  
		Last Modified: Fri, 31 Jan 2025 05:35:40 GMT  
		Size: 4.2 MB (4195917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0080e6dd884a99fb1a732f63583f786fffb7b4c09cc31d05e56aa0e1cca5ac4b`  
		Last Modified: Fri, 31 Jan 2025 05:35:40 GMT  
		Size: 36.4 KB (36394 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; s390x

```console
$ docker pull solr@sha256:9642252ce52d942ba11846aa30603a3f5f87354953f1700b6ab7c8595e9c2764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313800727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c818d65ea4e7a2d5c8103c9e29375748bef30963a0358d330f4e9f13b7b2f2c`
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
ADD file:82f0132f510f24adc12d74491187647b94a14baa7a57fd22a67a5c3767541496 in / 
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
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 24 Sep 2024 23:29:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='e4a00a3ea318a63ba97236633f34c8a5477f6cdb643cf6883788840818110f5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:b35596e17e863edd4c594d026a60e36f73cc6a076370f55a24732114fd25ff68`  
		Last Modified: Tue, 08 Apr 2025 11:48:56 GMT  
		Size: 26.4 MB (26368190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86df5de06adafff5e91defb0ae071cda11948fd1f3ad0b05fbc6819acc60390`  
		Last Modified: Wed, 09 Apr 2025 04:15:20 GMT  
		Size: 19.9 MB (19901168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e371fd1a825f59d90cf07ab962ad3cdac9759f326f6c50024bad112f42bfec6`  
		Last Modified: Wed, 09 Apr 2025 04:17:54 GMT  
		Size: 40.8 MB (40839296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79135bbb0a47a002857fe46a7cc6b3b6a987826cf602e54d73dd8ae8409910d`  
		Last Modified: Wed, 09 Apr 2025 04:17:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fa9889f00ec89fc12d3553ed7e41157ede95de543e8aa0ec89d780ad43a580`  
		Last Modified: Wed, 09 Apr 2025 04:17:53 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b121dd867a110eceac319f7c897732437fab18304124980d7e34c376dde15f8b`  
		Last Modified: Wed, 09 Apr 2025 06:23:10 GMT  
		Size: 1.3 MB (1262200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0165523f84c40ed8cc635cf0e95bbd9ee0e8d63ed6e2499a4839f3263c0bb234`  
		Last Modified: Wed, 09 Apr 2025 06:23:10 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ae3796e8694cec9b10c47740a834386dda4be1bfac32382fd1c7e396a0c748`  
		Last Modified: Wed, 09 Apr 2025 06:23:09 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ae3129a65edabba49ca88d81a2b0f253d6dfadde15953368f40656d4aafc5b`  
		Last Modified: Wed, 09 Apr 2025 06:23:14 GMT  
		Size: 225.4 MB (225413933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d11113a7962ac8dde885e994c7d3386c127c6d54a5a2ca1ca1285ba7b96823a`  
		Last Modified: Wed, 09 Apr 2025 06:23:10 GMT  
		Size: 6.3 KB (6271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:4d73bbc53dd1bb01e1dc4f3f84cf64ef7ab6a0caf70a7efbf25aeb1e82791aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4993cf35a5124b956a8c34749e9373f0c0fdb0a57e068350f4e5d5639e4f9f86`

```dockerfile
```

-	Layers:
	-	`sha256:780ffb6dd6a197c828b5cf4419254b84503d146b3ad36ad5e2d433ee6f71b723`  
		Last Modified: Wed, 09 Apr 2025 06:23:38 GMT  
		Size: 4.2 MB (4193513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c34ce09c9b35c3eb4952a5c3948fa33822837d20671cc2f09237ced797f063`  
		Last Modified: Wed, 09 Apr 2025 06:23:37 GMT  
		Size: 36.4 KB (36350 bytes)  
		MIME: application/vnd.in-toto+json
